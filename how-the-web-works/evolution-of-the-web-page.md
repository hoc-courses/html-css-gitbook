# Evolution of the Web Page

## History of HTML

In 1980, physicist Tim Berners-Lee, proposed a system for researchers to share documents. Ten years later, he specified the **HTML** language and wrote the browser and server software for the first operational system.

It consisted of a communication system between web browsers and servers where a user could request a document with a unique resource ID \(URL\) from a web server, and the web server would respond to the request and return the document to the browser to display.

Embedded within the text of the document were **hyper-links** to other documents so that it was possible to refer to other documents and simply click on the link to switch to viewing the new document.

![](../.gitbook/assets/image%20%28201%29.png)

#### HTML - Hypertext Markup Language

Within the document, the text was annotated to describe the structure and content using a mark-up language, called HTML. 

In computer text processing, a markup language is **a system for annotating a document in a way that is visually distinguishable from the content**. It is used only to format the text, so that when the document is processed for display, the markup language does not appear. The idea and terminology evolved from the "marking up" of paper manuscripts \(i.e., the revision instructions by editors\), which is traditionally written with a red pen or blue pencil on authors' manuscripts. - _Wikipedia_

HTML consists of a set of **markup elements** \(opening and closing tags\) that **wrap the text** to mark them for specific formatting as well as **markup attributes** \(name/value pairs\) **on the opening element tag** used to specify additional information.

#### Initial Version

In the initial version, the set of markup elements available was very limited. The main elements where: 

* title \(`<title>`\)
* headings \(`<h1-h6>`\)
* paragraphs \(`<p>`\)
* lists \(`<ul>`, `<li>`\)
* hyper-links \(`<a>`\) 
  * href attribute specifies document URL

The content is just text, and you can use the markup elements to annotate sections of the text to tell the web browser how to display it.

#### Here's the text content without any markup

```markup
A history of HTML

Included in this chapter is information on:
How the World Wide Web began

The events and circumstances that led to the World Wide Web's current popularity

How HTML has grown from its conception in the early 1990s

Summary
HTML has had a life-span of roughly seven years. During that time, it has evolved from a simple language with a small number of tags to a complex system of mark-up, enabling authors to create all-singing-and-dancing Web pages complete with animated images, sound and all manner of gimmicks. This chapter tells you something about the Web's early days, HTML, and about the people, companies and organizations who contributed to HTML+, HTML 2, HTML 3.2 and finally, HTML 4.

This chapter is a short history of HTML. Its aim is to give readers some idea of how the HTML we use today was developed from the prototype written by Tim Berners-Lee in 1992. The story is interesting - not least because HTML has been through an extremely bumpy ride on the road to standardization, with software engineers, academics and browser companies haggling about the language like so many Ministers of Parliament debating in the House of Commons.

1989: Tim Berners-Lee invents the Web with HTML as its publishing language
The World Wide Web began life in the place where you would least expect it: at CERN, the European Laboratory for Particle Physics in Geneva, Switzerland. CERN is a meeting place for physicists from all over the world, where highly abstract and conceptual thinkers engage in the contemplation of complex atomic phenomena that occur on a minuscule scale in time and space. This is a surprising place indeed for the beginnings of a technology which would, eventually, deliver everything from tourist information, online shopping and advertisements, financial data, weather forecasts and much more to your personal computer.

Tim Berners-Lee is the inventor of the Web. In 1989, Tim was working in a computing services section of CERN when he came up with the concept; at the time he had no idea that it would be implemented on such an enormous scale. Particle physics research often involves collaboration among institutes from all over the world. Tim had the idea of enabling researchers from remote sites in the world to organize and pool together information. But far from simply making available a large number of research documents as files that could be downloaded to individual computers, he suggested that you could actually link the text in the files themselves.

In other words, there could be cross-references from one research paper to another. This would mean that while reading one research paper, you could quickly display part of another paper that holds directly relevant text or diagrams. Documentation of a scientific and mathematical nature would thus be represented as a `web' of information held in electronic form on computers across the world. This, Tim thought, could be done by using some form of hypertext, some way of linking documents together by using buttons on the screen, which you simply clicked on to jump from one paper to another. Before coming to CERN, Tim had already worked on document production and text processing, and had developed his first hypertext system, `Enquire', in 1980 for his own personal use.

Tim's prototype Web browser on the NeXT computer came out in 1990.

Through 1990: The time was ripe for Tim's invention
The fact that the Web was invented in the early 1990s was no coincidence. Developments in communications technology during that time meant that, sooner or later, something like the Web was bound to happen. For a start, hypertext was coming into vogue and being used on computers. Also, Internet users were gaining in the number of users on the system: there was an increasing audience for distributed information. Last, but not least, the new domain name system had made it much easier to address a machine on the Internet.

Hypertext
lthough already established as a concept by academics as early as the 1940s, it was with the advent of the personal computer that hypertext came out of the cupboard. In the late 1980s, Bill Atkinson, an exceptionally gifted programmer working for Apple Computer Inc., came up with an application called Hypercard for the Macintosh. Hypercard enabled you to construct a series of on-screen `filing cards' that contained textual and graphical information. Users could navigate these by pressing on-screen buttons, taking themselves on a tour of the information in the process.

Hypercard set the scene for more applications based on the filing card idea. Toolbook for the PC was used in the early 1990s for constructing hypertext training courses that had `pages' with buttons which could go forward or backward or jump to a new topic. Behind the scenes, buttons would initiate little programs called scripts. These scripts would control which page would be presented next; they could even run a small piece of animation on the screen. The application entitled Guide was a similar application for UNIX and the PC.

Hypercard and its imitators caught the popular imagination. However, these packages still had one major limitation: hypertext jumps could only be made to files on the same computer. Jumps made to computers on the other side of the world were still out of the question. Nobody yet had implemented a system involving hypertext links on a global scale.

```

#### And with markup

```markup
<h1>A history of HTML</h1>

<h2>Included in this chapter is information on:</h2>
<ul>
  <li>How the World Wide Web began</li>
  
  <li>The events and circumstances that led to the World Wide Web's current popularity</li>
  
  <li>How HTML has grown from its conception in the early 1990s</li>
</ul>

<h2>Summary</h2>
<p>HTML has had a life-span of roughly seven years. During that time, it has evolved from a simple language with a small number of tags to a complex system of mark-up, enabling authors to create all-singing-and-dancing Web pages complete with animated images, sound and all manner of gimmicks. This chapter tells you something about the Web's early days, HTML, and about the people, companies and organizations who contributed to HTML+, HTML 2, HTML 3.2 and finally, HTML 4.</p>
<p>This chapter is a short history of HTML. Its aim is to give readers some idea of how the HTML we use today was developed from the prototype written by Tim Berners-Lee in 1992. The story is interesting - not least because HTML has been through an extremely bumpy ride on the road to standardization, with software engineers, academics and browser companies haggling about the language like so many Ministers of Parliament debating in the House of Commons.</p>


<h3>1989: Tim Berners-Lee invents the Web with HTML as its publishing language</h3>
<p>The World Wide Web began life in the place where you would least expect it: at CERN, the European Laboratory for Particle Physics in Geneva, Switzerland. CERN is a meeting place for physicists from all over the world, where highly abstract and conceptual thinkers engage in the contemplation of complex atomic phenomena that occur on a minuscule scale in time and space. This is a surprising place indeed for the beginnings of a technology which would, eventually, deliver everything from tourist information, online shopping and advertisements, financial data, weather forecasts and much more to your personal computer.</p>
<p>Tim Berners-Lee is the inventor of the Web. In 1989, Tim was working in a computing services section of CERN when he came up with the concept; at the time he had no idea that it would be implemented on such an enormous scale. Particle physics research often involves collaboration among institutes from all over the world. Tim had the idea of enabling researchers from remote sites in the world to organize and pool together information. But far from simply making available a large number of research documents as files that could be downloaded to individual computers, he suggested that you could actually link the text in the files themselves.</p>
<p>In other words, there could be cross-references from one research paper to another. This would mean that while reading one research paper, you could quickly display part of another paper that holds directly relevant text or diagrams. Documentation of a scientific and mathematical nature would thus be represented as a `web' of information held in electronic form on computers across the world. This, Tim thought, could be done by using some form of hypertext, some way of linking documents together by using buttons on the screen, which you simply clicked on to jump from one paper to another. Before coming to CERN, Tim had already worked on document production and text processing, and had developed his first hypertext system, `Enquire', in 1980 for his own personal use.</p>
<p>Tim's prototype Web browser on the NeXT computer came out in 1990.</p>

<h3>Through 1990: The time was ripe for Tim's invention</h3>
<p>The fact that the Web was invented in the early 1990s was no coincidence. Developments in communications technology during that time meant that, sooner or later, something like the Web was bound to happen. For a start, hypertext was coming into vogue and being used on computers. Also, Internet users were gaining in the number of users on the system: there was an increasing audience for distributed information. Last, but not least, the new domain name system had made it much easier to address a machine on the Internet.</p>

<h3>Hypertext</h3>
<p>Although already established as a concept by academics as early as the 1940s, it was with the advent of the personal computer that hypertext came out of the cupboard. In the late 1980s, Bill Atkinson, an exceptionally gifted programmer working for Apple Computer Inc., came up with an application called Hypercard for the Macintosh. Hypercard enabled you to construct a series of on-screen `filing cards' that contained textual and graphical information. Users could navigate these by pressing on-screen buttons, taking themselves on a tour of the information in the process.</p>
<p>Hypercard set the scene for more applications based on the filing card idea. Toolbook for the PC was used in the early 1990s for constructing hypertext training courses that had `pages' with buttons which could go forward or backward or jump to a new topic. Behind the scenes, buttons would initiate little programs called scripts. These scripts would control which page would be presented next; they could even run a small piece of animation on the screen. The application entitled Guide was a similar application for UNIX and the PC.</p>
<p>Hypercard and its imitators caught the popular imagination. However, these packages still had one major limitation: hypertext jumps could only be made to files on the same computer. Jumps made to computers on the other side of the world were still out of the question. Nobody yet had implemented a system involving hypertext links on a global scale.</p>
```

![](../.gitbook/assets/image%20%28145%29.png)

#### Major Feature Enhancements

As the popularity of the web increased, there was demand for more features.

* **Styling \(1999\)** - the ability to apply styles to the HTML elements, such as colors, fonts, and layout of elements.
* **Interactivity \(1999\)** - the ability to have the page change what is displayed based on input from the user.
* **Ajax \(2005\) - A**synchronous **Ja**vaScript and **X**ML, enabled Single-Page web applications that act more like Desktop Applications. Gmail or Google Maps were the first.
* **Audio, Video, Canvas - 2D/3D drawing \(2016 - HTML 5\)**

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

A good analogy for the HTML/CSS relationship within a web page is a resume.

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

#### A Simple Example

**HTML - Structure/Content** - defines the structure of the content

```markup
<h1 id="id1">Hello World!</h1>
```

**CSS - Styles** - sets initial styles for h1 element

```css
h1 {
   font: size 20px;
   background-color:blue;
   color:yellow;
   font-family: "Poppins";
   text-transform:uppercase;
 }
```

**JavaScript - Interactivity** - responds to button click and changes styles

```javascript
<button onClick="let element = document.getElementById('id1'); element.style.color = 'white'; element.style.backgroundColor = 'red'">Change color</button>

```

Page after it is first loaded

![](../.gitbook/assets/image%20%28142%29.png)

User clicks button - background color and text color are updated

![](../.gitbook/assets/image%20%28113%29.png)

## CSS - CSSZenGarden.com

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

## CSS - Animation

{% embed url="https://codepen.io/everylastpixel/pen/QWybxmV" caption="" %}

## JavaScript - Animation

First, JavaScript can be used to add what I'd call eye-candy to the site. The content is all there, but it's dull without some action. JavaScript can be used to display the content in visually appealing ways and add movement with advanced animations. Below is an example of JavaScript being use in this capacity.

{% embed url="https://www.charles-richard.net/" caption="" %}

{% embed url="https://www.legworkstudio.com" caption="" %}

{% embed url="http://knowlupus.org" caption="" %}

{% embed url="https://www.sbs.com.au/theboat/" caption="" %}

{% embed url="https://mrdoob.com/projects/chromeexperiments/ball-pool/" caption="" %}

## JavaScript - 2D/3D Graphics

{% embed url="http://www.craftymind.com/factory/html5video/CanvasVideo.html" %}

{% embed url="https://codepen.io/soulwire/full/Ffvlo" %}

## JavaScript - AJAX

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

### Resources

{% embed url="http://www.martinrinehart.com/frontend-engineering/engineers/html/html-tag-history.html" %}

