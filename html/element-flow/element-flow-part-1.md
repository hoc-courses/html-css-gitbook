# Element Flow - Overview

### Elements are Contained in Rectangles and Flow Down 

Here are some very important characteristics of how elements are rendered on a page:

1. Every HTML element on a web page is rendered as a **rectangular box**. 
2. By default, **elements flow from top to bottom**. 
3. There are two types of boxes: **block** and **inline.**
4. The type of box impacts how it behaves in terms of the page flow, and in relation to the other boxes on the page.

### Block Elements

* The box will break onto a new line 
* The box will extend horizontally to fill the space available in its container.

### Inline Elements

* The box will not break onto a new line.
* The box will only take up as much horizontal space as is necessary.

###  CSS display property

Whether an element is block or inline is determined by the CSS **display** property. We're not going to go into detail on how CSS properties are set and applied to an HTML element just yet, but I'll give a very brief introduction to make this topic clearer.

The **display** property is one of many that can be applied to an HTML element to effect how it is displayed on the page.  In the CSS code below, the `h1`, `h2` and `p` elements have all been configured to be block elements, whereas the `img` element has been configured to be an inline element.

```css
h1 {
    display: block;
}

h2 {
    display: block;
}

p {
    display: block;
}

img {
    display: inline;
}
```

The web browser provides default values for the display property for each element by loading and applying its own styles before loading any others. The default settings are typically what make sense for each element type. For example, headings and paragraphs are block elements, and therefore will always be on their own line. Whereas images and anchors are inline elements, and will only take up the minimum amount of space necessary, as they are often embedded in text.

In addition to always starting on their own line, block elements are configured to add a margin \(space\) between it and its neighboring boxes.

If you're curious to see what the Chrome default stylesheet looks like, you can take a look at it [here](../../appendix/chrome-default-stylesheet.md).

### Box Width

The screen capture below shows the space taken up by each of the different HTML elements. As you can see, the box for block elements \(`<h1>`, `<h2>`, `<p>`\) extends the entire horizontal width, even though the content inside the box does not.

Also notice that the first `img` element is on its own line. That is because the `p` element following it is a block element and block elements always starts on a new line. 

This is in contrast to the second `img` element that is embedded within a `p` element. While the `p` element that contains the img element does span the entire line, the `img` element inside flows horizontally with the inline text before and after it. 

### Box Height

Block elements, and inline elements, expand vertically to contain the content inside its box.

![](../../.gitbook/assets/image%20%28234%29.png)

```markup
<body>
  <h1>h1</h1>
  <h2>h2</h2>
  <p>p</p>
  <img
    src="https://images.unsplash.com/photo-1441555136638-e47c0158bfc9?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjh8fGplbGx5ZmlzaHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=60"
    alt=""
  />
  <p>p</p>
  <a>a</a>
  <p>
    Lorem ipsum <span style="font-size:xx-large">dolor sit amet,</span> consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
    veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
    commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
    velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
    cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
    est laborum.
  </p>
  <p>
    p
    <img
      src="https://images.unsplash.com/photo-1441555136638-e47c0158bfc9?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjh8fGplbGx5ZmlzaHxlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=100&q=60"
      alt=""
    />
  </p>
</body>
```

### 

### Inline Elements Embedded in a Paragraph

To re-enforce the your understanding of how inline and block elements behave in relation to each other, here is one more example.

The screen capture below shows how an `<img>` element, which we saw above is an inline element, behaves when it is positioned before, at the beginning and in the middle of a paragraph element. 

The difference is not due to the `img` element, but rather that the fact that the `p` element is a block element and a block element always starts on a new line. 

**Example \#1**: the `img` element is following an inline `h4` element and before an inline `p` element, so it ends up being on its own line, since the block elements neighbors must be one their own lines.

![](../../.gitbook/assets/image%20%28241%29.png)

```markup
<h4>Image placed before paragraph</h4>

<img src="images/photo.png"/>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam, quis nostrud exercitation ullamco 
    laboris nisi ut aliquip ex ea commodo consequat.  
</p>
```

**Example \#2**: the `img` element is embedded within the `p` element, so it only has a single neighbor, which is the text within the paragraph. Since text is an inline element, the text following the img element starts immediately after the `img` element.

![](../../.gitbook/assets/image%20%28214%29.png)

```markup
<h4>Image placed at the beginning of paragraph</h4>
<p>
    <img src="images/photo.png"/>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam, quis nostrud exercitation ullamco 
    laboris nisi ut aliquip ex ea commodo consequat. 
    Lorem ipsum dolor sit amet. 
</p>
    
```

**Example \#3**: the `img` element is again embedded in the paragraph, and its neighboring elements are the text before and after it. Since they are all inline, the `img` element takes up the minimal amount of horizontal space in the text.

![](../../.gitbook/assets/image%20%28216%29.png)

```markup
<h4>Image placed in the middle of paragraph</h4>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniamLorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam, <img src="images/photo.png"/>
    quis nostrud exercitation ullamco 
    laboris nisi ut aliquip ex ea commodo consequat.
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam 
</p>
```

### Resources

{% page-ref page="element-flow-part-1.md" %}

