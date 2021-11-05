<b><a href = "https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/">"Understanding the JS Call Stack"</a>

1. What is a ‘call’? A call is a function invocation.

2. How many ‘calls’ can happen at once? Call's happen one at a time, top to bottom.

3. What does LIFO mean? Last in, first out.

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

    <img src = "assets/images/LIFO Stack.png"/>

5. What causes a Stack Overflow? A recursice function without an exit point.

The key takeaways from the call stack are:
    - It is single-threaded. Meaning it can only do one thing at a time.
    - Code execution is synchronous.
    - A function invocation creates a stack frame that occupies a temporary memory.
    - It works as a LIFO — Last In, First Out data structure.

<b><a href = "https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c">"JS error messages"</a>

1. What is a ‘refrence error’? When you try to use a variable that has not yet been declared.

2. What is a ‘syntax error’? This occurs when you have something that cannot be parsred in terms of syntax.

3. What is a ‘range error’? Try to manipulate an object with some kind of length & give it an invalid length.

4. What is a ‘type error’? When the type (number, string, etc.) you're trying to use or access is incompatible, like accessing a property in an undefined type of variable.

5. What is a breakpoint? A debugger in the line in you want to break or stop the execution of your program.

6. What does the word ‘debugger’ do in your code? It stops the execution of your program where you inserted it.

Chrome developer tools - open pg with your JS code (Ctrl + o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again(F5).

<b><a href = "https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors">"JS errors ref. on MDN"</a>

These errors can be helpful debugging aid, but reported problem isn't always immediately clear. The pages will provide additional details about errors. Each error is an object based upon the Error object, and has a name and message. Errors displayed in the Web console may include a link to the corresponding page below to help you quickly comprehend the problem in your code.

These two properties provide a starting point toward understanding and resolving the error. For more information, follow the links!

- In this list: each page is listed by:
  - name (the type of error)
  - and message (a more detailed human-readable error message).

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
