---
layout: default
---

# Use String & List methods together

Ever needed to analyze a string? To make things easier create a list of objects with all the information needed.

To do that use String and Array/List object's methods together.

```javascript
var theString = "this is a really interesting string";

//to find all the words in the sentence - we can the string by spaces
var words = theString.split(" ");
//["this", "is", "a", "really", "interesting", "string"]
console.log(words)

var wordStats = words.map(function(word){
    //more attributes can be added below
    return {
        word : word,
        length : word.length
    }
});

// list of objects {name : "", length : ""}
console.log(wordStats);
//this list is very useful to find the longest word & word length,
// shortest word, average word length etc

```
