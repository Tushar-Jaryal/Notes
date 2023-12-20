## History of JavaScript
- In 1995, A netscape (browser) programmer named <u>Brandon Eich</u> developed a <u>scripting language</u> in just 10 days.
- Original Name: 
	- First Name: Mocha
	- Second Name: LiveScript
	- At that time java was a famous programming language. So, for marketing purpose LiveScript changed into JavaScript.

<mark><b>JAVA AND JAVASCRIPT BOTH ARE DIFFERENT PROGRAMMING LANGUAGE. NOTHING IS COMMON.</b></mark>

- In 1997, there was another famous browser which was <u>Internet Explorer</u>(Microsoft Browser). Then, Microsoft copied JavaScript features and made its own language named as JScript.
- In browser war (Netscape vs Internet Explorer), EcmaScript was born.
- <u>Ecma(European Computer Manufacturing Association) International</u> is an industry association founded in 1996, dedicated to the standardisation of information and communication systems.

<mark>JavaScript+Ecma(rules) -> EcmaScript</mark>

Problem Solved -> We can implement same scripting language for different browser.
First EcmaScript:
- ES1 -> 1997
- ES5 -> 2009 (lots of new features)
- ES6 -> 2015 (Biggest update for JS)
ES6 is also known as Modern JavaScript
Ecma have a technical community known as TC39 which has decided that after 2015 they will release JavaScript with new features every year (annual release).
After 2016, The new versions are named after the year
- ES2016,ES2017,ES2018,ES2019,ES2020,ES2021,ES2022,ES2023

## JavaScript Features
- Case Sensitive
- DynamicallyTyped
- Cross-Platform
- Interpreted
- Object-Oriented Scripting Language
- Backward Compatible

## JavaScript Variables
- <u>Variables</u> stores the data which can be changed or used when we need.
<mark>Keywords are the predefined words in programming languages</mark>
```JavaScript
var name = 10;
let name = 10;
const pi = 3.14;
```

## Datatype in JavaScript
There are two types of datatype
- Primitive
- Non-Primitive

### Primitive datatypes are
- Number
- Null
- String
- Bool
- Undefined
- Bigint
- Symbol

### Non-Primitive datatypes are
- Array
- Object
- RegExp

## JavaScript Hacks
- Convert string to number
- Put the + before the string
```JavaScript
let str='9';
console.log(typeof(+str));
```
- Convert number into string
- Add a empty string with the number
```JavaScript
let num = 10;
console.log(typeof(num+""));
```

## JavaScript String
- <u>Strings</u> are used to store textual form of data like word, sentence. It follows zero based indexing.
```JavaScript
let str = "pro";
let str = 'pro';
let str = `pro`;
```
### JavaScript String Method
```JavaScript
trim()           slice()
charat()         tostring()
concat()         substring()
indexof()        toUpperCase()
lastIndexof()    toLowerCase()
```

## Undefined in JavaScript
- Accessing an uninitialised variable returns undefined.
```JavaScript
let str;
console.log(str); //undefined
```
- Accessing a non-existing property of an object returns undefined.
- Accessing an out-of-bounds array element returns undefined.

## Null in JavaScript
- Null means <mark>no value</mark> assign to variable.
- typeof null returns <mark>object</mark>
- Null is treated as false value.

## JavaScript BigInt
- <u>BigInt</u> is a primitive datatype which is used for large numeric values. It doesn't represent decimal values.
- It is used to represent values greater than 2^53-1

## Declaration of BigInt
- By appending n at the end of numeric values.
```JavaScript
var num = 9876543219865252772n;
```
- By passing the values as an argument to the BigInt()
```JavaScript
var num = BigInt(9876543219865252772);
```

## Ternary Operator
- It is also called <u>conditional</u> operator.
- It takes three operands.
- It makes the code more concise.
```JavaScript
let variableName=Condition?True:False;
```
If the condition is true expression after <mark>?</mark> will execute. If it is false, expression after <mark>:</mark> will execute.
```JavaScript
let age = 18;
let warning;
age >= 18 ? (warning='You can play') : (warning='You cannot play');
console.log(warning);
```

## Boolean Datatype
<u>Boolean</u> can hold only two values, true and false.
```JavaScript
var read = true;
var Eat = False;
console.log(typeof(read))
```
Boolean values also come as a result of comparison.
```JavaScript
var a=1,b=4,c=8;
console.log(b>a); //output: true
console.log(b>c); //output: false
```

## <q>==</q>and<q>===</q>
### Double equals operator:
- It is known as <mark>Equality or abstract</mark> comparison operator.
- It compares variables, ignores datatype.
### Triple equals operator:
- It is known as the <mark>Identity or Strict</mark> comparison operator.
- It compares variables as well as datatype.

## Truthy and Falsy Values
- <u>Truthy values</u> is a value that is considered true when encountered in a boolean context
```JavaScript
true,{},[],42,"0","false",new Date(),-42,12n,3.14,-3.14,Infinity,-Infinity
```
- <u>Falsy Values</u> is a value that is considered false when encountered in a boolean context.
```JavaScript
undefined,null,NaN,false,"",0,-0,0n
```
```JavaScript
var values = 42;
if(values){
	console.log(true);
}
else{
	console.log(false);
}
```

## Control Flow
- <u>Control Flow</u> allows our program to make decisions about what code is executed and when
![[Pasted image 20231116145056.png]]
Control flow have two types of statements
- Conditional Statements
- Looping Statements

### Conditional Statements
<u>Conditional Statements</u> are basically checks to see if a certain condition is either true or false. if the condition is true then run code "yes", if it is false then run code "no".

Types of Conditional Statements:
- If statements -> IfElse, IfElseIf
- Switch
- Ternary

### Looping Statements
<u>Looping Statements</u> perform repetitive task with less code

Types of loops:
- For loop
- Do/While
- For...in
- For...of

### Switch statement
- It evaluates an expression compare its result with case values and execute the statement associated with the matching case.
```JavaScript
switch(expression){
	case value1:
		//body of case1
		break;
	case value2:
		//body of case2
		break;
	default
		//body of default
}
```
- <u>Break</u> is optional. It is used to end the switch statement.
- <u>Default</u> is when there is no matching case, the default body executes. It is optional.

### For loop
- It executes a block of code as long as a specified condition is true.
```JavaScript
for(initialiser;condition;iterator){
	//statements
}
```
- <u>Initializer</u> is an expression that initialise the loop, it executed once.
- <u>Condition</u> is a boolean expression that determines whether the for loop should execute or stop.
- <u>Iterator</u> is executed after each statement.
```JavaScript
for(let i=2;i<4;i++){
	console.log(i);
}
```

### While, DoWhile loops
- <u>While loop</u> executes statements as long as the conditions are true. If the condition become false, the loop is terminated.
```JavaScript
while(condition){
	//statements
}
```
- <u>Do While loop</u>, the block of code is executed once even before checking the condition.
```JavaScript
do{
	//statements
}
while(condition)
```

## JavaScript Functions
- A <u>function</u> is a block of code that performs a specific task/
```JavaScript
function funName(){
	//statements
}
```
<mark>function is declared using <u>function</u> keyword</mark>
- Call Function
```JavaScript
function myName(){
	console.log('Tushar Jaryal')
}
myName(); //call Function
```

### Advantage of function
- Reusability
- Less code
- Easy to understand

### Function Parameters
- When we declare function we specify the parameters.
```JavaScript
function example(Parameter){
	console.log(Parameter);
}
```
### Function Argument
- When we call function we specify argument.
```JavaScript
let argument = 'arg';
example(argument);
```

## Intro to Arrays
<u>Arrays</u> are ordered collection of homogenous items.
```JavaScript
//          Element/Item
let pets = ["cat","dog","cow"];
// Index ->   0     1     2 
```

### JavaScript Array Characteristics
- It can hold values of mixed types.
- Size of array is dynamic.
```JavaScript
let mixed = [1,2.5,"cat"]; //mixed type
mixed.push("Monkey"); //Dynamic Size
console.log(mixed);
```

### Accessing Array Elements
Arrays are zero-based indexed which means the first element of array starts at index zero.
```JavaScript
let pets = ['cat','dog'];
console.log(pets[0]); //Accessing Element
```

### Array Methods
##### Array length
- It returns the number of elements in an array.
```JavaScript
let num = [1,2,3,4];
console.log(num.length); //4
```
##### Array Push()
- It adds elements to the end of the array.
```JavaScript
let num = [1,2,3];
console.log(num.push(4)); //[1,2,3,4]
```
##### Array Pop()
- It removes the last element from an array and returns removed element.
```JavaScript
let num = [1,2,3,4]
let removednum = num.pop();
console.log(num); //[1,2,3]
console.log(removednum); //4
```
##### Array Shift
- It removes the first element and returns removed element
```JavaScript
let num = [1,2,3,4];
let removednum = num.shift();
console.log(num); //[2,3,4]
console.log(removednum); //1
```
##### Array Unshift()
- It adds elements to the beginning of an array.
```JavaScript
let num = [1,2,3,4]
console.log(num.unshift(0)); //[0,1,2,3,4]
```
##### Array Sort()
- It sorts the items of an array.
```JavaScript
let num = [0,2,4,1];
console.log(num.sort()); //[0,1,2,4]
```
##### Array Reverse()
- It returns the reverse items of an array.
```JavaScript
let num = [1,2,3,4];
console.log(num.reverse()); //[4,3,2,1]
```

| Primitive Types                                         | Reference Types                              |
|:------------------------------------------------------- |:-------------------------------------------- |
| It has a fixed size in memory                           | Do not have a fixed size in memory           |
| Data stored on the stack                                | Object stored in the heap                    |
| Stored directly in the location                         | Stored in variable location                  |
| Example - null, string, number, bool, undefined, symbol | Example - Arrays, objects, functions, dates  |
| We cannot add, delete, update in primitive data.        | We can add, delete, update in reference data |

### Spread Operator
- It is used to expand or spread an iterable or an array. It is denoted by three dots.
```JavaScript
let arrStr = ['a','b','c'];
console.log(arrStr); //['a','b','c']
console.log(...arrStr); //abc
```
##### Clone array using spread operator
```JavaScript
let arr1 = [1,2,3]
let arr2 = [...arr1];
conosle.log(arr1); //[1,2,3]
console.log(arr2); //[1,2,3]
//append an item to the array
arr1.push(4)
console.log(arr1); //[1,2,3,4]
console.log(arr2); //[1,2,3]
```
### Array Destructuring
- It is used to assign array values to distinct variables.
```JavaScript
const items = ['Books','Pen','Pencil'];
const [x,y,z] = items; //destructuring
console.log(x); //Books
console.log(y); //Pen
console.log(z); //Pencil
```
##### Destructuring by using spread operator
```JavaScript
const [x, ...y] = items;
console.log(x); //Books
console.log(y); //['Pen','Pencil']
const [...y,x]; //error
```

## Objects Introduction
##### Objects
- They are reference type
- Objects are good to handle real world data
- Objects stores data in key value pairs.
- Objects don't have index.
##### Object Declaration
```JavaScript
const person = {
	name : 'Coder', //key : value
	age : 20 //key : value
};
```
##### Access data from objects
```JavaScript
//Dot Notation
console.log(person.name); //Coder
console.log(person.age); //20
```
##### Add Key-Value pair to objects
```JavaScript
person.id = 5;
console.log(person); //{name:'Coder',age:20,id:5}
```
```JavaScript
const person = {
	name : 'Coder';
	"Person Age" : 20; //Key stored as a string
};
//Bracket Notation
console.log(person['name']); //Coder
```
##### Bracket Notation vs Dot Notation
```JavaScript
//Dot Notation
console.log(person.Person Age);
//error because it does not include spaces between names

//Bracket Notation
console.log(person['Person Age']);
//It works because it becomes string now
```
### Iterate Object
##### Using for....in loop
```JavaScript
let person = {
	firstName : "Tushar",
	lastName : "Jaryal",
	age : 22
};
for(let key in person){
	console.log(key); // It access only key
	// firstName
	// lastName
	// age
	console.log(person[key]); // It access only values
	// Tushar
	// Jaryal
	// 22
	console.log(key,":",person[key]); //It access both key-value
	// firstName:Tushar
	// lastName:Jaryal
	// age:22
}
```
##### Object.keys()
This method was introduced in ES6. It takes an object and returns an array of the object properties (keys).
```JavaScript
console.log(object.keys(person));
// ["firstName","lastName","age"]
```
##### Object.values()
This method takes an object and returns an array of the object values.
``` JavaScript
console.log(object.values(person));
// ["Tushar","Jaryal","22"]
```
##### Object.entries()
This method takes an object and returns the key-value pair.
```JavaScript
console.log(object.entries(person));
// [['firstName':'Tushar'],['lastName':'Jaryal'],['Age':22]]
```
### Object Destructuring
This assigns properties of an object to individual variables.
```JavaScript
let person = {
	name : "Tushar",
	age : "Twenty Two"
};
let name = person.name;
let age = person.age;
let {name,age} = person;
console.log(name); //Tushar
console.log(age); //Twenty Two
```
##### Setting default values
```JavaScript
let {name,age,clas=''} = person;
console.log(clas); // ''
```

## Arrow Functions
- It is another way to write a function.
- It is introduced in ES6 version
- It's syntax is shorter than regular function.
```JavaScript
let add = function(a,b){
	return a+b;
};
// Using arrow function
let add = (x,y) =>{
	return x+y;
};
// With single parameter
(p1) = {
	// statement
};
p1 = {
	// statement
};
// With no parameter
let a = () =>{
	return 0;
};
```

## Hoisting
- It is a behaviour in which a function or a variable can be used before declaration.
```JavaScript
console.log(name); //undefined
var name = "xyz";
// It doesn't cause an error because it looks like this in execution phase
var name;
console.log(name);
var name = "xyz";
// In case of let
console.log(name); // reference error
let name = "xyz";
// It causes an error because in let variable is hoisted but not initialized.
// In case of const
console.log(name); // Error
const name = "xyz";
// let and const variables are hoisted but the cannot be accessed before their declaration.
```
### Function Hoisting
- Function can be called before declaring it.
```JavaScript
name(); // function called
function name(){ //Declaration
	console.log("Tushar Jaryal"); // Tushar Jaryal
}
// Function Expression
//TypeError occurs in case of function expression
name();
var name = function(){
	console.log('Tushar Jaryal');
}
//Arrow Function
name(); //Type Error
var name = () =>{
	console.log('Tushar Jaryal')
}
// JavaScript doesn't hoist the. function expression and arrow functions.
```

## Lexical Scope
- It means that a variable defined outside a function can be accessible inside another function defined after the variable declaration, but the opposite is not true.
```JavaScript
function add(){
	var x = 4; // y is not accessible
	function mul(){
		// x is accessible, y is not
		function minus(){
			var y = 6; // x is accessible
		}
	}
}
```

##### Block Scope vs Function Scope
| Block Scope                                                                                                                  | Function Scope                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------- |:--------------------------------------------------------------------------------------------------------------- |
| It means that the variable is accessible within the block{}                                                                  | It means that the variables are only accessible in the function in which they are declared.                     |
| Let and  Const are block scope.                                                                                              | var is a function scope.                                                                                        |
| ```Example : for(let i = 0;i < 10; i++){//Block} console.log(i); //Error we are trying to access let variable outside the scope ```| ```Example : function fun(){var x=42;}fun();console.log(x);//Error we cannot access var outside the function scope ```|

### Default Parameters
- It allows us to give default values to the function parameters if no value is given
```JavaScript
function add(x=1,y=2){
	return x+y;
}
console.log(add(3,4)); //7
console.log(add(5)); //x=5,y=2 //7
console.log(add()); //7
// A parameter default value is undefined
function add(x){
	console.log(x);
}
add(); //undefined
```

### Rest Parameters
- It is used to gather parameters and put them all in an array.
```JavaScript
function test(a,b){
	console.log(a); //8
	console.log(b); //9
}
test(8,9);
test(8,9,7,6,5);
// Nothing will happen to 7,6,5
// To cover 7,6,5 rest parameters concept comes
function test(a,...b){
	console.log(a);
	console.log(b);
}
test(8,9,7,6,5);
//8,[9,7,6,5]
```

### Parameter Destructuring
- A couple of specific property values to pass as a parameter to the function definition, not in entire object.
```JavaScript
const user = {
	'name' : 'Tushar',
	'age' : '21'
}
function userdetails({name,age}){
	console.log(name);
	console.log(age);
}
userdetails(user);
// Tushar
// 21
```

### Callback Function
- It is defined as, we can also pass a function as an argument to a function.
```JavaScript
function second(name){
	console.log(name);
}
function first(callback){
	callback('Tushar');
}
first(second); //Tushar
```

- The callback function is helpful when you have to wait for a result that takes time.

## Sets in JavaScript
##### Sets
- Stores a collection of unique values
- No index-based access
- Order is not guaranteed
- Sets are iterable
- Sets have its own methods
```JavaScript
let items = new Set();
console.log(typeof(items)); // object
// Instance of sets is true
```

##### Arrays vs Sets
- Array can have duplicate values whereas sets cannot.
- In Array data is ordered by index whereas sets cannot

##### Useful Set Methods
```JavaScript
const items = new Set();
```
##### add()
- Append a new element to the end of the set.
```JavaScript
items.add("Hi"); // Set(1) {"Hi"}
```
##### clear()
- Remove all the elements and returns undefined
```JavaScript
const items = new Set([1,2,3]);
```
##### delete()
- It deletes a specific element from set.
```JavaScript
const items = new Set([1,2,3,4]);
items.delete(3);
```
##### has()
- Check whether an element exists in sets or not
```JavaScript
items.has(2) // true
```

## Map Data Structure
- A map is a collection of key-value pairs, similar to an object.
```JavaScript
const person = new Map();
```
##### Why we need map, if we have object?
- A map is similar to object, keys in objects are only strings and symbols. But we can use any value as key in map.
```JavaScript
const person = new Map();
person.set('Name','Tushar');
console.log(person);
//{'Name'=>'Tushar'}
```
### Methods in Maps
##### get()
- It returns the value associated with the key.
##### set()
- It sets the value of the key and returns the map.
##### delete()
- Delete the entry which has the key same as passed key.
##### clear()
- Delete all key-value pairs from the map.
##### has()
- Returns true if the map has the key provided.
##### keys()
- Returns the new iterator that contains the keys insertion order.

### Create own methods
- Function inside object is known as methods.
```JavaScript
const person = {
	name: 'Tushar',
	age: 21,
	about : function(){
		console.log("My name is ${this.name}");
	}
}
person.about();
// My name is Tushar
// When declaring a new object, use the object literal, not the new object() constructor.
```

## This Keyword
- 'This' keyword refers to an object that is executing the current piece of code.
```JavaScript
function Info(){
	console.log('My name is ${this.name}');
}
const person1 = {
	name : 'Tushar',
	about : Info
}
const person2 = {
	name : 'Boy',
	about : Info
}
person1.about(); // My name is Tushar
person2.about(); // My name is Boy
```

### Call, Apply, Bind Methods
##### Call
- It involves the function and allows you to pass in arguments one by one.
```JavaScript
const user1 = {
	name : 'Tushar',
	age : 22,
	intro : function(){
		console.log(this.name,this.age);
	}
}
const user2 = {
	name : 'Vishal',
	age : 21,
}
user1.intro.call(user2); // Vishal 21
```
##### Apply
- It invokes the function and allows you to pass in arguments as an array.
```JavaScript
var user1 = {
	name:'Tushar',
	age:22
};
var user2 = {
	name:'Vishal',
	age:21
};
function say(greet){
	console.log(greet+this.name);
}
say.apply(user2,['Hi ']);
// Hi Vishal
```
##### Bind
- It returns a new function, allowing you to pass in a this array and any number of arguments.
```JavaScript
var user1 = {
	name : 'Tushar',
	age : 22
};
var user2 = {
	name : 'Vishal',
	age : 21
};
function say(){
	console.log(this.name,this.age);
}
var myfun = say.bind(user1);
myfun(); // Tushar 22
```

## Prototype
- It is used to add new properties and methods to an existing object constructor.
```JavaScript
function Person(){
	this.name = 'Tushar',
	this.age = 22
}
const person = new Person();
// Checking the prototype value
console.log(Person.prototype); //{...}
// It shows an empty object
```
### Prototype Inheritance
- Objects inherit properties and methods from a prototype.
- Using the prototype makes faster object creation since properties/methods on the prototype don't have to be re-created each time a new object is created.
### New Keyword
<mark>Five things to remember about new keyword</mark>
- It creates a new object. The type of this object is simply object.
- It sets this new object's internal.
- It makes the this variable point to the newly created object.
- It executes the constructor function, using the newly created object whenever this is mentioned.
- It returns the newly created object.

## Function chaining 
- It is a <mark>pattern</mark> in javascript where multiple functions are called on the. same object <mark>consecutively</mark>. Using the same object reference, <mark>multiple functions can be invoked</mark>. It increases the readability of the code and means less redundancy.

```javascript
person
	.sleep() // is sleeping
	.wakeUp() // wake up
	.eat() // is eating
	.study() // is studying
	```
### Why use function chaining
- In programming it is a commonplace to have actions that need to run in <mark>a defined series of steps</mark>. Creating a single function that define all these actions is usually a terrible idea so we write <mark>a number of functions that deal with individual actions</mark>
- Function chaining can be created by defining several methods in an <mark>object that return this</mark> which is an instance of the object so we can call another function from the object.
#### Ways of Creating functions chaining 
1. object methods
2. class methods
3. functions prototype

##### Object Methods:
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
##### Class Methods:
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
##### Function Prototype:
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
## JavaScript information
- It is a versatile programming language that powers the interactive features and dynamic behaviour of modern websites.
- It is a client-side scripting language, meaning it runs directly in the web browser and can interact with HTML and CSS.
- It supports object-oriented programming (OOP) concepts such as encapsulation, inheritance, and polymorphism.
- Functions in JavaScript are first-class citizens, which means they can be assigned to variables, passed as arguments, and returned as values.
- It has a concept called "hoisting", where variable and function declarations are moved to the top of their respective scopes during the compilation phase.
- The DOM(Document Object Model) is a powerful feature of JavaScript that allows dynamic manipulation of we page elements, enabling interactive experiences.
- Asynchronous programming in JavaScript is facilitated through features like callbacks, Promises, and the modern async/await syntax.
- JavaScript framework and libraries like React, Angular, and Vue.js have revolutionised web development, enabling the creation of complex and interactive user interfaces.
- Node.js allows JavaScript to run on the server-side, enabling server-based applications and APIs.

## Number() vs parseInt()
JavaScript offers two ways to convert data into numbers:
Number() and paseInt()

### Number()
- It converts various data types to numbers. It directly converts strings representing valid numbers, handles true as 1, false as 0, and even turns dates into timestamps.
```JavaScript
Number('123'); //Output: 123
Number('hello'); //Output: NaN
Number('123hello'); //Output: NaN
Number(true); //Output: 1
Number(false); //Output: 0
```

### parseInt()
- It specifically parses strings into integers. It stops at the first non-numeric character.
- It also allows setting a radix (base) for conversion.
```JavaScript
parseInt('123'); //Output: 123
parseInt('123hello'); //Output: 123
parseInt('hello123'); //Output: NaN
parseInt('10',2); //Output: 2 //Parsing 10 as binary
```

## Object.groupBy
```JavaScript
//Data
const students = [
{ id: 1, name: 'Tushar', grade: 'A'},
{ id: 2, name: 'Vishal', grade: 'B'},
{ id: 3, name: 'Amit', grade: 'A'},
{ id: 4, name: 'Ankit', grade: 'C'},
{ id: 5, name: 'Aadarsh', grade: 'B'},
];
//Group students by grade using Object.groupBy with a callback function
const groupedStudents = Object.groupBy(students, ({grade}) => grade);

console.log(groupedStudents);
//Output:
{
	'A': [
	{ id: 1, name: 'Tushar', grade: 'A'},
	{ id: 3, name: 'Amit', grade: 'A'}
	],
	'B': [
	{ id: 2, name: 'Vishal', grade: 'B'},
	{ id: 5, name: 'Aadarsh', grade: 'B'}
	],
	'C': [
	{ id: 4, name: 'Ankit', grade: 'C'}
	]
}
```

## Map and Filter
Both are array methods and both return a new array when applying. Filter additionally eliminates items that don't match.
```JavaScript
const DATA = [
	{id: 1, title: 'first'},
	{id: 2, title: 'second'},
	{id: 3, title: 'third'},
	{id: 4, title: 'fourth'}
]

const upperData = DATA.map(el=>el.title.toUpperCase())
console.table(upperData)
//(index)    Value
//0          'FIRST'
//1          'SECOND'
//2          'THIRD'
//3          'FOURTH'
const moduloData = DATA.filter(el=>el.id % 2 === 0)
console.table(moduloData)
//(index)    id    title
//0          2     'second'
//1          4     'fourth'
console.table(DATA)
//(index)    id    title
//0          1     'first'
//1          2     'second'
//2          3     'third'
//3          4     'fourth'
```

## Slice and Splice
```JavaScript
const charactersArr = [
	'Tony Stark',
	'Harry Potter',
	'Witcher',
	'Luke Skywalker',
]

const copyArr = [...charactersArr]

copyArr.splice(0,1);
console.log(copyArr)
//['Harry Potter','Witcher','Luke Skywalker']
copyArr.splice(CopyArr.length,1,'Wonder Woman');
console.log(copyArr)
//['Harry Potter','Witcher','Luke Skywalker','Wonder Woman']
const selected = charactersArr.slice(0,2)
console.log(selected)
//['Tony Stark','Harry Potter']
console.log(charactersArr)
//['Tony Stark','Harry Potter','Witcher','Luke Skywalker']
```

## Concat
This method returns a new array of merging two or more arrays.
```JavaScript
const arr1 = [1,2,3,4]
const arr2 = [10,20,30,40]
const arr3 = [100,200,300,400]

const mergedArr = arr1.concat(arr2,arr3)
console.log(mergedArr)
//[1,2,3,4,10,20,30,40,100,200,300,400]
```

## Find and findIndex
The find method returns the first element that satisfies the condition, while findIndex returns the index of that element
```JavaScript
const DATA = [
	{id: 1,title: 'first'},
	{id: 2,title: 'second'},
	{id: 3,title: 'third'},
	{id: 4,title: 'fourth'},
]

const itemIdx = DATA.findIndex(el=> el.id === 2)
console.log(itemIdx)
//1
const item = DATA.find(el=>el.id === 2)
console.log(item)
//{id: 2, title: 'second'}
```

## Destructuring
The destructuring assignment is a special syntax which enables unpacking(assigning) values from arrays or object properties directly into variables.
```JavaScript
const name = ['Luke','Skywalker']
const [firstName, lastName] = name
console.log(firstName, lastName)
//Luke Skywalker
const jedi = {
	id: 1,
	name: 'Luke Skywalker',
	lightsaber: true,
	species: 'Human'
}
const {name:jediName, species, ...rest} = jedi
console.log(jediName)
console.group(species)
//Luke Skywalker
//Human
console.log(rest)
//{id: 1, lightsaber: true}
```

## rest and spread operator
Rest parameter enables us to pass unspecified number of parameters to a function which will be placed into array, while the spread operator enables us to spread the content of a iterable into individual elements
```JavaScript
const introduction = ['my','name','is','Tushar','Jaryal']
const copyArr = [...introduction]
console.log(copyArr)
//['my','name','is','Tushar','Jaryal']
console.log(...copyArr)
//my name is Tushar Jaryal
//REST
const getSize = (...args) => {
	return args.length
}
console.log(getSize(1,5,10))
//3
console.log(getSize(10,20,40,50,60))
//5
```

## Promises
Promises are used to handle asynchronous operations. Each promise can ens as a success or failure having 3 possible statuses: pending, fulfilled or rejected.
```JavaScript
const fetchData = async() => {
	try {
		const response = await fetch('https:site.com');
		if(!response.ok) throw new Error(repsonse.status);
		const result = await response.json();
		return result;
	}
	catch(e){
	console.log(e)
	}
}
```

## Difference Between synchronous and asynchronous code
1. Execution
	1. Synchronous
		- Executes Sequentially
	2. Asynchronous
		- Executes out of order, not waiting for one operation to complete before starting the next.
2. Behaviour
	1. Synchronous
		- Can lead to a blocking behaviour in applications, potentially making the UI unresponsive if a task takes a long time.
	2. Asynchronous
		- Non-Blocking behaviour, allowing other tasks to run simultaneously.
3. Example
	1. Synchronous
```JavaScript
const result = someFunction();
console.log(result);
console.log('After Function');
```

		2. Asynchronous
```JavaScript
fetch('https://api.example.com/data')
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error(error));
console.log('After Fetch Call');
```

4. Understanding and Debugging
	1. Synchronous
		- Generally easier to understand and debug due to its straightforward flow.
	2. Asynchronous
		- Can be more complex due to the use of callbacks, promises, or async/await.
5. Suitability for Unpredictable Task
	1. Synchronous
		- Not well-suited for tasks that can take an unpredictable amount of time, such as network requests or reading from disk.
	2. Asynchronous
		- Ideal for tasks like network requests, timers and other operations that shouldn't block the main thread.
6. Common Methods/Functions
	1. Synchronous
		- Array.forEach(),Math.max(),etc.
	2. Asynchronous
		- setTimeout(), fetch(), XMLHttpRequest, Promises, async/await.

