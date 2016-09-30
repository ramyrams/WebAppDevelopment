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

### Constants
```js
const prefix = '212';
```

### Escape single quote and double quote
```js
var answer = "It's alright";
var answer = "He is called 'Johnny'";
var answer = 'He is called "Johnny"';
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
