## Scope

Scope of a variable is the area where that variable is accesible.

JS variable scope can be 3 types now:

* Block scope (ES6)
* Function/Local Scope
* Global Scope

## Block scope

`{}` defines a block.

Variables declared inside a `{}` are not accesible from outside.

```javascript
{
    let x = 1;
}
console.log(x); //this will cause error
```

**Attention:** `var` variables cannot have block scope.

```javascript
{
  var x = 2;
}
console.log(x); // x CAN be used here
```

## Function/Local scope

Variables declared within a function are local to that function and cannot be accessed from outside.

```javascript
function myFunction() {
  var carName = "Volvo";   // Function Scope
  let x = 2;  // Function Scope
  const y = 3;  // Function Scope
}
```

**Note:** variables must be declared, assignment without declaration will make it automatically global.

## Global scope

Variables declared outside of any function are global variables and they have global scope.

```javascript
let carName = "Volvo"; // var/let/const use any
// code here can use carName

function myFunction() {
// code here can also use carName
}
```

## JavaScript Variables

In JavaScript, objects and functions are also variables.

Scope determines the accessibility of variables, objects, and functions from different parts of the code.

## Automatically Global

Undeclared variables automatically become **GLOBAL** variable.

```javascript
myFunction();

// code here can use carName

function myFunction() {
  carName = "Volvo";
}
```

**Note:** In "Strict Mode", undeclared variables are not automatically global.
