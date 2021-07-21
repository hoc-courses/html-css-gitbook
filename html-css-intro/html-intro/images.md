# Image

## Images - &lt;img&gt;

{% hint style="info" %}
The img element is a self-closing element. There is no content allowed between the opening and closing tags, so the correct syntax is &lt;img/&gt;
{% endhint %}

| Attribute | Description |
| :--- | :--- |
|  | Embeds an image in the document |
| src | The value of the src attribute can be a path to a local image or an url to a remote image. |
| alt | An alternative to identify the content of the image for screen readers. |

### Images are inline elements

This means that they only take up as much horizontal space as their width and it can effect how the content following it behaves. Here are three examples of an images positioned before, at the beginning and in the middle of a paragraph element. We'll learn more about inline vs block elements, but for now it's just important to be aware that a block element, such as a paragraph, always starts on a new line, whereas text following an image will flow immediately to the right on the same line.

![](../../.gitbook/assets/image%20%28236%29.png)

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        img {
            width:50px;
        }
    </style>
</head>
<body>
    
    <h4>Image placed before paragraph</h4>
    <img src="images/photo.png"/>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        Ut enim ad minim veniam, quis nostrud exercitation ullamco 
        laboris nisi ut aliquip ex ea commodo consequat.  </p>

    <hr/>

    <h4>Image placed at the beginning of paragraph</h4>
    <p><img src="images/photo.png"/>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        Ut enim ad minim veniam, quis nostrud exercitation ullamco 
        laboris nisi ut aliquip ex ea commodo consequat. 
        Lorem ipsum dolor sit amet. </p>
    
    <hr/>

    <h4>Image placed in the middle of paragraph</h4>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        Ut enim ad minim veniamLorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        Ut enim ad minim veniam, <img src="images/photo.png"/>
        quis nostrud exercitation ullamco 
        laboris nisi ut aliquip ex ea commodo consequat.
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
        sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        Ut enim ad minim veniam </p>

    <hr/>
</body>
```

### img element attributes

The &lt;img element is our first element that demonstrates the use of attributes on the element.

&lt;img src="images/pink-jelly.jpg" alt="jellyfish"&gt;

* **src** - the location of the image file
  * can be the relative location of an image file within the project directory
  * can also be an URL to a remote image file.
* **alt** - text used to support accessibility and search engines, or to display fallback text in case the image cannot be loaded.

### Image Guidelines

* The best format for images are jpeg, gif, or png.
* Save the image in the correct size for which it will be displayed so that it doesn't waste a lot of time downloading. If you need to crop or shrink an image, sites like [www.pixlr.com](https://github.com/annechinn/html-css-gitbook-v2/tree/a7a3384c0e35ad09c9a0505d39900561a21fec26/basic-html-labs/article-progression/www.pixlr.com) are a good choice.
* Store images in a special folder, named images, within the project to keep things organized.

### Finding Place-holder Images

Just like we used place-holder text for our paragraph content, we often need place-holder images to use for development purposes. The sites [unsplash.com](http://unsplash.com) and [pexels.com ](http://www.pexels.com) are great sites that have a wide assortment of free images to use in your pages. 

