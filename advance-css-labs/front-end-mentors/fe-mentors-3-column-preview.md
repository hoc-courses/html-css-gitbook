# FE Mentors - 3 Col Preview

We're going to do our first Front-end Masters challenge. Go to the page below and download the starter files. You want to start collecting projects to demonstrate what you have done. So, for this project I want you to create a GitHub repository and publish it to Netifly for your submission \(directions at the bottom in the Submission section\).

## Starter Files

{% embed url="https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-" caption="" %}

Start by reading the style-guide.md file for the general specs.

Use the design/desktop-design.png model.

Here's the original HTML file if you want to start from scratch.

```markup
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- displays site properly based on user's device -->

  <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">

  <title>Frontend Mentor | 3-column preview card component</title>
</head>
<body>

  Sedans
  Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city 
  or on your next road trip.

  SUVs
  Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation 
  and off-road adventures.

  Luxury
  Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury 
  rental and arrive in style.
</body>
</html>
```

## Solution

I am providing the solution below, but you should attempt to do as much as you can on your own. After you do it once, delete the code and try it again from scratch.

```css
body {
  color: white;
  margin: 100px;
  font-family: "Lexend Deca", sans-serif;
}

main {
  display:grid;
  grid-template-columns: 1fr 1fr 1fr;
}

section {
  padding: 40px;
}

.sedans {
  background-color: hsl(31, 77%, 52%);
}

.sedans > button {
  color: hsl(31, 77%, 52%);
}

.suvs {
  background-color: hsl(184, 100%, 22%);
}

.suvs > button {
  color: hsl(184, 100%, 22%);
}

.luxury {
  background-color: hsl(179, 100%, 13%);
}

.luxury > button {
  color: hsl(179, 100%, 13%);
}

p {
  opacity: 40%;
}

button {
  padding: 8px 20px;
  border-width:  0px;
  border-radius: 10px;
}

img {
  margin-bottom:20px;
}

.title {
  text-transform: uppercase;
  font-family: "Big Shoulders Display", sans-serif;
  font-size: 32px;
}
```

```markup
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href='http://fonts.googleapis.com/css?family=Lexend+Deca:400,700' rel='stylesheet' type='text/css'>
    <link href='http://fonts.googleapis.com/css?family=Big+Shoulders+Display:400,700' rel='stylesheet' type='text/css'>

    <link
      rel="icon"
      type="image/png"
      sizes="32x32"
      href="./images/favicon-32x32.png"
    />

    <link rel="stylesheet" href="styles.css" />
    <title>Frontend Mentor | 3-column preview card component</title>
  </head>
  <body>
    <main>
      <section class="sedans">
        <img src="images/icon-sedans.svg" alt="">
        <div class="title">Sedans</div>
        <p>
           Choose a sedan for its affordability and excellent fuel economy.
          Ideal for cruising in the city or on your next road trip.
        </p>  
        <button>Learn More</button> 
      </section>

      <section class="suvs">
        <img src="images/icon-suvs.svg" alt="">
        <div class="title">SUVs</div>
        <p>
          Take an SUV for its spacious interior, power, and versatility.
          Perfect for your next family vacation and off-road adventures.
        </p>  
        <button>Learn More</button>    
      </section>

      <section class="luxury">
        <img src="images/icon-luxury.svg" alt="">
        <div class="title">Luxury</div>
        <p>
          Cruise in the best car brands without the bloated prices. Enjoy
          the enhanced comfort of a luxury rental and arrive in style.
        </p>  
        <button>Learn More</button>  
      </section>
    </main>
  </body>
</html>
```

## Bonus

### Use CSS var function for colors

Currently, we are specifying the same color in two places for each of the different sections.

```markup
.luxury {
  background-color: hsl(179, 100%, 13%);
}

.luxury > button {
  color: hsl(179, 100%, 13%);
}
```

There is a better way to do this using the CSS var function.

Read how the var\(\) function works in CSS and use the var function to define each of these colors in a variable and then use the variable value for the value of the color.

{% embed url="https://blog.logrocket.com/how-to-use-css-variables-like-a-pro/" caption="" %}

I've provided the color variables in the html block below for you to add. All you need to do is use the var\(\) function where the colors are used to use these global color values.

```markup
html {
    --sedans-color:  hsl(31, 77%, 52%);
    --suvs-color: hsl(184, 100%, 22%);
    --luxury-color: hsl(179, 100%, 13%);
}
```

### Add border-radius to the four outside corners of overall box.

Hint: you need to set the border radius on specific section selectors, but targeting only the specific corners. Look up how to set the border-radius for a specific corner.

![](../../.gitbook/assets/image%20%28133%29.png)

