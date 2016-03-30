---
layout: default
---

# Group data using an object literal

Need to group data? You can use an object literal as a map/dictionary to group data into key value pairs.

To find how many times colors occurs in a list, you can use this technique.

```javascript
var colors = ["blue", "red", "green", "blue", "red", "blue", "green", "orange"]

// create an empty object
var colorCounts = {};

//loop through all the colors
colors.forEach(function(color){

    //initialize the value in the map/object
    if(colorCounts[color] === undefined){
        colorCounts[color] = 0;
    }

    // increment the counter for each color in the Map
    colorCounts[color] = colorCounts[color] + 1;
});

console.log((colorCounts));
// {"blue" : 3, "red" : 2, "green" : 2, "orange" : 1 }

//access colors count
console.log(colorCounts["green"]);

//2

```
