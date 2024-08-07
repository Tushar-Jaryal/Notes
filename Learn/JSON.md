- JSON stands for Javascript Object Notation.
- JSON is lightweight format for storing and transporting data.
- JSON is "self-describing" and easy to understand.
- JSON is often used when data is sent from a server to a web page.

## Example
```JSON
{
"employees":[
	{"firstname":"John","lastname":"Doe"},
	{"firstname":"Anna","lastname":"Smith"},
	{"firstname":"Peter","lastname":"Jones"}
]
}
```

This example defines an employees object : an array of 3 employees records (objects).

## Key and Values

The two primary parts that make up JSON are keys and values.
Together they make a key/value pair :-
- Key: A key is always a string enclosed in quotation marks.
- Value: A value can be a string, number, boolean expression, array, or object.

## JSON.parse()

When receiving data from a web server, the data is always a string.
```JSON
'{"name":"Aditya","Age":19,"country:"India"}'
```
Use the JavaScript function JSON.parse() to convert text into a JavaScript object
```JavaScript
var obj = JSON.parse('{"name":"Aditya","Age":19,"country":"India"}');
```

## JSON.stringify()

The JSON.stringify() method converts a Javascript object or value to JSON string, optionally replacing values if a replacer function is specified or optionally including only the specified properties if a replacer array is specified.

<u>SYNTAX</u>

JSON.stringify(value,replacer,space)

## JSON Values

In JSON, values must be one of the following data types:
- string
- number
- object (JSON object)
- array
- boolean
- null