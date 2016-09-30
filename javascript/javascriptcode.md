### Comments	
```js	
// Single line comments
 
/*---------------------------------------------------------------------------------	
multiline comments
-----------------------------------------------------------------------------------*/

/* You can't, however, /* nest comments */ SyntaxError */

```

### All valid variable names 
```js	
var myText;
var $;
var r8;
var _counter;
var $field;
var thisIsALongVariableName_butItCouldBeLonger;
var __$abc;
var OldSchoolNamingScheme;
```


### Data Types
```js
var a = 10;		//local variable
b = 10;			//global variable

var x;               							//undefined
var length = 16;                               	//Number
var lastName = "Johnson";                      	//String
var cars = ["Saab", "Volvo", "BMW"];           	//Array
var x = {firstName:"John", lastName:"Doe"};    	//Object
var y = false;									//Booleans
var person = null;           					//null
var	x6 = /()/           						//regular expression object
var x7 = function(){}; 		 					//empty function


// declaration
var task, complete;

// initialization
task = "Write the first chapter.";
	
// declaration & initialization
var task = "Write the first chapter.";

//One Statement, Many Variables
var person = "John Doe", carName = "Volvo", price = 200;

//A declaration can span multiple lines:
var person = "John Doe",
carName = "Volvo",
price = 200;

var x = "16" + "Volvo";			//"16Volvo"
var x = "Volvo" + 16 + 4;		//"Volvo164"
var x = 16 + 4 + "Volvo";		//"20Volvo"
var car = "";                	// The value is "", the typeof is "string"

var z = x + y;
var a = 3 > 5;      		//false
var k = 3+3;
var l = (5 > 3) && (2<4);  //true
```


### Specials
```js
var a = 10 / 0;           // => Infinity
var b = -10 / 0;          // => -Infinity
var c = Math.sqrt(-1);    // => NaN : Not a Number
```

### Between Undefined and Null
```js
null === undefined           // false
null == undefined            // true
```

### Constants
```js
const prefix = '212';
const pi = 3.14; 	// Define a constant and give it a value.
pi = 4; 			// Any future assignments to it are silently ignored.
const pi = 4; 		// It is an error to redeclare a constant.
var pi = 4; 		// This is also an error.
```

### Escape single quote and double quote
```js
var answer = "It's alright";
var answer = "He is called 'Johnny'";
var answer = 'He is called "Johnny"';
```


//Grouping statements
var a = function(){
	alert(“Statement 1”);
	alert(“Statement 2”);
};


Brackets: []
Hold arrays

Braces:{}
	Create Objects
	group statement

	
Parantheses:()
	supply parameters
	group expressions
	execute functions

```

### typeof Operator
```js	
typeof "John"                // Returns "string" 
typeof 3.14                  // Returns "number"
typeof false                 // Returns "boolean"
typeof [1,2,3,4]             // Returns "object" (not "array", see note below)
typeof {name:'John', age:34} // Returns "object"
typeof NaN                    // Returns number
typeof false                  // Returns boolean
typeof new Date()             // Returns object
typeof function () {}         // Returns function
typeof myCar                  // Returns undefined (if myCar is not declared)
typeof undefined              // undefined
typeof a;               		// "undefined"
typeof null;               		// "object" -- weird, bug
```

### Strings
```js	
var s = "hello, world" // Start with some text.
s.length

s[0] 						// => "h"
s[s.length-1] 				// => "d"
s.charAt(0) 				// => "h": the first character.
s.charAt(s.length-1) 		// => "d": the last character.
s.substring(1,1) 			// => empty
s.substring(1,4) 			// => "ell": the 2nd, 3rd and 4th characters. //This extracts the characters in a string between "start" and "end", not including "end" itself.
s.substring(4)				// => "o, world": 
s.substring(4, 1)			// => "ell": If "start" is greater than "end", it will swap the two arguments:
s.substring(-3)				// => "hello, world" 	//If "start" is less than 0, it will start extraction from index position 0

s.slice(1,4) 				// => "ell": same thing (same as substring)
s.slice(-3) 				// => "rld": last 3 characters (same as substring)
s.slice(4, 1)				// => empty (not as substring)

s.indexOf("l") 				// => 2: position of first letter l.
s.lastIndexOf("l") 			// => 10: position of last letter l.
s.indexOf("l", 3) 			// => 3: position of first "l" at or after 3

s.split(", ") 				// => ["hello", "world"] split into substrings
s.replace("h", "H") 		// => "Hello, world": replaces all instances
s.toUpperCase() 			// => "HELLO, WORLD"
s.toLowerCase()				// => "hello, world" 

//concat()
var str1 = "Hello ";
var str2 = "world!";
var res = str1.concat(str2);

//match()
var str = "The rain in SPAIN stays mainly in the plain"; 
var res = str.match(/ain/g);	// => ain,ain,ain: The result of res will be an array with the values:

//replace()
var str = "Visit Microsoft!";
var res = str.replace("Microsoft", "W3Schools");

var str = "Mr Blue has a blue house and a blue car";
var res = str.replace(/blue|house|car/gi, function myFunction(x){return x.toUpperCase();});

//search()
var str = "Visit W3Schools!";
var n = str.search("W3Schools");

//split()
var str = "How are you doing today?";
var res = str.split(" "); 		// => How,are,you,doing,today? : The result of res will be an array with the values:

var str = "How are you doing today?";
var res = str.split();			// => "How are you doing today?" : 

var str = "How are you doing today?";
var res = str.split("");		// => "H,o,w, ,a,r,e, ,y,o,u, ,d,o,i,n,g, ,t,o,d,a,y,?"

var str = "How are you doing today?";
var res = str.split(" ",3);		// =>	How,are,you	: The result of res will be an array with only 3 values


//substr()
var str = "Hello world!";
var res = str.substr(1, 4);
ello

var str = "Hello world!";
var res = str.substr(2);
llo world!

var str = "Hello world!";
var res = str.substr(0, 1);
H

/
var str = "Hello world!";
var res = str.substr(11, 1);
!


//trim()
var str = "       Hello World!        ";
alert(str.trim());

//toString()
var str = "Hello World!";
var res = str.toString();
Hello World!

//valueOf()
var str = "Hello World!";
var res = str.valueOf();
Hello World!
```



### Numbers
```js	

var intNum = 55; //integer

var octalNum1 = 070; 	//octal for 56
var octalNum2 = 079; 	//invalid octal - interpreted as 79
var octalNum3 = 08; 	//invalid octal - interpreted as 8

var hexNum1 = 0xA; 		//hexadecimal for 10
var hexNum2 = 0x1f; 	//hexedecimal for 31

var floatNum1 = 1.1;	//Floating-Point Values
var floatNum2 = 0.1;	//Floating-Point Values/
var floatNum3 = .1; 	//valid, but not recommended
var floatNum1 = 1.; 	//missing digit after decimal - interpreted as integer 1
var floatNum2 = 10.0; 	//whole number - interpreted as integer 10
var floatNum = 3.125e7; //equal to 31250000

var x = 34.00;    						// A number with decimals
var y = 34;       						// A number without decimals
var x = 123e5;    						// 12300000
var y = 123e-5;   						// 0.00123
var x = 0.2 + 0.1;         				// x will be 0.30000000000000004
var x = (0.2 * 10 + 0.1 * 10) / 10;		// x will be 0.3
var x = 0xFF;             				// x will be 255   Hexadecimal
var x =  2 / 0;          	// x will be Infinity
var y = -2 / 0;          	// y will be -Infinity
typeof Infinity;       		// returns "number"
typeof NaN;             	// returns "number"
var x = 100 / "Apple";  	// x will be NaN (Not a Number)
var x = 100 / "10";     	// x will be 10

var total = 4 + 26;
var average = total / 2;
var doublePi = 2*3.14159;
var removeItem = 50 – 25;
var remainder = total % 7;
var more = (1 + average * 10) / 5;


alert(NaN == NaN); 		//false
alert(isNaN(NaN)); 		//true
alert(isNaN(10)); 		//false - 10 is a number
alert(isNaN(“10”)); 	//false - can be converted to number 10
alert(isNaN(“blue”)); 	//true - cannot be converted to a number
alert(isNaN(true)); 	//false - can be converted to number 1

var num1 = Number(“Hello world!”); 	//NaN
var num2 = Number(“”); 				//0
var num3 = Number(“000011”); 		//11
var num4 = Number(true); 			//1

var num1 = parseInt(“1234blue”); 	//1234
var num2 = parseInt(“”); 			//NaN
var num3 = parseInt(“0xA”); 		//10 - hexadecimal
var num4 = parseInt(22.5); 			//22
var num5 = parseInt(“70”); 			//70 - decimal
var num6 = parseInt(“0xf”); 		//15 - hexadecimal

//56 (octal) in ECMAScript 3, 0 (decimal) in ECMAScript 5
var num = parseInt(“070”);
var num = parseInt(“0xAF”, 16); 	//175
var num1 = parseInt(”AF”, 16); 		//175
var num2 = parseInt(”AF”); 			//NaN


var num1 = parseInt(“10”, 2); 		//2 - parsed as binary
var num2 = parseInt(“10”, 8); 		//8 - parsed as octal
var num3 = parseInt(“10”, 10); 		//10 - parsed as decimal
var num4 = parseInt(“10”, 16); 		//16 - parsed as hexadecimal

var num1 = parseFloat(“1234blue”); 	//1234 - integer
var num2 = parseFloat(“0xA”); 		//0
var num3 = parseFloat(“22.5”); 		//22.5
var num4 = parseFloat(“22.34.5”); 	//22.34
var num5 = parseFloat(“0908.5”); 	//908.5
var num6 = parseFloat(“3.125e7”); 	//31250000


var num = 10;
alert(num.toString()); 			//”10”
alert(num.toString(2)); 		//”1010”
alert(num.toString(8)); 		//”12”
alert(num.toString(10)); 		//”10”
alert(num.toString(16)); 		//”a”



var myNumber = 128;
myNumber.toString(16);     // returns 80
myNumber.toString(8);      // returns 200
myNumber.toString(2);      // returns 10000000


var x = 100 / "Apple";
isNaN(x);               // returns true because x is Not a Number


var x = NaN;
var y = 5;
var z = x + y;         // z will be NaN


var x = NaN;
var y = "5";
var z = x + y;         // z will be NaN5



var myNumber = 2;
while (myNumber != Infinity) {          // Execute until Infinity
    myNumber = myNumber * myNumber;
}



var x = 123;
var y = new Number(123);

// typeof x returns number
// typeof y returns object



var x = 500;             
var y = new Number(500);

// (x == y) is true because x and y have equal values



var x = 500;             
var y = new Number(500);

// (x === y) is false because x and y have different types




var x = new Number(500);             
var y = new Number(500);

// (x == y) is false because objects cannot be compared





var x = 123;
x.toString();            // returns 123 from variable x
(123).toString();        // returns 123 from literal 123
(100 + 23).toString();   // returns 123 from expression 100 + 23


var x = 9.656;
x.toExponential(2);     // returns 9.66e+0
x.toExponential(4);     // returns 9.6560e+0
x.toExponential(6);     // returns 9.656000e+0



var x = 9.656;
x.toFixed(0);           // returns 10
x.toFixed(2);           // returns 9.66
x.toFixed(4);           // returns 9.6560
x.toFixed(6);           // returns 9.656000



var x = 9.656;
x.toPrecision();        // returns 9.656
x.toPrecision(2);       // returns 9.7
x.toPrecision(4);       // returns 9.656
x.toPrecision(6);       // returns 9.65600



x = true;
Number(x);        // returns 1
x = false;     
Number(x);        // returns 0
x = new Date();
Number(x);        // returns 1404568027739
x = "10"
Number(x);        // returns 10
x = "10 20"
Number(x);        // returns NaN



parseInt("10");         // returns 10
parseInt("10.33");      // returns 10
parseInt("10 20 30");   // returns 10
parseInt("10 years");   // returns 10
parseInt("years 10");   // returns NaN 


parseFloat("10");        // returns 10
parseFloat("10.33");     // returns 10.33
parseFloat("10 20 30");  // returns 10
parseFloat("10 years");  // returns 10
parseFloat("years 10");  // returns NaN


var x = 123;
x.valueOf();            // returns 123 from variable x
(123).valueOf();        // returns 123 from literal 123
(100 + 23).valueOf();   // returns 123 from expression 100 + 23
```


### Date
```js	
var then = new Date(2010, 0, 1); 				// The 1st day of the 1st month of 2010
var later = new Date(2010, 0, 1, 17, 10, 30); 	// Same day, at 5:10:30pm, local time

var now = new Date(); // The current date and time
var elapsed = now - then; 		// Date subtraction: interval in milliseconds
later.getFullYear() 			// => 2010
later.getMonth() 				// => 0: zero-based months
later.getDate() 				// => 1: one-based days
later.getDay() 					// => 5: day of week. 0 is Sunday 5 is Friday.
later.getHours() 				// => 17: 5pm, local time
later.getUTCHours() 			// hours in UTC time; depends on timezone
later.toString() 				// => "Fri Jan 01 2010 17:10:30 GMT-0800 (PST)"
later.toUTCString() 			// => "Sat, 02 Jan 2010 01:10:30 GMT"
later.toLocaleDateString() 		// => "01/01/2010"
later.toLocaleTimeString() 		// => "05:10:30 PM"
later.toISOString() 			// => "2010-01-02T01:10:30.000Z"; ES5 only


var d = new Date();
document.getElementById("demo").innerHTML = d.getTime();


new Date()
new Date(milliseconds)
new Date(dateString)
new Date(year, month, day, hours, minutes, seconds, milliseconds)

var d = new Date("2015-03-25");
var d = new Date("2015-03");
var d = new Date("2015");
var d = new Date("2015-03-25T12:00:00");
var d = new Date("Mar 25 2015");
var d = new Date("2015 Mar 25");
var d = new Date("January 25 2015");
var d = new Date("Jan 25 2015");
var d = new Date("2015, JANUARY, 25");
var d = new Date("03-25-2015");
var d = new Date("2015/03/25");
var d = new Date("Wed Mar 25 2015 09:56:24 GMT+0100 (W. Europe Standard Time)");
var d = new Date("Fri Mar 25 2015 09:56:24 GMT+0100 (Tokyo Time)");



var d = new Date();
var days = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
document.getElementById("demo").innerHTML = days[d.getDay()];

var d = new Date();
d.setFullYear(2020, 0, 14);
document.getElementById("demo").innerHTML = d;


var d = new Date();
d.setDate(20);
document.getElementById("demo").innerHTML = d;


var d = new Date();
d.setDate(d.getDate() + 50);
document.getElementById("demo").innerHTML = d;


var msec = Date.parse("March 21, 2012");
document.getElementById("demo").innerHTML = msec;


var msec = Date.parse("March 21, 2012");
var d = new Date(msec);
document.getElementById("demo").innerHTML = d;


var today, someday, text;
today = new Date();
someday = new Date();
someday.setFullYear(2100, 0, 14);

if (someday > today) {
    text = "Today is before January 14, 2100.";
} else {
    text = "Today is after January 14, 2100.";
}
document.getElementById("demo").innerHTML = text;
```


### Array
```js	
var a = [];                         // no elements
var b = new Array();                // equivalent to a
var c = [,,,,];                     // 4 elements, all undefined.
var d = new Array(4);               // equivalent to c
var e = ["the", 1, true];           // 3 elements of different types
var f = new Array("the", 1, true);  // equivalent to e
var fish = ["Lion", , "Angel"];		//fish[0] is "Lion", fish[1] is undefined, and fish[2] is "Angel"

var arr = ["hello world", 42, true];
typeof arr;     // "object"


//There’s no need to pre-populate an array with data, though. You can create an empty array and then add data to it later in several ways.
var myArray = [];
myArray[0] = "Hello";
myArray[1] = "World";

var empty = []; 					// Create an array with no elements and length = 0.
var primes = [2, 3, 5, 7, 11]; 		// An array with 5 numeric elements
var misc = [ 1.1, true, "a", ]; 	// 3 elements of various types + trailing comma
var cars = ["Saab", "Volvo", "BMW"];

var myArray = [];
myArray["fruit"] = "apple";
myArray["vehicle"] = "tank";


//Reading and writing
var a = ["white"];    // Start with a one-element array
var b = a[0];         // b => "white"
var c = a[100];       // c => undefined (no error)


a[1] = 3.14;          // a => ["white", 3.14]
var i = 2;
a[i] = 3;             // a => ["white", 3.14, 3]
a[i + 1] = "rabbit";  // a => ["white", 3.14, 3, "rabbit"]
a[a[i]] = a[0];       // a => ["white", 3.14, 3, "white"]


//Adding and deleting
var a = ["follow", "the", "white", "rabbit"];
var b = a.pop();             // a => ["follow", "the", "white"]
                             // b => "rabbit"
var c = a.push("RABBIT");    // a => ["follow", "the", "white", "RABBIT"]
                             // c => 4 (new length)
var d = a.shift();           // a => ["the", "white", "RABBIT"]
                             // d => "follow"
var e = a.unshift("FOLLOW"); // a => ["FOLLOW", "the", "white", "RABBIT"]
                             // e => 4 (new length)
var f = a.splice(2, 1);       // a => ["FOLLOW", "the", "RABBIT"]
                              // f => "white"
var g = a.splice(1, 2, "ME"); // a => ["FOLLOW", "ME"]
                              // g => ["the", "RABBIT"]
							  
							  
							  

var base = 1024;
var table = [base, base+1, base+2, base+3];

var count = [1,,3]; // An array with 3 elements, the middle one undefined.
var undefs = [,,]; // An array with 2 elements, both undefined.



a = new Array(5); // No elements, but a.length is 5.
a[1000] = 0; // Assignment adds one element but sets length to 1001.


var a1 = [,,,]; // This array is [undefined, undefined, undefined]
var a2 = new Array(3); // This array has no values at all
0 in a1 // => true: a1 has an element with index 0
0 in a2 // => false: a2 has no element with index 0


[].length // => 0: the array has no elements
['a','b','c'].length // => 3: highest index is 2, length is 3

var a = ["world"]; // Start with a one-element array
var value = a[0]; // Read element 0
a[1] = 3.14; // Write element 1
i = 2;
a[i] = 3; // Write element 2
a[i + 1] = "hello"; // Write element 3
a[a[i]] = a[0]; // Read elements 0 and 2, write element 3


a = [1,2,3,4,5]; // Start with a 5-element array.
a.length = 3; // a is now [1,2,3].
a.length = 0; // Delete all elements. a is [].
a.length = 5; // Length is 5, but no elements, like new Array(5)


Array.isArray([]) // => true
Array.isArray({}) // => false




//Furthermore, you can mix the types of data stored in the array:
var stuff = [1, "apple", undefined, 42, "tanks", null, []];

//You Can Have Different Objects in One Array
myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;


var cars = [
    "Saab",
    "Volvo",
    "BMW"
];


var car1 = "Saab";
var car2 = "Volvo";
var car3 = "BMW";


var cars = new Array("Saab", "Volvo", "BMW");



a = []; // Start with an empty array
a.push("zero") // Add a value at the end. a = ["zero"]
a.push("one", "two") // Add two more values. a = ["zero", "one", "two"]



a = [1,2,3];
delete a[1]; // a now has no element at index 1
1 in a // => false: no array index 1 is defined
a.length // => 3: delete does not affect array length


//join()
var a = [1, 2, 3]; // Create a new array with these three elements
a.join(); // => "1,2,3"
a.join(" "); // => "1 2 3"
a.join(""); // => "123"
var b = new Array(10); // An array of length 10 with no elements
b.join('-') // => '---------': a string of 9 hyphens



//reverse()
var a = [1,2,3];
a.reverse().join() // => "3,2,1" and a is now [3,2,1]


//sort()
var a = new Array("banana", "cherry", "apple");
a.sort();
var s = a.join(", "); // s == "apple, banana, cherry"


var a = [33, 4, 1111, 222];
a.sort(); // Alphabetical order: 1111, 222, 33, 4
a.sort(function(a,b) { // Numerical order: 4, 33, 222, 1111
return a-b; // Returns &lt; 0, 0, or &gt; 0, depending on order
});
a.sort(function(a,b) {return b-a}); // Reverse numerical order


a = ['ant', 'Bug', 'cat', 'Dog']
a.sort(); // case-sensitive sort: ['Bug','Dog','ant',cat']
a.sort(function(s,t) { // Case-insensitive sort
var a = s.toLowerCase();
var b = t.toLowerCase();
if (a < b) return -1;
if (a > b) return 1;
return 0;
}); // => ['ant','Bug','cat','Dog']


//concat()
var a = [1,2,3];
a.concat(4, 5) // Returns [1,2,3,4,5]
a.concat([4,5]); // Returns [1,2,3,4,5]
a.concat([4,5],[6,7]) // Returns [1,2,3,4,5,6,7]
a.concat(4, [5,[6,7]]) // Returns [1,2,3,4,5,[6,7]]


//slice()
var a = [1,2,3,4,5];
a.slice(0,3); // Returns [1,2,3]
a.slice(3); // Returns [4,5]
a.slice(1,-1); // Returns [2,3,4]
a.slice(-3,-2); // Returns [3]


//splice()
var a = [1,2,3,4,5,6,7,8];
a.splice(4); // Returns [5,6,7,8]; a is [1,2,3,4]
a.splice(1,2); // Returns [2,3]; a is [1,4]
a.splice(1,1); // Returns [4]; a is [1]


var a = [1,2,3,4,5];
a.splice(2,0,'a','b'); // Returns []; a is [1,2,'a','b',3,4,5]
a.splice(2,2,[1,2],3); // Returns ['a','b']; a is [1,2,[1,2],3,3,4,5]

//push() and pop()
var stack = []; // stack: []
stack.push(1,2); // stack: [1,2] Returns 2
stack.pop(); // stack: [1] Returns 2
stack.push(3); // stack: [1,3] Returns 2
stack.pop(); // stack: [1] Returns 3
stack.push([4,5]); // stack: [1,[4,5]] Returns 2
stack.pop() // stack: [1] Returns [4,5]
stack.pop(); // stack: [] Returns 1


//unshift() and shift()
var a = []; // a:[]
a.unshift(1); // a:[1] Returns: 1
a.unshift(22); // a:[22,1] Returns: 2
a.shift(); // a:[1] Returns: 22
a.unshift(3,[4,5]); // a:[3,[4,5],1] Returns: 3
a.shift(); // a:[[4,5],1] Returns: 3
a.shift(); // a:[1] Returns: [4,5]
a.shift(); // a:[] Returns: 1

//toString() and toLocaleString()
[1,2,3].toString() // Yields '1,2,3'
["a", "b", "c"].toString() // Yields 'a,b,c'
[1, [2,'c']].toString() // Yields '1,2,c'


//forEach()
var data = [1,2,3,4,5]; // An array to sum
// Compute the sum of the array elements
var sum = 0; // Start at 0
data.forEach(function(value) { sum += value; }); // Add each value to sum
sum // => 15
// Now increment each array element
data.forEach(function(v, i, a) { a[i] = v + 1; });
data // => [2,3,4,5,6]



function foreach(a,f,t) {
try { a.forEach(f,t); }
catch(e) {
if (e === foreach.break) return;
else throw e;
}
}
foreach.break = new Error("StopIteration");


//map()
a = [1, 2, 3];
b = a.map(function(x) { return x*x; }); // b is [1, 4, 9]

//filter()
a = [5, 4, 3, 2, 1];
smallvalues = a.filter(function(x) { return x < 3 }); // [2, 1]
everyother = a.filter(function(x,i) { return i%2==0 }); // [5, 3, 1]


//every() and some()
a = [1,2,3,4,5];
a.every(function(x) { return x < 10; }) // => true: all values < 10.
a.every(function(x) { return x % 2 === 0; }) // => false: not all values even.

a = [1,2,3,4,5];
a.some(function(x) { return x%2===0; }) // => true a has some even numbers.
a.some(isNaN) // => false: a has no non-numbers.


//reduce(), reduceRight()
var a = [1,2,3,4,5]
var sum = a.reduce(function(x,y) { return x+y }, 0); // Sum of values
var product = a.reduce(function(x,y) { return x*y }, 1); // Product of values
var max = a.reduce(function(x,y) { return (x>y)?x:y; }); // Largest value

var a = [2, 3, 4]
// Compute 2^(3^4). Exponentiation has right-to-left precedence
var big = a.reduceRight(function(accumulator,value) {
return Math.pow(value,accumulator);
});


//indexOf() and lastIndexOf()
a = [0,1,2,1,0];
a.indexOf(1) // => 1: a[1] is 1
a.lastIndexOf(1) // => 3: a[3] is 1
a.indexOf(3) // => -1: no element has value 3


var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;

var cars = [
    "Saab",
    "Volvo",
    "BMW"
];


var car1 = "Saab";
var car2 = "Volvo";
var car3 = "BMW";


var cars = new Array("Saab", "Volvo", "BMW");



//You Can Have Different Objects in One Array
myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;



var person = ["John", "Doe", 46];

var person = {firstName:"John", lastName:"Doe", age:46};


var x = cars.length;         // The length property returns the number of elements in cars
var y = cars.sort();         // The sort() method sort cars in alphabetical order


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.length;                       // the length of fruits is 4


//Adding Array Elements
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Lemon");                // adds a new element (Lemon) to fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Lemon";     // adds a new element (Lemon) to fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[10] = "Lemon";                // adds a new element (Lemon) to fruits


var index;
var fruits = ["Banana", "Orange", "Apple", "Mango"];
for	(index = 0; index < fruits.length; index++) {
    text += fruits[index];
}



var person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
var x = person.length;         // person.length will return 3
var y = person[0];             // person[0] will return "John"


var person = [];
person["firstName"] = "John";
person["lastName"] = "Doe";
person["age"] = 46;
var x = person.length;         // person.length will return 0
var y = person[0];             // person[0] will return undefined



var points = new Array();         // Bad
var points = [];                  // Good 


var points = new Array(40, 100, 1, 5, 25, 10)  // Bad
var points = [40, 100, 1, 5, 25, 10];          // Good


var points = new Array(40, 100);  // Creates an array with two elements (40 and 100)


var fruits = ["Banana", "Orange", "Apple", "Mango"];

typeof fruits;             // typeof returns object



function isArray(myArray) {
    return myArray.constructor.toString().indexOf("Array") > -1;
}



var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.valueOf();


var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();


var fruits = ["Banana", "Orange","Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");

//The pop() method removes the last element from an array:
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();              // Removes the last element ("Mango") from fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.pop();      // the value of x is "Mango"


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");       //  Adds a new element ("Kiwi") to fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.push("Kiwi");   //  the value of x is 5



var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();            // Removes the first element "Banana" from fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");    // Adds a new element "Lemon" to fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[0] = "Kiwi";        // Changes the first element of fruits to "Kiwi"


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Kiwi";          // Appends "Kiwi" to fruit

var fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];           // Changes the first element in fruits to undefined

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1);        // Removes the first element of fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();            // Sorts the elements of fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();            // Sorts the elements of fruits 
fruits.reverse();         // Reverses the order of the elements


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b});


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});
// now points[0] contains the highest value


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b});
// now points[0] contains the lowest value



var myGirls = ["Cecilie", "Lone"];
var myBoys = ["Emil", "Tobias","Linus"];
var myChildren = myGirls.concat(myBoys);     // Concatenates (joins) myGirls and myBoys


var arr1 = ["Cecilie", "Lone"];
var arr2 = ["Emil", "Tobias","Linus"];
var arr3 = ["Robin", "Morgan"];
var myChildren = arr1.concat(arr2, arr3);     // Concatenates arr1 with arr2 and arr3

var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1);

```

```js	
var person = ["John", "Doe", 46];
var person = {firstName:"John", lastName:"Doe", age:46};

var x = cars.length;         // The length property returns the number of elements in cars
var y = cars.sort();         // The sort() method sort cars in alphabetical order

//Mutator Methods

//Adding Array Elements
//push - push will add an item to the end of the array and return the array’s new length:

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Lemon");                // adds a new element (Lemon) to fruits


//pop - pop will remove the last element from the array and return it to you:
var tasks = [
"Pay phone bill",
"Write best-selling novel",
"Walk the dog"
];
tasks.pop(); // returns "Walk the dog"

//reverse - reverse will reverse the order of the items in the array
var tasks = [
"Pay phone bill",
"Write best-selling novel",
"Walk the dog"
];
tasks.reverse();


//shift - shift removes the first item in the array and returns it:
var tasks = [
"Pay phone bill",
"Write best-selling novel",
"Walk the dog"
];
tasks.shift(); // returns "Pay phone bill"
// tasks is now:
// ["Write best-selling novel",
// "Walk the dog"]


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.length;                       // the length of fruits is 4


//splice
//splice lets you perform selective surgery on an array, allowing you to simultaneously add and remove items from an array with just one command
var tasks = [
"Pay phone bill",
"Write best-selling novel",
"Walk the dog"
];
tasks.splice(1, 1, "World domination");
// tasks is now:
// ["Pay phone bill",
// "World domination",
// "Walk the dog"]


//slice
//slice will copy a part of an array and return it. Rather than modify the original array, it just makes a shallow copy.

var tasks, todo, cleanup, noCleaning;
tasks = [
"Fly a kite",
"Save the world",
[
"Clean bathroom",
"Clean garage",
"Clean up act"
]
];
todo = tasks.slice(0); // makes a copy of tasks
cleanup = tasks.slice(-1); // copies only the nested array
noCleaning = tasks.slice(0, 2);
➥// copies only the first two items


//toString - toString returns a string representing the array and its items

var arr = ["These", "words", "are", "separated", "by", "commas"];
arr.toString(); // returns "These,words,are,separated,by,commas"


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Lemon";     // adds a new element (Lemon) to fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[10] = "Lemon";                // adds a new element (Lemon) to fruits


var index;
var fruits = ["Banana", "Orange", "Apple", "Mango"];
for	(index = 0; index < fruits.length; index++) {
    text += fruits[index];
}

//indexOf
var alphabet;
alphabet = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v",  "w", "x", "y", "z"];
alert("The letter ’m’ is at index: " + alphabet.indexOf("m"));


//lastIndexOf works exactly like indexOf, but begins its search from the end of the array rather than the beginning
array.lastIndexOf(searchElement, [fromIndex]);


//forEach (JavaScript 1.6)
var arr, total;
arr = [4, 8, 15, 16, 23, 42];
total = 0;
arr.forEach(function(num) {
total = total + num;
});
alert("The total is: " + total);




var person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
var x = person.length;         // person.length will return 3
var y = person[0];             // person[0] will return "John"


var person = [];
person["firstName"] = "John";
person["lastName"] = "Doe";
person["age"] = 46;
var x = person.length;         // person.length will return 0
var y = person[0];             // person[0] will return undefined



var points = new Array();         // Bad
var points = [];                  // Good 


var points = new Array(40, 100, 1, 5, 25, 10)  // Bad
var points = [40, 100, 1, 5, 25, 10];          // Good


var points = new Array(40, 100);  // Creates an array with two elements (40 and 100)


var fruits = ["Banana", "Orange", "Apple", "Mango"];

typeof fruits;             // typeof returns object



function isArray(myArray) {
    return myArray.constructor.toString().indexOf("Array") > -1;
}



var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.valueOf();


var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();


var fruits = ["Banana", "Orange","Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");

//The pop() method removes the last element from an array:
var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();              // Removes the last element ("Mango") from fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.pop();      // the value of x is "Mango"


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");       //  Adds a new element ("Kiwi") to fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.push("Kiwi");   //  the value of x is 5



var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();            // Removes the first element "Banana" from fruits


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");    // Adds a new element "Lemon" to fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[0] = "Kiwi";        // Changes the first element of fruits to "Kiwi"


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Kiwi";          // Appends "Kiwi" to fruit

var fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];           // Changes the first element in fruits to undefined

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");


var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1);        // Removes the first element of fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();            // Sorts the elements of fruits

var fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();            // Sorts the elements of fruits 
fruits.reverse();         // Reverses the order of the elements


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b});


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});
// now points[0] contains the highest value


var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b});
// now points[0] contains the lowest value



var myGirls = ["Cecilie", "Lone"];
var myBoys = ["Emil", "Tobias","Linus"];
var myChildren = myGirls.concat(myBoys);     // Concatenates (joins) myGirls and myBoys


var arr1 = ["Cecilie", "Lone"];
var arr2 = ["Emil", "Tobias","Linus"];
var arr3 = ["Robin", "Morgan"];
var myChildren = arr1.concat(arr2, arr3);     // Concatenates arr1 with arr2 and arr3

var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
var citrus = fruits.slice(1);



//Conditional (Ternary) Operator
var voteable = (age < 18) ? "Too young":"Old enough";


//JavaScript Comparison and Logical Operators

//Array! Array! Array!
//One of the greatest love stories of all time is that between a data structure known as an array and the for loop:

var myArray = ["one", "two", "three"];
  
for (var i = 0; i < myArray.length; i++) {
    document.writeln(myArray[i]);
}


for (i = 0, len = cars.length, text = ""; i < len; i++) { 
    text += cars[i] + "<br>";
}


var i = 2;
var len = cars.length;
var text = "";
for (; i < len; i++) { 
    text += cars[i] + "<br>";
}



//You Don't Have to Use Numbers. When filling out your for loop, you don't have to only use numbers:

for (var i = "a"; i !="aaaaaaaa"; i += "a") {
    document.writeln("hmm...");
}


```


### Objects
```js	

var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};


var person = {
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};


var person = new Object();
person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";



//Using an Object Constructor
function person(first, last, age, eye) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eye;
}
var myFather = new person("John", "Doe", 50, "blue");
var myMother = new person("Sally", "Rally", 48, "green");



person.firstname + " is " + person.age + " years old.";


person["firstname"] + " is " + person["age"] + " years old.";


var person = {fname:"John", lname:"Doe", age:25}; 

for (x in person) {
    txt += person[x];
}


//Deleting Properties
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
delete person.age;   // or delete person["age"]; 


name = person.fullName();


name = person.fullName;



//Adding New Methods
function person(firstName, lastName, age, eyeColor) {
    this.firstName = firstName;  
    this.lastName = lastName;
    this.age = age;
    this.eyeColor = eyeColor;
    this.changeName = function (name) {
        this.lastName = name;
    }
}


function person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
person.prototype.nationality = "English";



function person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
person.prototype.name = function() {
    return this.firstName + " " + this.lastName;
};


var myObject = new Object();

//it is much better to do this:
var myObject = {};

var empty = {}; // An object with no properties
var point = { x:0, y:0 }; // Two properties
var point2 = { x:point.x, y:point.y+1 }; // More complex values
var book = {
"main title": "JavaScript", // Property names include spaces,
'sub-title': "The Definitive Guide", // and hyphens, so use string literals
"for": "all audiences", // for is a reserved word, so quote
author: { // The value of this property is
firstname: "David", // itself an object. Note that
surname: "Flanagan" // these property names are unquoted.
}
};

//Additionally, you can use a numeric or string literal for the name of a property or nest an object inside another. The following example uses these options.
var car = { manyCars: {a: "Saab", "b": "Jeep"}, 7: "Mazda" };
console.log(car.manyCars.b); // Jeep
console.log(car[7]); // Mazda


var foo = {a: "alpha", 2: "two"};
console.log(foo.a);    // alpha
console.log(foo[2]);   // two
//console.log(foo.2);  // Error: missing ) after argument list
//console.log(foo[a]); // Error: a is not defined
console.log(foo["a"]); // alpha
console.log(foo["2"]); // two


//:EX:1
var car = {type:"Fiat", model:500, color:"white"};

//:EX:1
var obj = {};
obj["firstName"] = "Hugo";
obj["lastName"] = "Reyes";

//:EX:1
var obj = {};
obj.firstName = "Hugo";
obj.lastName = "Reyes";

//:EX:2
//Reading from an Object
var obj = {};
obj.firstName = "Hugo";
obj.lastName = "Reyes";
alert("Hello, my name is " + obj.firstName + " " + obj.lastName + ".");

//:EX:2
//Unlike arrays, it’s not possible to read the contents of an object using a numeric index.
var obj = {};
obj.firstName = "Hugo";
obj[0]; // returns undefined
obj["firstName"]; // returns "Hugo"
obj.firstName; // returns "Hugo"


//:EX:2
//Nested Objects

var person;
person = {
name: {
first: "Hugo",
last: "Reyes"
}
};
person.name.first; // returns "Hugo"
person.name.last; // returns "Reyes"

//:EX:2
//Nested Objects - assign objects
var person;
person = {};
person.name = {};
person.name.first = "Hugo";
person.name.last = "Reyes";


//:EX:2
//Note, however, that the following will fail to work:
var person;
person = {};
person.name.first = "Hugo";


//:EX:2
//Namespacing through Nested Objects
Project.Strings.Warnings.sessionExpired =  "Your session has expired."

var Project = {
	Strings: {
		Warnings: {
			overQuota: "You've exceeded your quota!",
			outOfStock: "We're out of stock!"
		}
	}
};

//Looping over an Object
var data, key;
data = {
	firstName: "James",
	lastName: "Kirk",
	occupation: "Captain"
};

for (key in data) {
	alert(key + " is " + data[key]);
}




//:EX:2
// Define Person constructor function in order to create custom Person() objects later.
var Person = function (living, age, gender) {
this.living = living;
this.age = age;
this.gender = gender;
this.getGender = function () { return this.gender; };
};

// Instantiate a Person object and store it in the cody variable.
var cody = new Person(true, 33, 'male');
console.log(cody);


//Property Access Expressions
var o = {x:1,y:{z:3}}; // An example object
var a = [o,4,[5,6]]; // An example array that contains the object
o.x // => 1: property x of expression o
o.y.z // => 3: property z of expression o.y
o["x"] // => 1: property x of object o
a[1] // => 4: element at index 1 of expression a
a[2]["1"] // => 6: element at index 1 of expression a[2]
a[0].x // => 1: property x of expression a[0]


var person = {
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};

person.lastName;
person["lastName"];

name = person.fullName();


name = person.fullName;


//Do Not Declare Strings, Numbers, and Booleans as Objects!
var x = new String();        // Declares x as a String object
var y = new Number();        // Declares y as a Number object
var z = new Boolean();       //	Declares z as a Boolean object

//Avoid String, Number, and Boolean objects. They complicate your code and slow down execution speed.

```

var x = {};  									// new Empty Object
var x = {firstName:"John", lastName:"Doe"};    // Object


//Array of objects
var tasks;
tasks = [
			{
				text: "Pay phone bill",
				complete: false,
				priority: 1
			},
			{
				text: "Write best-selling novel",
				complete: false,
				priority: 3
			},
			{
				text: "Walk the dog",
				complete: false,
				priority: 2
			}
		];

```	


```js
var person = {fname:"John", lname:"Doe", age:25}; 

var text = "";
var x;
for (x in person) {
    text += person[x];
}


var cars = ["BMW", "Volvo", "Saab", "Ford"];
var i = 0;
var text = "";

for (;cars[i];) {
    text += cars[i] + "<br>";
    i++;
}



for (i = 0; i < 10; i++) {
    if (i === 3) { break; }
    text += "The number is " + i + "<br>";
}

```


### Functions
```js	

//Function Declarations
function myFunction(a, b) {
    return a * b;
}

//Function Expressions
var x = function (a, b) {return a * b};


//Self-Invoking Functions
(function () {
    var x = "Hello!!";      // I will invoke myself
})();


//Functions Can Be Used as Values
function myFunction(a, b) {
    return a * b;
}

var x = myFunction(4, 3);


//Invoking a Function with a Function Method
function myFunction(a, b) {
    return a * b;
}
myObject = myFunction.call(myObject, 10, 2);     // Will return 20


function myFunction(a, b) {
    return a * b;
}
myArray = [10, 2];
myObject = myFunction.apply(myObject, myArray);  // Will also return 20


//Sample:1
//function declaration 
function sayHello() {
alert("Hello, world!");
}

sayHello();


//function expression
var add = function(num1, num2) {
return num1 + num2;
};



//Sample:2
function sayHello(msg) {
alert(msg);
}

sayHello("Howdy, y'all!");


//Sample:3
function fullName() {
	var firstName = "Hugo";
	
	function alertFullName() {
		var lastName = "Reyes";
		alert("Full name: " + firstName + " " + lastName);
	}
	
	alertFullName();
}

fullName();

//Sample:4
function foo() {
    return 42;
}

foo.bar = "hello world";

typeof foo;         // "function"
typeof foo();       // "number"
typeof foo.bar;     // "string"




//Sample:4
// Declaring a global variable and giving it the value "a"
var a = "a";
function levelb() {
	// Declaring a variable that levelb and children can see
	var b = "b";
	function levelc() {
		// Declaring a variable only levelc and leveld can see
		var c = "c";
			function leveld() {
			// Declaring a variable only leveld can see
				var d = "d";
				console.log("leveld", a, b, c, d);
			}
		// Running leveld() will output a, b, c and d
		leveld();
		console.log("levelc", a, b, c);
	}
	// Running levelc() will output a, b, and c
	levelc();
	console.log("levelb", a, b);
}

// Running levelb() will output a and b
levelb();

// Only the variable named "a" is available globally
console.log("global", a);


//Sample:5
// declaration
function sayHello1() {
alert("Hello");
}
// expression
var sayHello2 = function() {
alert("Hello");
};
// constructor (not recommended)
var sayHello3 = new Function("alert('Hello')");


//Nested Functions
function hypotenuse(a, b) {
function square(x) { return x*x; }
return Math.sqrt(square(a) + square(b));
}

//Function Invocation
printprops({x:1});
var total = distance(0,0,2,1) + distance(2,1,3,5);
var probability = factorial(5)/factorial(13);



//Functions As Values
function square(x) { return x*x; }

var s = square; // Now s refers to the same function that square does
square(4); // => 16
s(4); // => 16



var o = {square: function(x) { return x*x; }}; // An object literal
var y = o.square(16); // y equals 256



//anonymous function
(function() { // mymodule function rewritten as an unnamed expression
// Module code goes here.
}()); // end the function literal and invoke it now.





//Sample:6
//Arguments
function person(firstName, lastName, age) {
alert(firstName);
alert(lastName);
alert(age);
}
person("John", "Doe", 44);


//Sample:6
function howManyArgs() {
alert(arguments.length);
}
howManyArgs(“string”, 45); //2
howManyArgs(); //0
howManyArgs(12); //1


//Sample:6
function doAdd() {
if(arguments.length == 1) {
alert(arguments[0] + 10);
} else if (arguments.length == 2) {
alert(arguments[0] + arguments[1]);
}
}
doAdd(10); //20
doAdd(30, 20); //50



var checking, savings;
// This is the definition of our Account class

function Account(accountNumber) {
	// This is the property we'll be storing the
	// account number in.
	this.accountNumber = accountNumber;
	// This is the property we'll be tracking the
	// account's funds in.
	this.funds = 0;
	// This is the setter method we'll be using to
	// add funds to the account.
	this.deposit = function(amount) {
		if (amount === Number(amount)) {
			this.funds += amount;
		}
	};
	// This is the getter method that returns the
	// account's balance.
	this.balance = function() {
		return this.funds;
	};
}

// The "new Account()" constructor returns a new account  object complete with deposit and balance methods. We
// store the account object in a variable called checking.
checking = new Account("87654321");

// Using the deposit method allows us to pass values to our account object.
checking.deposit(12.35);
checking.deposit(2.76);
checking.deposit(74.01);

// We now create a new account object and store that in a  variable called savings. It also has deposit and
// balance methods, and is distinct from the "checking" account object.
savings = new Account("12345678");
savings.deposit(225.57);
// Using the objects' balance method, we can ask each of them to report their balances.
checking.balance(); // returns 89.12
savings.balance(); // returns 225.57


//constructor
var foo, bar, baz;
function Foo() {
	this.ident = "foo";
}

foo = new Foo();
foo.ident; // returns "foo"

bar = new Foo();
bar.ident; // returns "foo"
bar.ident = "bar";
bar.ident; // now returns "bar"

baz = new bar.constructor();
baz.ident; // returns "foo"


"John".constructor                 // Returns function String()  { [native code] }
(3.14).constructor                 // Returns function Number()  { [native code] }
false.constructor                  // Returns function Boolean() { [native code] }
[1,2,3,4].constructor              // Returns function Array()   { [native code] }
{name:'John', age:34}.constructor  // Returns function Object()  { [native code] }
new Date().constructor             // Returns function Date()    { [native code] }
function () {}.constructor         // Returns function Function(){ [native code] }



//Overloading
function sayMessage(message) {
console.log(message);
}
function sayMessage() {
console.log("Default message");
}
sayMessage("Hello!"); // outputs "Default message"




//length - If you ever need to know how many arguments a function is expecting, you can check with the length property:

function foo(bar, baz) {
}
foo.length; // returns 2

//EX:3
//apply
var person, lastName;
lastName = "Reyes";

person = function() {
	return this.lastName;
};

person(); // returns "Reyes"
person.apply({lastName: "Cooper"}); // returns "Cooper"


//EX:3
//apply

var tax;
tax = function(price, provincial, federal) {
return price * provincial * federal;
};
tax.apply(null, [100, 1.05, 1.095]); // returns 114.975


//call
var tax;
tax = function(price, provincial, federal) {
return price * provincial * federal;
};
tax.call(null, 100, 1.05, 1.095); // returns 114.975


//bind
var hugo, person, names;
person = function () {
return this.lastName;
};
hugo = person.bind({lastName: "Reyes"});
hugo(); // returns "Reyes"
names = {
lastName: "Cooper",
hugo: hugo,
person: person
};
names.hugo(); // returns "Reyes"
names.person(); // returns "Cooper"

//toString

function foo() {
return "foo";
}

foo.toString();





function myFunction(p1, p2) {
    return p1 * p2;              // The function returns the product of p1 and p2
}

var x = myFunction(4, 3);        // Function is called, return value will end up in x


//Local JavaScript Variables

//Sample:1


// code here can not use carName

function myFunction() {
    var carName = "Volvo";

    // code here can use carName

}


//Global JavaScript Variables
//Sample:2

var carName = " Volvo";

// code here can use carName

function myFunction() {

    // code here can use	carName 

}


//Automatically Global
//Sample:3

// code here can use carName

function myFunction() {
    carName = "Volvo";

    // code here can use carName
}

function myFunction(p1, p2) {
    return p1 * p2;              // The function returns the product of p1 and p2
}


document.getElementById("demo").innerHTML = myFunction(4, 3);        // Function is called, return value will end up in x

function myFunction(a, b) {
    return a * b;                // Function returns the product of a and b
}


```


### Math
```js	
Math.random();       // returns a random number
Math.min(0, 150, 30, 20, -8, -200);      // returns -200
Math.max(0, 150, 30, 20, -8, -200);      // returns 150
Math.random();              // returns a random number
Math.round(4.7);            // returns 5
Math.round(4.4);            // returns 4
Math.ceil(4.4);             // returns 5
Math.floor(4.7);            // returns 4
Math.floor(Math.random() * 11);   // returns a random number between 0 and 10

Math.E          // returns Euler's number
Math.PI         // returns PI
Math.SQRT2      // returns the square root of 2
Math.SQRT1_2    // returns the square root of 1/2
Math.LN2        // returns the natural logarithm of 2
Math.LN10       // returns the natural logarithm of 10
Math.LOG2E      // returns base 2 logarithm of E
Math.LOG10E     // returns base 10 logarithm of E


Math.pow(2,53) // => 9007199254740992: 2 to the power 53
Math.round(.6) // => 1.0: round to the nearest integer
Math.ceil(.6) // => 1.0: round up to an integer
Math.floor(.6) // => 0.0: round down to an integer
Math.abs(-5) // => 5: absolute value
Math.max(x,y,z) // Return the largest argument
Math.min(x,y,z) // Return the smallest argument
Math.random() // Pseudo-random number x where 0 <= x < 1.0
Math.PI // π: circumference of a circle / diameter
Math.E // e: The base of the natural logarithm
Math.sqrt(3) // The square root of 3
Math.pow(3, 1/3) // The cube root of 3
Math.sin(0) // Trigonometry: also Math.cos, Math.atan, etc.
Math.log(10) // Natural logarithm of 10
Math.log(100)/Math.LN10 // Base 10 logarithm of 100
Math.log(512)/Math.LN2 // Base 2 logarithm of 512
Math.exp(3) // Math.E cubed
```


###  Conditions
```js	
//Conditional (Ternary) Operator
var voteable = (age < 18) ? "Too young":"Old enough";


if (i > 25) {
	alert(“Greater than 25.”);
} else if (i < 0) {
	alert(“Less than 0.”);
} else {
	alert(“Between 0 and 25, inclusive.”);
}


age = Number(age);
if (isNaN(age)) {
    voteable = "Error in input";
} else {
    voteable = (age < 18) ? "Too young" : "Old enough";
}




if (time < 10) {
    greeting = "Good morning";
} else if (time < 20) {
    greeting = "Good day";
} else {
    greeting = "Good evening";
}


```



### Switch
```js

switch (new Date().getDay()) {
    case 0:
        day = "Sunday";
        break;
    case 1:
        day = "Monday";
        break;
    case 2:
        day = "Tuesday";
        break;
    case 3:
        day = "Wednesday";
        break;
    case 4:
        day = "Thursday";
        break;
    case 5:
        day = "Friday";
        break;
    case 6:
        day = "Saturday";
        break;
}

```

### Loop 

### for loop
```js
for (i = 0; i < cars.length; i++) { 
    text += cars[i] + "<br>";
}

for (var i = 0; i < 10 && i % 2 === 0; i+=4) {
console.log(i);
}

//It’s also possible to have multiple initializations and end expressions:
for (var i = 0, j = 0; i < 3; i++, j+=2) {
console.log(i, j);
}
```


```js
//The for ... in Loop

var agents = {
	'005': "Michael Harp",
	'006': "John Smith",
	'007': "James Bond"
};
for (key in agents) {
	if ('007' === key) {
		console.log('Bond, ' + agents[key] + 'has been found!');
	} else {
		console.log('Standard spy, ' + agents[key] + 'has been found');
	}
}
```


### while loop
```js

while (i < 10) {
    text += "The number is " + i;
    i++;
}


var cars = ["BMW", "Volvo", "Saab", "Ford"];
var i = 0;
var text = "";

while (cars[i]) {
    text += cars[i] + "<br>";
    i++;
}
```

### do while loop
```js
do {
    text += "The number is " + i;
    i++;
}
while (i < 10);
```



## Operators


### Boolean Operators
```js	
alert(!false); //true
alert(!”blue”); //false
alert(!0); //true
alert(!NaN); //true
alert(!””); //true
alert(!12345); //false
alert(!!”blue”); //true
alert(!!0); //false
alert(!!NaN); //false
alert(!!””); //false
alert(!!12345); //true
```


### Comparison Operators
```js	
Operator	Description							Comparing	Returns	
==			equal to							x == 8		false	
												x == 5		true	
												x == "5"	true	
===			equal value and equal type			x === 5		true	
												x === "5"	false	
!=			not equal							x != 8		true	
!==			not equal value or not equal type	x !== "5"	true	
x 												!== 5		false	
>			greater than						x > 8		false	
<			less than							x < 8		true	
>=			greater than or equal to			x >= 8		false	
<=			less than or equal to				x <= 8		true

//Equal (==)
1 == 1 		// returns true
"1" == 1 	// returns true ("1" converts to 1)
1 == true 	// returns true
0 == false 	// returns true
"" == 0 	// returns true ("" converts to 0)
" " == 0 	// returns true (" " converts to 0)
0 == 1 		// returns false
1 == false 	// returns false
0 == true 	// returns false
var x, y; 	// declare x and y
x = {}; 	// create an object and assign it to x
y = x; 		// point y to x
x == y; 	// returns true (refers to same object in memory)
x == {}; 	// returns false (not the same object)

//Not Equal (!=)
1 != 1 // returns false
"1" != 1 // returns false ("1" converts to 1)
1 != true // returns false
0 != false // returns false
"" != 0 // returns false ("" converts to 0)
" " != 0 // returns false (" " converts to 0)
0 != 1 // returns true
1 != false // returns true
0 != true // returns true
var x, y; // declare x and y
x = {}; // create an object and assign it to x
y = x; // point y to x
x != y; // returns false (refers to same object in memory)
x != {}; // returns true (not the same object)


//Strict Equal (===)
1 === 1 // returns true
"1" === 1 // returns false ("1" is not converted)
1 === true // returns false
0 === false // returns false
"" === 0 // returns false ("" is not converted)
" " === 0 // returns false (" " is not converted)
0 === 1 // returns false
1 === false // returns false
0 === true // returns false
var x, y; // declare x and y
x = {}; // create an object and assign it to x
y = x; // point y to x
x === y; // returns true (refers to same object in memory)
x === {}; // returns false (not the same object)

//Strict Not Equal (!==)
1 !== 1 // returns false
"1" !== 1 // returns true ("1" is not converted)
1 !== true // returns true
0 !== false // returns true
"" !== 0 // returns true ("" is not converted)
" " !== 0 // returns true (" " is not converted)
0 !== 1 // returns true
1 !== false // returns true
0 !== true // returns true
var x, y; // declare x and y
x = {}; // create an object and assign it to x
y = x; // point y to x
x !== y; // returns false (refers to same object in memory)
x !== {}; // returns true (not the same object)


//Greater than (>)
0 > 1 // returns false
1 > 1 // returns false
2 > 1 // returns true
2 > "" // returns true ("" converts to 0)

//Greater than or Equal to (>=)
0 >= 1 // returns false
1 >= 1 // returns true
"1" >= 1 // returns true ("1" converts to 1)

//Less than (<)
0 < 1 // returns true
1 < 1 // returns false
2 < 1 // returns false
2 < "" // returns false ("" converts to 0)

//Less than or Equal to (<=)
0 <= 1 // returns true
1 <= 1 // returns true
"1" <= 1 // returns true ("1" converts to 1)
2 <= 1 // returns false
"2" <= 1 // returns false ("2" converts to 2)

//&& symbols (AND)
true && true; // returns true
true && false; // returns false
false && true; // returns false
0 && 1; // returns 0
0 && 2; // returns 0
1 && 0; // returns 0
2 && 0; // returns 0
"foo" && "bar" // returns "bar"


//|| symbols (OR)
true || true; // returns true
true || false; // returns true
false || true; // returns true
0 || 1; // returns 1
0 || 2; // returns 2
1 || 0; // returns 1
2 || 0; // returns 2
"foo" || "bar"; // returns foo


//!  symbols (NOT)
!true; // returns false
!false; // returns true
!0; // returns true
!1; // returns false
!"foo"; // returns false

```

### Logical Operators
```js
&&		and			(x < 10 && y > 1) is true		
||		or			(x == 5 || y == 5) is false		
!		not			!(x == y) is true
```
