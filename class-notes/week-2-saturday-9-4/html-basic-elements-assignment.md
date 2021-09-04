# HTML Basic Elements Assignment

## HTML Basic Elements

### Overview

Your task is to reproduce the HTML displayed in the screen capture below. This is a plain HTML page, no CSS.

![](https://raw.githubusercontent.com/hoc-labs/images/main/basic-elements.png)

### 1. Clone the Labs Assignment Repository

Review the **Assignments Info lesson** in the main course Gitbook if necessary.

### 2. Create index.html

Create your new HTML page in your project folder. Name it index.html. Once you have generated your boiler-plate HTML, don't forget to change the &lt;title&gt; element to something more meaningful for your page.

### 3. Create HTML Boilerplate Code

Boilerplate Code refers to sections of code that are often re-used, with little to no modifications. Every time we create a new HTML file, we need to add some boilerplate code. Fortunately, Visual Studio Code makes this very easy.

If you just add a "!" character and then the "Tab" key, the following HTML will be automatically added to your file.

```text
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

### 4. Reproduce the HTML in the Mockup

#### Elements Used

The following HTML elements are used in the page. You can find documentation for any of these elements on the [W3 Schools site](https://www.w3schools.com/tags/default.asp). Just click on the tag name in the left navigation menu.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Element</th>
      <th style="text-align:left">Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>h1</code>
      </td>
      <td style="text-align:left">top-level heading</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>h2</code>
      </td>
      <td style="text-align:left">second-level heading</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><code>ol</code>/<code>li</code>
        </p>
        <p><code>ul</code>/<code>li</code>
        </p>
      </td>
      <td style="text-align:left">lists - ordered and unordered</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>img</code>
      </td>
      <td style="text-align:left">image</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>blockquote</code>
      </td>
      <td style="text-align:left">quotation</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>p</code>
      </td>
      <td style="text-align:left">paragraph</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>hr</code>
      </td>
      <td style="text-align:left">horizontal rule, used for a thematic break in content</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>a</code>
      </td>
      <td style="text-align:left">anchor - hyper-link to another web page</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>strong</code>
      </td>
      <td style="text-align:left">emphasizes important/serious text</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>b</code>
      </td>
      <td style="text-align:left">draws attention to text</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>i</code>
      </td>
      <td style="text-align:left">italicizes text</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><code>&amp;lt; (&lt;)</code>
        </p>
        <p><code>&amp;gt; (&gt;)</code>
        </p>
        <p><code>&amp;nbsp; ( )</code>
        </p>
      </td>
      <td style="text-align:left">These are called HTML entities. It is how you insert special HTML characters
        as text in your page. Refer to this <a href="https://www.w3schools.com/html/html_entities.asp">documentation</a> for
        more details.</td>
    </tr>
  </tbody>
</table>

#### Notes on Particular Sections

**Links**

Pay attention to the type of list it should be: ordered vs unordered.

* The first link should navigate to a new page in the same tab \(replace the current page\)
* The second link should bring up a new, separate window and load that window with the new page\). Review documentation for the [target property](https://www.w3schools.com/tags/att_a_target.asp) of the anchor element to see how to make this happen.

**Images**

The profile image should use a local image. The image is in the images directory in the project folder.

The Google image should use a remote image URL. The URL is: [https://www.google.com/images/branding/googlelogo/1x/googlelogo\_color\_272x92dp.png](https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png)

**Common**

Pay attention to the type of list to use: ordered vs unordered.

Pay particular attention to the first bullet item. It displays the text `<div>` and `<span>` , separated by a space. The "&lt;" and "&gt;" characters have special meaning in HTML, so you have to use a special HTML entities syntax to escape them, `&th;` and `&gt;`

Space in your HTML document is ignored when rendering the page, so to insert a space character in your HTML, you also need to use the special HTML entities syntax, `&nbsp;`

### 6. Push Your Changes to GitHub using ACP git Commands

1. A \(git add .\)
2. C \(git commit -m"comment"\)
3. P \(git push\)

