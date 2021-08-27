# JavaScript Questions.

## 1. What are the different data types in JavaScript?

Primitive Values:
- String
- Number
- BigInt
- Boolean
- Symbol
- Undefined
- Null

Non-Primitive (Reference) Values:
- Object
- Array

**Notes**  
It would be good for them to understand the difference between primitive and non-primitive values, and you only want them to list a few of the primitive values.

---

## 2. Explain Hoisting in javascript.

This means that irrespective of where the variables and functions are declared, they are moved on top of the scope. The scope can be both local and global. So at compile time of JavaScript, all variables and functions in the scope are hoisted to the top so they can be referenced from anywhere in that scope.

**Notes**  
This is not the biggest thing they need to know, but a good to have.

---

## 3. What is the difference between “ == “ and “ === “ operators?

Both are comparison operators. The difference between both the operators is that,“==” is used to compare values whereas, “ === “ is used to compare both value and types.

**Notes**  
This is a must, they SHOULD know this, and it is also good if they express an opinion to always use 3 equals over 2.

---

## 4. Explain pass by value and pass by reference.

In JavaScript, primitive data types are passed by value and non-primitive data types are passed by reference.

**Notes**  
This is a big point to understand as it also affects frameworks like Vue, and React, where when you pass an object to a function, it is passed by reference and therefore changing the object in the function, will change the referencing variable as well - example passing an array of strings, and removing the first two, this will then affect the referencing variable outside of the function.

---

## 5. Explain higher order functions.

Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.

Higher order functions are a result of functions being first-class citizens in javascript.

Examples of higher order functions:

```javascript
// Example 1
function higherOrder(fn) {
	fn();
}

higherOrder(function() {
	console.log("Hello world");
});

// Example 2
function higherOrder2() {
	return function() {
		return "Do something";
	}
}

const x = higherOrder2();
```

**Notes**  
This is more for checking the depth of the candidate's knowledge of this topic, and it is not a must.

---

## 6. Explain the “this” keyword.

The “this” keyword refers to the object that the function is a property of. The value of “this” keyword will always depend on the object that is invoking the function.

Examples using classes:

```javascript
class Animal {
	constructor() {
		this.sound = 'No Sound';
	}

	makeSound() {
		console.log(this.sound);
	}
}

new Animal().makeSound();
// Output: 'No Sound'

class Cat extends Animal {
	constructor() {
		super();
		this.sound = 'Meow';
	}
}

new Cat().makeSound();
// Output: 'Meow'
```

**Notes**  
You want to hear that they understand that this references the scope the function was called from.

---

## 7. Explain the difference between a normal function and an arrow function.

* Arrow functions can only be used as a function expression.
* Arrows functions are anonymous functions.
* Arrow functions are lexically scoped.
* Arrow functions are not bound to a particular object.

**Notes**  
Here we want the candidate to understand that they are not bound to a particular object, and that they are lexically scoped, therefore calling `this` will go to the nearest parent function scope.