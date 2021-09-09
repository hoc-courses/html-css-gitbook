# Flexbox

Flexbox is a name for a set of CSS layout rules for laying out items in rows or columns. They allow you to apply rules to elements to place them side-by-side and re-arrange them. You just specify how you want your elements arranged and the browser will scale this arrangement depending on the screen size and device used for viewing.

The flex layout consists of a parent container referred to as a _**flex container**_ and its **immediate children** which are called _**flex items**_.

### The Container

To create a flex container, just set the display property to flex. All of its immediate children will now be considered flex items.

![](../../.gitbook/assets/image%20%2828%29.png)

### The Container Items

![](../../.gitbook/assets/image%20%28157%29.png)

### Container properties

* **flex-direction** - specifies flow of the flex items

![](../../.gitbook/assets/image%20%2874%29.png)

* **flex-wrap** - specifies whether the flex items should wrap if necessary and how.

![](../../.gitbook/assets/image%20%28139%29.png)

* **justify-content** - aligns flex items along main axis of container distributing free space among the items. 

![](../../.gitbook/assets/image%20%2851%29.png)

* **align-items** - align flex items in the cross-axis direction.

![](../../.gitbook/assets/image%20%28153%29.png)

### Navigation Bar Example

A very common use-case for arranging element horizontally is a navigation bar. Navigation bars are usually built by using unordered lists because they already support a nested outline structure that is useful for navigation bars.

To use lists for navigation, we need to set the list-style-type property to none so that the bullet points do not show.

We will then have each list item flowing vertically down the screen.

```markup
 <nav>
   <ul>
     <li><a href="#">Section 1</a></li>
     <li><a href="#">Section 2</a></li>
     <li><a href="#">Section 3</a></li>
     <li><a href="#">Section 4</a></li>
     <li><a href="#">Section 5</a></li>
   </ul>
 </nav>
```

```css
ul {
  list-style-type:none;
}
```

![](../../.gitbook/assets/image%20%2816%29.png)

What we want is to have each list item flow horizontally across the screen as shown below.

![](../../.gitbook/assets/image%20%289%29.png)

To do this we must specify the html element that is the container of the elements we want to arrange. This would be the `<ul>` element that is the parent of each of the `<li>` elements.

```css
ul {
  list-style-type:none;
  display:flex;
  flex-direction:row;
}
```

### 

### Flex Item properties

* **order** - the order of the item within the children \(default to position in HTML\)

![](../../.gitbook/assets/image%20%2864%29.png)

* **flex-grow** - how much the flex item will grow in relation to other items when positive free space is distributed. The remaining space is the size of the flex container minus the size of all flex items' sizes together. If all sibling items have the same flex grow factor, then all items will receive the same share of remaining space, otherwise it is distributed according to the ratio defined by the different flex grow factors. The default value is zero.

![](../../.gitbook/assets/image%20%28138%29.png)

* **flex-shrink** - how much the flex item will shrink in relation to other items when negative free space is distributed.

## Resources

{% embed url="https://css-tricks.com/snippets/css/a-guide-to-flexbox/" caption="" %}

{% embed url="https://scrimba.com/learn/flexbox/your-first-flexbox-layout-flexbox-tutorial-canLGCw" caption="" %}

