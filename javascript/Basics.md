# Where to put JS

- JavaScript code in HTML is inserted between `<script>` and `</script>` tags.
- JavaScript functions can be executed when an event occurs, like a user clicking a button.
- Scripts can be placed in the `<body>` or `<head>` section of an HTML page, or in external files with the .js extension.
- External scripts can be beneficial for reusing code in multiple web pages and improving page load speeds.
- External scripts can be referenced in 3 ways: with a full URL, file path, or no path.

# OUTPUT of JS

- The page is about JavaScript display possibilities, which include:
  - Writing into an HTML element using `innerHTML`
  - Writing into the HTML output using `document.write()`

    - `The document.write() method should only be used for testing`
  - Writing into an alert box using `window.alert()`

    - `You can skip the window keyword. In JavaScript, the window object is the global scope object. This means that variables, properties, and methods by default belong to the window object. This also means that specifying the window keyword is optional`
  - Writing into the browser console using `console.log()`
- To access an HTML element, JavaScript can use the `document.getElementById(id)` method
- The `window.print()` method can be used in the browser to print the content of the current window

# JS Statements

- JavaScript statements can be grouped together in code blocks, indicated by curly brackets `{}`.
- Semicolons are used to separate JavaScript statements and are recommended but not required.
- JavaScript ignores multiple spaces and allows line breaks after operators for readability.
- Keywords, such as `var`, `let`, `const`, `if`, `switch`, `for`, `function`, and `return`, identify the JavaScript action to be performed.
- JavaScript keywords are reserved words and cannot be used as names for variables.

# var let const

|       | Scope      | Redeclare | Reassign | Hoisted | Binds this |
| :---- | :--------- | :-------- | :------- | :------ | :--------- |
| var   | No(global) | Yes       | Yes      | Yes     | Yes        |
| let   | Yes        | No        | Yes      | No      | No         |
| const | Yes        | No        | No       | No      | No         |

## What is Good?

let and const have block scope.

let and const can not be redeclared.

let and const must be declared before use.

let and const does not bind to this.

let and const are not hoisted.

## What is Not Good?

var does not have to be declared.

var is hoisted.

var binds to this.

## When to use JavaScript const?

Always declare a variable with const when you know that the value should not be changed.

Use const when you declare:

* A new Array
* A new Object
* A new Function
* A new RegExp

---

## Constant Objects and Arrays

The keyword const is a little misleading.

It does not define a constant value. It defines a constant reference to a value.

Because of this you can NOT:

* Reassign a constant value
* Reassign a constant array
* Reassign a constant object
* But you CAN:Change the elements of constant array
* Change the properties of constant object

## Hoisting

Variables defined with var are hoisted to the top of the scope and can be initialized at any time.

Meaning: You can use the variable before it is declared

# Operators

## JavaScript Comparison Operators

| Operator | Description                       |
| :------- | :-------------------------------- |
| \==      | equal to                          |
| \===     | equal value and equal type        |
| \!=      | not equal                         |
| \!==     | not equal value or not equal type |
| \>       | greater than                      |
| \<       | less than                         |
| \>=      | greater than or equal to          |
| \<=      | less than or equal to             |
| ?        | ternary operator                  |

If you add a number and a string, the result will be a string\!

# Datatypes

### JavaScript has 8 Datatypes

1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object

The Object Datatype
The object data type can contain both built-in objects, and user defined objects:

Built-in object types can be:

objects, arrays, dates, maps, sets, intarrays, floatarrays, promises, and more.

Javascript numbers are always one type:
double (64-bit floating point).

# Functions

A JavaScript function is created using the `function` keyword, followed by a name, and then a pair of parentheses `()`. Function names can consist of letters, digits, underscores, and dollar signs, similar to variable naming rules. The parentheses can contain parameter names separated by commas: `(param1, param2, ...)`. The function's operations are defined inside curly brackets `{}`.

With functions you can reuse code

You can write code that can be used many times.

You can use the same code with different arguments, to produce different results.

## The () Operator

The () operator invokes (calls) the function.

Accessing a function without () returns the function and not the function result.

## Local Variables

Variables declared within a JavaScript function, become LOCAL to the function.

Local variables can only be accessed from within the function.

Since local variables are only recognized inside their functions, variables with the same name can be used in different functions.

Local variables are created when a function starts, and deleted when the function is completed.

# Objects

### How to Define a JavaScript Object

* Using an Object Literal
* Using the new Keyword
* Using an Object Constructor

## JavaScript Object Literal

An object literal is a list of name:value pairs inside curly braces {}.

{firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}

Objects written as name value pairs are similar to:

* Associative arrays in PHP
* Dictionaries in Python
* Hash tables in C
* Hash maps in Java
* Hashes in Ruby and Perl

## Accessing Object Properties

You can access object properties in two ways:

*objectName.propertyName*

*objectName\["propertyName"\]*

## JavaScript Object Methods

Methods are actions that can be performed on objects.

Methods are function definitions stored as property values.

| Property  | Property Value                                             |
| :-------- | :--------------------------------------------------------- |
| firstName | John                                                       |
| lastName  | Doe                                                        |
| age       | 50                                                         |
| eyeColor  | blue                                                       |
| fullName  | function() {return this.firstName\+ " " \+ this.lastName;} |

## In JavaScript, Objects are King.

If you Understand Objects, you Understand JavaScript.

Objects are containers for Properties and Methods.

Properties are named Values.

Methods are Functions stored as Properties.

Properties can be primitive values, functions, or even other objects.

In JavaScript, almost "everything" is an object.

* Objects are objects
* Maths are objects
* Functions are objects
* Dates are objects
* Arrays are objects
* Maps are objects
* Sets are objects

All JavaScript values, except primitives, are objects.

## Primitive Immutable

Primitive values are immutable (they are hardcoded and cannot be changed).

## JavaScript Objects are Mutable

Objects are mutable: They are addressed by reference, not by value.

If person is an object, the following statement will not create a copy of person:

const x \= person;

The object x is not a copy of person. The object x is person.

The object x and the object person share the same memory address.

Any changes to x will also change person.

# Object Display

Some solutions to display JavaScript objects are:

* Displaying the Object Properties by name
* Displaying the Object Properties in a Loop
* Displaying the Object using Object.values()
* Displaying the Object using JSON.stringify() ✅

# Object Constructors

## Object Constructor Functions

Sometimes we need to create many objects of the same type.

To create an object type we use an object constructor function.

It is considered good practice to name constructor functions with an upper-case first letter.

Example:
    function Person(first, last, age, eye) {
  this.firstName \= first;
  this.lastName \= last;
  this.age \= age;
  this.eyeColor \= eye;
}
    const myFather\= new Person("John", "Doe", 50, "blue");
const myMother \= new Person("Sally", "Rally", 48, "green");
const mySister \= new Person("Anna", "Rally", 18, "green");

const mySelf \= new Person("Johnny", "Rally", 22, "green");

## Adding a Property to an Object

Adding a property to a created object is easy:

### Example

myFather.nationality \= "English";

[Try it Yourself »](https://www.w3schools.com/js/tryit.asp?filename=tryjs_object_constructor2)

## Note:

The new property will be added to myFather. Not to any other Person Objects.

---

## Adding a Property to a Constructor

You can NOT add a new property to an object constructor:

### Example

Person.nationality \= "English";

To add a new property, you must add it to the constructor function prototype:

### Example

Person.prototype.nationality \= "English";

## Built-in JavaScript Constructors

JavaScript has built-in constructors for all native objects:

new Object()   // A new Object object

new Array()    // A new Array object

new Map()      // A new Map object

new Set()      // A new Set object

new Date()     // A new Date object

new RegExp()   // A new RegExp object

new Function() // A new Function object

## Did You Know?

Use object literals {} instead of new Object().

Use array literals \[\] instead of new Array().

Use pattern literals /()/ instead of new RegExp().

Use function expressions () {} instead of new Function().

# Events

HTML events are "things" that happen to HTML elements. An HTML event can be something the browser does, or something a user does.

\<*element* *event*\='*some JavaScript*'\>

Example:

\<button onclick\="document.getElementById('demo').innerHTML \= Date()"\>The time is?\</button\>

## Common HTML Events

Here is a list of some common HTML events:

| Event       | Description                                        |
| :---------- | :------------------------------------------------- |
| onchange    | An HTML element has been changed                   |
| onclick     | The user clicks an HTML element                    |
| onmouseover | The user moves the mouse over an HTML element      |
| onmouseout  | The user moves the mouse away from an HTML element |
| onkeydown   | The user pushes a keyboard key                     |
| onload      | The browser has finished loading the page          |

The list is much longer: [W3Schools JavaScript Reference HTML DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp).
