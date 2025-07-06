# Notes

## Embed a script:
```html
<script src="script.js"></script>
```
at bottom of `<body>`

## Basic codes

Get type of a variable `a`.  
```js
typeof a
```  

### Basic prompts/msgs
Give a message:  
```js
alert("Enter xyz");
```

Prompt for input:  
```js
var a = prompt("Enter xyz");
```

Confirm (yes or cancel) prompt:  
```js
var a = confirm("xyz?");
```  
`a` stores bool value.

**Types:**  
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
- `var` is globally scoped while `let` and `const` are block scoped
- `var` can be updated and redeclared within its scope
- `let` can't be redeclared

### Number can be added to string
```js
let a = "hehe";
let new_string = a + 9;
console.log(a);  // Gives hehe
console.log(new_string);  // Gives hehe9
console.log(typeof a);  // Gives string
console.log(typeof new_string);  // Gives string
```

## Objects
Collection of `key:value` pairs.  
Declared using var/let/const.  
**Syntax:**
```js
let object_name = {
    key1: "val1",
    key2: "val2"
};
```

- Key may or may not be written in double quotes, space containing key names must be in double quotes.  
  `name: "Rizen"` ✅  
  `"name": "Rizen"` ✅  
  `"job salary": 2000000` ✅  
  `job salary: 2000000` ❌  
- New keys can be added through:  
  ```js
  object_name.new_key = "value";
  ```

- Content of an object declared using `const` can be edited but the object itself cannot be changed.
  ```js
  const o = {
    name: "Rizen",
    "job salary": "2 Million"
  };
  o.age = 19;  // ✅
  o.name = "Someone else"  // ✅
  o = {"m":"n"}  // ❌
  o = "anything"  // ❌
  ```

## Condition check

|Operator|Use|
|---|---|
|==|Check value|
|===|Check value and type|
|?|[Ternary Operator](#--Ternary-Operator)|
|&&|Logical AND (just like `and` in python)|
|\|\||Logical OR (just like `or` in python)|
|!|Logical NOT (just like `not` in python)|

### Ternary Operator (?)
Uses if-else logic to give certain output based on certain condition.  
Syntax: `condition ? output_if_true : output_if_false;`  
**Example:**  
```js
let a=1;
let b=2;
let c = (a > b) ? "a is greater" : "b is greater";
console.log(c);  // Gives b is greater
```