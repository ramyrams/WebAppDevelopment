DOM Intro
DOM Methods
DOM Document
DOM Elements
DOM HTML
DOM CSS
DOM Animations
DOM Events
DOM EventListener
DOM Navigation
DOM Nodes
DOM Nodelist


### JS HTML DOM
```js
document.getElementById("demo").innerHTML = "Hello World!";
var x = document.getElementsByTagName("p");
var x = document.getElementById("main");
var y = x.getElementsByTagName("p");
var x = document.getElementsByClassName("intro");
var x = document.querySelectorAll("p.intro");


document.getElementById('intro').style.color = '#FF0000';

var myDocument = document;
var myIntro = myDocument.getElementById('intro');
var myIntroStyles = myIntro.style;
   
// And now, we can set the color:
myIntroStyles.color = '#FF0000';
```


###  Select single element
```js
var header = document.getElementById('header');
var nav = document.querySelector('#main-nav');
```

### Select a collection of elements
```js
var inputs = document.getElementsByTagName('li');
var radiosGroup = document.getElementsByName('genders');
var header = document.querySelectorAll('#main-nav li');
```

### Using predefined collections of elements
```js
var links = document.links;
var forms = document.forms;
```


### Using getElementsBy Methods
```js
var header = document.getElementById('header');
var posts = document.getElementsByClassName('post-item');
var sidebars = document.getElementsByTagName('sidebar');
var gendersGroup = document.getElementsByName('genders');
```

### Using querySelector Methods
```js
//the element with id="header"
var header = document.querySelector('#header');

//li elements contained in element with id=main-nav
var navItems = document.querySelectorAll('#main-nav li');
```



### Selecting Nested Elements
```js
var wrapper = document.getElementById('wrapper');

// returns all div elements inside the element with id "wrapper"
var divsInWrapper = wrapper.getElementsByTagName('div');
```

### NodeLists
```js
var divs = document.getElementsByTagName('div'),
    queryDivs = document.querySelectorAll('div');
for(var i = 0, length = divs.length; i < length; i += 1){
   // do stuff with divs[i]…
}



console.log(Array.isArray(divs)); // false

for (var i in divs) {
   console.log('divs[' + i + '] = ' + divs[i]);
}


```

	




### Update the content dynamically
```html
<html>
<body>
	<p id="demo"></p>
	<script>
		document.getElementById("demo").innerHTML = "Hello World!";
	</script>
</body>
</html>
```

### Changing the HTML Output Stream
```html
<!DOCTYPE html>
<html>
<body>
	<script>
		document.write(Date());
	</script>
</body>
</html>
```

### Changing HTML Content
```html
<html>
<body>
	<p id="p1">Hello World!</p>

	<script>
		document.getElementById("p1").innerHTML = "Updated Text!";
	</script>

</body>
</html>
```

### document.getElementById
```html
<html>
<body>
	<p id="intro">Hello World!</p>
	<p>This example demonstrates the <b>getElementById</b> method!</p>

	<p id="demo"></p>
	<script>
		var myElement = document.getElementById("intro");
		document.getElementById("demo").innerHTML = "The text from the intro paragraph is " + myElement.innerHTML;
	</script>
</body>
</html>
```

### Changing the Value of an Attribute
```html
<html>
<body>

	<img id="myImage" src="http://www.freeiconspng.com/uploads/green-button-icon-png-33.png">

	<script>
	    document.getElementById("myImage").src = "http://www.thehindu.com/multimedia/dynamic/02620/13kigkk03-tinse_RA_2620048g.jpg";
	</script>

</body>
</html>

```

### Changing HTML Style
```html
<html>
<body>

    <p id="p1">Hello World!</p>
    <p id="p2">Hello World!</p>

    <script>
        document.getElementById("p2").style.color = "blue";
        document.getElementById("p2").style.fontFamily = "Arial";
        document.getElementById("p2").style.fontSize = "larger";
    </script>

    <p>The paragraph above was changed by a script.</p>

</body>
</html>
```


### Using Events
```html
<!DOCTYPE html>
<html>
<body>
	<h1 id="id1">My Heading 1</h1>

	<button type="button" onclick="document.getElementById('id1').style.color = 'red'">Click Me!</button>
</body>
</html>
```

### Create the Animation Using JavaScript
```html
<html>
    <style>
        #container {
          width: 400px;
          height: 400px;
          position: relative;
          background: yellow;
        }

        #animate {
          width: 50px;
          height: 50px;
          position: absolute;
          background-color: red;
        }
    </style>
<body>

    <p> <button onclick="myMove()">Click Me</button> </p>

    <div id ="container">
    <div id ="animate"></div>
    </div>

    <script>
        function myMove() {
            var elem = document.getElementById("animate");
            var pos = 0;
            var id = setInterval(frame, 5);

            function frame() {
                if (pos == 350) {
                    clearInterval(id);
                } else {
                    pos++;
                    elem.style.top = pos + 'px';
                    elem.style.left = pos + 'px';
                }
            }
        }
    </script>

</body>
</html>

```

### JavaScript HTML DOM Events
```html
<html>
<body>

<h1 onclick="changeText(this)">Click on this text!</h1>

<script>
function changeText(id) { 
    id.innerHTML = "Ooops!";
}
</script>

</body>
</html>
```

### Assign Events Using the HTML DOM
```html
<html>
<body>

    <p>Click "Try it" to execute the displayDate() function.</p>

    <button id="myBtn">Try it</button>

    <p id="demo"></p>

    <script>
        document.getElementById("myBtn").onclick = displayDate;

        function displayDate() {
            document.getElementById("demo").innerHTML = Date();
        }
    </script>

</body>
</html>
```

### Two Events
```html
<html>
<body>

	<div onmouseover="mOver(this)" onmouseout="mOut(this)"
	style="background-color:#D94A38;width:120px;height:20px;padding:40px;">
	Mouse Over Me</div>

	<script>
	function mOver(obj) {
	    obj.innerHTML = "Thank You"
	}

	function mOut(obj) {
	    obj.innerHTML = "Mouse Over Me"
	}
	</script>

</body>
</html>
```



```html
<html>
<body>

	<p>Hello World!</p>

	<div id="main">
		<p>The DOM is very useful.</p>
		<p>This example demonstrates the <b>getElementsByTagName</b> method</p>
	</div>

	<p id="demo"></p>
	<script>
		var x = document.getElementById("main");
		var y = x.getElementsByTagName("p");
		document.getElementById("demo").innerHTML = 'The first paragraph (index 0) inside "main" is: ' + y[0].innerHTML;
	</script>

</body>
</html>
```

```html
<html>
<body>

	<p>Hello World!</p>

	<p class="intro">The DOM is very useful.</p>
	<p class="intro">This example demonstrates the <b>getElementsByClassName</b> method.</p>

	<p id="demo"></p>

	<script>
	var x = document.getElementsByClassName("intro");
	document.getElementById("demo").innerHTML = 
	'The first paragraph (index 0) with class="intro": ' + x[0].innerHTML;
	</script>

</body>
</html>
```


### Finding HTML Elements by HTML Object Collections
```html
<!DOCTYPE html>
<html>
<body>

<form id="frm1" action="form_action.asp">
  First name: <input type="text" name="fname" value="Donald"><br>
  Last name: <input type="text" name="lname" value="Duck"><br><br>
  <input type="submit" value="Submit">
</form>

<p>Click "Try it" to display the value of each element in the form.</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
    var x = document.forms["frm1"];
    var text = "";
    var i;
    for (i = 0; i < x.length ;i++) {
        text += x.elements[i].value + "<br>";
    }
    document.getElementById("demo").innerHTML = text;
}
</script>

</body>
</html>
```

### JavaScript HTML DOM EventListener
```html
<!DOCTYPE html>
<html>
<body>

<p>This example uses the addEventListener() method to attach a click event to a button.</p>

<button id="myBtn">Try it</button>

<p id="demo"></p>

<script>
document.getElementById("myBtn").addEventListener("click", displayDate);

function displayDate() {
    document.getElementById("demo").innerHTML = Date();
}
</script>

</body>
</html>
```

### Add an Event Handler to an Element
```html
<!DOCTYPE html>
<html>
<body>

<p>This example uses the addEventListener() method to execute a function when a user clicks on a button.</p>

<button id="myBtn">Try it</button>

<script>
document.getElementById("myBtn").addEventListener("click", myFunction);

function myFunction() {
    alert ("Hello World!");
}
</script>

</body>
</html>
```

### Event Bubbling or Event Capturing?
```html
<!DOCTYPE html>
<html>
<head>
<style>
div {
    background-color: coral;
    border: 1px solid;
    padding: 50px;
}
</style>
</head>
<body>

<p>This example demonstrates the difference between bubbling and capturing when adding event listeners.</p>

<div id="myDiv">
  <p id="myP">Click this paragraph, I am Bubbling.</p>
</div><br>

<div id="myDiv2">
  <p id="myP2">Click this paragraph, I am Capturing.</p>
</div>

<script>
document.getElementById("myP").addEventListener("click", function() {
    alert("You clicked the P element!");
}, false);

document.getElementById("myDiv").addEventListener("click", function() {
    alert("You clicked the DIV element!");
}, false);

document.getElementById("myP2").addEventListener("click", function() {
    alert("You clicked the P element!");
}, true);

document.getElementById("myDiv2").addEventListener("click", function() {
    alert("You clicked the DIV element!");
}, true);
</script>

</body>
</html>
```

### DOM Root Nodes
```html
<!DOCTYPE html>
<html>
<body>

<p>Hello World!</p>

<div>
<p>The DOM is very useful!</p>
<p>This example demonstrates the <b>document.body</b> property.</p>
</div>

<script>
alert(document.body.innerHTML);
</script>

</body>
</html>
```

### Creating new HTML Elements 
```html
<!DOCTYPE html>
<html>
<body>

<div id="div1">
<p id="p1">This is a paragraph.</p>
<p id="p2">This is another paragraph.</p>
</div>

<script>
var para = document.createElement("p");
var node = document.createTextNode("This is new.");
para.appendChild(node);

var element = document.getElementById("div1");
var child = document.getElementById("p1");
element.insertBefore(para,child);
</script>

</body>
</html>
```

### Removing Existing HTML Elements
```html
<!DOCTYPE html>
<html>
<body>

<div id="div1">
<p id="p1">This is a paragraph.</p>
<p id="p2">This is another paragraph.</p>
</div>

<script>
var parent = document.getElementById("div1");
var child = document.getElementById("p1");
parent.removeChild(child);
</script>

</body>
</html>
```


![1](https://s-media-cache-ak0.pinimg.com/originals/0c/06/80/0c06800a5268d4bd699b49f10806ac93.jpg)
