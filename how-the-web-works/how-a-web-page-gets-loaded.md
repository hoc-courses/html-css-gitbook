# How a Web Page Gets Loaded

![](../.gitbook/assets/image%20%28199%29.png)

The high-level steps the browser takes when you enter an URL into the search input box are the following:

1. Enter a URL into a web browser
2. Browser looks up the IP address for the domain name via DNS.
3. Browser sends a HTTP GET request to the server.
4. Server sends back a HTTP response.
5. Browser begins rendering the HTML.
6. Browser sends  HTTP GET requests for additional objects embedded in HTML \(images, CSS, JavaScript\) and repeats steps 3-5.
7. Once the page is loaded, the browser sends further asynchronous requests as needed.

Step 5-6: The web browser reads through and and parses the HTML text file line-by-line. As it encounters references to external files, it will send additional requests to the server for each one.

* Stylesheets
* Fonts
* JavaScript files
* Images

![](../.gitbook/assets/image%20%2836%29.png)

## Anatomy of a Page Request/Response

The image below shows the Request and Response taken from the Chrome Developer Tools when inspecting the Network traffic after the URL **csszengarden.com** is entered into the search input box of the browser.

### Default HTML Page - Request/Response

When you type in an URL into your web browser, the browser makes an HTTP GET request to the web server, supplying the requested URL.

![](../.gitbook/assets/image%20%28124%29.png)

The web server responds with the contents of the default HTML document for the site. 

Look at the line highlighted in red. This is an HTML element that specifies the URL of a file containing the styles for the document. 

### CSS File - Request Response

When the web browser reads the returned HTML document, and encounters this element, it will make an additional request to the web server for the stylesheet file and get backs the contents of that file in the response. 

That content will be used by the web browser to apply the specified styles to the HTML document. 

![](../.gitbook/assets/image%20%28158%29.png)

