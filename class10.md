# Read 10
<br>
<hr>
<br>

## Call stack
* A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.
* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.
* In summary, then, we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.
<br>
<hr>
<br>

## The JavaScript Call Stack - What It Is and Why It's Necessary
* The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
 
 * At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
 * LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.
 <br><br>
 `function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();`

* You will notice that the arrangement of the functions as a stack begins with the firstFunction() (which is the last function that got into the stack, and is popped out to throw the error), followed by the secondFunction(), and then the thirdFunction() (which is the first function that gets pushed into the stack when the code is executed).
* Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.
 <br><br>

What causes a stack overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

<br><br>

* In summary
The key takeaways from the call stack are:
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

<br>
<hr>
<br>

## JavaScript error messages && debugging
<br><br>
Types of error messages
The first thing that indicates you that something is wrong with your code is the (in)famous error message. it usually appears on your console (being developer tools of the browser, terminal or whatever else you are using).
<br><br>

* Reference errors :
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
`console.log(foo) // Uncaught ReferenceError: foo is not defined`
* Syntax errors
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
`JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`
* Range errors
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
`var foo= [] 
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length`
* Type errors
Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
`var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined`
<br><br>

## Debugging
* The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.
<br><br>

## Call stack
The red part of our first  represents the call stack, which is the path that your program has taken to reach the point were you set a breaking point or were you have an error.
* I would not insist in using the object to have the function, but I would recommend vividly of adding names to your functions whenever possible so that the call stack is more readable without having to dive into each step.
* Another way to see the stack trace at any given point in your code is to just write console.trace() were you want to log it.
<br><br>

## Handling errors
An alternative it’s to encapsulate our problematic function code with a try…catch which would make an error be thrown but this time, not “uncaught” so we can send it to a error logging to be checked later and send a fallback to the function so that our code continues without problems.
