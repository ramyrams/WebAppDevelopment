



/*CSS Quick Syntax Reference Book*/

/* Grouping */
/*Ungrouped rules*/
h1 { color: red; }
h1 { background: black; }
h2 { color: red; }
h2 { background: black; }

/*Grouped selectors  */
h1, h2 { color: red; }
h1, h2 { background: black; }

/*Grouped declarations  */
h1 {
color: red;
background: black;
}
h2 {
color: red;
background: black;
}

/*Grouped selectors and declarations  */
h1, h2 {
color: red;
background: black;
}


Class and id selectors
/* Selects any element with class name myclass */
.myclass {}

/* Selects any <p> element with class name myclass */
p.myclass {}


More than one class rule can be applied to a single element by separating each class  name with a space, which makes class rules very versatile.
<p class="style1 style2"></p>

Id selector

/* Selects the element with id set to myid */
#myid {}

/* Selects the <p> element with id set to myid */
p#myid {}



/* Attribute selectors*/

/* Attribute selector
The attribute selector will match elements that use the specified attribute, regardless  of its value.*/
input[type] {}


/* Attribute value selector*/
/*The [attribute=value]selector will match by both attribute and value.*/
input[type="submit"] {}


/* Language attribute selector*/
/*The language attribute selector is used to match the langattribute.*/
p[lang|="en"] {}

/*Delimited value selector*/
/*The [attribute~=value]selector will apply to elements whose attribute value contains  the given word among a space-separated list of words.*/
input[value~="word"] {

/*This rule will select both of the following elements. The word needs to be an exact  case-sensitive match; for example, the selector will not target “Word” or “words”.*/
<input type="text" value="word">
<input type="text" value="word word2">



/*Value substring selector*/
/*The [attribute*=value]selector matches elements whose attribute value contains the  specified substring.*/
p[title*="para"] {}

/*Paragraph elements with a title containing “para” will be matched by this rule.*/
<p title="my paragraph"></p>


/*Value start selector*/
/*The [attribute^=value]selector matches every element whose attribute value begins with the specified string.*/
p[title^="first"] {}
/*Paragraphs with a titlevalue starting with “first” will have this rule applied.*/
<p title="first paragraph"></p>


/*Value end selector*/
/*The [attribute$=value]selector matches an element if its attribute value ends with the  specified string.*/
p[title$="1"] {}

/*In the following code, the value of the titleattribute ends with “1” and will  therefore be matched by this rule:*/
<p title="paragraph 1"></p>




Pseudo selectors


Pseudo-elements

The pseudo-elements enable parts of an element to be styled. There are four of them in 
CSS, as discussed in the following sections.

The pseudo-elements :first-letterand :first-linecan apply styles to the first letter 
and the first line of an element. They work only on block elements such as paragraphs.
p:first-letter { font-size: 120%; }
p:first-line { font-weight: bold; }


before and after
As their names indicate, the :beforeand :afterpseudo-elements can target the location 
before and after an element. They are used together with the contentproperty to insert 
content before or after an element.
p:before { content: "Before"; }
p:after { content: "After"; }
These rules make the following paragraph display as “BeforeMiddleAfter”:
<p>Middle</p>

p.bullet:before { content: url(my-bullet.png); }


Pseudo-classes
Pseudo-classes permit styling based on element relationships and on information 
not found in the HTML document. Most of them fall into three categories: dynamic, 
structural, and user interface pseudo-classes.


Dynamic pseudo-classes
The first category of pseudo-classes is used to apply styles to links or other interactive 
elements when their state is changed. There are five of them, all of which were introduced 
in CSS 2.
link and visited
The dynamic pseudo-classes :linkand :visitedcan be applied only to the anchor 
element (<a>). The :linkpseudo-class matches links to pages that have not been viewed, 
whereas :visitedmatches links that have been viewed.
a:link {} /* unvisited links */
a:visited {} /* visited links */
active and hover
Another pseudo-class is :active, which matches elements as they are being activated, for 
example by a mouse click. This is most useful for styling anchor elements, but it can be 
applied to any element.
a:active {} /* activated links */
A selector with the :hoverpseudo-class appended to it is applied when the user 
moves a pointing device, such as a mouse, over the selected element. It is popularly used 
to create link roll-over effects.
a:hover {} /* hovered links */ 


           focus
The last dynamic pseudo-class is :focus, which can be used on elements that can receive 
focus, such as the form <input>element. The difference between :activeand :focus
is that :activelasts only for the duration of the click, whereas :focuslasts until the 
element loses focus.
input:focus {}


