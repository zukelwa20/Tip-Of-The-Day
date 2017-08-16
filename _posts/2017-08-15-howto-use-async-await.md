---
layout: default
---

# How to use async/await

The async/await operators make asynchronous programming in JavaScript much easier. To use it you need NodeJS version 8.1.x or bigger. We recommend version 8.3.0.

Remember the `await` operator can only be used inside of an `async` function.

Code using Promises - for example:

```javascript

function filterForDay(day){
    return Days.find({name : day})
}

filterForDay("Tuesday")
    .then(function(results){
        console.log(results);
    })
    .catch(function(error){
        console.log(error);
    })
```

Can be converted to `async/await`:

```javascript

function async filterForDay(day){
    try{
        let theDay = await Days.find({name : day})
        return theDay;
    }
    catch(err){
        return null;
    }
}

filterForDay("Monday");
```

Note that async functions returns a `Promise`. You use `await` operator to wait for a Promise to complete.

Read more about async/await [here](https://certsimple.com/blog/javascript-equals-async-await), [here](http://rossboucher.com/await/#/) or [here](https://pouchdb.com/2015/03/05/taming-the-async-beast-with-es7.html).
