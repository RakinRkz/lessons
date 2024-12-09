# Asynchronous Concept

JavaScript program is *single-threaded*

>  A thread is a sequence of instructions that a program follows.



- Asynchronous programming is a technique that allows a program to start a long-running task and still be responsive to other events.
- JavaScript programs are single-threaded, meaning they can only do one thing at a time, causing long-running synchronous functions to make the program unresponsive.
- Asynchronous functions enable a program to handle long-running tasks without blocking other operations.
- Event handlers are a form of asynchronous programming where a function is called when a specific event occurs, such as user actions or changes in object states.
- `XMLHttpRequest` API is an example of asynchronous programming using event handlers to handle the progress and completion of a request.
- Callbacks, though an early method of implementing asynchronous functions, can lead to hard-to-understand code when nested, and modern APIs prefer using Promises instead.

## Callback

Callback is a function passed into another function. The callback function is expected to be called by the other function at expected time.


## Event Handlers

Event handlers are functions that are passed into another function and are called at a later time when a specific event occurs. They are a form of asynchronous programming, often used to handle user actions or changes in the state of objects. An example of event handlers in action is the XMLHttpRequest API, which uses event listeners to notify the caller about the progress and completion of a request.


### Callback Hell

```js
function doStep1(init, callback) {
  const result = init + 1;
  callback(result);
}

function doStep2(init, callback) {
  const result = init + 2;
  callback(result);
}

function doStep3(init, callback) {
  const result = init + 3;
  callback(result);
}

function doOperation() {
  doStep1(0, (result1) => {
    doStep2(result1, (result2) => {
      doStep3(result2, (result3) => {
        console.log(`result: ${result3}`);
      });
    });
  });
}

doOperation();
```
