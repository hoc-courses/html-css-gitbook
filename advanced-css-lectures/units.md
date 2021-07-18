# Units

There are many CSS properties whose value represents a length. For example, width, margin, padding, font-size all expect a length value. But lengths can be expressed in different units and it is important to know the differences between them.

## Absolute Units

Absolute units are not relative to anything else and generally stay the same size. They are not affected by any screen size or fonts.

**Pixels - px \(**1px = 1/96th of 1 inch\) _\*\*_are the absolute unit that is used in web design. Pixels are very easy to use, because they specify the exact length. But they are not s good choice for accessibility. For example, if you increase your font to large in your browser settings, your hard-coded absolute font-sizes will not change.

## Font-relative Units

**em -** Em inherits size from its immediate parent’s font size. Say, if a parent element has font-size:18px, then 1em will be measured as 18px for all its child’s.

The advantage of using em is, if you decide to change the font-size, padding, and margin of each element proportionately, then you just have to change the parent element font size and all other elements will adjust accordingly.

That won’t be the case with absolute units like px, where you have to adjust each element individually.

**rem** - rem units always refer to the root element font size, not the parent element.

## Viewport-relative Units

There are a few units that depend on the viewport height and width.

{% hint style="info" %}
The **viewport** is the user's visible area of a web page. The **viewport** varies with the device, and will be smaller on a mobile phone than on a computer screen
{% endhint %}

Vh \(viewport height\) is measured as 1vh equal to 1% of the viewport’s height. This unit is very useful for creating full height elements. Vh reacts similarly to percentage, but doesn’t depend on the parent element height.

You can use vh anywhere but the most common use case of vh is for making full height elements.

## Percentage

Percentage\(%\) unit doesn’t belong to a any particular category mentioned above, but can be categorized as a relative unit. It is relative to its parent element.

Percentage is primarily associated with height and width of an element, but can be used anywhere where CSS length units are allowed.

## Resources

{% embed url="https://getflywheel.com/layout/choose-css-unit-create-better-site-layouts-how-to/" caption="" %}

