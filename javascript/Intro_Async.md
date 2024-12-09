# Asynchronous Concept

JavaScript program is *single-threaded*

>  A thread is a sequence of instructions that a program follows.

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
