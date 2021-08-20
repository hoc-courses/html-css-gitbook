# HTML

## HTML is a Markup-Language

A mark-up language is different than a programming language. It doesn't have any programming logic or code that is executed to perform some action. It just allows you to annotate the text in the document to provide extra meaning to the content. The browser uses the annotations to know how to display the page.

> In computer text processing, a markup language is **a system for annotating a document in a way that is visually distinguishable from the content**. It is used only to format the text, so that when the document is processed for display, the markup language does not appear. The idea and terminology evolved from the "marking up" of paper manuscripts \(i.e., the revision instructions by editors\), which is traditionally written with a red pen or blue pencil on authors' manuscripts. - _Wikipedia_

\_\_

HTML consists of **markup elements** \(opening and closing tags\) that **wrap content** to mark it for specific formatting.  

![](../../.gitbook/assets/image%20%28281%29.png)

Markup elements can contain **attributes** \(name/value pairs\)  **on the opening tag** to specify additional information.

![](../../.gitbook/assets/image%20%28262%29.png)

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
**Test for Understanding**: Identify opening and closing tags, attribute name/values and content in the following HTML.
{% endhint %}

```markup
<h1>Meet the Jellies</h1>
<ul>
  <li>Orange Jelly</li>
  <li>Pink Jelly</li>
  <li>Yellow Jelly</li>
</ul>

<h2>Orange Jelly</h2>
<img src="images/orange-jellyfish.jpg"/>
<p>This jelly fish is orange</p>

<h2>Pink Jelly</h2>
<img src="images/pink-jellyfish.jpg"/>
<p>This jelly fish is pink</p>

<h2>Yellow Jelly</h2>
<img src="images/yellow-jellyfish.jpg"/>
<p>This jelly fish is yellow</p>

<h3>More Resources</h3>
<a href="https://jellyfish.html">
  Jelly Fish Facts
</a>
```

There are lots of different markup elements: too many to list here. The [text-formatting](text-formatting-elemetns.md), [image](images.md) and [hyper-links](links.md) \(anchors\) elements, many of which were used in the example above, are what you will use most frequently. Other common elements support including [videos](video.md), [forms](../../miscellaneous-topics/forms.md) and [tables ](../../miscellaneous-topics/tables.md)in your page.

### Miscellaneous

#### Self-closing elements

Some elements do not contain any content between the opening and closing tags. In this case, the element is called a **self-closing tag** and can be simplified by having just a single tag with the "/" symbol at the end.

The image element is an example of a self-closing tag and can be written as follows.

```markup
<img src="logo.jpg"/>
```

For a full list of self-closing elements, see the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Glossary/Empty_element).

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

