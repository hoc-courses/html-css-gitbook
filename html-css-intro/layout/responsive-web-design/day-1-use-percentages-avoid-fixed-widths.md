# Basic Principles

### A website is responsive by default. 

The default width on a block element is 100% of the parent element. 

Setting widths or heights on an element prevents it from being responsive and you will either need to use lots of media queries to adjust the width/heights or have scroll bars appear.

#### Fixed-width on a parent

![](../../../.gitbook/assets/image%20%2855%29.png)

#### Setting fixed-width on a child element

![](../../../.gitbook/assets/image%20%287%29.png)

This is expected behavior with CSS because it is trying to do its best to not lose information. For example, if there is text in the child element, it's not desirable to have it scroll, but at least the user can scroll to see the text.

![](../../../.gitbook/assets/image%20%2837%29.png)

```css
.child {
    overflow:hidden;
}
```

You could add the property `overflow:hidden` to the child element, but then you lose the ability to read the text, which is worse.

![](../../../.gitbook/assets/image%20%2854%29.png)

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

