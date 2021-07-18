# Article - Basic CSS

So, now let's take a look at our article and see if we can make it look like this.

{% embed url="https://sharp-poincare-458620.netlify.app/" caption="" %}

## Create an external stylesheet for the Article

A common naming convention, if the project has a single stylesheet file, is to name it styles.css. This isn't a requirement, and most likely on larger projects, there will be multiple stylesheets that would be named to align with the area of the website that it is styling. If you are going to have multiple stylesheets, it is also common to create a folder to store them like the images and videos folders. For this exercise, create a folder called css, and add a single stylesheet styles.css file. Then add a &lt;link&gt; element to reference the styles.css file.

```markup
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jellies From the Deep</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
```

## Global Styles

### Article Margins

If you compare the two screen captures below, you'll notice that the final version has the content inset from the edges of the web browser.

How can we achieve this in our article?

![](../../.gitbook/assets/image%20%2850%29.png)

![](../../.gitbook/assets/image%20%2837%29.png)

### Font <a id="font"></a>

To set the font-family we want to use for our article we should set it on the body element. For this article, let's set the font to use a free one provided by Google, called "Poppins".‌

Let's also change the default font size, which is 16px, to 18px.

Now, the font is using the Poppins font. You can tell that it no longer has the serif typography.

![](../../.gitbook/assets/image%20%28160%29.png)

### Detail Section Spacing

Next, we want to add some space between each of the jellyfish sections. Typically we use margins for this, instead of padding. Let's add a 60px margin at the bottom of each of these sections. You can now see the nice spacing between the end of the Orange Jelly section and the start of the Yellow Jelly section.

![](../../.gitbook/assets/image%20%28171%29.png)

## Section-specific Styles

### Profile Avatar

Let's start with the profile picture up in the title section. That's typically called an avatar, when it's small round profile photo. Ours isn't currently small and round, so let's work on that.

First, we need to make it the correct size. Let's add a class with the value "avatar", so we can add some styles.

* set its width and height to 30px
* make the image round. 

![](../../.gitbook/assets/image%20%28117%29.png)

### Header Font Sizes

* Change the font-size to 32px

![](../../.gitbook/assets/image%20%28120%29.png)

### Header sub-title

We want to make a couple of modifications to the sub-title.

* change the font size to 24px
* remove the top margin on the sub-title and the bottom margin on the h1, so that there is less space between the h1 and the sub-title.

![](../../.gitbook/assets/image%20%2845%29.png)

### Header topic-link

* set the font size to 32px
* set the text color to the hex value "\#e7131a"
* remove the margin on the top of the h1 to reduce the space between the heading and the topic link.

![](../../.gitbook/assets/image%20%28108%29.png)

### Header Author section

We want to get each of these individual elements to line up horizontally on the same line and adjust the text color and font weight a bit.

* the address element is a block element by default. change it to be inline so that it does not return to the next line.
* set the text color for the address to be the same color as the topic-link.
* set the font size to be 11px for both the address and the time elements
* set the font weight to be 600 for both the address and the time elements
* adjust the avatar styles to make it center vertically and add a margin on the right of 5px.

![](../../.gitbook/assets/image%20%2892%29.png)

### Meet the Jellies Links

First, change the color of the links to the same red as the topic-link .

![](../../.gitbook/assets/image%20%28104%29.png)

![](../../.gitbook/assets/image%20%2858%29.png)

Next, we want to add some borders to make it look like this.

![](../../.gitbook/assets/image%20%2825%29.png)

## Styling Solutions

For each of these examples, I am just showing the specific style related to the properties I am discussing. For example, when I show the body element CSS rule for the font, I omitted the margin property. That way the code samples can just focus on the relevant CSS properties. But the final CSS file needs to contain all of the combined properties.

### Article Margins

```text
/* setting top/bottom;40px, left/right: 60px */
body {
    margin:40px 60px;
}
```

### Article Font

```text
body {
    font-family: Poppins, sans-serif;
    font-size: 18px;
}
```

### Jelly Section Margin

First, I'm going to add a class="jelly" to each of the detail sections. Then I'm going to create a CSS rule for that class to add a margin of 60px to the bottom of each section.

```markup
<section class="jelly">
    <h3 id="orange-jelly">Orange Jelly</h3>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing
        elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Egestas tellus rutrum tellus
        Tellus rutrum tellus pellentesque eu tincidunt tortor aliquam nulla facilisi. Libero justo laoreet sit amet cursus sit.
    </p>
    <p>Vel quam elementum pulvinar etiam non quam lacus suspendisse. Tincidunt dui ut ornare lectus sit amet
        est placerat in. Lectus nulla at volutpat diam ut  venenatis tellus.
    </p>
    <figure>
        <img src="images/orange-jellyfish.jpg" alt="jellyfish">
        <figcaption><address>Dan Dickerson</address></figcaption>
    </figure>
</section>
```

```css
.jelly {
    margin-bottom:60px;
}
```

### Avatar Image

```markup
<img src="images/author.png" alt="author" class="avatar">
```

```css
.avatar {
    width: 30px;
    height: 30px;
    border-radius: 50%;
}
```

### Header Font Size

```css
h1 {
    font-size: 32px;
}
```

### Header sub-title

```markup
<p class="sub-title">Tincidunt dui ut ornare lectus venenatis tellus.</p>
```

```css
h1 {
    font-size: 32px;
    margin-bottom:0px;
}

.sub-title {
    font-size:24px;
    margin-top:0px;
}
```

### Header topic-link

```markup
<p class="topic-link">SCIENCE</p>
```

```css
h1 {
    margin-top:0px;
}

.topic-link {
    font-size: 20px;
    color: #e7131a;
}
```

### Header Title address/time

```css
<section class="title-section">
  <p class="topic-link">SCIENCE</p>
  <h1>Jellies From the Deep</h1>
  <p class="sub-title">Tincidunt dui ut ornare lectus venenatis tellus.</p>
  <img src="images/author.png" alt="author" class="avatar">
  <address>RUBY RAILS</address>
  <time>JANUARY/FEBRUARY 2018</time>
  <hr/>
</section>
```

```css
.title-section > address {
    display: inline;
    color: #e7131a;
}

.title-section > address, .title-section > time {
    font-weight: 600;
    font-size: 11px;
}

.avatar {
    margin-right:5px;
    vertical-align: middle;
}
```

### Meet the Jellies

```markup
<section class="meet">
    <h2>MEET THE JELLIES</h2>
    <ul>
        <li>
                <a href="#pink-jelly">The Pink Jelly</a>
                <address>Sally Smith</address>
        </li>
        <li>
                <a href="#orange-jelly">The Orange Jelly</a>
                <address>Dan Dickerson</address>
        </li>
        <li>
                <a href="#yellow-jelly">The Yellow Jelly</a>
                <address>Pam Patterson</address>
        </li>
    </ul>
</section>
```

```css
.meet a {
    color: #e7131a;
}

.meet {
    border-bottom: 1px solid #000;
}

.meet > h2 {
    padding-bottom:12px;
    border-bottom: 1px solid #000;
}
```

## Assignment

Make sure your article is looking close to this.

{% embed url="https://sharp-poincare-458620.netlify.app/" caption="" %}

Check-in your changes and push them to GitHub \(which will automatically update the Netifly site\)

* git add .
* git commit -m""
* git push

Submit your assignment by just entering your Netifly url.

