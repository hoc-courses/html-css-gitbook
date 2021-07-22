# Anatomy of a Web Page

### First HTML Documents

In 1980, physicist Tim Berners-Lee, proposed a system for researchers to share documents. Ten years later, he specified the **HTML** language and wrote the browser and server software for the first operational system.

It consisted of a communication system between web browsers and servers where a user could request a document with a unique resource ID \(URL\) from a web server, and the web server would respond to the request and return the document to the browser to display.

Embedded within the text of the document were **hyper-links** to other documents so that it was possible to refer to other documents and simply click on the link to switch to viewing the new document.

![](../.gitbook/assets/image%20%28201%29.png)

### **Modern Web Pages**

Modern web pages depend on two additional technologies beyond HTML: **CSS** and **JavaScript**. These three components provide the underpinning of every web page.

| Technology | Description |
| :--- | :--- |
| **HTML** | **Hypertext Markup Language**. A _mark-up language_ to describe the content of web pages |
| **CSS** | **Cascading Style Sheet** - A _stylesheet language_ used to express the presentation of web pages. |
| **JavaScript** | A **programming language** used for both front-end and back-end development to add interactivity. |

![](../.gitbook/assets/image%20%2859%29.png)

### HTML - Hypertext Markup Language

> In computer text processing, a markup language is **a system for annotating a document in a way that is visually distinguishable from the content**. It is used only to format the text, so that when the document is processed for display, the markup language does not appear. The idea and terminology evolved from the "marking up" of paper manuscripts \(i.e., the revision instructions by editors\), which is traditionally written with a red pen or blue pencil on authors' manuscripts. - _Wikipedia_

HTML is use to annotate \(mark-up\) the content within a web page document.

HTML consists of **markup elements** \(opening and closing tags\) that **wrap content** to mark it for specific formatting.  

![](../.gitbook/assets/image%20%28264%29.png)

Markup elements can contain **attributes** \(name/value pairs\)  **on the opening tag** to specify additional information.

![](../.gitbook/assets/image%20%28240%29.png)

&lt;a href="http://page2.html" &gt;Go to Page 2&lt;/a&gt;

In the early days of the web, the set of markup elements available was very limited and there was no CSS or styling. The main elements where: 

* title \(`<title>`\)
* headings \(`<h1-h6>`\)
* paragraphs \(`<p>`\)
* lists \(`<ul>`, `<li>`\)
* hyper-links \(`<a>`\) 
  * href attribute to specify the document URL

HTML was used to supply simple annotations to the text to tell the web browser how to format it.

#### Here is a sample document without any HTML markup.

![](../.gitbook/assets/image%20%28113%29.png)

#### And the same document with HTML markup.

![](../.gitbook/assets/image%20%28253%29.png)

### CSS - Cascading Style Sheets

HTML deals with meaning and content. CSS was introduced to allow the browser to apply specific styling features such as colors, fonts, and positioning to the HTML elements on the page. 

In HTML we wrap content with elements to specify how it should be structured. 

With CSS, we can use a stylesheet language to specify which styling properties we want to change for specific HTML elements.

To change the style of an element you must target the element using **selectors** and then specify one or more style property-name property-value pairs to apply to the targeted element.

![](../.gitbook/assets/image%20%28195%29.png)

In the example above, the selector is the name of an HTML element. This would change the text color of every paragraph in the document to red.

#### What aspects of an HTML element can be styled?

The list is quite long. They can be loosely categorized into styles that deal with text and font, colors and backgrounds, margins, padding, and borders, and dimensions, display and positioning.

For a complete list, visit the website below.

{% embed url="https://htmldog.com/references/css/properties/" %}

#### CSS - CSSZenGarden.com

The site [csszengarden.com](http://csszengarden.com) is a site that educates on the role CSS plays in design and has a link to provide both the HTML and CSS files separately and to view the impact CSS can make.

Go to the site, and click on the HTML FILE link to download the HTML file. Then display that file in your browser by dragging in from your file explorer to a web browser window.

![](../.gitbook/assets/image%20%28131%29.png)

Below is the HTML with no CSS applied. Very basic, just text, links, and some standard headings.

![](../.gitbook/assets/image%20%2813%29.png)

#### What a Difference CSS can Make!

Next, click on the VIEW ALL DESIGNS link and browse through each of the different design links on the right. Each of these designs has the exact same underlying HTML content, just a different stylesheet!

**Note**: These examples on the site are periodically updated, so these may not represent what is currently on the site.

![](../.gitbook/assets/image%20%2852%29.png)

![](../.gitbook/assets/image%20%28119%29.png)

![](../.gitbook/assets/image%20%28132%29.png)

### 

### JavaScript - Programming/Interactivity

JavaScript is a programming language that enables web pages to provide animation, interactivity, and the relatively recent advances that makes websites behave more like desktop applications. 

#### JavaScript - Animation

JavaScript can be used to add what I'd call eye-candy to the site. The content is all there, but it's dull without some action. JavaScript can be used to display the content in visually appealing ways and add movement with advanced animations.

{% embed url="https://www.legworkstudio.com" caption="" %}

{% embed url="https://www.sbs.com.au/theboat/" caption="" %}

{% embed url="https://mrdoob.com/projects/chromeexperiments/ball-pool/" caption="" %}

#### JavaScript - Single Page Applications

In the last ten years there's been a huge change in how web sites update their content. It used to be that a web site consisted of a collection of individual pages with hyper-links between them. Clicking on a hyper-link would initiate a request to the web server for the new page and that page would be retrieved and replace the current page in the browser. This model lead to web sites feeling clunky and disjointed. 

Most web applications now attempt to mimic a desktop experience in that there isn't the constant refreshing of the web site when new pages are requested from the server. For example, Gmail, Google Maps, Google Drive, Twitter and Facebook all feel like a real application, but on the web.

A single page application creates the illusion of a page change, but you are actually on the same page the entire time you are on the site. The URL is changing as you navigate around the site, even though no new page is being loaded from the server.

**Google Search Input** - A really good example of this is the Google Search screen. As the user types into the search input box, JavaScript is being used to communicate with the server and seamlessly retrieve and present relevant search strings based on what the user is typing.

{% hint style="info" %}
Take a look at the Console Developer Tools Network Tab to see the network traffic.
{% endhint %}

![](../.gitbook/assets/image%20%2817%29.png)

**NY Times** - **Article Comments**

{% embed url="https://www.nytimes.com/2021/04/06/dining/croissant-recipes.html" caption="" %}

* Navigate to the article, click on the Comments button at the bottom
* JavaScript responds to the button click, sends as request to the server for all of the comments for the article, and then, without updating the entire page, inserts the new section for the user to interact with the comments.

