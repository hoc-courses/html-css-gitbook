# Intro to CSS

### Overview

CSS \(Cascading Style Sheets\) are a collection of rules for how specific styles, such as colors, fonts, lengths, and positioning should be applied by the web browser to the HTML elements in your web page.

### CSS Rules

The basic syntax, and preferred formatting, of a CSS Rule block is shown below. 

* You can specify a comma-separated list of selectors.
* You can specify multiple styles for each rule.
* The property-name is the specific aspect of the element you want to style.
* The property-name is the specific value for that property.

![](../.gitbook/assets/image%20%28246%29.png)

The first example is a single type selector for the body element with multiple styles. The second example of multiple selectors with a single style.

```css
body {
    background-color:red;
    color:white;
    text-transform: uppercase;
}

h1, 
h2,
h3 {
    color:red;
}

```

#### CSS Style Guide

I've included a link to the Google CSS Style Guide below. Look specifically starting at section 4.2.2, where the more general formatting rules are.

{% embed url="https://google.github.io/styleguide/htmlcssguide.html" %}

### What aspects of an HTML element can be styled?

These are the most common:

| \*\*\*\* |  |
| :--- | :--- |
| \*\*\*\*[**Color**](colors.md)\*\*\*\* |  |
| color | text color. named values, or numeric formats |
| background-color | background color. named values, or numeric formats |
| \*\*\*\*[**Font**](typography.md)\*\*\*\* |  |
| font-size | named sizes or different length units. default is 16px or 1 em. |
| font-family | Serif, Sans-Serif, etc... |
| font-weight | named weight, such as normal, bold, lighter, darker, or numeric value between 100-900 \(400 is normal\) |
| \*\*\*\*[**Content Rectangle**](box-model-box-sizing.md)\*\*\*\* | Think of each element on the page being a rectangular picture frame. |
| border | picture frame |
| margin | space outside of border \(space between pictures on the wall\) |
| padding | space inside of border \(inside picture frame, around picture\) |
| border-radius | rounding of corners |
| width, height | specific dimensions for content rectangle. |
| display | whether the element is inline, block, or inline-block. |

### Three Methods for Applying Styles

**1. Inline** - styles are specified as attributes directly on the HTML elements.

```markup
<body style="background-color:lightgray;">
</body>
```

**2. Embedded Stylesheets** - styles embedded directly in the html &lt;style&gt; element within the &lt;head&gt; section of the page.

```markup
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jellies From the Deep</title>
    <style>
        body {
            background-color: lightgray;
        }
    </style>
</head>
```

**3. External Stylesheets** - styles are loaded from an external stylesheet referenced in a &lt;link&gt; element. The styles are no different between these two options, except for where they are located.

```markup
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jellies From the Deep</title>
    <link rel="stylesheet" href="styles.css">
</head>
```

```css
// styles.css

body { 
    background-color: lightgray; 
}
```

### User-agent Default Styles

In addition to your own styles, the web browser provides a set of default styles. 

The link below is for the default styles applied by the Chrome browser. 

{% embed url="https://source.chromium.org/chromium/chromium/src/+/master:third\_party/blink/renderer/core/html/resources/html.css" %}

* display to set block elements \(h1-h6, p, hr\)
* font-size, font-weight for headings \(h1-h6\)
* list spacing, icon type for bullets at different indentation levels
* padding and margins - body has margin of 8px.

Below is a screen capture with no overrides except for colors to make it easier to see the margins and block elements. You can see that the font-size is different between the paragraph and the h1 and there is a margin around the content in the body. These are the default styles set in the user-agent stylesheet.

```css
/* Sample of Chrome default styles */

body {
    display: block;
    margin: 8px;
}

p {
    display: block;
}

h1 {
    display: block;
    font-size: 2em;
    font-weight: bold;
}
```

![](../.gitbook/assets/image%20%28251%29.png)

### Processing Order Matters

The web browser loads its default styles first, and then loads any styles defined by the web page author. If the the rule is repeated, the last one encountered will be used. For example, if our own stylesheet re-defined the h1 element to be an inline element instead of block, our rule would override the defined by the web browser.

```css
h1 {
    display: inline;
}
```

![](https://gblobscdn.gitbook.com/assets%2F-MWvM--ORajEf7cHwnl6%2F-MZ9qtzWadlVUcV_0URO%2F-MZAZJ7PoGnxowZuxqqE%2Fimage.png?alt=media&token=9467c626-d88e-4ee5-ad9d-f1bf8d7d0f13)



The same would be true if you re-defined the same style later in the same stylesheet file or in a stylesheet file that was loaded after the initial definition.  The rule is that the last definition will be used.

### Some Properties are Inherited

Inheritance is where some CSS properties are passed down the inheritance tree. 

```css
body {
    background-color:red;
    color:white;
    text-transform: uppercase;
}
```

```markup
<body>
    <p>p - this is a test</p>
    <h1>h1 - This is an h1</h1>
</body>
```

![](../.gitbook/assets/image%20%28252%29.png)

In the next screen capture, the background color and text transform have been overridden in the descendent elements.

```css
body {
    background-color:red;
    color:white;
    text-transform: uppercase;
}

h1 {
    background-color:purple;
}

p {
    background-color:orange;
    text-transform: none;
}
```

![](https://gblobscdn.gitbook.com/assets%2F-MWvM--ORajEf7cHwnl6%2F-MZ9qtzWadlVUcV_0URO%2F-MZAeFYYQseAft8dc9u8%2Fimage.png?alt=media&token=bdc091d9-6683-456e-8896-aa2421f89337)

**Text-related properties are typically inherited**. For example, font-family, font-size, font-style, font-weight, letter-spacing, line-height, text-align, text-indent, text-transform, and word-spacing.

**Some list styles are inherited.** For example, list-style-image, list-style-position, list-style-type.

**Text and background colors are inherited.** For example, color \(text color\) and background-color.

### Some Styles are not Inherited

It's pretty intuitive which styles are inherited and which are not. Inheritance of CSS styles is there to make the web developer's job easier, so it is applied for those elements where it makes sense.

Styles that you wouldn't want to be inherited are ones like borders, padding, margins.

For example, in the screen capture below the paragraph element has been set to have a dark cyan border. There is a span element within the paragraph, but it is not inheriting the border style.

```markup
<body>
    <p>p - this is a <span>test</span></p>
    <h1>h1 - This is an h1</h1>
</body>
```

```css
p {
    border: solid 3px darkcyan;
}
```

![](../.gitbook/assets/image%20%28249%29.png)



If the border style was inherited it would look like the screen capture below, which is obviously not what we would want.

![](https://gblobscdn.gitbook.com/assets%2F-MWvM--ORajEf7cHwnl6%2F-MZ9qtzWadlVUcV_0URO%2F-MZAhqNyAeQGr40nk-P2%2Fimage.png?alt=media&token=1e89396e-61ee-4a69-8263-df99e6aca8bb)

### Primary CSS Selectors

The "selector" selects which elements on an HTML page will be affected by the rule. All of the styles within the selector block will be applied to the selected elements.

There are many ways to select an element. To start off, we'll focus on the three primary ways:

**ID**: The ID selector targets any HTML element that has the relevant ID attribute value.

**Type**: The type selector targets every instance of the element type regardless of their position in the document tree.

**Class**: The class selector targets any HTML element that has the relevant class attribute value.

```markup
 <body>
    <p id="p1">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
    </p>

    <p id="p2">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      </p>

      <p class="p3">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      </p>
  </body>
```

![](../.gitbook/assets/image%20%28245%29.png)

```css
/* Type */
p {
    padding:20px;
}

/* ID */
#p1 {
    background-color:orange;
}

#p2 {
    background-color: darkcyan;
}

/* class */
.p3 {
    background-color:purple;
}
```

As you can see, there are lots of ways to target the same elements. So, how do you know which type of selector to use? Here are some general guidelines:

* most of your styles will use class selectors, as they are re-usable across multiple elements.
* reserve the use of type selectors for global settings, or values you want to be inherited.
* use id selectors very infrequently, as they are very specific and don't adapt to changes in surrounding styles.

### Child and Descendant CSS Selectors

These two selectors are used to target descendants of a given element. The child selector targets the immediate children, whereas the descendant selector targets any descendant.

**Child Selector: parent &gt; child.**

![](../.gitbook/assets/image%20%28244%29.png)

**Descendant Selector**: **parent descendant**.

![](../.gitbook/assets/image%20%28250%29.png)

```markup
<body>
  <section>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et <a href="http://www.google.com">dolore magna</a> aliqua. Ut enim ad minim
    veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
  </p>
  <a href="">Link to here...</a>
  <ul>
    <li><a href="">Link 1</a></li>
    <li><a href="">Link 2</a></li>
    <li><a href="">Link 3</a></li>
  </ul>
  </section>
</body>
```

```css
section > a {
    color: green;
    text-decoration: none;
}

ul a {
    color:deeppink;
    font-weight:800;
}
```

![](../.gitbook/assets/image%20%28248%29.png)

### Pseudo Selectors

A CSS **pseudo-class** is a keyword added to a selector that specifies a special state of the selected element\(s\). The most frequent use-case for pseudo classes are for styling links based on the different states:

* **:hover** - when the mouse hovers over link
* **:link** - default style for link
* **:visited** - style after link has been clicked/visited

You'll need to try this out yourself to test the hover style being applied.

```css
a {
    color:dodgerblue;
    font-weight:800;
    font-size:40px;
}

a:hover {
    color:deeppink;
}

```

### Advanced Selectors

There are a lot more selectors, but it's better to focus on these before moving on to the more advanced ones, such as combining selectors, attribute selectors, nth-child selectors and more. For the full list, consult [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors).

### CSS Specificity

There can be multiple selectors, each setting the same properties, that target the same element. For example, a selector for the font property could be set on the body element, as well as a paragraph element. 

When this happens, the browser needs to apply a set of rules to determine which selector will be applied to the element.

This is known as the specificity of the selector, or how strongly that selector binds to the element.  The specificity,  is given below from top \(highest specificity\) to bottom \(lowest specificity\):  

* **inline** style \(style attribute on element\)
* **id** attribute on element
* **class** attribute on element
* **type** selector in stylesheet

![](../.gitbook/assets/image%20%28247%29.png)

```markup
<ul>
    <li><a style="color:dodgerblue" href="">style="color:dodgerblue"</a></li>
    <li><a id="id-link" href="">id="id-link"</a></li>
    <li><a class="class-links" href="">class="class-links"</a></li>
    <li><a href="">Nothing on element</a></li>
</ul>
```

```css
a {
    color:black;
    font-weight:800;
    font-size:40px;
}

#id-link {
    color:green;
}

.class-links {
    color:hotpink;
}
```

### Summary - Cascading Style Sheets

As you have learned, there are many different origins for a style \(web browser defaults, inline, style element, and external CSS files\) and there are many different rules for how to resolve which style should be applied when there are multiple rules targeting the same element and style. The algorithm the web browser uses to apply the correct styles is what makes up the "Cascade" in Cascading Style Sheets. 

### 

### Resources

{% embed url="https://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048" %}

{% embed url="https://css-tricks.com/how-css-selectors-work/" %}

{% embed url="https://nanajeon.com/css-selectors-cheatsheet-details/" %}

{% embed url="https://flukeout.github.io/" %}

{% embed url="https://www.youtube.com/watch?v=b3zIKoZxDGQ" %}

{% embed url="https://wattenberger.com/blog/css-cascade" %}

{% embed url="https://www.slideshare.net/anuradhay\_2004/css-inheritance" %}

