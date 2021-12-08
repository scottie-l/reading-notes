<b><a href = "https://reactjs.org/docs/lists-and-keys.html">"Lists and Keys"</a>

1. What does .map() return? Items in an array.

2. If I want to loop through an array and display each value in JSX, how do I do that in React? We loop through the array using the JavaScript .map() function.

3. Each list item needs a unique? "Key".

4. What is the purpose of a key? Keys help React identify which items have changed, are added, or are removed.

Given code below, we use map() to take array of numbers and double values. We assign the new array, returned by map(), to variable doubled and log it:

const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map((number) => number * 2);

console.log(doubled);

This code logs [2, 4, 6, 8, 10] to the console.

In React, transforming arrays into lists of elements is identical.

Rendering Multiple Components: You can build collections of elements and include them in JSX using the curly braces {}.

We can loop through the numbers array using the JavaScript map() function. We'll return `<li>` element for each item. Then we'll assign resulting array to listItems

const numbers = [1, 2, 3, 4, 5];

const listItems = numbers.map((number) =>

 `<li>{number}</li>`

);

Must be sure to include listItems array inside a `<ul>` element, to render to the DOM:

ReactDOM.render(

  `<ul>{listItems}</ul>`,

  document.getElementById('root')

);

const numbers = [1, 2, 3, 4, 5];

ReactDOM.render(

  `<NumberList numbers={numbers} />`,

  document.getElementById('root')

);

When you run code above, you’ll be given warning that key should be provided for list items. A “key” is special string attribute needed to include when creating lists of elements. Let’s assign a key to our list items inside numbers.map() and fix the missing key issue.

function NumberList(props) {

  const numbers = props.numbers;

  const listItems = numbers.map((number) =>

    <li key={number.toString()}>

      {number}

    </li>

  );

  return (

    <ul>{listItems}</ul>

  );

}

const numbers = [1, 2, 3, 4, 5];

ReactDOM.render(

  `<NumberList numbers={numbers} />`,

  document.getElementById('root')

);

Keys: Keys help React identify which items have changed, added, or removed. Keys should be given to elements inside array to give elements stable identity. Best way to pick key is use a string that uniquely identifies list item among its siblings. Most often you would use IDs from your data as keys. When you don’t have a stable ID for rendered items, you may use item index as key as last resort:

It is not recommended to use indexes for keys if order of items may change. This can negatively impact performance and may cause issues with component state. If you choose not to assign explicit key to list items, then React will default to using indexes as keys.

Extracting Components with Keys:

Keys only make sense in context of surrounding array. Ex. you extract a ListItem component, you should keep the key on `<ListItem />` elements in the array rather than on `<li>` element in ListItem itself.

Good rule of thumb is elements inside map() call need keys. Keys must only be unique among siblings. Keys used within arrays should be unique among their siblings. However, they don’t need to be globally unique. Can use same keys and produce two different arrays.

Keys serve as hint to React, but don’t get passed to components. If you need same value in component, pass it explicitly as prop with different name.

const content = posts.map((post) =>

  `<Post`

    key={post.id}

    id={post.id}

    title={post.title} />

);

With example above, Post component can read props.id, but not props.key.

Embedding map() in JSX: JSX allows embedding any expression in curly braces so we could inline the map() result. Sometimes this results in clearer code, but style can also be abused. Keep in mind that if the map() body is too nested, it might be a good time to extract a component.

<b><a href = "https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab">"The Spread operator"</a>

1. What is the spread operator? The spread operator is useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

2. List 4 things that the spread operator can do? Copying an array, using Math functions, adding an item to a list, combining objects.

3. Give an example of using the spread operator to combine two arrays?

const myArray = [`crazyFace`,`bear`,`flags`]

const yourArray = [`smiley`,`joy`,`love`]

const ourArray = [...myArray,...yourArray]

console.log(...ourArray) crazyFace bear flags smiley joy love

4. Give an example of using the spread operator to add a new item to an array?
const fewFruit = ['apple','orange','banana']

const fewMoreFruit = ['watermelon', 'pineapple', ...fewFruit]

console.log(fewMoreFruit) Array(5) ["watermelon", "pineapple", "apple", "orange", "banana"]

5. Give an example of using the spread operator to combine two objects into one?
const objectOne = {hello}

const objectTwo = {world}

const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}

const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}

objectFour.laugh() 😂😂😂😂😂

How to Use the Spread Operator (…) in JavaScript: The spread operator is useful and quick syntax for adding items arrays, combining arrays or objects, and spreading array out into function’s arguments.

What is the spread operator? InJavaScript, spread syntax refers to use of an ellipsis of three dots " … " to expand iterable object into list of arguments. When ...arr is used for function call, it ‘expands’ iterable object "arr" into list of arguments.

Spread operator added to JavaScript in ES6.

What is ... used for? Looks similar to rest parameters, also using ..., but does the opposite.

To pass array to JavaScript function expecting separate arguments doesn't work. It produces a NaN result. Use " … " spread syntax “spreads” array into separate arguments.

What else can … do? The … spread operator is useful for many different tasks in JS. Copying an array, concatenating or combining arrays, using math functions, using an array as arguments, adding item to list, adding to state in React, combining objects, converting NodeList to an array.

In each case, spread syntax expands iterable object, usually array, though it can be used on any interable, including a string.

Concatenating arrays: The spread operator can quickly combine two arrays, an operation known as array concatenation.

Using Math functions: One of the best ways to understand use of spread operator in JavaScript is to look at built-in functions Math.min() and Math.max(), which both expect a list of arguments, not an array.

Using an array as arguments: Since spread operator “spreads” array into different arguments, any functions that accepts multiple any number of arguments can benefit from use spread operator.

Adding an item to a list: The spread operator can add item to another array with easy-to-understand syntax:

Adding to state in React: Adding item to array in React state is easily accomplished using spread operator.

Combining objects: Spread syntax is useful for combining properties and methods on objects into new object.

Converting NodeList to Array: The spread operator can convert NodeList and arguments objects to arrays.

The spread operator and older browsers: When programming to support Internet Explorer and browsers on older mobile devices, spread operator is NOT going to work. The function Function.prototype.apply() will have the same effect as the spread syntax. Another option would be using the tool Babel to compile JavaScript code along with plugin babel-plugin-transform-spread.

One of the benefits of using spread operator is it will create new reference to its primitive values, copying them. That means that changes to original array will not affect the copied array, which is what would happen if array had been linked to original with assignment operator =: .

Watch out for the deeply-nested Gotcha! When JavaScript objects, including arrays, are deeply nested, spread operator only copies first level with new reference, but deeper values are still linked together. This problem called "creating a deep copy". Deep copies can be made using lodash or R.clone() method from the Ramda functional programming library.

Conclusion: Spread operator can expand another item by splitting an iterable element like string or array into individual elements. The spread operator … is useful for working with arrays and objects in JS.

<b><a href = "https://www.youtube.com/watch?v=c05OL7XbwXU">"How to pass Functions Between Components"</a>

1. In the video, what is the first step that the developer does to pass functions between components? Creates a increment function to loop through array and update it.

2. In your own words, what does the increment function do? It is used to loop through array and search for the person that matches the input.

3. How can you pass a method from a parent component into a child component? Use the increment function using the this.setState({people: ppl}) in this case to loop through array and update.

4. How does the child component invoke a method that was passed to it from a parent component? Pass the increment function to the child, using this.props.increment(this.props.name)

<b><a href = "https://reactjs.org/tutorial/tutorial.html">"Reasct Docs - Declaring a Winner"</a>

<b><a href = "https://reactjs.org/docs/lifting-state-up.html">"React Docs - Lifting State Up"</a>

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
