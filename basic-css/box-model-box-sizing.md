# Box-Model/Box-Sizing

The box-model describes the box that surrounds every HTML element on the page. Each box consists of the following:

**Content** - The actual content \(text, images, videos...\) of the HTML element.

**Padding** - Defined by the padding property. In-between the border and content of an element. Is transparent.

**Border** - Defined by the border property. Surrounds the padding and content of an element.

**Margin** - Defined by the margin property. Adds space between the border and other HTML elements. Is transparent.

Measurements are specified: top right bottom left \(like a clock\). You can set a single value if all sides have the same value. You can set two values \(top/bottom right/left\), if top/bottom and left/right have the same values.

![](../.gitbook/assets/image%20%282%29.png)

When to use the margin vs. the padding property can be confusing. The way to think about it is that the padding is specific to the element, whereas the margin is the space between elements. One important aspect of margins is that they collapse vertically to the largest margin between the adjacent boxes. When adding a new section to a part of the page, you don't want to have to think about what the adjacent element's margin is. You just want to think about how much margin you want to be between them

![](../.gitbook/assets/image%20%2819%29.png)

{% hint style="info" %}
The margin and padding properties have four values: top right bottom and left. If they are all the same, you can specify a single value. If the top and bottom are the same, as well as the left and right, you can specify just two values, and the top value will be applied to the bottom and the right value will be applied to the left.
{% endhint %}

{% embed url="https://codepen.io/annechinn/full/dyNeLpQ" caption="" %}

## CSS Box-sizing

In CSS, by default, the width of the box is only the width of the content. To calculate the total width, we have to add the margin, border and padding. This can lead to unexpected results.

The solution is to use the box-sizing property to force the browser to include the margin, border and padding in the width calculation.

The setting is typically set on all elements.

```text
* {
  box-sizing: border-box;
}
```

{% embed url="https://www.w3schools.com/css/css3\_box-sizing.asp" caption="" %}

