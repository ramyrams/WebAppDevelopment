## Browser BOM
* JS Window
* JS Screen
* JS Location
* JS History
* JS Navigator
* JS Popup Alert
* JS Timing
* JS Cookies


## JS Window
```js
var w = window.innerWidth
|| document.documentElement.clientWidth
|| document.body.clientWidth;

var h = window.innerHeight
|| document.documentElement.clientHeight
|| document.body.clientHeight;

window.open() - open a new window
window.close() - close the current window
window.moveTo() -move the current window
window.resizeTo() -resize the current window

window.document.getElementById("header");
```


## JS Screen
```js
screen.width
screen.height
screen.availWidth
screen.availHeight
screen.colorDepth
screen.pixelDepth

document.getElementById("demo").innerHTML = "Screen Width: " + screen.width;
document.getElementById("demo").innerHTML = "Screen Height: " + screen.height;
document.getElementById("demo").innerHTML = "Available Screen Width: " + screen.availWidth;
document.getElementById("demo").innerHTML = "Available Screen Height: " + screen.availHeight;
document.getElementById("demo").innerHTML = "Screen Color Depth: " + screen.colorDepth;
document.getElementById("demo").innerHTML = "Screen Pixel Depth: " + screen.pixelDepth;
```


## JS Location
```js
window.location.href returns the href (URL) of the current page
window.location.hostname returns the domain name of the web host
window.location.pathname returns the path and filename of the current page
window.location.protocol returns the web protocol used (http:// or https://)
window.location.assign loads a new document

document.getElementById("demo").innerHTML = "Page location is " + window.location.href;
document.getElementById("demo").innerHTML = "Page hostname is " + window.location.hostname;
document.getElementById("demo").innerHTML = "Page path is " + window.location.pathname;
document.getElementById("demo").innerHTML = "Page protocol is " + window.location.protocol;
```

```js
<html>
<head>
	<script>
	function newDoc() {
		window.location.assign("http://www.w3schools.com")
	}
	</script>
	</head>
<body>

	<input type="button" value="Load new document" onclick="newDoc()">

</body>
</html>
```


### JS History
```js
<html>
<head>
	<script>
	function goForward() {
		window.history.forward()
	}
	</script>
</head>
<body>

	<input type="button" value="Forward" onclick="goForward()">

</body>
</html>
```

```js
history.back() - same as clicking back in the browser
history.forward() - same as clicking forward in the browser
```


## JS Navigator
```js
navigator.appName
navigator.appCodeName
navigator.platform

<p id="demo"></p>

<script>
	document.getElementById("demo").innerHTML = "Cookies Enabled is " + navigator.cookieEnabled;
	document.getElementById("demo").innerHTML = navigator.userAgent;
	document.getElementById("demo").innerHTML = navigator.platform;
	document.getElementById("demo").innerHTML = navigator.language;
	document.getElementById("demo").innerHTML = navigator.javaEnabled();
	document.getElementById("demo").innerHTML = navigator.appVersion;
	document.getElementById("demo").innerHTML = navigator.product;
	document.getElementById("demo").innerHTML = "Name is " + navigator.appName + ". Code name is " + navigator.appCodeName;
</script>
```

