# this is read10 from 301
# The JavaScript Call Stack:
![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQqXN2nfKwXvfKnETqYBrkCcnNIVfCxqZ2C1g&usqp=CAU)

The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.The call stack is primarily used for function invocation (call). Since the call stack is single, functions execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.
LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

# What causes a stack overflow?

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

The key takeaways from the call stack are:
  1. It is single-threaded. Meaning it can only do one thing at a time.
  2. Code execution is synchronous.
  3. A function invocation creates a stack frame that occupies a temporary memory.
  4. It works as a LIFO — Last In, First Out data structure.

# JavaScript error messages && debugging :
Most of your time as a developer is spent reading code followed by debugging that same code, most likely to be able to read it or solve an “unexpected feature” (which, joking aside, is more correctly known as a “bug”).

# Types of error messages :
The first thing that indicates you that something is wrong with your code is the infamous error message that the one we saw just moments ago, it usually appears on your console (being developer tools of the browser, terminal or whatever else you are using.

 1. Reference errors :This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

 2. Syntax errors:this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful.

 3. Range errors :Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

 4. Type errors :this types of errors show up when the types (number, string ) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

 There are also warnings, for instance telling you about a deprecated method, which can be found more frequently in firefox developer tools.

 # Debugging :
 To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting.
 The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values. 
 Using Node.js with Visual Studio Code you can press the debug tab and add a configuration.You can run the debugger by pressing F5 or pressing the green play button.

 # Call stack :
 The red part represents the call stack, which is the path that your program has taken to reach the point were you set a breaking point or were you have an error.

 1. testing is automatically called since it’s an IIFE (immediately Invoked Function Expression)
 2. obj variable is declared with the function add (using ES6 shorthand for functions in objects.
 3. the function add is called from the obj variable with two strings has parameters, there are added which makes them “12” in this scenario and then split is called before returning [“1”, “2”].
 4. the function add is called again, this time with number, the values are added making it 3 but then, split (which is not available for number type variables) is called which makes an error being thrown.

 The call stack it’s better to navigate when you have names to your functions, meaning that if you use anonymous functions you will most probably have an harder time since the call stack will not show the name of the parent function.
 Another way to see the stack trace at any given point in your code is to just write console.trace() were you want to log it.

# Handling errors :
About the light blue part of our earliest example of an error message, that shows up like that when we do not handle errors properly, meaning that anything after that error will not be executed. To avoid this we usually try to catch the errors so we can gracefully fallback to a default state of our application in case of an error this fallback can be a 404 page which is normally not that graceful but is better than a page to just stop working.
The function will break when we send a number, this could be handled by checking for the type of the arguments like we discussed before and sending something back.It would work in this one since we only have to worry about string but in other scenarios we might have to check for all other types, making our function “half validation, half logic” which can be cumbersome to read and maintain.
An alternative it’s to encapsulate our problematic function code with a try…catch which would make an error be thrown but this time, not “uncaught” so we can send it to a error logging to be checked later and send a fallback to the function so that our code continues without problems.

The worthiest outcome of using try…catch tough is the fact that your application will keep on running, maybe with some side effects due to the fact that numberResult now contains an empty array but at least it didn’t just crash onto itself ;just make sure the code you have afterwards is bearing in mind the default values of the errors. recommend using try…catch when the type checks are becoming “longer than your function logic”, when a request is made and you aren’t sure if the response might change or temporarily when a code is continuously giving you problems and you still haven’t got around to refactor it.

# Tools to avoid runtime errors :
JS is not a compiled language like Java so your errors will happen at runtime, that means that you can only see whatever is wrong with your code after your run it.For using tools of you looking to make JS a more strong typed experience you can check out stuff like TypeScript:
 
  1. quokka to evaluate your code as you type
  2. eslint to make sure your style guide is consistency and it will grab you an error or two along the way and












 

