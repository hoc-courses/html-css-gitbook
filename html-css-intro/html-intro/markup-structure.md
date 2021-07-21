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

### Resources

{% embed url="https://developer.mozilla.org/en-US/docs/Web/HTML/Element" %}

