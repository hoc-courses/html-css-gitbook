# Day 1 - Use Percentages, Avoid Fixed Widths

Often see web developers set a fixed-width and a margin, but this forces the use of media queries to adjust the width to make the site responsive. 

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

![](../../../.gitbook/assets/image%20%2816%29.png)

