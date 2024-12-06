# This

## What is `this`?

AKA: the execution context

`this` keyword refers to an object.

The this keyword refers to different objects depending on how it is used:


| In an object method, this refers to the object.                          |
| :------------------------------------------------------------------------- |
| Alone, this refers to the global object.                                 |
| In a function, this refers to the global object.                         |
| In a function, in strict mode, this is undefined.                        |
| In an event, this refers to the element that received the event.         |
| Methods like call(), apply(), and bind() can refer `this` to any object. |

## Note

In a word, **`this`** depends on which it has the `binding`.

Important concept: binding, strict mode
