# CSS

## CSS - Cascading Style Sheets

HTML is used to give structure to the page content. CSS was introduced to allow the browser to apply specific styling features such as colors, fonts, and positioning to the HTML elements on the page. 

![https://blog.templatetoaster.com/what-is-css/](../../.gitbook/assets/image%20%28230%29.png)

With CSS, we can use a stylesheet language to specify which styling properties we want to change for specific HTML elements.

### CSS Rules

To change the style of an element you must target the element using a CSS Rule.

![](../../.gitbook/assets/image%20%28289%29.png)

A CSS rule is made up of **selectors**, **properties**, and **values**.

* A **selector** describes which HTML elements to style
  * `h1` is the **selector**
* A **property** is the specific style to apply
  * `font-size` is the **property**
* A **value** is the value for the property
  * `1.5rem` is the **value**
* A **declaration** is the combination of the property and value
  * `font-size: 1.5rem;` is the **declaration**
* A **rule** is the combination of the selector and its declarations
  * `h1 { font-size: 1.5rem; }` is the **rule**

### Three Methods for Applying Styles

**1. External Stylesheets** - styles are loaded from an external stylesheet referenced in a `<link>` element. This is the **preferred method**, as all of the styles are maintained in one place and can be shared across web pages.

```markup
<head>
    <title>Jellies From the Deep</title>
    <link rel="stylesheet" href="styles.css">
</head>
```

```css
// styles.css

a {
  text-decoration: none;
  color:red;
  font-size:36px;
}

#pink-jelly {
  color: deeppink;
}

#yellow-jelly {
  color: #ff9900;
}

#orange-jelly {
  color: #ff3300;
}

li:before {
  content: '🎐'
}
```

**2. Embedded Stylesheets** - styles embedded directly in the html `<style>` element within the `<head>` section of the page. This method is discouraged because it is harder to maintain and re-use styles.

```markup
<head>
    <title>Jellies From the Deep</title>
    <style>
      a {
        text-decoration: none;
        color:red;
        font-size:36px;
      }
      #pink-jelly {
        color: deeppink;
      }

      #yellow-jelly {
        color: #ff9900;
      }

      #orange-jelly {
        color: #ff3300;
      }
      li:before {
        content: '🎐'
      }
    </style>
</head>
```

**3. Inline** - styles are specified as attributes directly on the HTML element to which you want to apply the style.  This method is also discourages for the reasons explain for embedded styles.

```markup
<h2 style="color:#ff9900">Orange Jelly</h2>
```

