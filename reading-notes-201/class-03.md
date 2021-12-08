<b>Ch.3 "Lists"

<ol> ordered list, and uses numbers & <ul> is unordered list and uses bullets

<li> list items & contained within the list tags.

<dl> definition list.

<dt> used to contain term being defined & <dd> used to contain the definition. Both tags are within the <dl> tag

Lists are indented by default. Lists can also be nested inside other lists & will indent further.


<b>Ch.13 "Boxes"

By default, box is sized just big enough to hold contents.

Set dimensions using pixels, %, or ems.

% = size of box based on size of browser window.

ems = size of box based on size of text within.

min-width, max-width, min-height, max-height can also be used to set box.

Overflow tells browser what to do with content within box that is larger than box itself. Can have 2 values.

hidden= hides content that doesn't fit in box.

scroll= adds sidebar to box.

Borders:

border-width= controls width of border.

border-style= how border line looks. Can be solid, dotted, dashed, double, groove, ridge, inset, outset, hidden, none

border-color= changes color of border line.

Padding= space between contents of element & its border.

Margin= the gap between boxes

Use text-align to center, right, left contents

Change display using:

inline= contents act as inline block

block= contents act as block line

inline-block= contents flow like inline block but retain some block level.

none= hides element from page.

Visibility- hides boxes but leaves space where they should be. Can have 2 values. Hidden, which hides contents & Visible, which shows element.

Border-image & Border-shadow (Ref. on pg 320, Jon Duckett, HTML & CSS.)

Border-radius used to round corners on boxes, or make circles. Ref. on pg 321-322, Jon Duckett, HTML & CSS.

<b>Ch.2 review

Arrays store multiple variables. Consider using with lists, or a set of values related to each other.

Create arrays same as variables. Values sit inside [ ] and are separated with commas. They can be any data type and mixed.

Each item in an array is given a number. It starts at <b>0 not 1.

<b>Ch.4 "Decisions & Loops"

if else= if the 1st code block meets the if statement, code executes, otherwise it goes to else statement and executes that code block.

Switch= starts with variable called switch value. Each case indicates possible value for variable & code. It should execute if values match. Entire statement lives in 1 code block, separated by colon and break; @ the end of each line of code to execute.

Falsey values= treated as false, or 0.

Truthy values= treated as true, or 1. Arrays are often truthy.

Logic operators are processed from left to right & stop @ result, but will return a value it stopped at.

Loops check a condition, if returns true, it will run again & if still true, will run again until false. Can get an infinite loop, which run forever, breaking your code. Abort on infinite loops!

Common Loops are:

For= used to run a code a specific number of times.

While= will continue to run until false.

Do while= like a while loop, but will run condition at least once more if evaluates to false.

For loops= Initialize: create a variable & set to 0

            Condition: loop runs until condition (counter) is met.

            Update: each time code runs, it adds 1 to the counter.

Keywords for loops:

        break; causes termination of loop

        continue; stop iteration, update & check condition again.

<a href = "https://github.com/scottie-l/reading-notes/blob/main/reading-notes-201/README.md">Back</a>
