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

