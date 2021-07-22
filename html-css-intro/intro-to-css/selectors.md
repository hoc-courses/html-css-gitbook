# Selectors

The basic syntax, and preferred formatting, of a CSS Rule block is shown below. 

* You can specify a comma-separated list of selectors.
* You can specify multiple styles for each rule.
* The property-name is the specific aspect of the element you want to style.
* The property-name is the specific value for that property.

![](../../.gitbook/assets/image%20%28246%29.png)

The first example is a single type selector for the body element with multiple styles. The second example of multiple selectors with a single style.

```css
body {
    background-color:red;
    color:white;
    text-transform: uppercase;
}

h1, 
h2,
h3 {
    color:red;
}
```

