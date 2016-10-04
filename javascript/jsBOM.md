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


## JS History
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

## JS Popup Alert
```js
alert("I am an alert box!");
alert("Hello\nHow are you?");

var r = confirm("Press a button");
if (r == true) {
    x = "You pressed OK!";
} else {
    x = "You pressed Cancel!";
}


var person = prompt("Please enter your name", "Harry Potter");
if (person != null) {
    document.getElementById("demo").innerHTML =
    "Hello " + person + "! How are you today?";
}
```


##JS Timing
```js
<button onclick="setTimeout(myFunction, 3000)">Try it</button>
<script>
function myFunction() {
    alert('Hello');
}
</script>
```

```js
<button onclick="myVar = setTimeout(myFunction, 3000)">Try it</button>
<button onclick="clearTimeout(myVar)">Stop it</button>
```

```js
var myVar = setInterval(myTimer, 1000);
function myTimer() {
    var d = new Date();
    document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
```

```js
<p id="demo"></p>

<button onclick="clearInterval(myVar)">Stop time</button>

<script>
var myVar = setInterval(myTimer, 1000);
function myTimer() {
    var d = new Date();
    document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}
</script>
```



## JS Cookies
```js
document.cookie = "username=John Doe";
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC";
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";
var x = document.cookie;



function setCookie(cname, cvalue, exdays) {
    var d = new Date();
    d.setTime(d.getTime() + (exdays*24*60*60*1000));
    var expires = "expires="+ d.toUTCString();
    document.cookie = cname + "=" + cvalue + "; " + expires;
}



function getCookie(cname) {
    var name = cname + "=";
    var ca = document.cookie.split(';');
    for(var i = 0; i <ca.length; i++) {
        var c = ca[i];
        while (c.charAt(0)==' ') {
            c = c.substring(1);
        }
        if (c.indexOf(name) == 0) {
            return c.substring(name.length,c.length);
        }
    }
    return "";
}



function checkCookie() {
    var username=getCookie("username");
    if (username!="") {
        alert("Welcome again " + username);
    } else {
        username = prompt("Please enter your name:", "");
        if (username != "" && username != null) {
            setCookie("username", username, 365);
        }
    }
}
```

![1](http://images.cnblogs.com/cnblogs_com/daibao9922/bom.gif)
![1](http://javascript.info/files/tutorial/browser/JSTop.png)
![1](http://code-tricks.com/wp-content/uploads/2014/02/javaScript-DOM-vs-BOM.jpg)

