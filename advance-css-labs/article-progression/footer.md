# Footer

## What We're Aiming For...

![](../../.gitbook/assets/image%20%28127%29.png)

## Adding the Footer Grid

We'll use a grid to setup the layout for the footer row and set the background-color/text to dark/white. We now have three columns in the footer row.

```css
<footer class="footer-container">
</footer>
```

```css
.footer-container {
  background-color: var(--dark-color);
  color: #fff;
  padding: 32px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 24px;
}
```

## Adding the First Column Content

There is a logo, followed by a paragraph of text.

```css
<div>
  <img src="images/logo_light.png" />
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam
    dolorem magnam sunt possimus perspiciatis quis suscipit quidem
    tempora, error numquam.
  </p>
</div>
```

```css
.footer-container img {
  width: 150px;
}
```

## Adding the Second Column Content

Here, we're introducing a new type of HTML element, the form. For this exercise, we're going to do a brief initial introduction to forms, before studying them in greater detail in a later exercise.

### Form Overview

The purpose of a form is to collect input from the user. The &lt;form&gt; element is a container that contains &lt;input&gt; elements that receive the user input. There is a wide variety of input types that HTML supports. A few examples include numeric, text, email, password, date, checkbox, and radio button. The type "submit" which is used in the second &lt;input&gt; element in the form below, is used to specify the button that will be used to submit the form.

```markup
<div>
  <h3>Sign-up for our Newsletter</h3>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit.
    Reprehenderit, totam!
  </p>
  <form>
    <input type="email" name="email" placeholder="Enter your email" />
    <input type="submit" value="Subscribe" class="btn btn-primary" />
  </form>
</div>
```

### Attribute CSS Selector

And here's one more type of CSS selector that we have not yet introduced. It's called an attribute selector, because the bracket notation allows you to select on an element and additionally specify the value of an attribute that must be present for the selection to be a match.

Attribute selectors are a more advanced feature, and there are a lot more options for how they can be used. If you want to learn more about them you can read the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors).

This CSS attribute selector is targeting the specific &lt;input&gt; element that has the type attribute set to "email".

```css
.footer-container input[type='email'] {
  padding: 8px;
  margin-bottom: 8px;
}
```

## Adding the Third Column Content

You should be starting to recognize the patterns. Everything in this column has been introduced in previous exercises.

```markup
<div>
  <h3>Connect with Us</h3>
  <ul>
    <li><a href="#">Contact</a></li>
    <li><a href="#">Careers</a></li>
    <li><a href="#">Subscriptions</a></li>
    <li><a href="#">Help</a></li>
  </ul>
</div>
```

```css
.footer-container a {
  color: #fff;
}

.footer-container a:hover {
  color: red;
}
```

## Making the Footer Responsive

The modifications to the footer are similar to those for the article grid, just changing the default number of columns to be one and increasing it to three when the screen width is greater than 600px.

```css
  .footer-container {
    grid-template-columns: 1fr;
  }

  @media screen and (min-width:600px) {
    .footer-container {
      grid-template-columns: 1fr 1fr 1fr;
    }
  }
```

![](../../.gitbook/assets/image%20%28170%29.png)

{% embed url="https://objective-torvalds-73b689.netlify.app/" caption="" %}

