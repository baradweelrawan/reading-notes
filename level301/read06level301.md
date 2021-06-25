# this is read06 from 301
# Node :

![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRcfBOcz_p4uXEUnm_ovmr-qaI6xxLRnL1DbLayi9yfijEYj8Tw-iI4ZbMOn_G8AFa2wV4&usqp=CAU)

# What Is Node and When Should I Use It?
Node.js: is a JavaScript runtime built on Chrome’s V8 JavaScript engine.it is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.“event-based”, “non-blocking”, “asynchronous I/O” — that’s quite a lot to digest in one go.

# Node Is Built on Google Chrome’s V8 JavaScript Engine :
1. The V8 engine :is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.when we say that Node is built on the V8 engine, we don’t mean that Node programs are executed in a browser. They aren’t. Rather, the creator of Node (Ryan Dahl) took the V8 engine and enhanced it with various features.This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

# Node Binaries vs Version Manager :
This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.

# How Do I Install Node.js? 
You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed. This is the current LTS version at the time of writing.This uses Node’s built-in console module to display a message in a terminal window.

# Node.js Has Excellent Support for Modern JavaScript
Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime a specific version of the V8 engine, this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers.

# Introducing npm, the JavaScript Package Manager:
Node comes bundled with a package manager called npm. To check which version you have installed on your system, type npm -v.In addition to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.

# Installing a Package Globally :
1. Open your terminal and type the following:
  * npm install -g jshint
  * index.js
 You should now see a number of ES6-related errors. If you want to fix them up, add /* jshint esversion: 6 */ to the top of the index.js file, re-run the command and linting should pass.

# Installing a Package Locally :
You can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that directory:
1. npm init -y :This will create and auto-populate a package.json file in the same folder.
2. npm install lodash --save :to install the lodash package and save it as a project dependency
3. Create a file named test.js.
4. run the script using node test.js

# Working with the package.json File :
When you look at the contents of the test directory, you’ll notice a folder entitled node_modules. This is where npm has saved lodash and any libraries that lodash depends on. The node_modules folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running npm install from within the project’s root.If you open the package.json file, you’ll see lodash listed under the dependencies field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.

# What Is Node.js Used For?
These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

# The Node.js Execution Model:
In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request. In a language such as PHP or Ruby, any subsequent I/O operations for example, interacting with a database block the execution of your code until the operation has completed. That is, the server has to wait for the database lookup to complete before it can move on to processing the result.If new requests come in while this is happening, the server will spawn new threads to deal with them. This is potentially inefficient, as a large number of threads can cause a system to become sluggish — and, in the worst case, for the site to go down. The most common way to support more connections is to add more servers.
  * Node.js:is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. when a new request comes in (one kind of event) the server will start processing it If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished another kind of event, the server will execute the callback and continue working on the original request.
  Node uses the libuv library to implement this asynchronous that is, non-blocking behavior.Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. 

# Are There Any Downsides?
The fact that Node runs in a single thread does impose some limitations.blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process.

# What Kind of Apps Is Node.js Suited To?
Node is particularly suited to building applications that require some form of real-time interaction or collaboration chat sites, or apps such as CodeShare, where you can watch a document being edited live by someone else. It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven such as those needing to perform operations on a database, or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded. 

# What Are the Advantages of Node.js?
1. speed and scalability :an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes.
2. You can do everything in the same language, which, as a developer, makes you more productive and hopefully, happier.
3. speaks JSON :SON is probably the most important data exchange format on the Web, and the lingua franca for interacting with object databases (such as MongoDB). 
4. JavaScript is ubiquitous :most of us are familiar with JavaScript, or have used it at some point. This means that transitioning to Node development is potentially easier than to other server-side languages.







   





