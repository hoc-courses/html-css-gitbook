# Evolution of the Web Page

## History of HTML

In 1980, physicist Tim Berners-Lee, proposed a system for researchers to share documents. Ten years later, he specified the **HTML** language and wrote the browser and server software for the first operational system.

It consisted of a communication system between web browsers and servers where a user could request a document with a unique resource ID \(URL\) from a web server, and the web server would respond to the request and return the document to the browser to display.

Embedded within the text of the document were **hyper-links** to other documents so that it was possible to refer to other documents and simply click on the link to switch to viewing the new document.

![](../.gitbook/assets/image%20%28201%29.png)

In the initial version, the content of the documents was limited to text, lists, hyper-links, and images. There was no styling. The content just flowed down the page from top to bottom.

![](../.gitbook/assets/image%20%28193%29.png)

#### HTML - Hypertext Markup Language

Within the document, the text was annotated to describe the structure and content using a mark-up language, called HTML. 

In computer text processing, a markup language is **a system for annotating a document in a way that is visually distinguishable from the content**. It is used only to format the text, so that when the document is processed for display, the markup language does not appear. The idea and terminology evolved from the "marking up" of paper manuscripts \(i.e., the revision instructions by editors\), which is traditionally written with a red pen or blue pencil on authors' manuscripts. - _Wikipedia_

HTML consists of a set of **markup elements** \(opening and closing tags\) that **wrap the text** to mark them for specific formatting. Additionally, **markup attributes** \(name=value pairs on the  beginning tag\) are used to specify additional information. 

For example, in the HTML document below, the ****`<h1>`and `<h3>`elements are used to indicate **headings** of varying importance. There are six possible heading elements ranging from `<h1>`being the most important \(larger, bolder\) to `<h6>`being the least important.

The `<p>`element specifies a paragraph.

The `<ul>`and `<li>`elements specify a list and the items within the list.

The `<Img>`element specifies an image, and the **src attribute** specifies the location \(URL\) where the image file resides. When the web browser is loading the HTML document, and it encounters and ****`<img>`element, it reads the src attribute value, and makes a request to the web server to retrieve the image file and displays it in the browser.

The `<a>`element ****specifies a hyper-link to another document. When it is clicked by the user, the web browser will initiate a new HTML document request for the document specified in the **href attribute.**

```markup
<html>
  <body>
    <h1>Page Title</h1>
    <h3>Section 1</h3>
    <img src="https://images.unsplash.com/photo-1507413245164-6160d8298b31?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8c2NpZW5jZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60" />
    <h3>Section 2</h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      commodo consequat. <a href="">Duis aute irure dolor</a> in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
      est laborum.
    </p>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
  </body>
</html>
```

#### Major Feature Enhancements

As the popularity of the web increased, there was demand for more features.

* **Styling \(1999\)** - the ability to apply styles to the HTML elements, such as colors, fonts, and layout of elements.
* **Interactivity \(1999\)** - the ability to have the page change what is displayed based on input from the user.
* **Ajax \(2005\) - A**synchronous **Ja**vaScript and **X**ML, enabled Single-Page web applications that act more like Desktop Applications. Gmail or Google Maps were the first.
* **Audio, Video, Canvas to support drawing \(2016 - HTML 5\)**

## HTML/CSS/JAVASCRIPT

Modern web pages depend on two additional technologies beyond HTML: **CSS** and **JavaScript**. These three components provide the underpinning of every web page.

All the front-end libraries and frameworks that web developers use to build web sites are just making it easier to create a web pages that contain these three components.

So, let's breakdown these three components and what their individual purposes are.

| Technology | Description |
| :--- | :--- |
| **HTML** | **Hypertext Markup Language**. A _mark-up language_ to describe the content of web pages |
| **CSS** | **Cascading Style Sheet** - A _stylesheet language_ used to express the presentation of web pages. |
| **JavaScript** | A **programming language** used for both front-end and back-end development. |

![](../.gitbook/assets/image%20%2859%29.png)

## Best Explained with Examples

## HTML/CSS - Resume

A good analogy for the HTML/CSS relationship within a web page is when you are creating a resume.

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>HTML</b> - Text Content</th>
      <th style="text-align:left"><b>HTML</b> - Structure</th>
      <th style="text-align:left"><b>CSS - Style</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <ul>
          <li>Personal Info</li>
          <li>Work Experience</li>
          <li>Education</li>
          <li>Extra-curriculars</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Headings</li>
          <li>Bullet List, Ordered List</li>
          <li>Paragraphs</li>
          <li>Image</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>Colors</li>
          <li>Fonts</li>
          <li>Font-size</li>
          <li>Positioning</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

![](../.gitbook/assets/image%20%28206%29.png)

![](../.gitbook/assets/image%20%28205%29.png)

{% embed url="https://codepen.io/annechinn/embed/LYxmMZJ?" %}

## HTML/CSS - CSSZenGarden.com

The site [csszengarden.com](http://csszengarden.com) is a site that educates on the role CSS plays in design and has a link to provide both the HTML and CSS files separately and to view the impact CSS can make.

Go to the site, and click on the HTML FILE link to download the HTML file. Then display that file in your browser by dragging in from your file explorer to a web browser window.

![](../.gitbook/assets/image%20%28131%29.png)

Below is the HTML with no CSS applied. Very basic, just text, links, and some standard headings.

![](../.gitbook/assets/image%20%2813%29.png)

## What a Difference CSS can Make!

Next, click on the VIEW ALL DESIGNS link and browse through each of the different design links on the right. Each of these designs has the exact same underlying HTML content, just a different stylesheet!

**Note**: These examples on the site are periodically updated, so these may not represent what is currently on the site.

![](../.gitbook/assets/image%20%2852%29.png)

![](../.gitbook/assets/image%20%28119%29.png)

![](../.gitbook/assets/image%20%28132%29.png)

## CSS - Animation

{% embed url="https://codepen.io/everylastpixel/pen/QWybxmV" caption="" %}

## JavaScript - Animation

First, JavaScript can be used to add what I'd call eye-candy to the site. The content is all there, but it's dull without some action. JavaScript can be used to display the content in visually appealing ways and add movement with advanced animations. Below is an example of JavaScript being use in this capacity.

{% embed url="https://www.charles-richard.net/" caption="" %}

{% embed url="https://www.legworkstudio.com" caption="" %}

{% embed url="http://knowlupus.org" caption="" %}

{% embed url="https://www.sbs.com.au/theboat/" caption="" %}

{% embed url="https://mrdoob.com/projects/chromeexperiments/ball-pool/" caption="" %}

### Canvas - 2D/3D Graphics

{% embed url="http://www.craftymind.com/factory/html5video/CanvasVideo.html" %}

{% embed url="https://codepen.io/soulwire/full/Ffvlo" %}



## JavaScript - Seamlessly Updates Content with AJAX

* Users want a Desktop feel. No full page refreshes on changes.
* JavaScript communicates with back-end services to retrieve/update data.

**Google Search Input** - A really good example of this is the Google Search screen. As the user types into the search input box, JavaScript is being used to communicate with the server and seamlessly retrieve and present relevant search strings based on what the user is typing.

{% hint style="info" %}
Take a look at the Console Developer Tools Network Tab to see the network traffic.
{% endhint %}

![](../.gitbook/assets/image%20%2817%29.png)

**NY Times** - **Article Comments**

{% embed url="https://www.nytimes.com/2021/04/06/dining/croissant-recipes.html" caption="" %}

* Navigate to the article, click on the Comments button at the bottom
* JavaScript responds to the button click, sends as request to the server for all of the comments for the article, and then, without updating the entire page, inserts the new section for the user to interact with the comments.

### Summary

![](../.gitbook/assets/image%20%2843%29.png)

#### HTML - Structure/Content

```markup
<h1>Hello World!</h1>
```

#### CSS - Styles

```css
h1 {
    padding-top: 0;
    padding-bottom: 5px;
    border-bottom: none;
    font-family: 'Julius Sans One', sans-serif;
    font-size: 3.2em;
    text-transform: uppercase;
}
```

#### JavaScript - Interactivity

![](../.gitbook/assets/image%20%2871%29.png)

```javascript
function processForm(event) {
  event.preventDefault();
  
  let form = document.getElementById("form");

  let username = form.elements.username.value);
  let password = form.elements.password.value);
  
  // call to the server with the username/password
  // to authenticate the user and redirect to
  // the dashboard page if succeeds
 } 
```

