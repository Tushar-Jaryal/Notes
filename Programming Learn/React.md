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

## Different ways to fetch data in React
### Fetch Method
The fetch method in JS is used to request to the server and load the information in the webpages. The request can be of any APIs that return the data of the format JSON or XML.
```JavaScript
function App(){
	useEffect(() => {
		fetch('https://site.com/')
		.then(response => response.json())
		.then(json => console.log(json))
	}, []);

	return (
		<div>Fetch Data</div>
	);
}
```

### Async-Await
It is the preferred way of fetching the data from an API as it enables us to remove our .then() callbacks and return asynchronously resolved data. In the async block, we can use Await function to wait for the promise.
```JavaScript
function App(){
	useEffect(() => {
		(async () => {
			try {
				const result = await axios.get('https://site.com/')
				console.log(result.data)
			} catch (error) {
				console.error(error)
			}
		})()
	})

	return <div>Async-Await</div>
}
```

### Axios library
With Axios, we can easily send asynchronous HTTP requests to REST APIs and perform create, read, update and delete operations. Axios can be imported in plain JavaScript or with any library accordingly.
```JavaScript
function App() {
	useEffect(() => {
		axios.get('https://site.com')
			.then((response) => console.log(response.data));
	}, []);

	return (
		<div>Axios Library</div>
	);
}
```

### Custom Hook
It is basically a React component whose name will start with *"use"* like ***useFecth***. It can use one or more React hooks inside them.
```JavaScript
const useFetch = (url) => {
	const [isLoading, setIsLoading] = useState(false)
	const [apiData, setApiData] = useState(null)
	const [serverError, setServerError] = useSate(null)

	useEffect(() => {
		setIsLoading(true)
		const fetchData = async () => {
			try {
				const resp = await axios.get(url)
				const data = await resp?.data

				setApiData(data)
				setIsLoading(false)
			} catch (error) {
				setServerError(error)
				setIsLoading(false)
			}
		}

		fetchData()
	}, [url])

	return {isLoading, apiData, serverError}
}
```

### Usage in the component
Import the ***useFetch*** hook and pass the url of the API endpoint from where you want to fetch data.
Now just like any React hook we can directly use our custom hook to fetch the data.
```JavaScript
import useFetch from './useFetch';

const App = () => {
	const { isLoading, serverError, apiData } = useFetch('https://site.com/')

	return (
		<div>
			<h2>API data</h2>
			{isLoading && <span>Loading.....</span>}
			{!isLoading && serverError ? (
				<span>Error in fetching data ... </span>
			) : (
				<span>{JSON.stringify(apiData)}</span>
			)}
		</div>
	)
}
```

### React Query Library
With this we can achieve a lot more than just fetching data. It provides support for caching and refetching, which impacts the overall user experience by preventing irregularities and ensuring our app feels faster.
```JavaScript
import axios from 'axios'
import { useQuery } from 'react-query'

function App() {
	const {isLoading, error, data } = 
	useQuery('posts', () => axios('https://site.com'))

	console.log(data)

	return <div>React Query Library</div>
}
```

## Dynamic Imports 
- Dynamic imports is a JavaScript feature.
- It allows you to load components or modules only when they are needed, rather than loading everything up front.
- In React, this technique is crucial for optimising application performance, especially in large applications.
- This concept is part of a broader strategy known as code splitting, which helps in reducing the initial load time and improving the user experience.

### Basics
- Dynamic import is a method for loading JavaScript modules asynchronously.
- Unlike static imports, dynamic imports load modules on-demand, which can significantly reduce the initial load time of your application.
```JavaScript
import('./MyComponent').then(MyComponent =>{
	//Use Component Here
});
```

- This approach returns a promise, making it ideal for scenarios where module availability is conditional or needs to align with user interactions.

### React.lazy
- React.lazy is a function that simplifies the integration of dynamic imports in React.
- It allows components to be loaded dynamically and renders them like regular components.
```JavaScript
const MyComponent = React.lazy(() => import('./MyComponent'));
```

- React.lazy accepts a function that must call a dynamic 'import()'.
- The function will return a promise, which resolves to the module containing the default export of the React component.

### Handling the Loading State
- React's Suspense component is used to specify a fallback content (like a loading indicator).
- This is used to prevent another JSX while the component, which is dynamically imported, is being loaded.
```JavaScript
<Suspense fallback={<div>Loading..</div>}>
	<MyComponent />
</Suspense>
```

- The 'fallback' prop holds the JSX content to be displayed while the component, in this case MyComponent, is loading.

### Use Cases
- Dynamic imports can be used in a great range of situations.
- They are perfect for large applications where not all scripts are needed at once.
- It can be very beneficial for features that are accessed conditionally, like modal dialogs, tabs, and certain forms.
- Examples:
	- Dashboard Widgets: Load widgets or panels dynamically in a dashboard app.
	- E-commerce: Dynamically load reviews, related products, and customisation options on product pages.
	- Conditional Admin Interfaces: Load admin sections dynamically for users with necessary permissions.

### Best Practices
- Use dynamic import thoughtfully to balance performance gains with code complexity.
- While code splitting helps in reducing initial load times, too much splitting can lead to excessive network requests, which might harm performance.
- Consider preloading components that the user is likely to interact with next.
- Provide informative loading indicators or placeholders to maintain a good user experience during component load.
- Regularly monitor the size of your code bundles to understand the impact of dynamic imports.

### Conclusion
- Dynamic imports in React represents a significant step forward in optimising web application performance.
- By allowing developers to load components and modules only when needed, it dramatically reduces the initial load time of applications, making them faster and more responsive.
- This technique aligns perfectly with modern web development practices where performance, efficiency, and user engagement are of significant importance.