Function chaining 
- It is a <mark>pattern</mark> in javascript where multiple functions are called on the. same object <mark>consecutively</mark>. Using the same object reference, <mark>multiple functions can be invoked</mark>. It increases the readability of the code and means less redundancy.

```javascript
person
	.sleep() // is sleeping
	.wakeUp() // wake up
	.eat() // is eating
	.study() // is studying
	```
Why use function chaining
- In programming it is a commonplace to have actions that need to run in <mark>a defined series of steps</mark>. Creating a single function that define all these actions is usually a terrible idea so we write <mark>a number of functions that deal with individual actions</mark>
- Function chaining can be created by defining several methods in an <mark>object that return this</mark> which is an instance of the object so we can call another function from the object.
Ways of Creating functions chaining 
1. object methods
2. class methods
3. functions prototype

Object Methods:
- We define methods in an object which returns <mark>this (an instance of the object)</mark> as following
```javascript
const person = {
	sleep : function() {
		console.log('is sleeping')
		return this
	},
	wakeUp : function() {
		console.log('woke up')
		return this
	},
	eat : function() {
		console.log('is eating')
		return this
	},
	study : function() {
		console.log('is studying')
		return this
	}
}
```
Class Methods:
- We define methods in a class which returns <mark>this (an instance of the class)</mark> as following
```javascript
class Person {
	sleep(){
		console.log('is sleeping');
		return this
	}
	wakeUp(){
		console.log('Woke Up');
		return this
	}
	eat(){
		console.log('is eating');
		return this
	}
	study(){
		console.log('is studying');
		return this
	}
}
```
Function Prototype:
- The prototype of a function is also called the <mark>signature of the function</mark>. The prototype data property of a function <mark>instance</mark> is used when the function is used as a constructor with the <mark>new operator</mark>. It will become the new object's prototype.
```javascript
function Person() {}

Person.prototype.sleep = function(){
	console.log('is sleeping');
	return this
}
Person.prototype.wakeUp = function(){
	console.log('Woke up');
	return this
}
Person.prototype.eat = function(){
	console.log('is eating');
	return this
}
Person.prototype.study = function(){
	console.log('is studying');
	return this
}

const person = new Person()

person
	.sleep() // is sleeping
	.wakeUp() // Woke Up
	.eat() // is eating
	.study() // is studying
```
JavaScript information
- It is a versatile programming language that powers the interactive features and dynamic behaviour of modern websites.
- It is a client-side scripting language, meaning it runs directly in the web browser and can interact with HTML and CSS.
- It supports object-oriented programming (OOP) concepts such as encapsulation, inheritance, and polymorphism.
- Functions in JavaScript are first-class citizens, which means they can be assigned to variables, passed as arguments, and returned as values.
- It has a concept called "hoisting", where variable and function declarations are moved to the top of their respective scopes during the compilation phase.
- The DOM(Document Object Model) is a powerful feature of JavaScript that allows dynamic manipulation of we page elements, enabling interactive experiences.
- Asynchronous programming in JavaScript is facilitated through features like callbacks, Promises, and the modern async/await syntax.
- JavaScript framework and libraries like React, Angular, and Vue.js have revolutionised web development, enabling the creation of complex and interactive user interfaces.
- Node.js allows JavaScript to run on the server-side, enabling server-based applications and APIs.