# Day 1 - Use Percentages/Avoid Heights

### Setting fixed-width on a parent element

Often see web developers set a fixed-width and a margin, but causes side-scrolling to show up and forces the use of media queries to adjust the width to make the site responsive. 

```markup
  <div class="parent">
    <div class="child"></div>
  </div>
```

```css
.parent {
  background-color:#23424A;
  padding:50px;

  width: 900px;
  margin: 0 auto;
}

.child {
  background-color:#38CFD9;

  /* normally wouldn't hard-code a height,
  using it here just for demonstration purposes */
  height:250px;
}
```

![](../../../.gitbook/assets/image%20%2853%29.png)

If we don't assign a width the layout becomes responsive. If there was text as the content, it would still be responsive.  

A website is responsive by default. The default width on a block element is 100% of the parent element.

```css
.parent {
  background-color:#23424A;
  padding:50px;

  width: 80%;
  margin: 0 auto;
}
```

### Setting fixed-width on a child element

```css
.parent {
  background-color:#23424A;
  padding:50px;

  width: 80%;
  margin: 0 auto;
}

.child {
  background-color:#38CFD9;
  
  width:750px;

  /* normally wouldn't hard-code a height,
  using it here just for demonstration purposes */
  height:250px;
}
```

![](../../../.gitbook/assets/image%20%287%29.png)

This is expected behavior with CSS because it is trying to do its best to not lose information. For example, if there is text in the child element, it's not desirable to have it scroll, but at least the user can scroll to see the text.

![](../../../.gitbook/assets/image%20%2834%29.png)

```css
.child {
    overflow:hidden;
}
```

You could add the property `overflow:hidden` to the child element, but then you lose the ability to read the text, which is worse.

![](../../../.gitbook/assets/image%20%2850%29.png)

### Percentages are always relative to the parent.

```css
.parent {
  width: 80%;
  margin: 0 auto;
}

.child { 
  width:50%;
  height:250px;
}
```

![](../../../.gitbook/assets/image%20%2831%29.png)

