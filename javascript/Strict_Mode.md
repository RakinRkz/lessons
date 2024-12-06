# Use Strict

## The "use strict" Directive

The `"use strict"` directive was new in ECMAScript version 5.

It is not a statement, but a literal expression, ignored by earlier versions of JavaScript.

The purpose of `"use strict"` is to indicate that the code should be executed in "strict mode".

If declared at the beginning of a script, it has global scope (all code in the script will execute in strict mode)

```js
"use strict";
x = 3.14;       // This will cause an error because x is not declared
```

Declared inside a function, it has local scope (only the code inside the function is in strict mode):

```js
x = 3.14;       // This will not cause an error.
myFunction();

function myFunction() {
  "use strict";
  y = 3.14;   // This will cause an error
}
```


## Why Strict Mode?

Strict mode makes it easier to write "secure" JavaScript.

Strict mode changes previously accepted "bad syntax" into real errors.

As an example, in normal JavaScript, mistyping a variable name creates a new global variable. In strict mode, this will throw an error, making it impossible to accidentally create a global variable.

In normal JavaScript, a developer will not receive any error feedback assigning values to non-writable properties.

In strict mode, any assignment to a non-writable property, a getter-only property, a non-existing property, a non-existing variable, or a non-existing object, will throw an error.

- Objects are variables too. Using an object, without declaring it, is not allowed.
- Deleting a variable (or object) is not allowed.
- Deleting a function is not allowed.
- Duplicating a parameter name is not allowed

  ```
  "use strict";
  function x(p1, p1) {};	// This will cause an error
  ```
- Octal numeric literals are not allowed:

  ```
  "use strict";
  let x = 010;             // This will cause an error
  ```
- Octal escape characters are not allowed

  ```
  "use strict";
  let x = "\010";            // This will cause an error
  ```
- Writing to a read-only property is not allowed
- Writing to a get-only property is not allowed
- Deleting an undeletable property is not allowed
- The words `eval` , `arguments` cannot be used as a variable
- The `with` statement is not allowed
- For security reasons, `eval()` is not allowed to create variables in the scope from which it was called.
- The `this` keyword in functions behaves differently in strict mode.

  The `this` keyword refers to the object that called the function.

  If the object is not specified, functions in strict mode will return `undefined` and functions in normal mode will return the global object (window)

## Future Proof!

Keywords reserved for future JavaScript versions can NOT be used as variable names in strict mode.

These are:

* implements
* interface
* let
* package
* private
* protected
* public
* static
* yield
