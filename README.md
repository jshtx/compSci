# compSci

# JS in more Depth

## Table of Contents

1. Table of Contents
2. Homework Details
3. Core JavaScript Questions
4. ES6 Questions
5. Node.js Questions
6. React.js Questions
7. Internet/Network questions

## Homework Details

This homework is designed to prepare you for questions you may face during an interview. It should take you no more than 4 hours. It's akin to an open book quiz since you can use the internet to look things up. But first, try going through and seeing how many questions you can answer without using google/stackoverflow/anyOtherInternetSource! And then go back and look up the answers to the ones that stumped you.

## Core JavaScript Questions

1. What is the difference between `undefined` and `not defined` in JavaScript?
	An undefined variable is a variable that has been declared, but no value assigned to it.
	A not defined variable is a variable that has never been declared.

2. What is "Hoisting" in JavaScript?
	Hoisting is when JS moves all variable and function declarations to the top of the current scope. But, only the actual declarations are hoisted, the assigned values stay in the same place.

3. What would be the output of the following code?
```javascript
    var y = 1;
      if (function f(){}) {
        y += typeof f;
      }
     console.log(y);
```
	Returns: 1object

4. What is a "private method"?
	Private methods are the inner methods of a constructor and cannot be accessed outside the constructor.

5. What is the drawback of creating true private methods in JavaScript?
	Private methods cannot be used by public methods without using a priveleged method.

6. What is a “closure” in JavaScript? Provide an example.
	Closures are functions that refer to independent variables that are used locally, but defined in an enclosing scope. These functions 'remember' the environment in which they were created.

	```javascript
	var add = (function () {
    var counter = 0;
    return function () {return counter += 1;}
	})();
	```
7. Write a mul function which will produce the following outputs when invoked.
```javascript
function mul(num1, num2, num3){
	return num1 * num2 * num3;	
};
console.log(mul(2)(3)(4)); // output : 24 
console.log(mul(4)(3)(4)); // output : 48
```
8. How would you empty an array in JavaScript? Provide at least 2 methods of doing so.
	array.length = 0;
	OR
	while(myArray.length > 0) {
    myArray.pop();
	}

9. What will be the output of the following code?
```javascript
var output = (function(x){
    delete x;
    return x;
  })(0);
  
  console.log(output);
```
	Output: 0

What about this code?
```javascript
var x = 1;
var output = (function(){
    delete x;
    return x;
  })();
  
  console.log(output);
```
	Output: 1

And what about this one?
```javascript
var x = { foo : 1};
var output = (function(){
    delete x.foo;
    return x.foo;
  })();
  
  console.log(output);
```
	Output: undefined

And finally, what about this one?
```javascript
var Employee = {
  company: 'xyz'
}
var emp1 = Object.create(Employee);
delete emp1.company
console.log(emp1.company);
```
	Output: xyz

10. What would this code return?
```javascript
var trees = ["xyz","xxxx","test","ryan","apple"];
delete trees[3];
  
  console.log(trees.length);
```
	Output: 5

11. What will be the output of the code below?
```javascript
var bar = true;
console.log(bar + 0);   
console.log(bar + "xyz");  
console.log(bar + true);  
console.log(bar + false);   
```
	Output: 1
			truexyz
			2
			1

12. What will be the output of the code below?
```javascript
var z = 1, y = z = typeof y;
console.log(y);  
```
	Output: undefined

13. What would be the output of the code below?
```javascript
 var salary = "1000$";

 (function () {
     console.log("Original salary was " + salary);

     var salary = "5000$";

     console.log("My New Salary " + salary);
 })();

```
	Output: Original Salary was undefined
			My New Salary is 5000$

14. What is the instanceof operator in JavaScript? What would be the output of the code below?
```javascript
function foo(){ 
  return foo; 
}
new foo() instanceof foo;
```
	The instanceof operator tests whether an object has in its prototype chain the prototype property of a constructor.

	Output: false

15. What constitutes a "Primitive" value in Javascript?
	There are 6 primitive values: string, number, boolean, null, undefined, and symbol

16. What is the difference between a reference type variable and a value type variable?
	A value type actually holds the value of the variable, but a reference type variable just references back to the value of the variable.

17. How would you describe the difference between class-based inheritance and prototypical inheritance?
	Class inheritance is a description of the object to be created and a prototype is a working object instance. Objects inherit directly from other objects.

## ES6 Questions

1. What is the difference between JavaScript and ECMAScript?
	ECMAScript is the standardized version of JavaScript. When JS was first developed by netscape there were different versions for different browsers, EScript standardized everything.

2. What do `const` and `let` do? And when would we use them?
	const creates an immutable binding. 

3. How would you describe the difference between `function` and `function*`?
4. When would you NOT use an arrow function in the place of a regular function expression?
5. Refactor the following code to use an ES6 Template Literal.
```javascript
var name = 'Tiger';
var age = 13;

console.log('My cat is named ' + name + ' and is ' + age + ' years old.');
```
6. How would you refactor the following code to use ES6 default parameters?
```javascript
function addTwoNumbers(x, y) {
    x = x || 0;
    y = y || 0;
    return x + y;
}
```
7. What is a "Promise" in ES6? And how many different states do they have?
8. What is a practical use case for Promises? 
9. What is wrong with the following code? And how could it be better?
```javascript
new Promise((resolve, reject) => {  
  throw new Error('error')
}).then(console.log)
```
10. Describe the .fetch() method. What is one disadvantage to using the .fetch() method over existing methods?

## Node.js Questions

1. What is Node.js?
	Node.js is a server-side platform built with javascript.
2. What is an "Error-First" Callback?
3. What is the Node.js Event Loop?
4. Why might someone choose to use the Node.js Async single-threaded model over a more traditional multi-threaded model?
5. What is meant by the term "non-blocking I/O"?
6. What is the "memory stack"? And what happens when you exceed it?

## React.js Questions

1. What makes React.js more efficient at updating the DOM?

2. What is the difference between a Logical component and a Pure component?
3. What happens when you call "setState" in React?
4. What is the React method to create a component? Alternatively, how would you accomplish the same thing using ES6 classes?
5. In which React lifecycle event would you make AJAX requests? And why?
6. Why would you use `React.Children.map(props.children, () => )` instead of `props.children.map(() => )`?
7. What is JSX?
	JSX is a preprocessor step that adds XML syntax to JavaScript

## Internet/Network Questions

1. What does TCP/IP stand for?
	 Transmission Control Protocol/Internet Protocol

2. Behind the scenes, how does HTTPS differ from HTTP?
	HTTPS encrypts what is being sent so even it is intercepted, it cannot be read, while HTTP is not secure

3. Define the general response status code categories.
	100s: Informational
	200s: Success
	300s: Redirection
	400s: Client error
	500s: Server error

4. What does DDOS stand for?
	Distributed Denial of Service

5. What is CORS? How does it work?
	Cross Origin Resource Sharing. It allows resources to be requested from domains outside the first domain being served.

6. What does REST stand for when we refer it in the context of a "RESTful API"?
	Representational State Transer. A RESTful API means the client does not need to know anything about how the API is structured and that the server provides the information necessary for the browser to use the API.