## JavaScript XML (JSX)
```JavaScript
//JSX elements
let element = <h1>Hello, World!</h1>;
let emptyHeading = <h1 />;

//JSX Expressions
let name = 'Tushar Jaryal';
let element = <h1>Hello, {name}</h1>;
function fullName(firstName, lastName) {
	return firstname + ' ' + lastName;
}
let element = <h1>Hello, {fullName('Tushar','Jaryal')}</h1>;

//JSX Attributes
const element = <img src={user.avaarUrl} />;
const element = <button className='btn'>Click me</button>;

//JSX Functions
name() {
	return 'Tushar';
}
return (
	<h1>
		Hi {name()}!
	</h1>
)
```

## Functional Components
```JavaScript
import React from 'react';
//simple functional component
export default function UserProfile() {
	return(
		<div className='UserProfile'>
			<div>Hello</div>
			<div>World</div>
		</div>
	);
}
//functional component with props
export default fucntion Hello(props) {
	function fullName() {
		return `${props.firstName} ${props.lastName}`;
	}
	return(
		<p>
			{fullName()}
		</p>
	);
}
//props
<Hello firstName='Tushar' lastName='Jaryal' />
```

## Embed Components
```JavaScript
import React from 'react';
import UserAvatar from './UserAvatar';

export default function UserProfile(){
	return (
		<div className='UserProfile'>
			<UserAvatar />
			<UserAvatar />
		</div>
	);
}

//Embed external Components
import React from 'react';
import ComponentName from 'component-name';
export default function UserProfile() {
	return (
		<div className='UserProfile'>
			<componentName />
		</div>
	);
}
```

## CSS in a React
```JavaScript
import React from 'react';
import './Student.css';
export default function Student() {
	return (
		<div className='Student'>
			Tushar Jaryal
		</div>
	)
}
```

## Event Listeners
```JavaScript
import React from 'react';
export default function Hello() {
	function handleClick(event) {
		event.preventDefault();
		alert('Hello World');
	}

	return (
		<a href='/' onClick={handleClick}>
			Say hi
		</a>
	);
}
```

## React State
```JavaScript
import React, {useState} from 'react';
export default function Hello(props) {
	let [name, setName] = useState('Tushar');
	function updateName() {
		let newName = prompt('What is your name?');
		setName(newName);
	}

	return (
		<div>
			<h1>
				{name}
			</h1>
			<button onClick={updateName}>
				Update name
			</button>
		</div>
	);
}
```

## React Forms
```JavaScript
import React, {useState} from 'react';
export default function LoginForm() {
	let [username, setUsername] = useState('');
	let [password, setPassword] = useState('');

	function handleSubmit(event) {
		event.preventDefault();
		alert(`Logging in with ${username} and ${password}`);
	}

	function updateUsername(event) {
		setUsername(event.target.value);
	}

	function updatePassword(event) {
		setPassword(event.target.value);
	}

	return (
		<form onSubmit={handleSubmit}>
			<input type='text' placeholder='Username' onChange={updateUsername} />
			<input type='password' placeholder='Password' onChange={updatePassword} />
			<input type='Submit' value='Login' />
		</form>
	);
}
```

## Map Elements
```JavaScript
let elements = [{
	name: 'one',
	value: 1
},
{
	name: 'two',
	value: 2
},
{
	name: 'three',
	value: 3
}]
return (
	<ul>
		{elements.map(function(element, index) {
			return <li key={index}>The value for {element.name} is {element.value}</li>
		})}
	</ul>
);
```