
* jQuery Basics
 * What’s $, anyway?
 * $ vs $()
 * document ready
 * Get some elements
 * Other ways to create a jQuery object
 * Creating new elements
 * Testing a selection
 * Chaining
* jQuery Core 
 * CSS, Styling, & Dimensions
 * Data Methods
 * Utility Methods
 * Attributes
 * Selecting Elements
 * Working with Selections
 * Manipulating Elements
 * The jQuery Object
* Traversing 
 * Filtering selections
 * Finding elements relative to a selection
 * Getting back to your original selection
* Manipulating
 * Altering elements
 * Changing form values
 * Getting information from elements
 * Placing elements in the document
 * Copying elements
 * Removing elements
* Events & Event Delegation
 * jQuery Event Basics
 * Event Helpers
 * Introducing Events
 * Handling Events
 * Inside the Event Handling Function
 * Understanding Event Delegation
 * Triggering Event Handlers
 * History of jQuery Events
 * Introducing Custom Events
 * jQuery Event Extensions
 * Namespaced events
 * Binding multiple events at once
 * Passing named functions as event handlers
 * The event object
 * Inside the event handler
 * Preventing the default action
 * Event bubbling
 * Event delegation
* Effects
 * Built-in effects
 * Managing animations
* AJAX & Deferreds
 * $.ajax
 * jQuery’s Ajax-Related Methods
 * Ajax and Forms
 * Working with JSONP
 * Ajax Events
* Plugins
 * Finding & Evaluating Plugins
 * How to Create a Basic Plugin
 * Advanced Plugin Concepts
 * Writing Stateful Plugins with the jQuery UI Widget Factory



$(selector)

//by tag
$("div") //document.querySelectorAll("div");

//by class
$(".menu-item") 
//document.querySelectorAll(".menu-item");

//by id
$("#navigation")

//by combination of selectors
$("ul.menu li")

$("#divTest1").text("Hello, world!");

// select the item
$("#something").hide();
$(".widgets").fade(1);


## Adding Elements
$("<ul><li>Hello</li></ul>").appendTo("body");
$("body").prepend("<h1>header</h1>");

// Removing elements
$('p').remove();


## jQuery Events

function onButtonClick(){
  $(".selected").removeClass("selected");
  $(this).addClass("selected");
}

$("a.button").on("click", onButtonClick);



function onListItemClick(){
  $(".selected").removeClass("selected");
  $(this).addClass("selected");
}

$("ul").on("click", "li", onListItemClick);



## jQuery Chaining
$('<button>')
  .addClass('btn-success')
  .html('Click me for success')
  .on('click', onSuccessButtonClick)
  .appendTo(document.body);




var listItems = jQuery( 'li' ); or $( 'li' );


// Expose jQuery to the global object
window.jQuery = window.$ = jQuery;


$.support property for information on what the current browser environment supports,
$.ajax method to make an AJAX request.



$("span.bold").css("font-weight", "bold");


$( document ).ready(function() {
  console.log( 'ready!' );
});

$(function() {
  console.log( 'ready!' );
});

## Get some elements
$( '#header' ); // select the element with an ID of 'header'
$( 'li' );      // select all list items on the page
$( 'ul li' );   // select list items that are in unordered lists
$( '.person' ); // select all elements with a class of 'person'


## Other ways to create a jQuery object
// create a jQuery object from a DOM element
$( document.body.children[0] );

// create a jQuery object from a list of DOM elements
$( [ window, document ] );

// make a selection in the context of a DOM element
var firstBodyChild = document.body.children[0];
$( 'li', firstBodyChild );

// make a selection within a previous selection
var paragraph = $( 'p' );
$( 'a', paragraph );


### Did my selection get anything?
if ( $( '#nonexistent' ) ) {
  // Wrong! This code will always run!
}

if ( $( '#nonexistent' ).length > 0 ) {
  // Correct! This code will only run if there's an element in your page
  // with an ID of 'nonexistent'
}


### Getting single elements from a selection
var listItems = $( 'li' );
var rawListItem = listItems[0]; // or listItems.get( 0 )
var html = rawListItem.innerHTML;

### Creating new elements
$( '<p>' ); // creates a new <p> element with no content
$( '<p>Hello!</p>' ); // creates a new <p> element with content
$( '<p class="greet">Hello!</p>' ); // creates a new <p> with content and class

$( '<p>', {
  html: 'Hello!',
  'class': 'greet'
});

###v Testing a selection
$( 'li' ).eq( 0 ).is( '.special' ); // false
$( 'li' ).eq( 1 ).is( '.special' ); // true


## Chaining
$( 'li' )
  .click(function() {
    $( this ).addClass( 'clicked' );
  })
  .find( 'span' )
    .attr( 'title', 'Hover over me' );
   
   
   
var listItems = $( 'li' );
var spans = listItems.find( 'span' );

listItems
  .click(function() {
    $( this ).addClass( 'clicked' );
  });

spans.attr( 'title', 'Hover over me' );



### Filtering selections
var listItems = $( 'li' );

// filter the selection to only items with a class of 'special'
var special = listItems.filter( '.special' );

// filter the selection to only items without a class of 'special'
var notSpecial = listItems.not( '.special' );

// filter the selection to only items that contain a span
var hasSpans = listItems.has( 'span' );

### Finding elements relative to a selection
// get the first list item on the page
var listItem = $( 'li' ).first(); // also: .last()

// get the siblings of the list item
var siblings = listItem.siblings();

// get the next sibling of the list item
var nextSibling = listItem.next(); // also: .prev()

// get the list item's parent
var list = listItem.parent();

// get the list items that are immediate children of the list
var listItems = list.children();

// get ALL list items in the list, including nested ones
var allListItems = list.find( 'li' );

// find all ancestors of the list item that have a class of "module"
var modules = listItem.parents( '.module' );

// find the closest ancestor of the list item that has a class of "module"
var module = listItem.closest( '.module' );


http://cdn.lucemorker.com/blog/wp-content/uploads/2014/02/table.jpg



$( document ).ready(function() {
        console.log( "document loaded" );
    });
 
    $( window ).load(function() {
        console.log( "window loaded" );
    });



 
function readyFn( jQuery ) {
    // Code to run when the document is ready.
}
 
$( document ).ready( readyFn );
// or:
$( window ).load( readyFn );



Attributes.attr() method
$( "a" ).attr( "href", "allMyHrefsAreTheSameNow.html" );
 
$( "a" ).attr({
    title: "all titles are the same too!",
    href: "somethingNew.html"
});


var url = $( "a" ).attr( "href" );


// Testing whether a selection contains elements.
if ( $( "div.foo" ).length ) {
    ...
}



// Refining selections.
$( "div.foo" ).has( "p" );         // div.foo elements that contain <p> tags
$( "h1" ).not( ".bar" );           // h1 elements that don't have a class of bar
$( "ul li" ).filter( ".current" ); // unordered list items with class of current
$( "ul li" ).first();              // just the first unordered list item
$( "ul li" ).eq( 5 );              // the sixth




Selecting Elements by ID
$( "#myId" ); // Note IDs must be unique per page.

Selecting Elements by Class Name

$( ".myClass" );

Selecting Elements by Attribute
$( "input[name='first_name']" );

Selecting Elements by Compound CSS Selector
$( "#contents ul.people li" );

Selecting Elements with a Comma-separated List of Selectors
$( "div.myClass, ul.people" );


//link Pseudo-Selectors
$( "a.external:first" );
$( "tr:odd" );
 
// Select all input-like elements in a form (more on this below).
$( "#myForm :input" );
$( "div:visible" );
 
// All except the first three divs.
$( "div:gt(2)" );
 
// All currently animated divs.
$( "div:animated" );




# Traversing




<div class="grandparent">
    <div class="parent">
        <div class="child">
            <span class="subchild"></span>
        </div>
    </div>
    <div class="surrogateParent1"></div>
    <div class="surrogateParent2"></div>
</div>

## Parents

// Selecting an element's direct parent:
 
// returns [ div.child ]
$( "span.subchild" ).parent();
 
// Selecting all the parents of an element that match a given selector:
 
// returns [ div.parent ]
$( "span.subchild" ).parents( "div.parent" );
 
// returns [ div.child, div.parent, div.grandparent ]
$( "span.subchild" ).parents();
 
// Selecting all the parents of an element up to, but *not including* the selector:
 
// returns [ div.child, div.parent ]
$( "span.subchild" ).parentsUntil( "div.grandparent" );
 
// Selecting the closest parent, note that only one parent will be selected
// and that the initial element itself is included in the search:
 
// returns [ div.child ]
$( "span.subchild" ).closest( "div" );
 
// returns [ div.child ] as the selector is also included in the search:
$( "div.child" ).closest( "div" );


## Children
// Selecting an element's direct children:
 
// returns [ div.parent, div.surrogateParent1, div.surrogateParent2 ]
$( "div.grandparent" ).children( "div" );
 
// Finding all elements within a selection that match the selector:
 
// returns [ div.child, div.parent, div.surrogateParent1, div.surrogateParent2 ]
$( "div.grandparent" ).find( "div" );





## Siblings
// Selecting a next sibling of the selectors:
 
// returns [ div.surrogateParent1 ]
$( "div.parent" ).next();
 
// Selecting a prev sibling of the selectors:
 
// returns [] as No sibling exists before div.parent
$( "div.parent" ).prev();
 
// Selecting all the next siblings of the selector:
 
// returns [ div.surrogateParent1, div.surrogateParent2 ]
$( "div.parent" ).nextAll();
 
// returns [ div.surrogateParent1 ]
$( "div.parent" ).nextAll().first();
 
// returns [ div.surrogateParent2 ]
$( "div.parent" ).nextAll().last();
 
// Selecting all the previous siblings of the selector:
 
// returns [ div.surrogateParent1, div.parent ]
$( "div.surrogateParent2" ).prevAll();
 
// returns [ div.surrogateParent1 ]
$( "div.surrogateParent2" ).prevAll().first();
 
// returns [ div.parent ]
$( "div.surrogateParent2" ).prevAll().last();






## CSS, Styling, & Dimensions

// Getting CSS properties.
$( "h1" ).css( "fontSize" ); // Returns a string such as "19px".
$( "h1" ).css( "font-size" ); // Also works.

// Setting CSS properties.
$( "h1" ).css( "fontSize", "100px" ); // Setting an individual property.

// Setting multiple properties.
$( "h1" ).css({
    fontSize: "100px",
    color: "red"
});


## link Using CSS Classes for Styling
// Working with classes.
 
var h1 = $( "h1" );
 
h1.addClass( "big" );
h1.removeClass( "big" );
h1.toggleClass( "big" );
 
if ( h1.hasClass( "big" ) ) {
    ...
}

## Dimensions
// Basic dimensions methods.
 
// Sets the width of all <h1> elements.
$( "h1" ).width( "50px" );
 
// Gets the width of the first <h1> element.
$( "h1" ).width();
 
// Sets the height of all <h1> elements.
$( "h1" ).height( "50px" );
 
// Gets the height of the first <h1> element.
$( "h1" ).height();
 
 
// Returns an object containing position information for
// the first <h1> relative to its "offset (positioned) parent".
$( "h1" ).position();


# Data Methods

// Storing and retrieving data related to an element.
$( "#myDiv" ).data( "keyName", { foo: "bar" } );
$( "#myDiv" ).data( "keyName" ); // Returns { foo: "bar" }



// Storing a relationship between elements using .data()
 
$( "#myList li" ).each(function() {
 
    var li = $( this );
    var div = li.find( "div.content" );
 
    li.data( "contentDiv", div );
 
});
 
// Later, we don't have to find the div again;
// we can just read it from the list item's data
var firstLi = $( "#myList li:first" );
 
firstLi.data( "contentDiv" ).html( "new content" );


# Utility Methods
// Returns "lots of extra whitespace"
$.trim( "    lots of extra whitespace    " );

//$.each()
$.each([ "foo", "bar", "baz" ], function( idx, val ) {
    console.log( "element " + idx + " is " + val );
});
 
$.each({ foo: "bar", baz: "bim" }, function( k, v ) {
    console.log( k + " : " + v );
});


//$.inArray()
var myArray = [ 1, 2, 3, 5 ];
 
if ( $.inArray( 4, myArray ) !== -1 ) {
    console.log( "found it!" );
}


//$.extend()
var firstObject = { foo: "bar", a: "b" };
var secondObject = { foo: "baz" };
 
var newObject = $.extend( firstObject, secondObject );
 
console.log( firstObject.foo ); // "baz"
console.log( newObject.foo ); // "baz"

## Testing Type

$.isArray([]); // true
$.isFunction(function() {}); // true
$.isNumeric(3.14); // true
$.type( true ); // "boolean"
$.type( 3 ); // "number"
$.type( "test" ); // "string"
$.type( function() {} ); // "function"
 
$.type( new Boolean() ); // "boolean"
$.type( new Number(3) ); // "number"
$.type( new String('test') ); // "string"
$.type( new Function() ); // "function"
 
$.type( [] ); // "array"
$.type( null ); // "null"
$.type( /test/ ); // "regexp"
$.type( new Date() ); // "date"



## Imperative Data-Binding with jQuery

<!-- jQuery Markup -->
<div>
    <input id="name" type="text" />
    <span id="greeting">Hello</span>
</div>

// jQuery
//look up the input element
var name = $('#name');

//look up the output element
var greeting = $('#greeting');

//listen for keyboard events
name.keyup(function() {

  //update the output element with the new input
  greeting.text('Hello ' + name.val());

});


