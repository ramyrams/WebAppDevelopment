

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


