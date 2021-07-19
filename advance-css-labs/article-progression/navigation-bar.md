# Navigation Bar

## What We're Aiming For...

We want to create a navigation bar with a logo on the left and the nav elements distributed evenly along the horizontal line.

![](../../.gitbook/assets/image%20%2879%29.png)

## Add the nav container

First, we use the &lt;nav&gt; semantic element to wrap the navigation bar. And we'll add a class so that we can target it for styling.

```markup
<nav class="nav-container">
</nav>
```

### Add the navbar logo

Next, we'll add the img element for the logo. I've wrapped it in an anchor. This is how you create a link with an image instead of text. So when the user clicks on the logo, it would take them to the home page.

```markup
<nav class="nav-container">
     <a href="index.html">
          <img src="images/logo.png" class="logo" />
     </a>
</nav>
```

The image size needs to be scaled down to fit in the navigation bar. I've picked a size that looks like it fits well.

```css
.nav-container .logo {
    width: 180px;
}
```

### Add the horizontal links

```markup
<nav class="nav-container">
  <a href="index.html">
    <img src="images/logo.png" class="logo" />
  </a>
  <ul>
    <li><a href="">Tech</a></li>
    <li><a href="">Science</a></li>
    <li><a href="">Food</a></li>
    <li><a href="">Arts</a></li>
    <li><a href="">Sports</a></li>
    <li><a href="">Account</a></li>
  </ul>
</nav>
```

Unordered list elements \(&lt;ul&gt;, &lt;li&gt;\) are used to implement navigation bars because they are ideally suited to the task since they are designed to represent a hierarchical structure of any depth. This navigation bar is only one level, but that's not always the case \(take a look at the navigation bar on the [cnbc.com](http://cnbc.com) site\)

There are three CSS properties on the list element \(ul or ol\) that must be changed from the defaults to make a list into a navigation bar.

* **list-style: none** This removes to bullet icon for each list item
* **display: flex**  In this situation we are using it to cause the list items to flow from left to right across the available space. 

```css
.nav-container ul {
  display: flex;
  list-style: none;
}

.nav-container li {
  font-weight: bold;
}
```

## Adding a :hover selector for mouse-over events on the navigation bar

We used this in the last exercise to hover over the "Learn More" button on the showcase article. We're going to apply the same technique here on the navigation item links. The link color will change as long as the user's mouse remains hovered over the list item.

```css
.nav-container a:hover {
  color: var(--primary-color);
}
```

## Solution

```markup
<nav class="nav-container">
  <a href="index.html">
    <img src="images/logo.png" class="logo" />
  </a>
  <ul>
    <li><a href="">Tech</a></li>
    <li><a href="">Science</a></li>
    <li><a href="">Food</a></li>
    <li><a href="">Arts</a></li>
    <li><a href="">Sports</a></li>
    <li><a href="">Account</a></li>
  </ul>
</nav>
```

```css
.nav-container {
  background: #fff;
  padding: 18px;
  display: flex;
  width:100%;
}

/* this style centers the image within the anchor */
.nav-container > a {
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-container .logo {
  width: 180px;
}

/* default style for mobile width */
.nav-container ul {
  display: flex;
  flex-direction: column;
  list-style: none;
}

/* style for larger widths */
@media screen and (min-width:600px) {
  .nav-container ul {
    flex-direction:row;
    width:100%;
    justify-content:space-around;
  }
}

.nav-container li {
  font-weight: bold;
}

.nav-container a:hover {
   color: var(--primary-color);
}
```

