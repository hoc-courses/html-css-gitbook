# Typography Best-Practices

#### Make sure to set a good max-width for our paragraphs but also ensure that we set the widths on a parent class to keep our code readable.

This is typically referred to as the **measure** in typographic circles and highly esteemed typographers will recommend that a paragraph have a width of around 75 characters for legibility reasons. Anything longer than that becomes difficult to read and causes unnecessary strain on the eyes because of the distance the eye has to travel left-to-right and back again \(assuming `ltr` that is\).

```markup
<div class="container">
  <p>This is where our text goes.</p>
</div>
```

```css
p {
  font-size: 18px;
  line-height: 24px;
}

.container {
  max-width: 600px;
}
```

#### Example: Medium

See how the paragraph text of the article width is limited and makes it easier to read.

{% embed url="https://medium.com/weekly-webtips/react-ecosystem-in-2021-87da221e5f71" %}



{% embed url="https://css-tricks.com/six-tips-for-better-web-typography/" %}



