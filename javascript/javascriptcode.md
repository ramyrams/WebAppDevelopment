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
