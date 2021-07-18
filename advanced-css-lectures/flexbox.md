# Flexbox

The flex layout consists of parent container referred as _flex container_ and its **immediate children** which are called _flex items_.

## The Container

To create a flex container, just set the display property to flex. All of its immediate children will now be considered flex items.

```css
.flex-container {
    display: flex;
}
```

![](../.gitbook/assets/image%20%2828%29.png)

## The Container Items

![](../.gitbook/assets/image%20%28157%29.png)

### Container properties

* **flex-direction** - specifies flow of the flex items

![](../.gitbook/assets/image%20%2874%29.png)

* **flex-wrap** - specifies whether the flex items should wrap if necessary and how.

![](../.gitbook/assets/image%20%28139%29.png)

* **justify-content** - aligns flex items along main axis of container distributing free space among the items. 

![](../.gitbook/assets/image%20%2851%29.png)

* **align-items** - align flex items in the cross-axis direction.

![](../.gitbook/assets/image%20%28153%29.png)

### Flex Item properties

* **order** - the order of the item within the children \(default to position in HTML\)

![](../.gitbook/assets/image%20%2864%29.png)

* **flex-grow** - how much the flex item will grow in relation to other items when positive free space is distributed.

![](../.gitbook/assets/image%20%28138%29.png)

* **flex-shrink** - how much the flex item will shrink in relation to other items when negative free space is distributed.

## Resources

{% embed url="https://css-tricks.com/snippets/css/a-guide-to-flexbox/" caption="" %}

{% embed url="https://scrimba.com/learn/flexbox/your-first-flexbox-layout-flexbox-tutorial-canLGCw" caption="" %}

