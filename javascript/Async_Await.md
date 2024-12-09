# Async Await


## Promises vs Async/Await in JavaScript

Before async/await, to make a promise we wrote this:

```javascript
function order(){
   return new Promise( (resolve, reject) =>{

    // Write code here
   } )
}
```

Now using async/await, we write one like this:

```javascript
//👇 the magical keyword
 async function order() {
    // Write code here
 }
```


## Try and Catch keywords

We use the `try` keyword to run our code while we use `catch` to catch our errors. It's the same concept we saw when we looked at promises.

```js
let stocks = {
    Fruits : ["strawberry", "grapes", "banana", "apple"],
    liquid : ["water", "ice"],
    holder : ["cone", "cup", "stick"],
    toppings : ["chocolate", "peanuts"],
 };
 
let is_shop_open = true;

function time(ms) {

   return new Promise( (resolve, reject) => {

      if(is_shop_open){
         setTimeout(resolve,ms);
      }

      else{
         reject(console.log("Shop is closed"));
      }
    });
}

async function kitchen(){
    try{
    await time(2000)
    console.log(`${stocks.Fruits[0]} was selected`)

    await time(0000)
    console.log("production has started")

    await time(2000)
    console.log("fruit has been chopped")

    await time(1000)
    console.log(`${stocks.liquid[0]} and ${stocks.liquid[1]} added`)

    await time(1000)
    console.log("start the machine")

    await time(2000)
    console.log(`ice cream placed on ${stocks.holder[1]}`)

    await time(3000)
    console.log(`${stocks.toppings[0]} as toppings`)

    await time(2000)
    console.log("Serve Ice Cream")
    }

    catch(error){
     console.log("customer left")
    }
}   

kitchen();
```


can we use Async/ Await here instead of Promise?


No, you **cannot entirely replace Promises** when using `async/await`, because `async/await` is syntactic sugar built on top of Promises. To use `async/await`, the function being `await`-ed must return a Promise. Here's why:

### Key Concepts:

1. **Async functions** :

* Automatically return a Promise.
* Allow you to use `await` to pause execution until a Promise resolves or rejects.

2. **`await`** :

* Can only be used to wait for Promises.

**Why Can't We Remove Promises?**

* `setTimeout` doesn't natively support `async/await`. It uses a callback instead. To make `setTimeout` work with `await`, it must be wrapped in a Promise.
* If you attempt to use `await` without a Promise, it won't work because `await` requires something that conforms to the Promise interface.

### Summary:

Even with `async/await`, Promises are still necessary to handle asynchronous operations like `setTimeout`. You cannot replace Promises, but you can simplify their usage with `async/await` for cleaner, more readable code.
