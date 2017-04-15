# compSci

JS in more Depth

Table of Contents

Table of Contents
Homework Details
Core JavaScript Questions
ES6 Questions
Node.js Questions
React.js Questions
Internet/Network questions
Homework Details

This homework is designed to prepare you for questions you may face during an interview. It should take you no more than 4 hours. It's akin to an open book quiz since you can use the internet to look things up. But first, try going through and seeing how many questions you can answer without using google/stackoverflow/anyOtherInternetSource! And then go back and look up the answers to the ones that stumped you.

Core JavaScript Questions

What is the difference between undefined and not defined in JavaScript?
What is "Hoisting" in JavaScript?
What would be the output of the following code?
    var y = 1;
      if (function f(){}) {
        y += typeof f;
      }
     console.log(y);
What is a "private method"?
What is the drawback of creating true private methods in JavaScript?
What is a “closure” in JavaScript? Provide an example.
Write a mul function which will produce the following outputs when invoked.
console.log(mul(2)(3)(4)); // output : 24 
console.log(mul(4)(3)(4)); // output : 48
How would you empty an array in JavaScript? Provide at least 2 methods of doing so.
What will be the output of the following code?
var output = (function(x){
    delete x;
    return x;
  })(0);
  
  console.log(output);
What about this code?

var x = 1;
var output = (function(){
    delete x;
    return x;
  })();
  
  console.log(output);
And what about this one?

var x = { foo : 1};
var output = (function(){
    delete x.foo;
    return x.foo;
  })();
  
  console.log(output);
And finally, what about this one?

var Employee = {
  company: 'xyz'
}
var emp1 = Object.create(Employee);
delete emp1.company
console.log(emp1.company);
What would this code return?
var trees = ["xyz","xxxx","test","ryan","apple"];
delete trees[3];
  
  console.log(trees.length);
What will be the output of the code below?
var bar = true;
console.log(bar + 0);   
console.log(bar + "xyz");  
console.log(bar + true);  
console.log(bar + false);   
What will be the output of the code below?
var z = 1, y = z = typeof y;
console.log(y);  
What would be the output of the code below?
 var salary = "1000$";

 (function () {
     console.log("Original salary was " + salary);

     var salary = "5000$";

     console.log("My New Salary " + salary);
 })();
What is the instanceof operator in JavaScript? What would be the output of the code below?
function foo(){ 
  return foo; 
}
new foo() instanceof foo;
What constitutes a "Primitive" value in Javascript?
What is the difference between a reference type variable and a value type variable?
How would you describe the difference between class-based inheritance and prototypical inheritance?
ES6 Questions

What is the difference between JavaScript and ECMAScript?
What do const and let do? And when would we use them?
How would you describe the difference between function and function*?
When would you NOT use an arrow function in the place of a regular function expression?
Refactor the following code to use an ES6 Template Literal.
var name = 'Tiger';
var age = 13;

console.log('My cat is named ' + name + ' and is ' + age + ' years old.');
How would you refactor the following code to use ES6 default parameters?
function addTwoNumbers(x, y) {
    x = x || 0;
    y = y || 0;
    return x + y;
}
What is a "Promise" in ES6? And how many different states do they have?
What is a practical use case for Promises?
What is wrong with the following code? And how could it be better?
new Promise((resolve, reject) => {  
  throw new Error('error')
}).then(console.log)
Describe the .fetch() method. What is one disadvantage to using the .fetch() method over existing methods?
Node.js Questions

What is Node.js?
What is an "Error-First" Callback?
What is the Node.js Event Loop?
Why might someone choose to use the Node.js Async single-threaded model over a more traditional multi-threaded model?
What is meant by the term "non-blocking I/O"?
What is the "memory stack"? And what happens when you exceed it?
React.js Questions

What makes React.js more efficient at updating the DOM?
What is the difference between a Logical component and a Pure component?
What happens when you call "setState" in React?
What is the React method to create a component? Alternatively, how would you accomplish the same thing using ES6 classes?
In which React lifecycle event would you make AJAX requests? And why?
Why would you use React.Children.map(props.children, () => ) instead of props.children.map(() => )?
What is JSX?
Internet/Network Questions

What does TCP/IP stand for?
Behind the scenes, how does HTTPS differ from HTTP?
Define the general response status code categories.
What does DDOS stand for?
What is CORS? How does it work?
What does REST stand for when we refer it in the context of a "RESTful API"?