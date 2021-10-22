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
  `render() {`
    `return (`
      `<button className="square">`
        `{/* TODO */}`
      `</button>`
    `);`
  `}`
`}`

`class Board extends React.Component {`
  `renderSquare(i) {`
    `return <Square />;`
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

The Square component renders a single `<button>` and the Board renders 9 squares. The Game component renders a board with placeholder values which we’ll modify later. There are currently no interactive components.







<b><a href = "https://reactjs.org/docs/hello-world.html">"React Docs - Hello world"</a>

<b><a href = "https://reactjs.org/docs/introducing-jsx.html">"React Docs - Introducing JSX"</a>

<b><a href = "https://reactjs.org/docs/rendering-elements.html">"React Docs - Rendering elements"</a>

<b><a href = "https://reactjs.org/docs/components-and-props.html">"React Docs - Components and props"</a>



<a href="https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
