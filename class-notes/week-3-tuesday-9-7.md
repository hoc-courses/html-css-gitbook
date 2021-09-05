# Week 3: Tuesday 9/7

### HTML Document Boilerplate code

Every HTML document must contain the following basic structure. 

```markup
<!DOCTYPE html>
<html>
  <head>
    <!-- meta-data goes here -->
  </head>
  <body>
    <!-- Content goes here -->
  </body>
</html>
```

```markup

```

### 

### HTML Element Syntax

![](../.gitbook/assets/image%20%283%29.png)

### Common HTML Elements

* text-formatting
* anchors
* images
* video
* tables
* semantic elements



### 

### Element Content

* Which elements have content?
* Which elements do not have content?
* How can you tell the difference?
* What elements have attributes? What are the attribute name/value?

```markup
<article>
  <h1>Learning HTML</h1>
  <p>Get to know the HTML basics.</p>
  <a href="http://html5rocks.com">Read Article</a>
  <img src="images/photo.jpg"/>
</article>
```

### Hierarchical Content

HTML tags are arranged in a hierarchy. This is sometimes called **nesting** tags or creating an HTML **tree**. 

Between the opening `<header>` tag and the closing `</header>` tag there are two other tags. We call these **child** tags, because they have a parent-child relationship.

```markup
<div>
  <header>
    <h1>Title</h1>
    <nav>
      <a href="#">A link</a>
      <a href="#">Another link</a>
    </nav>
  </header>
  <main>
    <img src="http://enes.in/f.png" />
    <p>Ea commodo consequat duis autem vel eum iriure dolor in hendrerit.</p>
    <p>Decima eodem modo typi qui nunc nobis videntur.</p>
    <p>Tincidunt ut laoreet dolore magna, aliquam erat volutpat ut wisi enim ad minim.</p>
    <p>Id quod mazim, placerat facer possim assum typi non!</p>
    <p>Legere me lius quod ii, <a href="#">legunt saepius</a> claritas.</p>
    <p>Gothica quam nunc putamus parum claram anteposuerit litterarum formas humanitatis per seacula.</p>
  </main>
  <footer>
    <ul>
      <li><a href="#">Foo</a></li>
      <li><a href="#">Bar</a></li>
      <li><a href="#">Bam</a></li>
      <li><a href="#">Baz</a></li>
      <li><a href="#">Trek</a></li>
    </ul>
  </footer>
</div>
```

The tree structure can be seen more easily below.

![](../.gitbook/assets/image%20%28287%29.png)

* Name all of the parent/child elements

```markup
<article>
  <h1>Learning HTML</h1>
  <p>
    <span>Author:</span>
    <a href="http://codeyourfuture.io">Code Your Future</a>
  </p>
  <p>Get to know the HTML basics.</p>
  <a href="http://html5rocks.com">Read Article</a>
</article>
```

* What is wrong with the following HTML?

```markup
<!DOCTYPE html>
<html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta http-equiv="X-UA-Compatible" content="IE=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>My First Article</title>
       
       <h1>Jellies From the Deep</h1>
       <p>Written by Anne Chinn</p>
       <p>Vel quam elementum dignissim enim.</p>
    </head>
    <body>
    </body>
 </html>
```

### 

### Project: Article Progression

This is an assignment that has four parts. You'll work on it both in and outside of class over the next week and a half. You'll work on new features as you learn them. 

Here is a [link ](https://ecstatic-liskov-5f80b2.netlify.app/)to the finished page.

You can start working on progression \#1.

* Click on this link to start the assignment: [https://classroom.github.com/a/pc8Gqynb](https://classroom.github.com/a/pc8Gqynb)
* Clone the GitHub assignment repo to your local computer.
* Instructions are in the README.md file in the root of the project directory.

