# Grid vs Flexbox

### Grid and Flex Display Properties

Two new CSS display properties \(**grid and flex**\) greatly improved the ability to specify the layout/positioning of sub-sections of an HTML document. These new CSS properties allow the web developer to specify a precise layout for how the children within a parent element's rectangular box are positioned. The parent container can be the HTML element for the overall page, or any sub-section of the HTML element hierarchy.

Grid is ideally suited for lining things up in two dimensions, whereas flexbox is ideally suited for lining things up in one dimension.

![](../../.gitbook/assets/image%20%28169%29.png)

![](../../.gitbook/assets/image%20%2824%29.png)

But Grid can be used in one-dimension only.

![](../../.gitbook/assets/image%20%2865%29.png)

![](../../.gitbook/assets/image%20%2872%29.png)

Flex only needs to be used when you need to control the distribution of the elements. In the layout below, the elements within the Yellow and Red sections will evenly distribute themselves by default and so do not need to be in a flex container.

![](../../.gitbook/assets/image%20%28114%29.png)

Whereas, in the following examples, the elements take up different proportions of the container and the order of the elements is reversed. These are properties of the flex container.

![](../../.gitbook/assets/image%20%28159%29.png)

![](../../.gitbook/assets/image%20%2884%29.png)

## Flexbox Wrapping

Flexbox can wrap elements, but it still is only laying the elements out in a single direction.

![](../../.gitbook/assets/image%20%2856%29.png)

![](../../.gitbook/assets/image%20%2826%29.png)

{% embed url="https://codepen.io/rachelandrew/pen/YqqdXL" caption="" %}

## Flexbox is ideally suited for one-dimension

This example demonstrates the different flex settings and how it effects the layout of a horizontal `<nav>` element.

{% embed url="https://codepen.io/chriscoyier/pen/FAbpm" caption="" %}

## Resources

{% embed url="https://www.youtube.com/watch?v=hs3piaN4b5I" caption="" %}

