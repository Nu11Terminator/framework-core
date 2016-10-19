---
title: Strings - format
---

# format
Use this method to process and transform a string according to a replacement pattern.
 

## Syntax
`format(pattern, data)`


## Parameters

**pattern**  
A string containing replacement tokens.

**data**  
An object or array containing replacement values.


## Return value
The transformed string


## Errors thrown
None


## Example

```javascript
//using an object
var person = {
    first: "John", last: "Smith", age: 30
};
var str = Core.Strings.format("{first} is {age} years old", person);
console.log(str); // John is 30 years old
 
// using an array
var str = Core.Strings.format("His {0}'s name is {1}", ['mother', 'Jane']);
console.log(str); // His mother's name is Jane
```

