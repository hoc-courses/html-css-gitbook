# Element Flow

Here are some very important characteristics of how elements are rendered on a page:

### [Box Model](box-model-box-sizing.md)

Every element on a page is displayed as a rectangular box

**Content** - The actual content \(text, images, videos...\) of the HTML element.

**Padding** - Defined by the padding property. In-between the border and content of an element. It is transparent.

**Border** - Defined by the border property. Surrounds the padding and content of an element.

**Margin** - Defined by the margin property. Adds space between the border and other HTML elements. Is transparent.

![](../../.gitbook/assets/image%20%28257%29.png)

### Element Flow

* Without added positioning styles, the boxes flow from top to bottom. 
* Properties that specify position are needed to place HTML elements outside of this default flow.

### [Block vs Inline Elements](element-flow-part-2.md)

The CSS display property has two primary values that are used to determine how much horizontal and vertical space a box takes up.

* **block**: take up the entire line, unless they are empty. headings, paragraphs, lists are examples of elements that have their display property set to block by default. 
* **inline**: take up width of their content only. images, links, spans are examples of elements that have their display property set to inline by default.

