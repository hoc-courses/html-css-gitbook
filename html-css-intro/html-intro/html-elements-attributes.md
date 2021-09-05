# HTML Elements/Attributes

### HTML Element Syntax

![](../../.gitbook/assets/image%20%283%29.png)

#### HTML Elements

HTML consists of **markup elements** \(opening and closing tags\) that **wrap content** to mark it for specific formatting.

#### HTML Attributes

Markup elements can contain **attributes** \(name/value pairs\) **on the opening tag** to specify additional information.

```markup
<a href="https://jellyfish.html">Jelly Fish Facts</a>
```

* A **tag** is the HTML element name enclosed in angle brackets
  * `<a>` is the **opening tag**
  * `</a>` is the **closing tag**
* An **attribute** comes after the HTML element name within the angle brackets
  * `href="https://jellyfish.html"` is the **attribute**
  * `href` is the **attribute name**
  * `http://jellyfish.html` is the **attribute value**
* The **content** is the part of the code in between the opening and closing tags
  * `Jelly Fish Facts` is the **content**

{% hint style="success" %}
**Test for Understanding**: In the code sample below:

* Which elements have content?
* Which elements do not have content?
* How can you tell the difference?
* What elements have attributes?
{% endhint %}

```markup
<article>
  <h1>Learning HTML</h1>
  <p>Get to know the HTML basics.</p>
  <a href="http://html5rocks.com">Read Article</a>
  <img src="images/photo.jpg"/>
</article>
```

#### Self-closing elements

Some elements do not contain any content between the opening and closing tags. In this case, the element is called a **self-closing tag** and can be simplified by having just a single tag with the "/" symbol at the end.

The image element is an example of a self-closing tag and can be written as follows.

```markup
<img src="logo.jpg"/>
```

For a full list of self-closing elements, see the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Glossary/Empty_element).

### Common HTML Elements

There are lots of different markup elements: too many to list here. There's a small set that you will use very frequently and then some more obscure ones that you will use for specialized situations. The elements, and their attributes are not something that you need to memorize. You learn to use them as you need them and can always consult the online documentation.

These are the most common:

* [text-formatting](text-formatting-elemetns.md) \(headers, lists, emphasis, pull quotes, paragraph, etc.\)
* [image](images.md)
* [hyper-links](links.md) \(anchors\) 
* [videos](video.md)
* [forms](../../miscellaneous-topics/forms.md)
* [tables](tables.md)

### 

### Miscellaneous

#### Adding comments in HTML

Anything that starts with **&lt;!--** and ends with **--&gt;** will be ignored by the browser. This is useful for documenting your code and making notes to yourself, or for commenting out HTML that you are debugging.

```markup
<body>
    <!-- This will be ignored -->
    <p>Lorem ipsum dolor sit amet, consectetur 
        sed do eiusmod tempor</p>
    <!-- <p>Lorem ipsum dolor sit amet, consect, 
        sed do eiusmod tempor</p> -->  
</body>
```

#### White-space in HTML is ignored

You can add as much white-space as you want within the text of an element, and it will be ignored.

![](../../.gitbook/assets/image%20%28275%29.png)

#### Browsers are Forgiving

While there are ways to enforce HTML code to follow the rules, browsers have always attempted to gracefully handle syntax errors in HTML. The HTML that currently exists on the web is full of such errors, so it is not possible to change this behavior now without breaking lots of websites.

It's up to you to carefully review your HTML code to make sure the syntax is correct, otherwise you'll get unexpected results as the web browser attempts to correct errors.

