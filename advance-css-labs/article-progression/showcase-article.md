# Showcase Article

## What We're Aiming For...

We're going to build the front page of a newspaper website. In this exercise we're going to add a showcase article at the top of the landing with a link to a feature article.

![](../../.gitbook/assets/image%20%28168%29.png)

## Setting a Background Image

{% page-ref page="../../advanced-css/background-image.md" %}

We've added a &lt;header&gt; element to place the showcase section. The showcase section will have a background image with text and a button layered on top of it. The technique necessary to get the image to be in a layer below the text and buttons is to set it using the CSS background property, instead of inserting an &lt;img&gt; element within the HTML page.

The background property has the following values that we will set:

* **url** - the location of the image
* **center/cover** - cover tells the browser to make sure the image always covers the entire container, even if it has to stretch the image or cut a little bit off one of the edges.

```css
.showcase {
  background: url('../images/robot.jpg') center/cover;
}
```

```css
<main>
    <!-- Showcase -->
    <header class="showcase">
    </header>

    <!-- Articles -->
    <section id="articles"></section>
</main>
```

## Setting the Showcase Height

We have set the height to 40vh, which means 40% of the viewport, or visible screen. We are using vh units so that the header is adjusted relative to the other content that is visible on the screen. We'll take a look at how this works once we get the showcase finished. We've also created some padding around the showcase content and set the text color to white.

```css
.showcase {
  height: 40vh;
}
```

## Other Styles

```css
.showcase {
 color: #fff;
 padding: 32px;
}
```

## Adding the Showcase Article Content

Now we just add the content, which includes the category tag, a title, and a description. We're going to stick with the default settings for the font size and weight for the text, so we don't need to add any additional CSS.

```css
<main>
    <!-- Showcase -->
    <secton id="showcase">
        <h1>An Article About Technology</h1>
        <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita
        recusandae consequatur similique doloribus. Corporis, et a ullam
        praesentium facere veritatis veniam? Aperiam ipsa totam veniam,
        atque illo sed suscipit accusamus.
        </p>
    </section>

    <!-- Articles -->
    <section id="articles"></section>
</main>
```

Set the width of the paragraph within the showcase to be 50%.

```css
.showcase p {
  width:50%;
}
```

## Adding the "Learn More" Button

The last item we need to add is the button at the bottom of the showcase section that links to the article. Most of the CSS in the code below should be familiar to you at this point. There is one new one we're going to introduce.

### Pseudo-classes

The ":" character indicates a special keyword is associated with a selector. This is called a pseudo-class. They are used to indicate a special state of the selected element. For example, :hover can be used to change a button's color when the user's pointer hovers over it. In our case, we're going to use it to change the opacity \(darkness\) or the button when the user hovers over it.

{% hint style="info" %}
They are called "pseudo-classes" because they let you apply a style to an element in relation to external factors like the history of the navigator \(:visited\), the status of its content \(like :checked on certain form elements\), or the position of the mouse \(like :hover, which lets you know if the mouse is over an element or not\).
{% endhint %}

```css
.btn {
  display: inline-block;
  border: none;
  background: var(--dark-color);
  color: #fff;
  padding: 8px 12px;
}

.btn-primary {
  background: var(--primary-color);
}

.btn:hover {
  opacity: 0.9;
}
```

## Solution

```css
<section class="showcase">
  <span class="category category-tech">Technology</span>
  <h1>An Article About Technology</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita
    recusandae consequatur similique doloribus. Corporis, et a ullam
  </p>
  <a href="" class="btn btn-primary">Learn More</a>
</section>
```

```css
.showcase {
  color: #fff;
  padding: 32px;
  height: 40vh;
  background: url("../images/robot.jpg") center/cover;
}

@media screen and (min-width:600px) {
  .showcase p {
    width:50%;
  }
}

.btn {
  border: none;
  background: var(--dark-color);
  color: #fff;
  padding: 8px 12px;
}

.btn-primary {
  background: var(--primary-color);
}

.btn:hover {
  opacity: 0.9;
}
```

