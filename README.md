# Notes

## Embed a script:
`<script src="script.js"></script>` at bottom

## Basic prompts/msgs
Give a message:
`alert("Enter xyz");`

Prompt for input:
`var a = prompt("Enter xyz");`

Confirm (yes or cancel) prompt:  
`var a = confirm("xyz?");`  
`a` stores bool value.

## Basic codes
`typeof a`  
Gives type of a variable `a`.  

Types:  
string, number (both int and float), boolean, undefined, object (`null` is also an object)

**Why typeof null is an object?**
`null` is in js ever since its *initial phase* and back then it was written as an `object` type. Many devs consider this a mistake but it *cannot be changed* because now a *lot of code* in the world uses `null` and considers it an `object`.

## Change document features:
```js
document.body.style.backgroundColor="red";
document.title="new title";
```

## Variables:
- letters, digits, underscores and $ are allowed
- must begin with `_` or `letter` or `$`

### Var vs Let:
- var is globally scoped while let and const are block scoped
- var can be updated and redeclared within its scope
- let can't be redeclared
