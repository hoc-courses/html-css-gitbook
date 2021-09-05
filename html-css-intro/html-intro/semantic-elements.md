# Semantic Elements

Semantics, put simply, is the study of meanings. In web design, a semantic element is an element that has intrinsic meaning, and conveys that meaning to both the browser and the developer.

For example, `<div>` and `<span>` , which are two elements that are used purely for styling purposes, are non-semantic elements. They tell us nothing about their contents. But &lt;form&gt;, &lt;table&gt;, and &lt;article&gt; _are_ semantic elements: They clearly define their content.

To enrich the semantic content of documents, HTML5 introduced several new semantic elements.

Some of the most important semantic elements are those that allow us to divide our page into sections.

![](https://syllabus.codeyourfuture.io/c4fbd24f5cbf819fd867bd5b4785e795.png)

The image above shows a common layout of a web page. We can use specific HTML elements for each of these sections.

* We can use a `<header>` tag for the header content
* We can use a `<footer>` tag for the footer content
* We can use a `<main>` tag for the main content of the page
* Sidebar content can go in an `<aside>` tag
* If there is a list of links, such as in the `<header>`, they can go in a `<nav>` tag
* Additionally, we can use `<article>` and `<section>` to divide these sections into more sections.

The code below demonstrates the use of semantic elements. Semantic elements often do not contain text themselves, but just wrap other elements to separate the page into semantic sections.

{% hint style="success" %}
**Check for understanding**: What are the semantic container elements in the code below?
{% endhint %}

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
    <article>
      <img src="http://enes.in/f.png" />
      <p>Ea commodo consequat duis autem vel eum iriure dolor in hendrerit.</p>
      <p>Decima eodem modo typi qui nunc nobis videntur.</p>
      <p>Tincidunt ut laoreet dolore magna, aliquam erat volutpat ut wisi enim ad minim.</p>
      <p>Id quod mazim, placerat facer possim assum typi non!</p>
      <p>Legere me lius quod ii, <a href="#">legunt saepius</a> claritas.</p>
      <p>Gothica quam nunc putamus parum claram anteposuerit litterarum formas humanitatis per seacula.</p>
     </article>
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

