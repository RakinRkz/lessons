# JavaScript **Hoisting**

Hoisting is JavaScript's default behavior of moving declarations to the **top of the current scope** (to the top of the current script or the current function).

## JavaScript Declarations are Hoisted

In JavaScript, a variable can be declared after it has been used.

In other words; a variable can be used before it has been declared.


## The let and const Keywords

Variables defined with `let` and `const` are hoisted to the top of the block, but not  *initialized* .

Meaning: The block of code is aware of the variable, but it cannot be used until it has been declared.

Using a `let` variable before it is declared will result in a `ReferenceError`.

The variable is in a "temporal dead zone" from the start of the block until it is declared.

```js
//This will result in a ReferenceError:
carName = "Volvo";
let carName;
```

Using a `const` variable before it is declared, is a syntax error, so the code will simply not run.

```js
//This will cause syntax error
carName = "Volvo";
const carName;
```
