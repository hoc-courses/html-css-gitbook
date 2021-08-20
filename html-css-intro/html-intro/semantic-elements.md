# Semantic Elements

In addition to the individual HTML elements that display content, such as `<p>`, `<h1>`, etc., there are HTML elements that are used to describe the content contained within a larger group of HTML elements. They are container elements that give semantic meaning to the content contained within them.

Some of the most important semantic elements are those that allow us to divide our page into sections.

![Wireframe of a web page with &amp;lt;header&amp;gt; at the top, &amp;lt;main&amp;gt; at the middle, &amp;lt;footer&amp;gt; at the bottom, and &amp;lt;aside&amp;gt; at the right](https://syllabus.codeyourfuture.io/c4fbd24f5cbf819fd867bd5b4785e795.png)

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

