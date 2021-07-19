# Forms

## What is a Form?

An HTML form on a web page allows a user to enter data that will be sent to a server for processing. The &lt;form&gt; element is the container for one or more &lt;input&gt; elements that specify the input fields and the types of input data that will be collected and included in the form submission.

The following attributes are associated with sending the data to the server:

### form action and method attributes

The purpose of the **action** attribute is to specify the URL to which the form data will be sent when the user submits the form. The **method** attribute specifies how the data will be sent. This method value typically would be "POST", which indicates that the input data will be included in the request body.

### input name attribute

The **name** attribute is the form field name that will be used when the data is included in the request body.

```markup
<form action="https://formspree.io/f/xpzkzqpn" method="POST">
    <input name="firstName" type="text" />
    <input name="lastName" type="text" />
    <input type="submit" value="Submit"/>
</form>
```

![](../.gitbook/assets/image%20%2839%29.png)

## Form Input Data

The essential elements contained within the &lt;form&gt; element are &lt;input&gt; elements. The &lt;input&gt; elements tell the web browser what the data elements are included on the form and the type attribute describes the type of data the element contains.

HTML supports many different input data types for the &lt;input&gt; element. The web browser will present the appropriate UI control and validate based on the data type specified. The full list of data types supported by HTML5 can be[ found here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input). The input type is a client-side attribute to assist in collecting the data and is not sent to with the form data sent to the server for processing. The only form data that is sent to the server is the names of the input fields and their associated values.

## Form Styling

In the HTML code sample above, I omitted the elements that I added for the field labels and the CSS to make everything look nice. HTML forms need a lot of CSS to properly position and style their elements. For example, here is what is displayed in the browser with just the minimal HTML from the code block above. There are just two &lt;input&gt; elements of type text, for the first and last name, and a single &lt;input&gt; element of type submit, which will be rendered as a button with default styling.

![](../.gitbook/assets/image%20%285%29.png)

## Adding Input Field Labels

The &lt;label&gt; element is used to associate a label with a form input element. To associate the two, the label element must have the **for attribute** set to the value of the **id attribute** on the associated input element.

{% hint style="info" %}
The **id attribute** is necessary to associate a label, whereas the **name attribute** is necessary to indicate the field name to the POST request.
{% endhint %}

```markup
<label for="firstName">First Name:</label>
<input id="firstName" name="firstName" type="text" />
<label for="lastname">Last Name:</label>
<input id="lastName" name="lastName" type="text" />
```

![](../.gitbook/assets/image%20%2810%29.png)

## Adding Input Field Block Display

By default, the &lt;input&gt; and &lt;label&gt; elements are both inline elements, which is causing the entire form to be displayed on a single line. A common technique to get each input field to be in its own row is to wrap each with a &lt;div&gt; element \(which is a block element\) and add a margin on the bottom of each.

![](../.gitbook/assets/image%20%28152%29.png)

```markup
<form action="https://formspree.io/f/xpzkzqpn" method="POST">
    <div>
        <label for="firstName">First Name:</label>
        <input id="firstName" name="firstName" type="text" />
    </div>
    <div>
        <label for="lastname">Last Name:</label>
        <input id="lastName" name="lastName" type="text" />
    </div>
    <input type="submit" value="Submit"/>
    </form>
```

```css
form > div {
    margin-bottom:20px;
}
```

## Additional Input Types

Below are a few of the common input types that are available. As you can see, the browser has provided type-specific input controls to gather and validate the data.

![](../.gitbook/assets/image%20%2873%29.png)

## Styling

A big part of form development is the additional styling that is required to make the form look presentable, as the default styling by the web browser is pretty limited. Additionally, validation of the data is necessary. This functionality is often a selling point of adopting a front-end framework, such as Bootstrap, which provides extensive support for forms.

## Advanced Form Layout

We're going to build a form using both grid and flex to layout the elements.

### Grid Areas

An easy way to specify the grid structure is to use the **grid-template-areas** property on the grid container element. All you have to do is create the rows using strings representing the columns each area takes up in each row.

In this form the top row will have two columns and the bottom row will have one column, so we just duplicate the bottom area for both columns. Then we define a style that is associated with the grid area.

```css
<form class="myForm">
  <div class="left"></div>
  <div class="right"></div>     
  <div class="bottom"></div>
</form>
```

```css
.myForm {
    display: grid;
    grid-gap:12px;
    grid-template-areas: 
        "left right"
        "bottom bottom";
}

.left {
    grid-area: left;
}

.right {
grid-area: right;
}

.bottom {
    grid-area:bottom;
}
```

![](../.gitbook/assets/image%20%2893%29.png)

### Left Region Flex

Each label/input pair is grouped in a div with the class of "input-group". These will flow from top to bottom on their own. On the input-group div, we set the display property to flex to get each child label and input element pair to flow from left to right.

### Right Region Flex

Each fieldset element will flow from top to bottom on their own. On the fieldset, we set the display property to flex to get the fieldset child elements to flow from top to bottom.

![](../.gitbook/assets/image%20%28162%29.png)

```css
 <form class="myForm">
    <div class="left">
        <div class="input-group">
            <label for="customer_name">Name</label>
            <input id="customer_name">
        </div>
        <div class="input-group">
            <label for="phone_number">Phone</label>
            <input type="tel" id="phone_number">
        </div>
        <div class="input-group">
            <label for="email_address">Email</label>
            <input type="email" id="email_address">
        </div>
        <!-- code removed for clarity -->
    </div>
     <div class="right">
        <fieldset class="taxi">
            <legend>Which taxi do you require?</legend>
            <label> <input type="radio" id="taxi_car" value="car"> Car </label>
            <label> <input type="radio" id="taxi_van" value="van"> Van </label>
        </fieldset>

        <fieldset class="extras">
            <legend>Extras</legend>
            <label> <input type="checkbox" id="extras_baby" value="baby"> Baby Seat </label>
            <label> <input type="checkbox" id="extras_wheel" value="wheelchair"> Wheelchair Access </label>
        </fieldset>
    </div>     
</form>
```

```css
.left > .input-group {
    display: flex;
    flow-direction: row;
}

.right fieldset {
    display:flex;
    flex-direction: column;
}
```

### Flex-grow

The flex-grow property specifies what happens to the element when distributing extra space across the width of the container. The default value is zero. We are setting the value to one for the form elements to the right of the labels, so that they will stretch to fill the available space and the label will remain a fixed size.

```css
.myForm input,
.myForm select {
    flex-grow: 1; 
}
```

## Wrapping Up

That's pretty much it for the main styling of the form. The rest is padding and margins to spread the elements out nicely across the form.

