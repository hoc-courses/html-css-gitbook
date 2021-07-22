# Stylesheets

### Overview

CSS stands for Cascading Style Sheets. It is a collection of rules for how specific styles, such as colors, fonts, lengths, and positioning should be applied by the web browser to the HTML elements in your web page. 

Every HTML element has two attributes available to use to target the element to apply styles. The attributes are class and id. You can create CSS rules based targeting HTML elements with specific values for these two attributes. In addition, you can target all elements of a particular type.

{% embed url="https://htmldog.com/guides/css/" %}



A single stylesheet can be shared by multiple HTML pages.

![https://blog.templatetoaster.com/what-is-css/](../../.gitbook/assets/image%20%28255%29.png)

The CSS cascade assigns a weight to each style rule. When several rules apply, the one with the greatest weight take precedence.

Order of precedence \(from weakest to strongest\)

* default browser styles
* user stylesheet
* author stylesheet
* author embedded styles
* author inline styles

| Selector Type | HTML | CSS |
| :--- | :--- | :--- |
| ID based \(\#\) | &lt;div id="content"&gt; | \#content { width: 200px; } |
| Class \(.\) | &lt;div class="content"&gt; | .content { width: 200px; } |
| Element \(tag name\) | &lt;div&gt;&lt;/div&gt; | div { width: 200px; } |

Multiple selectors can be grouped

Descendant selectors, Child selectors, universal selector, attribute selector, pseudo classes

{% embed url="https://www.slideshare.net/webdevninja/how-css-works" %}



![](../../.gitbook/assets/image%20%28240%29.png)

![](../../.gitbook/assets/image%20%28253%29.png)

 It was introduced to keep the presentation information information separate from the HTML markup \(content\). Initially web developers used HTML elements like `<font>`, `<b>`, `<br>`, and &lt;table&gt; to control the design of web pages. 

CSS stands for Cascading Style Sheets.



and is responsible for the presentation layer of web pages. 

### What is a Style?

* The property-name is the specific aspect of the element you want to style.
* The property-name is the specific value for that property.

### Three Methods for Applying Styles

**1. Inline** - styles are specified as attributes directly on the HTML elements. This is discouraged because it makes code maintenance difficult.

```markup
<body style="background-color:lightgray;">
</body>
```

**2. Embedded Stylesheets** - styles embedded directly in the html &lt;style&gt; element within the &lt;head&gt; section of the page. This method is also discouraged, for the same reasons.

```markup
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jellies From the Deep</title>
    <style>
        body {
            background-color: lightgray;
        }
    </style>
</head>
```

**3. External Stylesheets** - styles are loaded from an external stylesheet referenced in a &lt;link&gt; element. This is the preferred method, as all of the styles are maintained in one place.

```markup
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jellies From the Deep</title>
    <link rel="stylesheet" href="styles.css">
</head>
```

```css
// styles.css

body { 
    background-color: lightgray; 
}
```

### 

