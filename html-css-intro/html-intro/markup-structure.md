# Markup

## HTML is a Markup-Language

A mark-up language is different than a programming language. It doesn't have any programming logic or code that is executed to perform some action. It just allows you to annotate the text in the document to provide extra meaning to the content. The browser uses those annotations to know how to display the page.

### **Elements**

HTML elements are the building blocks for defining the structure of the page content. Each **element** has an opening and closing **tag.**  The closing tag has a "/" symbol before the tag-name. The content that falls between the opening and closing tags is the content of that element. 

![](../../.gitbook/assets/image%20%2827%29.png)

The element provides information about the content that lies between the tags.  Each **element type** \(`<h1>`, `<p>`, `<img>`, etc.\) has a unique purpose. For example, the `h1` element surrounds text that should be formatted to indicate the title of the page.

```markup
<h1> Welcome to this Page</h1>
```

### **Attributes** 

Attributes are used to specify additional information about the element. Attributes are specified on the opening element tag. An attribute consists of two parts: the attribute name \(use lower case\) and a value \(wrap in double-quotes\). Not all elements have attributes,  as we saw with the `<h1>` element above. They are necessary when the element requires additional information.

![](../../.gitbook/assets/image%20%2848%29.png)

For example, an  `<img>` element requires a **src attribute**, to specify the URL for the image file.

```markup
<img src="logo.jpg"></img>
```

And the `<a>` element, used for hyper-links to other documents, requires the **href attribute** to specify the URL for the document to load when the anchor is clicked.

```markup
<a href="http://www.google.com">Google</a>
```

### Self-Closing Tags

Some elements do not contain any content between the opening and closing tags. In this case, the element is called a **self-closing tag** and can be simplified by having just a single tag with the "/" symbol at the end.

The image element is a self-closing tag and can be written as follows.

```markup
<img src="logo.jpg"/>
```

{% hint style="info" %}
For a full list of the self-closing elements, see the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Glossary/Empty_element).
{% endhint %}

## HTML Elements Can Be Nested

The element content is not always text. It can be another element. For example,  the `<a>` element ****contains content, that when clicked, will cause the browser to navigate to a new document. In most cases, the content is some text that is displayed to the user. But, an image can also be the content within an anchor element, such as when you click on the logo for a site to return to the Home page.

```markup
<a href="home.html"><img src="logo.jpg"/></a>
```

The entire HTML document is a hierarchy of nested HTML elements. The HTML is not valid if the elements do not have the correct opening and closing tags.

```markup
<body>
    <h2>Loreum Ipsum</h2>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Nunc mattis enim ut tellus elementum sagittis vitae. In iaculis nunc sed augue lacus viverra vitae. Nec ullamcorper sit amet risus
        nullam eget felis eget. Sed nisi lacus sed viverra tellus in hac habitasse platea. Integer malesuada nunc vel risus. Hendrerit gravida rutrum quisque non. Fusce ut placerat orci nulla. Enim lobortis scelerisque fermentum dui faucibus in ornare
        quam. Id leo in vitae turpis massa sed elementum tempus. Eu tincidunt tortor aliquam nulla facilisi cras. Laoreet id donec ultrices tincidunt. Nec nam aliquam sem et tortor consequat. Imperdiet dui accumsan sit amet nulla facilisi morbi tempus.
        Suspendisse potenti nullam ac tortor vitae purus faucibus. Viverra suspendisse potenti nullam ac tortor vitae purus faucibus.
    </p>
    <ul>
      <li>consectetur adipiscing</li>
      <li>
          <span>turpis massa</span>
      </li>
      <li>leo in vitae</li>
    </ul>
    <p>
        <img src="image1.jpg">
    </p>
</body>
```

## Browsers are Forgiving

While there are ways to enforce HTML code to follow the rules, browsers have always attempted to gracefully handle errors in HTML. The HTML that currently exists on the web is full of such errors, so it is not possible to change this behavior.

It's up to you to carefully review your HTML to make sure the syntax is correct, otherwise you'll get unexpected results as the web browser attempts to correct errors.

## White-space in HTML is ignored

You can add as much white-space as you want within the text of an element, and it will be ignored.

```markup
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor incididunt ut labore et dolore 
        magna aliqua. Ut enim ad minim veniam, quis nostrud 
        exercitation ullamco laboris nisi ut aliquip ex ea 

        a
        a
        as  b
        s fsd
         g sdfa g



        commodo consequat. Duis aute irure dolor in reprehenderit 
        in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
         Excepteur sint occaecat cupidatat non proident, 
         sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
```

![](../../.gitbook/assets/image%20%2820%29.png)

## Comments are Ignored

Anything that starts with **&lt;!--** and ends with **--&gt;** will be ignored by the browser. This is useful for documenting your code and making notes to yourself, or for commenting out HTML that you are debugging.

```markup
<body>
    <!-- This will be ignored -->
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor</p>
    <!-- <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor</p> -->  
</body>
```

### HTML - Hypertext Markup Language

> In computer text processing, a markup language is **a system for annotating a document in a way that is visually distinguishable from the content**. It is used only to format the text, so that when the document is processed for display, the markup language does not appear. The idea and terminology evolved from the "marking up" of paper manuscripts \(i.e., the revision instructions by editors\), which is traditionally written with a red pen or blue pencil on authors' manuscripts. - _Wikipedia_

HTML is use to annotate \(mark-up\) the content within a web page document.

HTML consists of **markup elements** \(opening and closing tags\) that **wrap content** to mark it for specific formatting.  

![](../../.gitbook/assets/image%20%28266%29.png)

Markup elements can contain **attributes** \(name/value pairs\)  **on the opening tag** to specify additional information.

![](../../.gitbook/assets/image%20%28254%29.png)

&lt;a href="http://page2.html" &gt;Go to Page 2&lt;/a&gt;

In the early days of the web, the set of markup elements available was very limited and there was no CSS or styling. The main elements where: 

* title \(`<title>`\)
* headings \(`<h1-h6>`\)
* paragraphs \(`<p>`\)
* lists \(`<ul>`, `<li>`\)
* hyper-links \(`<a>`\) 
  * href attribute to specify the document URL

HTML was used to supply simple annotations to the text to tell the web browser how to format it.

### CSS - Cascading Style Sheets

HTML deals with meaning and content. CSS was introduced to allow the browser to apply specific styling features such as colors, fonts, and positioning to the HTML elements on the page. 

In HTML we wrap content with elements to specify how it should be structured. 

With CSS, we can use a stylesheet language to specify which styling properties we want to change for specific HTML elements.

To change the style of an element you must target the element using **selectors** and then specify one or more style property-name property-value pairs to apply to the targeted element.

![](../../.gitbook/assets/image%20%28215%29.png)

In the example above, the selector is the name of an HTML element. This would change the text color of every paragraph in the document to red.

#### What aspects of an HTML element can be styled?

The list is quite long. They can be loosely categorized into styles that deal with text and font, colors and backgrounds, margins, padding, and borders, and dimensions, display and positioning.

For a complete list, visit the website below.

{% embed url="https://htmldog.com/references/css/properties/" %}

### Resources

{% embed url="https://developer.mozilla.org/en-US/docs/Web/HTML/Element" %}

