## Components

React JS is a component-based front-end library which means that all parts of a web application are divided into small components.

A component is a small piece of the User interface. Every React.js application is a tree of components.

Components let you split the UI into independent, reusable parts. So when you're building on application with React, you'll build independent and reusable components, and then you'll combine them to build a full fledged web application.

In React, there are two types of components - Functional Components & Class Component
```JavaScript
//Class-based Component
import Reacr, {Componnet} from 'react'
class Example extends Component {
	render(){
		return <div>Hello World!</div>
	}
}
```
```JavaScript
//Functional Component
import React from 'react'
const Example = () => {
	return <div>Hello World!</div>
	//This tag syntax is neither a string nor HTML
}
```

JSX is a syntax extension to JavaScript. It is used in React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React "elements". JSX forms the core syntax of React. So, to learn it better, let's dive into the code and set up our first React.js application.

```JavaScript
return(
	<div classname="greetings">
		<h1>Hello, {prop.name} </h1>
	</div>
)
```

There are a few differences between HTML & JSX, although generally it's incredibly similar. Some of the differences are:
Writing className instead of class,
<p>className -> class</p>
Because the class is a reserved keyword in JavaScript. Since we use JSX in React, the extension of JavaScript, we have to use 'className' instead of the class attribute.

Some as class, there's also one more reserved keyword of JavaScript that is used in HTML. That is the 'for' attribute used with the label element.

So, to define for attribute in JSX, you do it as <q>htmlFor</q>.

<p>label htmlfor='' -> label for=''</p>

```JavaScript
return(
	<form className='form'>
		<label htmlFor='name'>Name</label>
		<input type='text' id='name' />
	</form>
)
```

One of the major differences between HTML and JSX is that in JSX, you must return a single parent element, or it won't compile.

You can use <b>'React fragments'</b> instead of divs

You can also use divs instead of React fragments, it's not necessary to use a particular, but using <b>'React fragments'</b> makes the code more readable.

You can implement JavaScript directly in JSX. To use JavaScript expressions, we use curly brackets {...}
```JavaScript
return(
	<div>
		<h1>Hello, {prop.name}</h1>
		<p>{3 + 7} is ten</p>
	</div>
)
```
Whereas in HTMLL, you need a script tag or an external JavaScript file to implement JavaScript

## What are Props?

To make our components accept different data, we can use props. Props are arguments passed into React components. They are passed to components via HTML attributes.

Props is just a shorter way of saying properties.

We use props in React to pass data from one component to another (from a parent component to child components), But you can't pass props from a child component to parent components.

Data from props is read-only and cannot be modified by a component receiving it from outside.

## What is State?

A state is a plain JavaScript object used by React to represent a piece of information about the component's current situation. It's managed in the component (just like any variable declared in a function).

The state object is where you store property values that belongs to the component. When the state object changes, the component re-renders.

State data can be modified by its own component, but is private (cannot be accessed from outside)

## What is Events?

An event is an action that could be triggered as a result of the user action or a system-generated event. For example, a mouse click, pressing a key, and other interactions are called events.

Handling events with React elements is similar to handling events on DOM elements. There are just some syntax differences.

- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

## How to add Events?

```JavaScript
const handleClick = () => {...}
return(
	<button onClick={handleClick}>
		Explore More
	</button>
)
```
## What are React.js Hooks?

Hooks are a new addition to React in version 16.8 that allows you to use state and other React features, like lifecycle methods. Using hooks makes your code cleaner.

Hooks don't work inside classes - they let you use React without classes.

Hooks let you always use functions instead of having to constantly switch between functions, classes, higher-order components, and render props

Nowadays, hooks are widely used. So you should start using it as well. You can also create your own Hooks to reuse stateful behaviour between different components.