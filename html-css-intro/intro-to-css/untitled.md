# Untitled

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

![](../../.gitbook/assets/image%20%28251%29.png)

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

![](../../.gitbook/assets/image%20%28252%29.png)

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

![](../../.gitbook/assets/image%20%28249%29.png)



If the border style was inherited it would look like the screen capture below, which is obviously not what we would want.

![](https://gblobscdn.gitbook.com/assets%2F-MWvM--ORajEf7cHwnl6%2F-MZ9qtzWadlVUcV_0URO%2F-MZAhqNyAeQGr40nk-P2%2Fimage.png?alt=media&token=1e89396e-61ee-4a69-8263-df99e6aca8bb)

### 

### CSS Specificity

There can be multiple selectors, each setting the same properties, that target the same element. For example, a selector for the font property could be set on the body element, as well as a paragraph element. 

When this happens, the browser needs to apply a set of rules to determine which selector will be applied to the element.

This is known as the specificity of the selector, or how strongly that selector binds to the element.  The specificity,  is given below from top \(highest specificity\) to bottom \(lowest specificity\):  

* **inline** style \(style attribute on element\)
* **id** attribute on element
* **class** attribute on element
* **type** selector in stylesheet

![](../../.gitbook/assets/image%20%28247%29.png)

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

### ser-agent Default Styles

### 

### Resources

{% embed url="https://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048" %}

{% embed url="https://css-tricks.com/how-css-selectors-work/" %}

{% embed url="https://nanajeon.com/css-selectors-cheatsheet-details/" %}

{% embed url="https://flukeout.github.io/" %}

{% embed url="https://www.youtube.com/watch?v=b3zIKoZxDGQ" %}

### U

{% embed url="https://wattenberger.com/blog/css-cascade" %}

{% embed url="https://www.slideshare.net/anuradhay\_2004/css-inheritance" %}

