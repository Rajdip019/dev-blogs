## .this Explained in the most Simple Way!! (JavaScript) ✨

.this Alone refers to the global object.

## Now What is global Object?

In JavaScript everything is considered as object, so the whole window displayed by the browser is also a JavaScript object .

### Code Example:

```jsx
console.log(this);
```

This statement in a .js/.jsx file only refers to the Window object. 

In case it is just a normal function .this refers the same means Global Object.

```jsx
//This is the example of a regular function.

function sum(){
	var add = 2+2;
	console.log("Sum of two number is: " +  add);
	console.log(this);
}

sum();

//Here ".this" doesnot refer to the sum() function this still refers to the global function.
```

### In a method:

In a method ,this refers to the owner object. 

### What is a Method?

When you make a function in a java Script Object then it is called as method. Method of that parent object.

Example of a method:

```jsx
const note={
    name: "Rajdeep Sengupta",
    class: "1st Year B.tech",

    sum: function(){
        var add= 2+2;
        console.log("Sum of this tow number is:  "+ add);
        console.log(this);
				console.log(this.name);
    }
}

note.sum()
```

 

### Output:

```jsx
//Result in the console pannel.

Sum of thois tow number is:  4

//here .this console logs the whole parent object.Which is 'note

Object
class: "1st Year B.tech"
name: "Rajdeep Sengupta"
sum: ƒ ()
[[Prototype]]: Object

//here it console logs the Name as expected. By (
.this.name)
Rajdeep Sengupta
```

## Strict Mode:

Example of Strict Mode:

```jsx
"use strict"

function sum(){
	var add = 2+2;
	console.log("Sum of two number is: " +  add);
	console.log(.this);
}
```

But here even though it is a regular Function it will not give a the Global Object. This will be simply Undefined.

## For More info Visit this Link.

[this - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)