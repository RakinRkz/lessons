# Execution Context

It's basically the different levels or slices of logic(and related components) that enter and exit accordingly in the call stack.

## Global Execution Context

In the beginning, JS starts with this.

It is starts the loading/creation phase.

It contains:

* window: global object
* this: window
* variable object
* scope chain

Example code:

```js
var topic = "Js execution context"

function getTopic(){
	return topic;
}

getTopic();
```

Global execution context, at the loading/creation phase will have:

- window: global object
- this: window
- topic: undefined
- getTopic: fn()
- scope chain

At execution phase:

- topic: "Js execution context"

When function is called/invoked from global context, function context enters the call stack. It creates:

- parameters/arguments object
- this object
- memory space for function and variables
- variables set as undefined

At execution phase: returns the value and exits from call stack.

After that global context has nothing more to do. It also exits from the call stack.
