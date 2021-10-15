<a href="https://github.com/codefellows/domain_modeling#domain-modeling">"Domain Modeling"</a>

Domain modeling is process of creating a model, in code, for a specific problem. Model describes the various entities, attributes & behaviors, as well as the constraints that govern the problem domain. Entity that stores data in properties, and encapsulates the behaviors in methods, is commonly referred to as an object-oriented model. A good domain model can verify and validate the understanding of a specific problem among various stakeholders. It can define vocabulary that can be used within & between both technical and business teams.

Research to find essential metrics. Then use those to build self-contained objects with same attributes and behaviors.

Constructor function defined using function expression. Variable declared, and then assigned a functin with 2 parameters. When called, data inside these parameters is stored inside the two variables. This can now be referenced later. After the constructor function definition, 2 objects are instantiated with the 'new' keyword and properties are initialized by calling the constructor function. After instantized and initialized, objects are stored inside the variables.

Object-oriented programming in JavaScript at its most fundamental level. 1- The new keyword instantiates 'creates' an object. Constructor function initializes the properties inside the object using the '.this' variable. Object is now stored in variable for later use.

Summary (Copied from Codefellows, "Domain Modeling" link):

Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

Here's some tips to follow when building your own domain models.

1- When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.

2- Model its attributes with a constructor function that defines and initializes properties.

3- Model its behaviors with small methods that focus on doing one job well.

4- Create instances using the new keyword followed by a call to a constructor function.

5- Store the newly created object in a variable so you can access its properties and methods from outside.

6- Use the this variable within methods so you can access the object's properties and methods from inside.

<b>Ch.6 "Tables"

`<table>`= used to create a table

`<tr>`= table row, used to start new row

`<td>`= Table data, used to enter the data into the table

`<th>`= Table heading, Use like `<td>`

Use colspan to span more than 1 cell

Use rowspan to span more than 1 cell

`<thead>`= Used for screen readers and are inside the header element

`<tbody>`= Used for screen readers and are inside the body element

`<tfoot>`= Used for screen readers and are inside the footer element

<b>Ch.3 "Functions and Methods"

Creating object using constructor notation= var hotel = new Object()

                                            hotel.name= 'Quay';

Hotel is object, name is the key, and Quay is the value.

Can use dot notation or [].

Creating many objects:

Make function= function Hotel(name, rooms, booked) {
    this.name= name;
    this.rooms= rooms;
    this.booked= booked;
} this.name, rooms and booked are the key, and values follow.

Constructor functions usually start with a capital letter.

Object created on 1st line of code. Properties & methods then added after.

Literal Notation- colon separates key/value pairs. Commas between each key/value pair.

Objectg constructor Notation- Used to create multiple objects. The 'this' keyword is used instead of objects name

In JS, data represented using name/value pairs.

To organize data, can use array or object to group set of relative values. Arrays/Objects, name is known as key.

Variable= 1 key/1 value

Array= Store multiple information. Each piece separated by a comma. Order is important because indexed.

Individual Objects= Objects store sets of name/value pairs. Can be properties or methods.

Multiple Objects= Use object constructor to provide template, then create instances of object using new keyword, then call to constructor function

Arrays are objects. Can combine arrays and objects.

Browser Object Model= creates model of browser tab or window (Ref. on pg 124, Jon Duckett, JavaScript & JQuery.)

Document Object model= creates model of current web page (Ref. on pg 126, Jon Duckett, JavaScript & JQuery.)

Global JavaScript Objects= group of individual objects that relate to different parts of JS language (Ref. on pg 128, Jon Duckett, JavaScript & JQuery.)

6th data type= Object

Global Object Strings=  strings (Ref. on pg 129, Jon Duckett, JavaScript & JQuery.)

                        numbers (Ref. on pg 132, Jon Duckett, JavaScript & JQuery.)

                        math objects (Ref. on pg 134, Jon Duckett, JavaScript & JQuery.)

                        date & time (Ref. on pg 137, Jon Duckett, JavaScript & JQuery.)

<a href="https://github.com/scottie-l/Reading-notes-201">Back</a>