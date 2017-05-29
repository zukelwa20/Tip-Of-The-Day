---
layout: default
---

# Factory functions

Factory functions are functions that create and returns a new Object.

Here is a Factory function that creates an Object using the Object Literal notation:

```javascript

var FruitDeal = function(fruitName, fruitPrice){
    return {
        fruit : fruitName,
        price : fruitPrice
    }
};

//Instantiate (create an instance ) it like this
var appleDeal = FruitDeal('apples', 2.50);

//this prints `2.50`
console.log(appleDeal.price);

```

You can create a more useful factory function that creates a deal message like this:

```javascript

var FruitDeal = function(fruitName, fruitPrice){

    var createMessage = function(){
        return "You bought " + fruitName + " for R" + fruitPrice.toFixed;
    }

    return {
        message : createMessage
    }
}

//Instantiate (create an instance ) it like this

var appleDeal = FruitDeal('apples', 2.50);

// This prints 'You bought apples for R2.50'
console.log(appleDeal.message());
```

> **Note** that Object literals can have functions that have access to variables in their scope. Functions that can access variables from their surrounding scope is called a `Closure`. You can learn more about Objects and Object literals in JavaScript [here](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics).

As JavaScript have function scope one can use factory functions to create private variables, that can only be accessed from the object functions returned from the factory. One can use this concept to hide state, create complex variables with internal state and functions that can access the state - these are Objects, they have state and behaviour.  

## Using Factories

Using factories you can create code that is easily testable as it don't depend on global variables.

Let's create a testable fruit shopping basket, that allows you to buy fruit and keeps count how many different types of fruit you have in your basket.

You can test the basket like this:

```javascript

var shoppingBasket = ShoppingBasket();

shoppingBasket.buy('apple');
shoppingBasket.buy('pear');
shoppingBasket.buy('apple');
shoppingBasket.buy('bananas');

var howManyApples = shoppingBasket.check('apple');

assert.equal('You got 2 apple(s) in your basket', howManyApples);

assert.equal('You got 1 pear(s) in your basket', shoppingBasket.check('pear'));

```

The code for the ShoppingBasket factory function looks like this:

```javascript

var ShoppingBasket = function(){

    // this is scoped inside the ShoppingBasket function
    var fruitsBought = {};

    var buyFruit = function(fruitName){
        if (fruitsBought[fruitName] === undefined){
            fruitsBought[fruitName] = 0;
        }
        fruitsBought[fruitName] += 1;
    };

    var checkFruit = function(fruitName){
        return "You have " + fruitsBought[fruitName] + " " + fruitName + "(s) in your basket.";
    }

    return {
        buy : buyFruit,
        check : checkFruit
    }
}

```

Watch these two videos to learn more about [Closures](https://youtu.be/CQqwU2Ixu-U) and [Factory Functions](https://youtu.be/ImwrezYhw4w).
