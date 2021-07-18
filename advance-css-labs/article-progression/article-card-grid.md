# Article Card Grid

## What We're Aiming For...

We're going to build the front page of a newspaper website. The page will contain a collection of article cards within a grid layout. Each card will be have a photo, category tag, title, and a brief description.

![](../../.gitbook/assets/image%20%28147%29.png)

## Setting up a New Project

For this exercise, you need to download the set of starter files that you will use in your Visual Studio Code project.

### 1.Click on the link below to go to the GitHub repository where the files are stored.

{% embed url="https://github.com/annechinn/article-grid-starter" caption="" %}

### 2. Download the ZIP containing the starter files.

![](../../.gitbook/assets/image%20%28140%29.png)

### 3. Store the Zip file in your projects folder.

The file name will default to article-grid-starter-main.zip.

### 4. Unzip the zip file.

Use WinZip or [7Zip](https://www.7-zip.org/download.html) to extract the contents. Choose the "Extract Here" to extract the directory.

## Defining Default Colors for Article Cards

The starter project contains these pre-defined colors that we'll use throughout the web page.

```css
html {
    --primary-color: #c72727;
    --light-color: #f3f3f3;
    --dark-color: #333;
    --link-color: #333;

    --sports-color: #f99500;
    --arts-color: #a66bbe;
    --tech-color: #009cff;
    --science-color: #3bd142;
    --food-color: #d1483b;
}
```

## Setting page defaults

Set the background color to the light color and the color for the links. And remove the underline on the links.

```css
body {
    background-color: var(--light-color);
}

a {
  color: var(--link-color);
  text-decoration: none;
}
```

## Loading a Google Font via @import in CSS

To include an external font, there are two methods. It appears from the stack overflow discussion, that the link method is preferred.

### Link

```text
<link href='http://fonts.googleapis.com/css?family=Kameron:400,700' rel='stylesheet' type='text/css'>
```

### Import

```text
@import url(http://fonts.googleapis.com/css?family=Kameron:400,700);
```

![](../../.gitbook/assets/image%20%28148%29.png)

{% embed url="https://stackoverflow.com/questions/12316501/including-google-web-fonts-link-or-import" caption="" %}

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
```

## Basic Grid Layout

There are two components to establishing a grid layout. The parent element that acts as the grid container and the child elements that need to be organized within that container.

Here is the basic layout for our article grid. The &lt;section&gt; element is the parent container and each &lt;article&gt; element is a child that will be arranged within that container. Our grid will have two rows, with three article cards in each row.

```markup
<body>
    <main>
        <section class="articles">
            <article></article>
            <article></article>
            <article></article>
            <article></article>
            <article></article>
      </section>
    </main> 
</body>

<!-- emmet
section.articles>article*6>img
-->
```

### CSS Grid Properties

While grids can be quite complex, ours is very basic and pretty easy to conceptualize what's going on.

```css
.articles {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 16px;
}
```

For any grid, the parent container must set the CSS **display property to grid**.

Next, we define how many columns and rows we want the grid to have. In our case, we only need to define the number of columns and the grid will automatically wrap and start a new row after the number of columns we have specified have been filled.

Grids have introduced a new unit, called a **fractional unit \(FR\)**, that allows you to express the percentage of the overall width or height very easily. One FR is one unit and you can simply define each column's width in FR units. Our grid is going to have three columns with equal width. So the value of the grid-template-columns property is just 1fr for each column. If, for example, we wanted the middle column to be twice as wide as the other two, we would simply change the middle 1fr to 2fr.

Last, the grid-gap property specifies the padding between each of the cells in the grid. These are often referred to as the grid "gutters".

![](../../.gitbook/assets/image%20%28101%29.png)

## Article Card Images

Next, we'll start filling out each article card with an image. I've included six images in the project images folder to use if you don't want to get your own.

```markup
<article>
    <img src="images/jellyfish.jpg" alt="" />
</article>
```

Refresh your page and you'll notice that the images are very large. To fix this, add a style to set the image width to 100%. This will force the image to take up the space of its container.

```css
.articles img {
  width:100%;
}
```

Your page should now look like this, with your own images substituted.

![](../../.gitbook/assets/image%20%2811%29.png)

## Styling the Card

We'd like to add a little styling to make each article card have a frame around it. To do this, we'll define a selector to be able to target all of the articles in the section.

```css
.articles article {
  background-color: #fff;
  padding: 16px;
}
```

```markup
<section class="articles">
    <article>
        <img src="images/jellyfish.jpg" alt="" />
    </article>
    <article>
        <img src="images/french-toast.jpg" alt="" />
    </article>
    <article>
        <img src="images/weight-lifter.jpg" alt="" />
    </article>
    <article>
        <img src="images/robot.jpg" alt="" />
    </article>
    <article>
        <img src="images/break-dancer.jpg" alt="" />
    </article>
    <article>
        <img src="images/snowboarder.jpg" alt="" />
    </article>
</section>
```

The grid should now look something like this, with white padding surrounding the content of each card.

![](../../.gitbook/assets/image%20%28112%29.png)

## Adding Category CSS

Next, we'll add the category tags to each article. These are often referred to as "pills".

![](../../.gitbook/assets/image%20%281%29.png)

## Add Category HTML

I've shown one article example below. Add the category tags for all six of your articles. There are two classes that need to be specified for each category element and you need to use the correct category-{tagName} for each article.

```css
<section id="articles">
    <article>
        <img src="images/jellyfish.jpg" alt="" />
        <span class="category category-science">Science</span>
    </article>
</section>
```

### Category Colors

Earlier we added the global variables that defined the colors for the different categories. We'll now define some selectors to use those colors to apply to the category tags in our HTML.

```css
.category-sports {
  background-color: var(--sports-color);
}
.category-arts {
  background-color: var(--arts-color);
}
.category-tech {
  background-color: var(--tech-color);
}
.category-food {
  background-color: var(--food-color);
}
.category-science {
  background-color: var(--science-color);
}
```

![](../../.gitbook/assets/image%20%2887%29.png)

### Category Shape

```css
.category {
  color: #fff;
  font-size: 9px;
  text-transform: uppercase;
  padding: 4px 8px;
  border-radius: 10px;
}
```

Here's what the page should look like at this point.

![](../../.gitbook/assets/image%20%2894%29.png)

## Add Card Title/Description

Last, we're going to add a title and description to each card. This is simply adding a header followed by a paragraph element. Typically, we would have the title be a link to the article page, but we're just focusing on the single articles page for now, so we'll leave the href attribute empty. The &lt;h3&gt; element has a nice default value, so there's no need for us to change it.

Copy/Paste the &lt;h3&gt;&lt;p&gt; elements into each of the articles in our page.

```css
 <section id="articles">
    <article class="card">
        <img src="images/jellyfish.jpg" alt="" />
        <span class="category category-science">Science</span>
        <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
        <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
        impedit libero, beatae animi provident nesciunt molestias ipsam
        nemo ad.
        </p>
    </article>
</section>
```

Here's what the page should look like now.

![](../../.gitbook/assets/image%20%2895%29.png)

## Making the Grid Responsive

Currently our Grid is not responsive, meaning that the layout isn't adjusting to accommodate narrower screen sizes. In order to make our grid responsive, we are going to use media queries.

Media queries allow you to specify CSS property values that should be used when different screen widths are detected. Best practice is to start off designing for "mobile-first", and then expanding the content as the screen width increases. So we're going to modify our default CSS properties to be mobile-friendly, and then add media queries to add more content within the screen width when it exceeds 600px.

Below is screen capture within the Chrome Developer Tools showing you how to open the screen size viewer to test your media queries.

![](../../.gitbook/assets/image%20%28146%29.png)

The only change necessary to make our grid responsive is to set the default number of columns in the grid to one for the mobile case and then set a media query to expand the grid to have three columns when the target device is a screen and the width is greater than 600px.

The @media query syntax is defined in more detail in the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries).

```css
#articles {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 16px;
}

@media screen and (min-width:600px) {
  #articles {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
```

Now, when the width is less than 600px, there is just one column.

![](../../.gitbook/assets/image%20%28118%29.png)

## Solution

```markup
<section class="articles">
  <article>
    <img src="images/jellyfish.jpg" alt="" />
    <span class="category category-science">Science</span>
    <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
      impedit libero, beatae animi provident nesciunt molestias ipsam nemo
      ad.
    </p>
  </article>
  <article>
    <img src="images/french-toast.jpg" alt="" />
    <span class="category category-food">Food</span>
    <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
      impedit libero, beatae animi provident nesciunt molestias ipsam nemo
      ad.
    </p>
  </article>
  <article>
    <img src="images/weight-lifter.jpg" alt="" />
    <span class="category category-sports">Sports</span>
    <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
      impedit libero, beatae animi provident nesciunt molestias ipsam nemo
      ad.
    </p>
  </article>
  <article>
    <img src="images/break-dancer.jpg" alt="" />
    <span class="category category-arts">Arts</span>
    <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
      impedit libero, beatae animi provident nesciunt molestias ipsam nemo
      ad.
    </p>
  </article>
  <article>
    <img src="images/snowboarder.jpg" alt="" />
    <span class="category category-sports">Sports</span>
    <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
      impedit libero, beatae animi provident nesciunt molestias ipsam nemo
      ad.
    </p>
  </article>
  <article>
    <span class="category category-science">Science</span>
    <h3><a href="">Lorem ipsum dolor sit amet.</a></h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Et ea
      impedit libero, beatae animi provident nesciunt molestias ipsam nemo
      ad.
    </p>
    <img src="images/skull.jpg" alt="" />
  </article>
</section>
```

```css
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

html {
  --primary-color: #c72727;
  --light-color: #f3f3f3;
  --dark-color: #333;
  --link-color: #333;
  --sports-color: #f99500;
  --arts-color: #a66bbe;
  --tech-color: #009cff;
  --science-color: #3bd142;
  --food-color: #d1483b;
}

body {
  font-family: "Poppins", sans-serif;
  background-color: var(--light-color);
}

a {
  color: var(--link-color);
  text-decoration: none;
}

.articles {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 16px;
}

@media screen and (min-width: 600px) {
  .articles {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

.articles > article {
  background: #fff;
  padding: 16px;
}

article img {
  width: 100%;
}

.category {
  color: #fff;
  font-size: 9px;
  text-transform: uppercase;
  padding: 4px 8px;
  border-radius: 10px;
}

.category-sports {
  background-color: var(--sports-color);
}
.category-arts {
  background-color: var(--arts-color);
}
.category-tech {
  background-color: var(--tech-color);
}
.category-food {
  background-color: var(--food-color);
}
.category-science {
  background-color: var(--science-color);
}
```

