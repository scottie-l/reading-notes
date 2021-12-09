<b><a href = "https://reactjs.org/docs/forms.html">"Forms"</a>

1. What is a ‘Controlled Component’? A form that acts as setState and the form submission function making a React state a single source of truth and able to control its data.

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? When they submit the form, unless you specify.

Why? It's selected by value and changes, rather than the selection on the form.

3. How do we target what the user is entering if we have an event handler on an input field? You add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

HTML form elements work differently from other DOM elements in React, because form elements keep some internal state.

Default HTML form behavior of browsing to page when user submits form. If you want this behavior in React, it just works. In most cases, it’s convenient to have a JavaScript function that handles the submission of the form, and has access to data that user entered into the form. Standard way to achieve this is with technique called “controlled components”.

Controlled Components:

In HTML, form elements such as `<input>`, `<textarea>`, and `<select>` typically maintain their state and update based on user input. In React, mutable state is kept in state property of components, and only updated with setState(). Can combine the two by making React state be “single source of truth”. Then React component that renders form also controls what happens in form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

Since value attribute is set on form element, displayed value will be this.state.value, making React state the source of truth. Since handleChange runs on every keystroke to update React state, displayed value will update as user types.

With controlled component, input’s value is always driven by React state. You can now pass value to other UI elements too, or reset it from other event handlers.

The textarea Tag:

In HTML, a `<textarea>` element defines its text by its children. In React, `<textarea>` uses value attribute instead. This way, form using a <textarea> can be written very similarly to form that uses a single-line input.

The select Tag:

In HTML, `<select>` creates a drop-down list where you can select a value. React, uses value attribute on the root select tag. This is more convenient in controlled component because only need to update in one place. This makes it so that `<input type = "text">`, `<textarea>`, and `<select>` all work very similarly. They all accept value attribute that you use to implement controlled component.

Note: You can pass an array into the value attribute, allowing you to select multiple options in a select tag. Ex. `<select multiple = {true} value = {['B', 'C']}>`

The file input Tag:

In HTML, an `<input type = "file">` lets user choose one or more files from device storage to be uploaded to server or manipulated by JS via a File API.

Because its value is read-only, it's an uncontrolled component in React.

Handling Multiple Inputs:

When need to handle multiple controlled input elements, can add name attribute to each element and let handler function choose what to do based on value of event.target.name.

Since setState() automatically merges a partial state into the current state, we only needed to call it with the changed parts.

Controlled Input Null Value:

Specifying value prop on controlled component prevents user from changing input unless you desire. If you’ve specified value but input is still editable, you may have accidentally set value to undefined or null.

Alternatives to Controlled Components:

Can sometimes be tedious to use controlled components, because need to write event handler for every way data can change and pipe all input state through a React component. Can become annoying when converting preexisting codebase to React, or integrating React application with non-React library. Might want to check out uncontrolled components, alternative technique for implementing input forms.

<b><a href = "https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff">"The Conditional (Ternary) Operator Explained"</a>

1. Why would we use a ternary operator? To write a more succinct line of code to evaluate a condition using a Boolean value.

2. Rewrite the following statement using a ternary statement: x === y ? true : false;

  if(x === y){

 console.log(true);

  } else {

 console.log(false);

  }

Starting with the Basics — The if statement:

Using conditional, like if statement, allows us to specify certain block of code should be executed if certain condition is met. Consider the following example: We have a person object that consists of a name, age, and driver property.

We want to test age of our person is greater than or equal to 16. If true, they’re old enough to drive and driver should say 'Yes'. If not true, driver should be set to 'No'. We could use an if statement to accomplish this.

We could do same thing in one line of code.

person.driver = person.age > = 16 ? 'Yes' : 'No';

Shorter code yields us same result of person.driver = 'Yes';

The Conditional (Ternary) Operator:

First, we’ll take a look at the syntax of a typical if statement:

if ( condition ) {

  value if true;

} else {

  value if false;

}

Now, the ternary operator:

condition - ? value if true, : value if false

The condition is what you’re actually testing. Result of your condition should be true or false or at least coerce to either Boolean value.

A " ? " separates our conditional from our true value. Anything between the ? and the : is what is executed if condition evaluates to true.

A " : " colon, if your condition evaluates to false, any code after the colon is executed.

Most important thing to note order of operations. Lets add some parenthesis to help you visualize the order in which code is executing:

person.driver = ((person.age > = 16) ? 'Yes' : 'No';)

As you can now visualize, first thing that happens is conditional is checking to see if person.age > = 16 is true or false.

Since 20 is greater than 16, this evaluates to true. Here’s where we are now:

person.driver = (true ? 'Yes' : 'No';)

Since condition of our conditional is true, value between the ? and : is returned, 'Yes'. Now that we have our return value, final thing to do is to set it equal to our variable:

person.driver = 'Yes';

Example — Nested Ternary: What if a movie theater gives a discount to students and seniors? We can nest ternary operators to test multiple conditions.

For this scenario, assume tickets are: $12 for the general public, $8 for students, and $6 for seniors. Here’s what the code for a Senior citizen would look like:

let isStudent = false;

let isSenior = true;

let price = isStudent ? 8 : isSenior ? 6 : 10

console.log(price);

6

Code break down: First, check to see if patron is student. Since isStudent is false, only code after first : is executed. After the : , we have a new conditional. Our second conditional tests, isSenior. Since this is true, only code after the ? but before the : is executed. Price then assigned value of 6 which we later console log to screen.

Example — Multiple operations: Also possible to run multiple operations within ternary. To do, must separate operations with comma. Can also, optional, use parenthesis to help group code:

let isStudent = true;

let price = 12;

isStudent ? (

  price = 8,

  alert('Please check for student ID')

) : (

  alert('Enjoy the movie')

);

In above example, price of movie is set to $12. If isStudent is true, we adjust price down to $8 & send alert to cashier to check for student ID. If isStudent is false, above code is skipped, and simply alert to enjoy the movie.

<b><a href = "https://react-bootstrap.github.io/components/forms/">"React Bootstrap Forms"</a>

<b><a href = "https://reactjs.org/docs/conditional-rendering.html">"React Docs - Conditional Rendering"</a>

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
