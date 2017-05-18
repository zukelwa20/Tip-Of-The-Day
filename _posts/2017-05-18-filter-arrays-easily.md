---
layout: default
---

# Easily filter arrays

How can you filter a JavaScript List easily? You can use the `filter` method.

You can filter over this dataset:

```javascript
const fruits = [
    {name : "oranges", day : Monday, qty : 8},
    {name : "apples", day : Tuesday, qty : 5},
    {name : "pears", day : Wednesday, qty : 1},
    {name : "oranges", day : Thursday, qty : 3},
    {name : "apples", day : Friday, qty : 4},
    {name : "oranges", day : Friday, qty : 13}
]
```

For `apples` like this:

```javascript
const apples =  fruits.forEach(function(fruit){
    // the condition you are filtering on
    return fruit.name === 'apples';
});

//contains two entries
console.log(apples);
```

The `filter` method is an easy way to find values in a list. All the values that match the condition in function parameter will be returned in a new list.

The function parameter will be called with each entry in the list as a parameter. Entries in the list for which the function returns true will be included in the resulting List. The original list is not changed.

Read more about [filter](http://devdocs.io/javascript/global_objects/array/filter).
