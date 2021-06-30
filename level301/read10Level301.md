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



 

