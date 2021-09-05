# Semantic Elements

In addition to the individual HTML elements that display content, such as `<p>`, `<h1>`, etc., there are HTML elements that are used to describe the content contained within a larger section of HTML elements. These elements are called semantic elements, because they give meaning to group of descendant elements contained within them.

Some of the most important semantic elements are those that allow us to divide our page into sections.

![](https://syllabus.codeyourfuture.io/c4fbd24f5cbf819fd867bd5b4785e795.png)

The image above shows a common layout of a web page. We can use specific HTML elements for each of these sections.

* We can use a `<header>` tag for the header content
* We can use a `<footer>` tag for the footer content
* We can use a `<main>` tag for the main content of the page
* Sidebar content can go in an `<aside>` tag
* If there is a list of links, such as in the `<header>`, they can go in a `<nav>` tag

Additionally, we can use `<article>` and `<section>` to divide these sections into more sections.

{% hint style="info" %}
Use these sectioning HTML elements in every website you build. This lets screen reader users jump to these sections of the website quickly.
{% endhint %}

Below is the code we saw earlier when we were demonstrating the hierarchical nature of HTML. This code also demonstrates the use of semantic elements. Semantic elements often do not contain text themselves, but just wrap other elements to separate the page into semantic sections.

{% hint style="success" %}
Check for understanding: What are the semantic elements, without their own text content, in the code below?
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

![](../../.gitbook/assets/image%20%28287%29.png)

