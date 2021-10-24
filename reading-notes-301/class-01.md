<b><a href = "https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm">"Component based Architecture"</a>

What is a "Component"?

- Software object, intended to interact with other components, encapsulating certain functionality or set of functionalities.
- Can be defined as a unit of composition with contractually specififed interface and explicit context dependencies only.

What are the characteristics of a component?

- Modular & portable.
- Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.
- Replaceable − Components may be freely substituted with other similar components.
- Not context specific − Components are designed to operate in different environments and contexts.
- Extensible − Component can be extended from existing components to provide new behavior.
- Encapsulated − Component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.
- Independent − Components are designed to have minimal dependencies on other components.
- An obviously defined interface and conforms to a recommended behavior common to all components within the architecture.

What are the advantages of using a component-based arcitecture?

- Reduced time in market and the development cost by reusing existing components.
- Ease of deployment − As new compatible versions become available, it's easier to replace existing versions with no impact on other components or system as a whole.
- Reduced cost − Use of third-party components allows you to spread cost of development and maintenance.
- Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of system.
- Reusable − Use of reusable components means they can be used to spread the development and maintenance cost across several applications or systems.
- Modification of technical complexity − A component modifies the complexity through use of component container and its services.
- Reliability − Overall system reliability increases since the reliability of each individual component enhances reliability of whole system via reuse.
- System maintenance and evolution − Easy to change and update implementation without affecting rest of system.
- Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.

Focuses on decomposition of the design into individula functional or logical components that represent well defined communication interfaces containing methods events and properties.

Provides higher level of abstraction and divides the problem into subproblems.

Can have 3 different views:  

- Object oriented view: 1 or more cooperating classes. Each problem domain class and infrastructure class are explianed to id all attributes & operations that apply to its implementation. Also involves defining interfaces that enable classes to communicate and cooperate.
- Conventional view: It's viewed as functional element or module of program that integrates the processing logic, the internal data structures that are required to implement processing logic and interface that enables component to be invoked, and data to be passed to it.
- Process-related view: Instead of creating each component from scratch system is building from existing components maintained in library. As software architecture is formulated, components are selected from library and used to populate the architecture.
  - User interface component includes grids, buttons, referred as controls, and utility components expose a specific subset of functions used in other components.
  - Other common types of components are those that are resource intensive, not frequently accessed, and must be activated using the just-in-time (JIT) approach.
  - Many components are invisible, which are distributed in enterprise business applications and internet web applications, such as Enterprise JavaBean (EJB), .NET components, and CORBA components.

Principles of Component-based Design:

Component-level design can be represented by using some intermediary representation that can be translated into source code. Design of data structures, interfaces, and algorithms should conform to well-established guidelines to help avoid introduction of errors.

- Software system is decomposed into reusable, cohesive, and encapsulated component units.
- Each component has own interface that specifies required ports and provided ports; each component hides its detailed implementation.
- Component should be extended without the need to make internal code or design modifications to existing parts of component.
- Depend on abstractions component do not depend on other concrete components, which increase difficulty in expendability.
- Connectors connected components, specifying and ruling interaction among components. The interaction type is specified by interfaces of components.
- Components interaction can take form of method invocations, asynchronous invocations, broadcasting, message driven interactions, data stream communications, and other protocol specific interactions.
- For a server class, specialized interfaces should be created to serve major categories of clients. Only operations that are relevant to particular category of clients should be specified in interface.
- Component can extend to other components and still offer its own extension points. It is the concept of plug-in based architecture. This allows a plugin to offer another plugin API.

Design Guidelines:

Creates naming conventions for components that are specified as part of architectural model, then refines, or elaborates, as part of component-level model.

- Attains architectural component names from problem domain and ensures that they have meaning to all stakeholders who view architectural model.
- Extracts business process entities that can exist independently without any associated dependency on other entities.
- Recognizes and discover these independent entities as new components.
- Uses infrastructure component names that reflect their implementation-specific meaning.
- Models any dependencies from left to right and inheritance from top to bottom.
- Model any component dependencies as interfaces rather than representing them as direct component-to-component dependency.

Conducting Component-Level Design:

Recognizes all design classes that correspond to the problem domain as defined in analysis model and architectural model.

- Recognizes all design classes that correspond to the infrastructure domain.
- Describes all design classes that are not acquired as reusable components, and specifies message details.
- Identifies appropriate interfaces for each component and elaborates attributes, and defines data types and data structures, required to implement them.
- Describes processing flow within each operation, in detail, by means of pseudo code or UML activity diagrams.
- Describes persistent data sources and identifies the classes required to manage them.
- Develop and elaborates behavioral representations for class or component. Can be done by elaborating the UML state diagrams created for analysis model and by examining all use cases that are relevant to design class.
- Elaborates deployment diagrams to provide additional implementation detail.
- Demonstrates the location of key packages, or classes of components, in system by using class instances and designating specific hardware and operating system environment.
- Final decision made by using established design principles and guidelines. Experienced designers consider all of the alternative design solutions before settling on final design model.

<b><a href = "https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0">"What is Props and How to Use it in React"</a>

React is component-based library that divides UI into little reusable pieces. Those components need to communicate and the way to pass data between components is by using props.Furthermore, props data is read-only (immutable), which means that data coming from the parent should not be changed by child components.

What is "props" short for? “Props” is a special keyword in React, which stands for properties. Used for passing data from one component to another.

What is the flow of props? Data is being passed in uni-directional flow. One way, from parent to child.

How are props used in React? Step by step Ex.

1. Define an attribute and its value(data).

- We can assign attributes and values to HTML tags: `<a href="www.google.com">Click here to visit Google</a>`
- Can do same for React components. We can define our own attributes & assign values with interpolation { }: `<ChildComponent someAttribute={value} anotherAttribute={value}/>`
- Here, declaring a “text” attribute to ChildComponent, then assign string value: “I’m the 1st child”: `<ChildComponent text={“I’m the 1st child”} />`
- Now, ChildComponent has property and value. We need to pass it via Props.

2. Pass it to child component(s) by using Props.

- Passing props is like we pass arguments to a function; we pass props into a React component, and props bring all the necessary data.
- Arguments passed to a function:

`const addition = (firstNum, secondNum) => {`

  `return firstNum + secondNum;`

`};`

- Arguments passed to a React component:

`const ChildComponent = (props) => {`

 `return` `<p>I'm the 1st child!</p>;`

`};`

3. Render the Props Data.

- A prop is an Object; we will render the props object by using string interpolation: `{props}`
- In JavaScript, can access object elements with dot(.) notation. So we can render our text property with an interpolation:

`const ChildComponent = (props) => {`

  `return` `<p>{props.text}</p>;`

`};`

- Do the same for other child components:

`class ParentComponent extends Component {`

  `render() {`

    `return (`

      `<h1>`
        
        `I'm the parent component.`

        `<ChildComponent text={"I'm the 1st child"} />`

        `<ChildComponent text={"I'm the 2nd child"} />`

        `<ChildComponent text={"I'm the 3rd child"} />`

      `</h1>`

    `);`

  `}`

`}`

- Each ChildComponent will render its own prop data. This is how we use Props to pass data and convert static components into dynamic ones.

<b><a href = "https://reactjs.org/tutorial/tutorial.html">"React Tutorial" through ‘Passing Data Through Props’</a>

The normal render method returns description of what you want to see on screen, but the React takes description and displays result. In particular, render returns a "React element", which is lightweight description of what to render.

Most React devs use special syntax called “JSX” which makes these structures easier to write. You can put any JavaScript expressions within braces inside JSX. Each React element is a JavaScript object that you can store in a variable or pass around in your program.

You can compose and render custom React components. Ex. we can refer to the whole shopping list by writing `<ShoppingList />`. Each React component is encapsulated and can operate independently; this allows you to build complex UIs from simple components.

Building a Tic-Tac-Toe game: Starter code used from Reactjs.org

`class Square extends React.Component {`

C. First, we’ll add a constructor to the class to initialize the state:

  `constructor(props) {`

  `super(props);`

    `this.state = {`

        `value: null,`

    `};`

`}`

  `render() {`

    `return (`

B. Change the button tag that is returned from the Square component’s render() function to this:

      `<button className="square">` change to: `<button className = "square" onClick = {() => console.log('click')}>`

C. Replace this.props.value with this.state.value inside the `<button>` tag.

`<button className = "square" onClick = {() => console.log('click')}>` change to: 

`<button`

    className = "square"

    onClick = {() => this.setState({value: 'X'})}

`>`

    {this.state.value}

A. In Board’s renderSquare method, change the code to pass a prop called value to the Square:

        `{/* TODO */}` change to: `{this.props.value}

      `</button>`

    `);`

  `}`

`}`

`class Board extends React.Component {`

  `renderSquare(i) {`

A. In Board’s renderSquare method, change the code to pass a prop called value to the Square:

    `return <Square />;` change to: `return <Square value = {i} />;

  `}`

  `render() {`

    `const status = 'Next player: X';`

    `return (`
      `<div>`
        `<div className="status">{status}</div>`
        `<div className="board-row">`
          `{this.renderSquare(0)}`
          `{this.renderSquare(1)}`
          `{this.renderSquare(2)}`
        `</div>`
        `<div className="board-row">`
          `{this.renderSquare(3)}`
          `{this.renderSquare(4)}`
          `{this.renderSquare(5)}`
        `</div>`
        `<div className="board-row">`
          `{this.renderSquare(6)}`
          `{this.renderSquare(7)}`
          `{this.renderSquare(8)}`
        `</div>`
      `</div>`
    `);`
  `}`
`}`

`class Game extends React.Component {`
  `render() {`
    `return (`
      `<div className="game">`
        `<div className="game-board">`
          `<Board />`
        `</div>`
        `<div className="game-info">`
          `<div>{/* status */}</div>`
          `<ol>{/* TODO */}</ol>`
        `</div>`
      `</div>`
    `);`
  `}`
`}`

`========================================`

`ReactDOM.render(`

  `<Game />,`

  `document.getElementById('root')`

`);`

We have three React components:

- Square
- Board
- Game

The "Square" component renders a single `<button>` and the "Board" renders 9 squares. The "Game" component renders a board with placeholder values, which we’ll modify later. There are currently no interactive components.

To pass some data from our Board component to our Square component, see Ex. "A" above.

To make interactive, let’s fill the Square component with an “X” when we click it. See Ex. "B" above.

We want the Square component to “remember” that it got clicked, and fill it with an “X” mark. To “remember” things, components use state.

React components can have state by setting this.state in their constructors. this.state should be considered as private to a React component that it’s defined in. To store the current value of the Square in this.state, and change it when the Square is clicked, see Ex. "C" above. We’ll also change the Square’s render method to display the current state’s value when clicked. See Ex. "C" above.

The React Devtools extension for Chrome lets you inspect a React component tree with your browser’s developer tools. The React DevTools let you check the props and the state of your React components.

After installing React DevTools, can right-click on any element on page, click “Inspect” to open the developer tools, and the React tabs (“⚛️ Components” and “⚛️ Profiler”) will appear as the last tabs to the right. Use “⚛️ Components” to inspect the component tree.

<b><a href = "https://reactjs.org/docs/hello-world.html">"React Docs - Hello world"</a>

<b><a href = "https://reactjs.org/docs/introducing-jsx.html">"React Docs - Introducing JSX"</a>

JSX may remind you of a template language, but it comes with the full power of JavaScript. JSX produces React “elements”.

React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

You can put any valid JavaScript expression inside curly braces in JSX.

We split JSX over multiple lines for readability. It isn’t required, we also recommend wrapping it in parentheses to avoid the pitfalls of automatic semicolon insertion.

After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects. This means you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions.

You may use quotes to specify string literals as attributes. May also use curly braces to embed a JavaScript expression in an attribute.

Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute. You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute.

If a tag is empty, you may close it immediately with />, like XML. JSX tags may contain children.

It is safe to embed user input in JSX. By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.

Babel compiles JSX down to React.createElement() calls. These objects are called “React elements”. You can think of them as descriptions of what you want to see on the screen. React reads these objects and uses them to construct the DOM and keep it up to date.

<b><a href = "https://reactjs.org/docs/rendering-elements.html">"React Docs - Rendering elements"</a>

An element describes what you want to see on the screen. Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

Let’s say there is a `<div>` somewhere in your HTML file: We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like. To render a React element into a root DOM node, pass both to ReactDOM.render():

React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time. With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

Even though we create an element describing the whole UI tree on every tick, only the text node whose contents have changed gets updated by React DOM.

<b><a href = "https://reactjs.org/docs/components-and-props.html">"React Docs - Components and props"</a>

Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

The simplest way to define a component is to write a JavaScript function:

`function Welcome(props) {`

  `return <h1>Hello, {props.name}</h1>;`

`}`

This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

You can also use an ES6 class to define a component:

`class Welcome extends React.Component {`
  `render() {`
    `return <h1>Hello, {this.props.name}</h1>;`
  `}`
`}`

The above two components are equivalent from React’s point of view.

Previously, we only encountered React elements that represent DOM tags.

const element = `<div />;`

However, elements can also represent user-defined components.

const element = `<Welcome name="Sara" />;`

When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.

We call ReactDOM.render() with the `<Welcome name="Sara" />` element. React calls the Welcome component with {name: 'Sara'} as the props. Our Welcome component returns a `<h1>Hello, Sara</h1>` element as the result. React DOM efficiently updates the DOM to match `<h1>Hello, Sara</h1>`.

Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

Typically, new React apps have a single App component at the very top. However, if you integrate React into an existing app, you might start bottom-up with a small component like Button and gradually work your way to the top of the view hierarchy.

Don’t be afraid to split components into smaller components.

For example, consider this Comment component:

function Comment(props) {
  
  return (
  
    `<div className="Comment">`
  
      `<div className="UserInfo">`
  
        `<img className="Avatar"`
  
          src={props.author.avatarUrl}
  
          alt={props.author.name}
  
        />
  
        `<div className="UserInfo-name">`
  
          {props.author.name}
  
        `</div>`
  
      `</div>`
  
      `<div className="Comment-text">`
  
        {props.text}
  
      `</div>`
  
      `<div className="Comment-date">`
  
        {formatDate(props.date)}
  
      `</div>`
  
    `</div>`
  
  );

}

It accepts author (an object), text (a string), and date (a date) as props, and describes a comment on a social media website.

This component can be tricky to change because of all the nesting, and it is also hard to reuse individual parts of it. Let’s extract a few components from it. First, we will extract Avatar:

function Avatar(props) {
  
  return (

    <img className="Avatar"
    
      src={props.user.avatarUrl}
    
      alt={props.user.name}
    
    />

  );

}

The Avatar doesn’t need to know that it is being rendered inside a Comment. This is why we have given its prop a more generic name, user, rather than author.

We recommend naming props from the component’s own point of view rather than the context in which it is being used.

We can now simplify Comment a tiny bit:

function Comment(props) {
  
  return (
  
    <div className="Comment">
  
      <div className="UserInfo">
  
        <Avatar user={props.author} />
  
        <div className="UserInfo-name">
  
          {props.author.name}
  
        </div>
  
      </div>
  
      <div className="Comment-text">
  
        {props.text}
  
      </div>
  
      <div className="Comment-date">
  
        {formatDate(props.date)}
  
      </div>
  
    </div>
  
  );

}

Next, we will extract a UserInfo component that renders an Avatar next to the user’s name:

function UserInfo(props) {

  return (

    <div className="UserInfo">

      <Avatar user={props.user} />

      <div className="UserInfo-name">

        {props.user.name}

      </div>

    </div>

  );

}

This lets us simplify Comment even further:

function Comment(props) {

  return (

    <div className="Comment">

      <UserInfo user={props.author} />

      <div className="Comment-text">

        {props.text}

      </div>

      <div className="Comment-date">

        {formatDate(props.date)}

      </div>

    </div>

  );

}

A good rule of thumb is that if a part of your UI is used several times (Button, Panel, Avatar), or is complex enough on its own (App, FeedStory, Comment), it is a good candidate to be extracted to a separate component.

Whether you declare a component as a function or a class, it must never modify its own props.

Some functions are called “pure” because they do not attempt to change their inputs, and always return the same result for the same inputs.

React is pretty flexible but it has a single strict rule: All React components must act like pure functions with respect to their props.

<a href="https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
