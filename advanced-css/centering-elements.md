# Centering Elements

One of the best resources, but might be a little advanced to start.

{% embed url="https://css-tricks.com/centering-css-complete-guide/" caption="" %}

## Using a width and left and right margins of auto

* set a width on the element
* set the margin-left and margin-right to auto

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        body {
            border: solid 1px darkslategray;
            padding:50px;
        }
        .container {
            width: 300px;
            margin-left:auto;
            margin-right:auto;
        }

        #green {
            background-color: #baffc9;
        }

        #yellow {
            background-color:   #ffffba;
        }
    </style>
</head>
<body>
    <div class="container">
        <p id="green">Lorem ipsum dolor sit amet, consectetur 
            adipiscing elit, sed do eiusmod tempor 
                incididunt ut labore.
            </p>
            <p id="yellow">Lorem ipsum dolor sit amet, consectetur 
            adipiscing elit, sed do eiusmod tempor 
                incididunt ut labore.
            </p>
    </div>
</body>
</html>
```

![](../.gitbook/assets/image%20%28103%29.png)

## Using flex and align-items, justify-content of center

You can use the flex-direction property to set the child elements to flow across the row or down a single column.

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

        body {
            border: solid 1px darkslategray;
            padding:50px;
        }
        .container {
            display:flex;
            flex-direction: column;
        }

        #green {
            background-color: #baffc9;
        }

        #yellow {
            background-color:  #ffffba;
        }
    </style>
</head>
<body>
    <div class="container">
        <p id="green">Lorem ipsum dolor sit amet, consectetur 
            adipiscing elit, sed do eiusmod tempor 
                incididunt ut labore.
            </p>
            <p id="yellow">Lorem ipsum dolor sit amet, consectetur 
            adipiscing elit, sed do eiusmod tempor 
                incididunt ut labore.
            </p>
    </div>
</body>
</html>
```

![](../.gitbook/assets/image%20%28161%29.png)

### Resources

{% embed url="https://css-tricks.com/centering-css-complete-guide/" %}



