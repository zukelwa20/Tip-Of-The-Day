---
layout: default
---

# String methods to the rescue

Built-in Javascript objects have lots of useful methods. The [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) object is no exception.

Let's look at how to split a string up into a list, how to replace parts of it and to remove spaces.

```javascript

var theString = "this is a a really interestingg string...          ";

//we can clean this string up using replace
var fixedString = theString
    .replace("a a", "a")
    .replace("gg", "g")
    .replace("...", "");

//string with errors removed
console.log(fixedString);
//"this is a really interesting string          "

//remove the spaces
var trimmedString = fixedString.trim();
// no spaces at the end of the string now
console.log(trimmedString);
//"this is a really interesting string"

// note that the original variable wasn't changed.
console.log(fixedString);

//to find all the words in the sentence - we can the string by spaces
var words = trimmedString.split(" ");
//["this", "is", "a", "really", "interesting", "string"]
console.log(words)
```
