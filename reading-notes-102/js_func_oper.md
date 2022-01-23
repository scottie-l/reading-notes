# Javascript Functions & Operations

Function '()' is a block of code designed to perform a particular task

Ex:

function to Celsius(farenheit) {return (5/9) * (farenheit-32);

}

document.getElementById("demo").innerHTML = toCelsius;

Can also assign values. Ex:

let x = toCelsius(77);

let text = "The temperature is" + x + "Celsius";

let text = "The temperature is" + toCelsius(77) + "Celsius";

Functions() in JS become local to that function & cannot be called unless you tell it to reference the function().

[JS Functions](https://www.w3schools.com/js/js_functions.asp)

For statements:

"for" loops repeat until specified condition evaluates to false.

for ([initialExpression]; [conditionExpression]; [incrementExpression])

Statement starts left to right starting with initialExpression. If true, executes to conditionExpression. If condition's true, the loop continues to execute to incrementalExpression.

If at any point the result is false, execution stops the loop.

Increment can also be used to count down to certain event.

While statement:

"While" loops execute as long as condition remains true, and only stops when it returns false. AVOID INFINITE LOOPS! This will cause computer to execute program forever as it never reaches a false to stop the execution of program.

Some Assignment Operators:

Assignment: x = y, x = y;

Addition assignment: x += y, x = x + y;

Subtraction assignment: x -= y, x = x - y;

Multiplication assignment: x *= y, x = x* y;

Division assignment: x /= y, x = x / y;

Remainder assignment: x %= y, x = x % y;

Exponentiation assignment: `x **= y, x = x** y;`

Left shift assignment: x <<= y, x = x << y;

Right shift assignment: x >>= y, x = x >> y;

Unsigned right shift assignment: x >>>= y, x = x >>> y;

Bitwise AND assignment: x &= y, x = x & y;

Bitwise XOR assignment: x ^= y, x = x ^ y;

Bitwise OR assignment: x |= y, x = x | y;

Logical AND assignment: x &&= y, x && (x = y);

Logical OR assignment: x ||= y, x || (x = y);

Logical nullish assignment: x ??= y, x ?? (x = y);

**[Back](README.md)**