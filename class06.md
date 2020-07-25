# Read 6
<br>
<hr>
<br>

## Node.js
* Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.
* Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.
* V8  was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.
* Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.
* use a version manager instead. This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.
<br><br><br>

## “Hello, World!” the Node.js Way
* You can check that Node is installed on your system by opening a terminal and typing `node -v`
<br>

* Node.js Has Excellent Support for Modern JavaScript
*  Node comes bundled with a package manager called npm. To check which version you have installed on your system, type `npm -v`.
* Installing a Package Globally ,Open your terminal and type the following: `npm install -g jshint`
* Installing a Package Locally ,Open your terminal and type the following:`npm init -y` , This will create and auto-populate a package.json file in the same folder.
* If you open the package.json file, you’ll see lodash listed under the dependencies field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.
* if you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm (or maybe Yarn). 

<br><br><br>

## The Node.js Execution Model
<br><br>

![img](https://dab1nmslvvntp.cloudfront.net/wp-content/uploads/2012/10/1516152673node_event_loop.png)
<br><br><br>

## “Hello, World!” — Server Version
`const http = require('http');
http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
}).listen(3000);
console.log('Server running on http://localhost:3000');`

<br><br>

We start by requiring Node’s native HTTP module. We then use its createServer method to create a new web server object, to which we pass an anonymous function. This function will be invoked for every new connection that’s made to the server.
The anonymous function is called with two arguments (request and response). These contain the request from the user and the response, which we use to send back a 200 HTTP status code, along with our “Hello World!” message.
Finally, we tell the server to listen for incoming requests on port 3000, and output a message to the terminal to let us know it’s running.
<br><br><br>

## What Are the Advantages of Node.js?
Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes. You can do everything in the same language, which, as a developer, makes you more productive (and hopefully, happier). For example, you can easily share code between the server and the client.