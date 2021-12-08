<b><a href = "https://reactjs.org/docs/thinking-in-react.html">"Thinking in React"</a>

1. What is the single responsibility principle and how does it apply to components? A component should ideally only do one thing. It if it grows, it should be decomposed into smaller sub components. Each component should match 1 piece of your data model.

2. What does it mean to build a ‘static’ version of your application?  A build version that takes your data model and renders it to UI but has no interactivity.

3. Once you have a static application, what do you need to add? All build components that reuse other components and pass data using props. Then render using ReactDOM.render().

4. What are the three questions you can ask to determine if something is state?

- Is it passed in from a parent via props?
- Does it remain unchanged over time?
- Can you compute it based on any other state or props in your component?

5. How can you identify where state needs to live?

- Identify every component that renders something based on that state.
- Find common owner component (single component above all components that need state in hierarchy).
- Either the common owner or another component higher up in the hierarchy should own the state.

Start With A Mock: Imagine that we already have a JSON API and a mockup from our designer. Our JSON API returns some data that looks like this:

[

  {category: "Sporting Goods", price: "$49.99", stocked: true, name: "Football"},

  {category: "Sporting Goods", price: "$9.99", stocked: true, name: "Baseball"},

  {category: "Sporting Goods", price: "$29.99", stocked: false, name: "Basketball"},

  {category: "Electronics", price: "$99.99", stocked: true, name: "iPod Touch"},

  {category: "Electronics", price: "$399.99", stocked: false, name: "iPhone 5"},

  {category: "Electronics", price: "$199.99", stocked: true, name: "Nexus 7"}

];

`1. Breaking The UI Into A Component Hierarchy:

First thing you’ll need to do is draw boxes around every component in mock and give them all names. But how do you know what should be its own component? Use same techniques for deciding if should create new function or object. One such technique is the single responsibility principle: a component should ideally only do one thing. If it grows, should be decomposed into smaller subcomponents.

Since often displaying a JSON data model to user, you’ll find that if model was built correctly, UI will map. That’s because UI and data models tend to adhere to same information architecture. Separate your UI into components, where each component matches 1 piece of data model.

Diagram showing nesting of components: Say we have five components in our app.

FilterableProductTable (orange): contains the entirety of the example.

SearchBar (blue): receives all user input.

ProductTable (green): displays and filters the data collection based on user input.

ProductCategoryRow (turquoise): displays a heading for each category.

ProductRow (red): displays a row for each product.

ProductTabl: the table header, containing “Name” and “Price” labels, isn’t its own component. This is matter of preference. It's part of ProductTable because it is part of rendering the data collection which is ProductTable’s responsibility. However, if this header grows to be complex, would certainly make sense to make it its own ProductTableHeader component.

Now that we’ve identified components in our mockup, we can arrange them into a hierarchy. Components that appear within another component in mockup should appear as child the hierarchy:

FilterableProductTable

SearchBar

ProductTable
    - ProductCategoryRow
    - ProductRow

`2. Build A Static Version in React

We have component hierarchy, now time to implement app. Easiest way is to build version that takes data model and renders UI but has no interactivity. Best to decouple processes, because building static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing.

To build static version of app that renders data model, we’ll want to build components that reuse other components and pass data using props. Props are way of passing data from parent to child. If familiar with the concept of state; don’t use state at all to build static version. State is reserved only for interactivity, or data that changes over time.

Can build top-down or bottom-up. Meaning, can either start with building components higher up hierarchy, or with ones lower in it. On smaller projects, it’s usually easier to go top-down, and on larger projects, easier to go bottom-up and write tests as you build.

At end of step, have library of reusable components that render data model. The components will only have render() methods since this is static version of app. The component at the top of the hierarchy will take data model as prop. If make a change to underlying data model and call ReactDOM.render() again, UI will be updated. Can see how UI is updated and where to make changes. React’s one-way data flow keeps everything modular and fast.

A Brief Interlude - Props vs State: There are two types of “model” data in React: props and state. Important to understand distinction between two.

`3. Identify Minimal Representation Of UI State: To make UI interactive, need to be able to trigger changes to underlying data model. React achieves this with state.

To build your app correctly, first need to think of minimal set of mutable state that app needs. Key here is DRY: Don’t Repeat Yourself. Figure out absolute minimal representation of state your application needs, and compute everything else you need on-demand. Ex. if you’re building a TODO list, keep array of TODO items around; don’t keep separate state variable for count. Instead, you want to render the TODO count, take the length of the TODO items array.

Think of all pieces of data in example application. We have: The original list of products. The search text the user has entered. The value of the checkbox. The filtered list of products. Let’s go through each one and figure out which one is state.

Ask three questions about each piece of data:

1. Is it passed in from a parent via props? If so, it probably isn’t state.

2. Does it remain unchanged over time? If so, it probably isn’t state.

3. Can you compute it based on any other state or props in your component? If so, it isn’t state.

Original list of products is passed as props, so not state. Search text and checkbox seem to be state, since they change over time, and can’t be computed from anything. Finally, filtered list of products isn’t state because it can be computed by combining original list of products with search text and value of checkbox.

Finally, our state is: The search text the user has entered & the value of checkbox.

`4. Identify Where Your State Should Live: Need to identify which component mutates, or owns, this state. Remember: React is all about one-way data flow down component hierarchy.

Follow these steps to figure it out - for each piece of state in application:

1. Identify every component that renders something based on that state.

2. Find common owner component (single component above all components that need state in hierarchy). Either the common owner or another component higher up in the hierarchy should own the state.

If can’t find component where it makes sense to own state, create new component solely for holding state and add somewhere in hierarchy above common owner component.

Run down of application: ProductTable needs to filter product list based on state, and SearchBar needs to display search text, checked state. Common owner component is FilterableProductTable. It makes sense for filter text and checked value to live in FilterableProductTable.

Add instance property this.state = {filterText: '', inStockOnly: false} to FilterableProductTable’s constructor to reflect initial state of application. Then, pass filterText and inStockOnly to ProductTable and SearchBar as prop. Finally, use these props to filter rows in ProductTable and set values of form fields in SearchBar. Set filterText to "ball" and refresh app. The data table is updated.

`5. Add Inverse Data Flow: the form components deep in the hierarchy need to update the state in FilterableProductTable. React makes data flow explicit to help you understand how program works, but require more typing than traditional two-way data binding. If try to type or check box in previous version of example, you’ll see that React ignores input. This is intentional. Set the value prop of input to always be equal to state passed in from FilterableProductTable.

Want to make sure that whenever user changes form, we update state to reflect user input. Since components should only update own state, FilterableProductTable will pass callbacks to SearchBar that will fire whenever state should be updated. Can use onChange event on inputs to be notified of. Callbacks passed by FilterableProductTable will call setState(), and app will be updated.

<b><a href = "https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK">"Higher Order Functions"</a>

1. What is a “higher-order function”? Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing? Evaluating if m is less than n.

3. Explain how either map or reduce operates, with regards to higher-order functions? The first function builds array by applying function to all its elements from returned data. Another function uses this newly created array to apply its function to all elements and use its returned data for another function.

Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.

Higher-order functions allow us to abstract over actions, not just values. Come in several forms. For example, we can have functions that create new functions.

Script data set: One area where higher-order functions shine is data processing. Unicode from Chapter 1, the system that assigns a number to each character in written language. The standard contains 140 different scripts—81 are still in use today, and 59 are historic.

Filtering arrays: To find scripts in data set that are still in use, following function might be helpful. Filters out elements in array that don’t pass test.

function filter(array, test) {

  let passed = [];

  for (let element of array) {

    if (test(element)) {

      passed.push(element);

    }

  }

  return passed;

}

console.log(filter(SCRIPTS, script => script.living));

// → [{name: "Adlam", …}, …]

Function uses argument named test, a function value, to fill gap in computation. Process of deciding which elements to collect.

Note how filter function, rather than deleting elements from existing array, builds up new array with only elements that pass test. It does not modify the array it is given.

Like forEach, filter is standard array method.

Transforming with map: Say we have array of objects representing scripts. But we want an array of names, which is easier to inspect. The map method transforms array by applying function to all of its elements and building new array from returned values. New array will have the same length as input array, but content will have been mapped to new form the function. Like forEach and filter, map is a standard array method.

function map(array, transform) {

  let mapped = [];

  for (let element of array) {

    mapped.push(transform(element));

  }

  return mapped;

}

Summarizing with reduce: Another common thing to do with arrays is compute single value from them. Higher-order operation that represents this pattern called reduce (also called fold sometimes). Builds value by repeatedly taking single element from array and combining with current value. When summing numbers, you’d start with number zero and, for each element, add that to sum.

Parameters to reduce are, apart from the array, a combining function and start value. Function is a less straightforward than filter and map.

function reduce(array, combine, start) {

  let current = start;

  for (let element of array) {

    current = combine(current, element);

  }

  return current;

}

console.log(reduce([1, 2, 3, 4], (a, b) => a + b, 0));

// → 10

The standard array method reduce, has added convenience. If array contains at least one element, are allowed to leave off the starting argument. The method will take the first element of array as its start value and start reducing at second element.

console.log([1, 2, 3, 4].reduce((a, b) => a + b));

// → 10

To use reduce, twice, to find the script with most characters.

function characterCount(script) {

  return script.ranges.reduce((count, [from, to]) => {

    return count + (to - from);

  }, 0);

}

console.log(SCRIPTS.reduce((a, b) => {

  return characterCount(a) < characterCount(b) ? b : a;

}));

// → {name: "Han", …}

CharacterCount function reduces ranges assigned to a script by summing their sizes. Second call to reduce then uses this to find largest script by repeatedly comparing two scripts and returning larger one.

The Han script has more than 89,000 characters assigned to it in the Unicode standard, making it by far the biggest writing system in the data set. Han is a script (sometimes) used for Chinese, Japanese, and Korean text. Those languages share a lot of characters, though they tend to write them differently. The (U.S.-based) Unicode Consortium decided to treat them as a single writing system to save character codes. This is called Han unification and still makes some people very angry.

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
