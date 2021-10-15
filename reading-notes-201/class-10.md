<b>Ch.10 "Error Handling & Debugging"

Execution context: Global= code is in script, but not in function. Can be called only 1 unique identifier. Function context= code inside a function. Each function has its own context. Eval context= text execute like code in internal function called eval().

Variable scope:

Global scope: variable declared outside a function & can be used anywhere.

Function level scope: variable declared inside a function & can only be used inside that function.

JS interpreters stacking tasks (Ref. on pg 454-455 , Jon Duckett, JavaScript & JQuery.)

Each time script enters newly executed context there are 2 phases: 1) prepare= new scope created. Variables, functions & arguments created. 2) Execute= Assign values to variables refer functions & code executes statements.

In interpreter, each execution context has its own variable object. It holds variables, function, & parameters available within it. Each execution context can also access its parent variable object.

If error happens, interpreter will look in code for an exception, working out until its global & then stops process & sends error message.

Error object: Contains name, message, fileNumber & lineNumber, displayed in console.

7 types of error objects: 

Error= general message which all others are based on.

Syntax error= syntax is not correct. Usually a typo.

Reference error= variable not declared or out of scope.

Type error= value is unexpected data type, usually when trying to use object or method that doesn't exist.

Range error= number outside of range.

URI error= characters are not escaped & cause error.

Eval error= incorrect use of function.

NaN= not an error, but returned when something is Not a Number.

2 ways to deal with errors: 1) Debug the script. 2) Try using= try, catch, throw, finally statements.

Debug workflow= Where's the problem? What's the problem?

Dev tools in console can write directly to it, or use console.log(). Pass many variables, separated by commas. Should always remove before going live.

More console methods= console.info(), for general. console.warn(), used for warnings. console.error(), used to hold errors.

Can group data in console with console.group(). Put the name you want to use for group as parameter, then list your other console.commands() under and close at bottom with console.group() no parameters in parenthesis.

console.table= output table contents

console.assert= test if condition is met, will only output if false.

Breakpoints- use to step through code; can be conditional or can also use 'debugger' keyword in your code.

try-catch-finally= similar in construction to a else if statement. Code will 'try' to execute; if this fails, it will try to 'catch' it & suggest a code solution; 'finally' gives a refresh option to user to refresh page with new code.

Debugging tips & common errors= (Ref. on pg 484-485 , Jon Duckett, JavaScript & JQuery.)

<a href="https://github.com/scottie-l/Reading-notes-201">Back</a>