# Centering Elements

You often want to center items on the page as a whole, or within a container element. There are two common techniques to achieve this goal.

![](../.gitbook/assets/image%20%28257%29.png)

## Specific width with auto left and right margins

This technique works well when you know the width of the content to be centered or you want it to take up a specific percentage of the screen.

* set a width on the element
* set the margin-left and margin-right to auto

```css
  body {
    margin-left:auto;
    margin-right:auto;
    width:300px;
  }
```

```css
body {
    margin-left:auto;
    margin-right:auto;
    width:85%;
  }
```

## Using flex and center in both horizontal/vertical directions.

On the container of the element\(s\) you want to be centered: set the value of the display property to be flex in the column direction, and then center the items in both the horizontal and vertical directions.

```css
body {
  display:flex;
  flex-direction:column;
  justify-content: center;
  align-items: center;
}
```

## Resources

{% embed url="https://css-tricks.com/centering-css-complete-guide/" caption="" %}

