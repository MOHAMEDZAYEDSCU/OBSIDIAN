```javascript
<!------------------------------!>

# JavaScript Comments:

- Single Line Comments ⇒ // hello

- Multi-line Comments ⇒ /*hello*/

<!------------------------------!>

# JavaScript Variables:

var:

let

const

<!------------------------------!>

# JavaScript Operators:

const x = 10

const y = 5

---

# JavaScript Arithmetic Operators

+ = x + y ⇒ 15

- = x - y ⇒ 5

* = x * y ⇒ 50

** = x ** y ⇒ 100,000

/ = x / y ⇒ 2

% = x % y ⇒ 0

---

# JavaScript Assignment Operators

+= ⇒ x += y ⇒ x = x + y

-= ⇒ x -= y ⇒ x = x - y

*= ⇒ x *= y ⇒ x = x * y

/= ⇒ x /= y ⇒ x = x / y

%= ⇒ x %= y ⇒ x = x % y

**= ⇒ x **= y ⇒ x = x ** y

---

# JavaScript Comparison Operators

== ⇒ equal to

=== ⇒ equal value and equal type

!= ⇒ not equal

!== ⇒ not equal value or not equal type

> ⇒ greater than

< ⇒ less than

>= ⇒ greater than or equal to

<= ⇒ less than or equal to

? ⇒ ternary operator

---

# JavaScript Logical Operators

&& ⇒ logical and

|| ⇒ logical or

! ⇒ logical not

---

# JavaScript Type Operators

typeof ⇒ Returns the type of a variable

instanceof ⇒ Returns true if an object is an instance of an object type

<!------------------------------!>

JavaScript Data Types:

1. String ⇒ let lastName = "Johnson";

2. Number ⇒ let length = 16;

3. Boolean ⇒ let x = true

4. Undefined ⇒ let car;

5. Array ⇒ const cars = ["Saab", "Volvo", "BMW"];

6. Object ⇒ const person = {firstName:"John", lastName:"Doe"};

<!------------------------------!>

# JavaScript Functions:

function NameOfFunction (params) {

Block OF Code

}

<!------------------------------!>

# JavaScript Events:

HTML:

<elemnt event=’Some JavaScript’>

Like :

onchange ⇒ An HTML element has been changed

onclick ⇒ The user clicks an HTML element

onmouseover ⇒ The user moves the mouse over an HTML element

onmouseout ⇒ The user moves the mouse away from an HTML element

onkeydown ⇒ The user pushes a keyboard key

onload ⇒ The browser has finished loading the page

<!------------------------------!>

# JavaScript Strings:

let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";

let length = text.length;

# Escape Characters

\’ ⇒ ‘

\” ⇒ “

\\ ⇒ \

\b ⇒ BackSpace

\f ⇒ Form Feed

\n ⇒ New Line

\r ⇒ Carriage Return

\t ⇒ Horizontal Tabulator

\v ⇒ Vertical Tabulator

---

# Basic String Methods:

String length

String charAt()

String charCodeAt()

String at()

String [ ]

String slice()

String substring()

String substr()

String toUpperCase()

String toLowerCase()

String concat()

String trim()

String trimStart()

String trimEnd()

String repeat()

String replace()

String split()

<!------------------------------!>

# JavaScript Number:

# JavaScript Number Methods:

toString() ⇒ Returns a number as a string

toExponential() ⇒ Returns a number written in exponential notation

toFixed() ⇒ Returns a number written with a number of decimals

toPrecision() ⇒ Returns a number written with a specified length

ValueOf() ⇒ Returns a number as a number

<!------------------------------!>

# JavaScript Array:

// arrayVV.length => return length of array

// arrayVV.toString() => converts an array to a string of (comma separated) array values

// arrayVV.join() => method also joins all array elements into a string and add character betwen values

// arrayVV.pop() => remove last element from a array

// arrayVV.push() => method adds a new element to an array (at the end):

// arrayVV.shift() => remove first element from a array

// arrayVV.unshift() => method adds a new element to an array (at the first):

// arrayVV.concat() => The concat() method creates a new array by merging (concatenating) existing arrays

// arrayVV.copywithin() => The copyWithin() method copies array elements to another position in an array

// arrayVV.splice => The splice() method can be used to add new items to an array:

// arrayVV.slice => The slice() method slices out a piece of an array into a new array:

<!------------------------------!>

# JavaScript Date:

# Date Get Methods:

getFullYear() ⇒ Get year as a four digit number (yyyy)

getMonth() ⇒ Get month as a number (0-11)

getDate() ⇒ Get day as a number (1-31)

getDay() ⇒ Get weekday as a number (0-6)

getHours() ⇒ Get hour (0-23)

getMinutes() ⇒ Get minute (0-59)

getSeconds() ⇒ Get second (0-59)

getMilliseconds() ⇒ Get millisecond (0-999)

getTime() ⇒ Get time (milliseconds since January 1, 1970)

<!------------------------------!>

# JavaScript If..Else:

The else if Statement

Use the else if statement to specify a new condition if the first condition is false.

# Syntax:

if (condition1) {

block of code to be executed if condition1 is true

} else if (condition2) {

block of code to be executed if the condition1 is false and condition2 is true

} else {

block of code to be executed if the condition1 is false and condition2 is false

}

<!------------------------------!>

# JavaScript Switch:

Use the switch statement to select one of many code blocks to be executed.

## Syntax

switch(expression) {

case x:

// code block

break;

case y:

// code block

break;

default:

// code block

}

<!------------------------------!>

# JavaScript Loop (For):

let cars = [”bmw”, ”farary”, “marseds”]

for (let i = 0; i < cars.length; i++) {

text += cars[i] + "<br>";

}

<!------------------------------!>

# JavaScript Loop (For in):

for (key in object) {

*code block to be executed*

}

<!------------------------------!>

# JavaScript Loop (For Of) :

for (variable of iterable) {

*code block to be executed*

}

<!------------------------------!>

# JavaScript While:

while (i < 10) {

text += "The number is " + i;

i++;

}

<!------------------------------!>

# JavaScript RegExp:

Exp-2

let text = "Visit W3Schools";

let n = text.search(/GLITCH/i); ⇒ 6

Exp-1

let text = "Visit Microsoft!";

let result = text.replace(/microsoft/i, "W3Schools"); ⇒ The replace() method replaces a specified value with another value in a string

Regular Expression Modifiers

**Modifiers** can be used to perform case-insensitive more global searches:

i ⇒ Perform case-insensitive matching

g ⇒ Perform a global match (find all)

m ⇒ Perform multiline matching

d ⇒ Perform start and end matching

—

Regular Expression Patterns:

[abc] ⇒ Find any of the characters between the brackets

[0-9] ⇒ Find any of the digits between the brackets

(x|y) ⇒ Find any of the alternatives separated with |

—

**Metacharacters** are characters with a special meaning:

\d ⇒ Find a digit

\s ⇒ Find a whitespace character

\b ⇒ Find a match at the beginning of a word like this: \bWORD, or at the end of a word like this: WORD\b

—

**Quantifiers** define quantities:

n+ ⇒ Matches any string that contains at least one *n*

n* ⇒ Matches any string that contains zero or more occurrences of *n*

n? ⇒ Matches any string that contains zero or one occurrences of *n*

<!------------------------------!>

# JavaScript Classes:

Syntax

class ClassName {

constructor() {

...

}

}

Example

class Car {

constructor(name, year) {

this.name = name; this.year = year;

}

}

const myCar1 = new Car("Ford", 2014);

<!------------------------------!>
```