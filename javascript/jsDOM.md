## DOM

* [Document]()
* [Elements]()
* [HTML & CSS Sytle]()
* [Events & EventListener]()
* [Navigation, Nodes & Nodelist]()
* [Animations]()

* [15 JavaScript Methods For DOM Manipulation for Web Developers](http://www.hongkiat.com/blog/dom-manipulation-javascript-methods/)


### Using getElementsBy Methods
```js
	var header = document.getElementById('header');
	var posts = document.getElementsByClassName('post-item');
	var sidebars = document.getElementsByTagName('sidebar');
	var gendersGroup = document.getElementsByName('genders');
```

### JS HTML DOM
```js
document.getElementById("demo").innerHTML = "Hello World!";

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



### Using querySelector Methods
```js
//the element with id="header"
var header = document.querySelector('#header');

//li elements contained in element with id=main-nav
var navItems = document.querySelectorAll('#main-nav li');
```
### Get value from input element
```js
<div>
    <input id="txtname" type="text" size="10" /><br />
</div>

<button onclick="echovalue()">Alert</button>
<p id="P2"></p>
<script>
    function echovalue() {
	var x = document.getElementById("txtname").value;
	alert(x);
    }
</script>
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

## Using Events

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





### Finding HTML Elements by HTML Object Collections
```html
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
            for (i = 0; i < x.length ; i++) {
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

### Child Nodes and Node Values
```html
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
    element.appendChild(para);
</script>

</body>
</html>
```

### Creating new HTML Elements - insertBefore
```html
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
        element.insertBefore(para, child);
    </script>
</body>
</html>
```

### Removing Existing HTML Elements
```html
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

###  Replacing HTML Elements 

<div id="div1">
<p id="p1">This is a paragraph.</p>
<p id="p2">This is another paragraph.</p>
</div>

<script>
var para = document.createElement("p");
var node = document.createTextNode("This is new.");
para.appendChild(node);

var parent = document.getElementById("div1");
var child = document.getElementById("p1");
parent.replaceChild(para,child);
</script>



## DOM Sample
```html
<!DOCTYPE html>
<html>
<head>
    <base id="htmldom" target="_self" href="http://www.w3schools.com/jsref/">
    <title></title>
</head>
<body>

    <!--Document-->
    <fieldset> <legend>Document Object</legend>
        <div>
            <p id="P4"></p>
            <p id="P5"></p>
        </div>

        <script>
            document.getElementById("demo").innerHTML = "Base target for all links: " + document.getElementById("htmldom").target;
            document.getElementById("demo").innerHTML = document.getElementById("htmldom").href;
        </script>

    </fieldset>


    <!--Document-->
    <fieldset> <legend>Document Object</legend>
        <div>
             <!--The Document Object-->
            <p id="cookie"></p>
            <p id="domain"></p>
            <p id="lastModified"></p>
            <p id="referrer"></p>
            <p id="title"></p>
            <p id="URL"></p>


            <script>
                //Display all name/value pairs of cookies in a document
                document.getElementById("cookie").innerHTML = "Cookies associated with this document: " + document.cookie;

                //Display the domain name of the server that loaded the document
                document.getElementById("domain").innerHTML = document.domain;

                //Display the date and time the document was last modified
                document.getElementById("lastModified").innerHTML = document.lastModified;

                //Display the URL of the document that loaded the current document
                document.getElementById("referrer").innerHTML = document.referrer;

                //Display the title of a document
                document.getElementById("title").innerHTML = "The title of this document is: " + document.title;

                //Display the full URL of a document
                document.getElementById("URL").innerHTML = document.URL

		//Metadata	
		document.write("charsetSet: " + document.characterSet + "<br>");
		document.write("charset: " + document.charset + "<br>");
		document.write("compactMode: " + document.compatMode + "<br>");
		document.write("defaultCharset: " + document.defaultCharset + "<br>");
		document.write("dir: " + document.dir + "<br>");
		document.write("lastModified: " + document.lastModified + "<br>");
		document.write("referrer: " + document.referrer + "<br>");
		document.write("title: " + document.title + "<br>");
		document.write("location: " + document.location + "<br>");
            </script>
        </div>
    </fieldset>


       <!--Document-->
    <fieldset> <legend>Document Object</legend>
        <div>

            <!--//Replace the content of a document-->
            <p id="Replace">Click the button to replace this document with new content.</p>
            <button onclick="myFunction()">Replace the text</button>
            <script >

                function myFunction() {
                    document.open("text/html", "replace");
                    document.write("<h2>Learning about the HTML DOM is fun!</h2>");
                    document.close();

                    //or
                    //var w = window.open();
                    //w.document.open();
                    //w.document.write("<h1>Hello World!</h1>");
                    //w.document.close();
                }
            </script>


    
            <!--Display the number of elements with a specific name-->
            <p>
                Cats: <input name="x" type="radio" value="Cats">
                Dogs: <input name="x" type="radio" value="Dogs">
            </p>
              <p id="allelementscount"></p>
            <input type="button" onclick="getallElements()" value="How many elements named x?">

          
            <script>
                function getallElements() {
                    var x = document.getElementsByName("x");
                    document.getElementById("allelementscount").innerHTML = x.length;
                }
            </script>

            <br /> <br />
      
            <!--Display the number of elements with a specific tag name-->
            <input type="text" size="20"><br>
            <input type="text" size="20"><br>
            <input type="text" size="20"><br>

            <input type="button" onclick="getElementsLen()" value="How many input elements?">

            <p id="ByTagName"></p>
            <script>
                function getElementsLen() {
                    var x = document.getElementsByTagName("input");
                    document.getElementById("ByTagName").innerHTML = x.length;
                }
            </script>
        </div>
    </fieldset>

    <!--The Button Collection-->
    <fieldset> <legend>Button Object</legend>
        <div>
    
            <form id="form1">
               <input type="button" id="btn01" value="OK">
                <button id="Button1" name="subject" type="submit" value="HTML">HTML123</button>
            </form>
             <script>
                 document.getElementById("btn01").disabled = true;
                 console.log(document.getElementById("Button1").name);
                 console.log(document.getElementById("Button1").type);
                 console.log(document.getElementById("Button1").value);
                 console.log(document.getElementById("Button1").innerHTML);
                 console.log(document.getElementById("Button1").form.id);
            </script>
        </div>
    </fieldset>
  
    <!--The Anchors Collection-->
    <fieldset> <legend>Anchors Object</legend>
        <div>
            <a id="google" href="http://www.google.com">Google </a><br>
            <a id="msn" href="http://www.msn.com">MSN</a><br>
            <a id="youtube" href="http://www.youtube.com">Youtube</a><br>

            <p id="NoOfA"></p>
            <p id="FirstA"></p>

            <script>
                //Find the number of anchors in a document
                document.getElementById("NoOfA").innerHTML = "Number of anchors are: " + document.anchors.length;
                //Find the innerHTML of the first anchor in a document
                document.getElementById("FirstA").innerHTML = document.anchors[0].innerHTML;
            </script>

            <p><a id="myAnchor" href="http://www.google.com/" type="text/html" target="_self" rel="nofollow" hreflang="en-us" >google link</a></p>

            <p id="Ahref"></p>
            <p id="Ahreflang"></p>
            <p id="Aid"></p>
            <p id="Arel"></p>
            <p id="Atarget"></p>
            <p id="Atype"></p>

            <script>
                document.getElementById("Aid").innerHTML = document.getElementById("myAnchor").id;
		document.getElementById("Ahref").innerHTML = document.getElementById("myAnchor").href;
		document.getElementById("Atype").innerHTML = document.getElementById("myAnchor").type;
		document.getElementById("Atarget").innerHTML = document.getElementById("w3s").target;
		document.getElementById("Arel").innerHTML = document.getElementById("myAnchor").rel;
		document.getElementById("Ahreflang").innerHTML = document.getElementById("myAnchor").hreflang;
		
            </script>

        </div>
     </fieldset>



    <!--The Links Collection -->
    <!-- get js, css links from the head tag -->
    <fieldset> <legend>Links Object</legend>
        <div>
	    	<p id="totallinks"></p>
		<p id="firstlink"></p>
            <script>
                //Display the number of links in a document
                document.getElementById("totallinks").innerHTML = "Number of links: " + document.links.length;
                //Display the href attribute of the first link in a document
                document.getElementById("firstlink").innerHTML = "The href of the first link is " + document.links[0].href;
            </script>
        </div>
     </fieldset>

    
    <!--The Forms Collection-->
    <fieldset> <legend>Forms Object</legend>
        <div>
            <form action="">
                First name: <input type="text" name="fname" value="Donald">
                <input type="submit" value="Submit">
            </form>
            <form name="Form2"></form>
            <form name="Form3"></form>

            <p id="P1"></p>
            <p id="P2"></p>

            <script>
                //Find the number of forms in a document
                document.getElementById("P1").innerHTML = "Number of forms: " + document.forms.length;
                //Find the name of the first form in a document
                document.getElementById("P2").innerHTML = "The name of the first for is " + document.forms[0].name;
            </script>

        </div>
    </fieldset>


     <!--The Images Collection-->
    <fieldset> <legend>Images Object</legend>
        <div>  
            <img id="img1" src="pic_htmltree.gif">
            <img id="img2" src="pic_navigate.gif">

            <p id="NoOfImages"></p>
            <p id="ImageID"></p>
            <script>
                //Return the number of images in a document
                document.getElementById("NoOfImages").innerHTML = "Number of images: " + document.images.length;
                //Return the id of the first image in a document
                document.getElementById("ImageID").innerHTML = "The id of the first image is " + document.images[0].id;
            </script>
        </div>
    </fieldset>

  
     <!--CSS Manipulation-->
    <fieldset> <legend>Images Object</legend>
        <div> 
             <p id="p3">
                This is a text.
                This is a text.
                This is a text.
            </p>

            <input type="button" value="Hide text" onclick="document.getElementById('p3').style.visibility = 'hidden'">
            <input type="button" value="Show text" onclick="document.getElementById('p3').style.visibility = 'visible'">

            <h2>Change background color</h2>
            <p>Mouse over the squares!</p>

            <table style="width:300px;height:100px">
              <tr>
                <td onmouseover="bgChange(this.style.backgroundColor)" onmouseout="bgChange('transparent')" style="background-color:Khaki"> </td>
                <td onmouseover="bgChange(this.style.backgroundColor)" onmouseout="bgChange('transparent')" style="background-color:PaleGreen"> </td>
                <td onmouseover="bgChange(this.style.backgroundColor)" onmouseout="bgChange('transparent')" style="background-color:Silver"> </td>
              </tr>
            </table>

            <script>
                function bgChange(bg) {
                    document.body.style.background = bg;
                }
            </script>
        </div>
    </fieldset>


    <!-- Table Objects-->
    <fieldset> <legend>Table Object</legend>
        <div> 

            <table style="border:1px solid black" id="myTable">
            <tr>
             <td>100</td>
             <td>200</td>
            </tr>
            <tr>
                <td>300</td>
                <td>400</td>
            </tr>
            </table>

            <input type="button" onclick="changeBorder('myTable')" value="Change Border">
            <input type="button" onclick="padding('myTable')" value="Change padding">

            <input type="button" onclick="getCellContent('myTable', 0, 0)" value="Display first cell">

            <input type="button" onclick="createCaption('myTable')" value="Create caption">

            <input type="button" onclick="insRow('myTable')" value="Insert row">
            <input type="button" value="Delete one Row" onclick="deleteRow('myTable')">
            <input type="button" onclick="changeContent('myTable', 0, 0, 'Hello')" value="Change content">

            <script>
                //Change the width of a table border
                function changeBorder(id) {
                    document.getElementById(id).style.border = "5px solid";
                }

                //Change the padding of a table
                function padding(id) {
                    document.getElementById(id).style.padding = "15px";
                }

                //Find the innerHTML of a cell
                function getCellContent(id, row, cell) {
                    var x = document.getElementById(id).rows[0].cells;
                    document.getElementById("result1").innerHTML = x[0].innerHTML;
                }

                //Create a caption for a table
                function createCaption(id) {
                    document.getElementById(id).createCaption().innerHTML = "My new caption";
                }

                //Add rows to a table
                function insRow(id) {
                    var x = document.getElementById(id).insertRow(0);
                    var y = x.insertCell(0);
                    var z = x.insertCell(1);
                    y.innerHTML = z.innerHTML = "New";
                }

                //Delete rows in a table
                function deleteRow(id) {
                    document.getElementById(id).deleteRow(0)

                }

                //Change the content of a table cell
                function changeContent(id, row, cell, content) {
                    var x = document.getElementById(id).rows[row].cells;
                    x[cell].innerHTML = content;
                }
            </script>

            <p id="result1"></p>
        </div>
    </fieldset>
    
 	<!--Form Object-->
	 <fieldset> <legend>Form Object</legend>
        <div>
    
        <form id="frm1" action="form_action.asp" method="post" accept-charset="ISO-8859-1" target="_self">
            First name: <input type="text" name="fname"><br>
            Last name: <input type="text" name="lname"><br><br>
            <input type="button" onclick="mySubmit()" value="Submit">
            <input type="button" onclick="myreset()" value="Reset">
            <button onclick="myFunction()">Try it</button>
        </form>

        <p id="txtvalues"></p>

        <script>
            console.log(document.getElementById("frm1").acceptCharset);
            console.log(document.getElementById("frm1").action);
            console.log(document.getElementById("frm1").enctype);
            console.log(document.getElementById("frm1").length);
            console.log(document.getElementById("frm1").method);
            console.log(document.getElementById("frm1").id);
            console.log(document.getElementById("frm1").target);

            function mySubmit() {
                document.getElementById("frm1").submit();
            }

            function myreset() {
                document.getElementById("frm1").reset();
            }

            function myFunction() {
                var x = document.getElementById("frm1");
                var text = "";
                var i;
                for (i = 0; i < x.length ;i++) {
                    text += x.elements[i].value + "<br>";
                }
                document.getElementById("txtvalues").innerHTML = text;
            }
        </script>
        </div>
    </fieldset>
    
     <!--Select Object-->
    <fieldset> <legend>Select Object</legend>
        <div>
            <form>
                <select id="mySelect">
                  <option>Apple</option>
                  <option>Pear</option>
                  <option>Banana</option>
                  <option>Orange</option>
                </select>
                <br><br>
                <input type="button" onclick="disable()" value="Disable list">
                <input type="button" onclick="enable()" value="Enable list">
                <input type="button" onclick="changeSize()" value="Change size">
                <input type="button" onclick="selectMultiple()" value="Select multiple">
                <input type="button" onclick="getOptions()" value="Output all options">
                <input type="button" onclick="changeText()" value="Set text of selected option">
                <input type="button" onclick="removeOption()" value="Remove the selected option">
            </form>

        </div>
    </fieldset>

    <script>
        document.getElementById("mySelect").form.id;
        document.getElementById("mySelect").length;
        function disable() {
            document.getElementById("mySelect").disabled = true;
        }
        function enable() {
            document.getElementById("mySelect").disabled = false;
        }
        function changeSize() {
            document.getElementById("mySelect").size = 4;
        }
        function selectMultiple() {
            document.getElementById("mySelect").size = 4;
            document.getElementById("mySelect").multiple = true;
        }
        function getOption() {
            var obj = document.getElementById("mySelect");
            console.log(obj.options[obj.selectedIndex].text);
            console.log(obj.selectedIndex);
        }
        function getOptions() {
            var x = document.getElementById("mySelect");
            var txt = "";
            var i;
            for (i = 0; i < x.length; i++) {
                txt = txt + " " + x.options[i].text;
            }
            document.getElementById("demo").innerHTML = txt;
        }

        function changeText() {
            x = document.getElementById("mySelect");
            x.options[x.selectedIndex].text = "Melon";
        }
        function removeOption() {
            var x = document.getElementById("mySelect");
            x.remove(x.selectedIndex);
        }
    </script>

</body>
</html>
```

## DOM Events
```html
<!--Example1: onclick event and inline script-->
<h1 onclick="this.innerHTML='Ooops!'">Click on this text!</h1>

<!--Example2: onclick event and function script and display time-->
<h1 onclick="changeText(this)">Click on this text!</h1>
<p id="displayDate"></p>
<script>
    function changeText(id) {
        id.innerHTML = "Ooops!";
        document.getElementById("displayDate").innerHTML = Date();
    }
</script>

<!--Example3: onchange event and update case-->
Enter your name and exit: <input type="text" id="fname" onchange="myFunction()">

<script>
    function myFunction() {
        var x = document.getElementById("fname");
        x.value = x.value.toUpperCase();
    }
</script>


    <!--Example3: onmouseover and onmouseout Events-->
<div onmouseover="mOver(this)" onmouseout="mOut(this)" style="background-color:red;width:120px;height:20px;padding:40px;">Mouse Over Me</div>
<script>
    function mOver(obj) {
        obj.innerHTML = "Thank You"
    }

    function mOut(obj) {
        obj.innerHTML = "Mouse Over Me"
    }
</script>


<!--Example4: onmousedown, onmouseup and onclick Events-->
<div onmousedown="mDown(this)" onmouseup="mUp(this)" style="background-color:#D94A38;width:90px;height:20px;padding:40px;">Click Me</div>

<script>
    function mDown(obj) {
        obj.style.backgroundColor = "#1ec5e5";
        obj.innerHTML = "Release Me";
    }

    function mUp(obj) {
        obj.style.backgroundColor = "#D94A38";
        obj.innerHTML = "Thank You";
    }
</script>


<!--# EventListener-->

    <!--Add a named event--> 
<button id="myBtn">Display Date</button>
<p id="P1"></p>

<script>
    document.getElementById("myBtn").addEventListener("click", displayDate);

    function displayDate() {
        document.getElementById("P1").innerHTML = Date();
    }
</script>


<!--Add a ananomouse event--> 
<p>This example uses the addEventListener() method to attach a click event to a button.</p>
<button id="Button1">Try it</button>

<script>
    document.getElementById("myBtn").addEventListener("click", function () {
        alert("Hello World!");
    });
</script>

<!--add two click events to the same button.-->
<p>This example uses the addEventListener() method to add two click events to the same button.</p>

<button id="Button2">Try it</button>

<script>
    var x = document.getElementById("myBtn");
    x.addEventListener("click", myFunction);
    x.addEventListener("click", someOtherFunction);

    function myFunction() {
        alert("Hello World!");
    }

    function someOtherFunction() {
        alert("This function was also executed!");
    }
</script>



<p>This example uses the addEventListener() method to add many events on the same button.</p>

<button id="Button3">Try it</button>

<p id="demo1"></p>

<script>
    var x = document.getElementById("myBtn");
    x.addEventListener("mouseover", myFunction);
    x.addEventListener("click", mySecondFunction);
    x.addEventListener("mouseout", myThirdFunction);

    function myFunction() {
        document.getElementById("demo1").innerHTML += "Moused over!<br>";
    }

    function mySecondFunction() {
        document.getElementById("demo1").innerHTML += "Clicked!<br>";
    }

    function myThirdFunction() {
        document.getElementById("demo1").innerHTML += "Moused out!<br>";
    }
</script>


<!--Passing Parameter-->
<p>Click the button to perform a calculation.</p>

<button id="Button4">Try it</button>

<p id="demo"></p>

<script>
    var p1 = 5;
    var p2 = 7;

    document.getElementById("myBtn").addEventListener("click", function () {
        myFunction(p1, p2);
    });

    function myFunction(a, b) {
        var result = a * b;
        document.getElementById("demo").innerHTML = result;
    }
</script>


<!--bubbling and capturing--> 
<div "style=background-color: coral;border: 1px solid;padding: 50px;" id="myDiv">
    <p id="myP">Click this paragraph, I am Bubbling.</p>
</div><br>

<div  "style=background-color: coral;border: 1px solid;padding: 50px;" id="myDiv2">
    <p id="myP2">Click this paragraph, I am Capturing.</p>
</div>

<script>
    document.getElementById("myP").addEventListener("click", function () {
        alert("You clicked the P element!");
    }, false);

    document.getElementById("myP2").addEventListener("click", function () {
        alert("You clicked the P element!");
    }, true);

    document.getElementById("myDiv").addEventListener("click", function () {
        alert("You clicked the DIV element!");
    }, false);

    document.getElementById("myDiv2").addEventListener("click", function () {
        alert("You clicked the DIV element!");
    }, true);
</script>

<!--Remove Event-->
<div id="myDIV">This div element has an onmousemove event handler that displays a random number every time you move your mouse inside this orange field.
  <p>Click the button to remove the DIV's event handler.</p>
  <button onclick="removeHandler()" id="myBtn">Try it</button>
</div>

<p id="demo"></p>

<script>
document.getElementById("myDIV").addEventListener("mousemove", myFunction);

function myFunction() {
    document.getElementById("demo").innerHTML = Math.random();
}

function removeHandler() {
    document.getElementById("myDIV").removeEventListener("mousemove", myFunction);
}
</script>

```

# DOM Animation
```html
<!DOCTYPE html>
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

<p>
<button onclick="myMove()">Click Me</button>
</p>

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


# Nodes
```html

<script>
    var myText = document.getElementById("intro").childNodes[0].nodeValue;
    myText = document.getElementById("intro").firstChild.nodeValue;
    alert(document.body.innerHTML);
    alert(document.documentElement.innerHTML);
    document.getElementById("demo").innerHTML = myText;
</script>


    <!--Creating New HTML Elements (Nodes)-->
    <div id="div3">
    <p id="p4">This is a paragraph.</p>
    <p id="p5">This is another paragraph.</p>
    </div>

    <script>
        var para = document.createElement("p");
        var node = document.createTextNode("This is new.");
        para.appendChild(node);
        var element = document.getElementById("div1");
        element.appendChild(para);
    </script>


    <!--Creating--> new HTML Elements - insertBefore()
    <div id="div4">
    <p id="p6">This is a paragraph.</p>
    <p id="p7">This is another paragraph.</p>
    </div>

    <script>
        var para = document.createElement("p");
        var node = document.createTextNode("This is new.");
        para.appendChild(node);

        var element = document.getElementById("div1");
        var child = document.getElementById("p1");
        element.insertBefore(para, child);

        //Removing Existing HTML Elements
        //parent.removeChild(child);


        //Replacing HTML Elements 
        //parent.replaceChild(para, child);

        //HTML DOM Node List Length
        var myNodelist = document.getElementsByTagName("p");
        document.getElementById("demo").innerHTML = myNodelist.length;

    </script>

    <!--Loop Nodes-->
    <p>This is a p element</p>
    <p>This is also a p element.</p>
    <p>This is also a p element - Click the button to change the background color of all p elements in this document.</p>

    <button onclick="myFunction()">Try it</button>

    <script>
        function myFunction() {
            var myNodelist = document.getElementsByTagName("p");
            var i;
            for (i = 0; i < myNodelist.length; i++) {
                myNodelist[i].style.backgroundColor = "red";
            }
        }
    </script>

```


![1](https://s-media-cache-ak0.pinimg.com/originals/0c/06/80/0c06800a5268d4bd699b49f10806ac93.jpg)
![2](https://code.snipcademy.com/code/img/tutorials/javascript/bom/bom.svg)
.![1](http://javascript.info/files/tutorial/browser/dom/simpledom.png)
![1](http://javascript.info/files/tutorial/browser/dom/simpledom2.png)
![1](http://javascript.info/files/tutorial/browser/dom/simpledom2_white.png)
![1](http://javascript.info/files/tutorial/browser/dom/documentElement.png)
![1](http://javascript.info/files/tutorial/browser/dom/children.png)
![1](http://javascript.info/files/tutorial/browser/dom/siblings.png)

