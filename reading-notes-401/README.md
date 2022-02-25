# **Code 401 Reading-notes**

-  *All reading notes can be navigated to from here for code 401*

- # ***Table of Contents***

## **Daily Readings**

---
**[Day 00](Prep.md)**

- <a href = "https://simpleprogrammer.com/solving-problems-breaking-it-down/">"How to Solve Programming Problems"</a>
- <a href = "https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/">"How to think like a programmer"</a>
- <a href = "https://www.mindtools.com/pages/article/newTMC_5W.htm">"The 5 Whys"</a>

**[Day 01](class-01.md)**

- Describe what `Array.map()`, `Array.reduce()` does?
- Code snippets showing how to use superagent() to fetch data from a URL and log the result.
        - With normal Promise .then() syntax?
        - Again with async / await syntax?
- Explain promises as though you were mentoring a Code 301 level student?
- Are all callback functions considered to be Asynchronous? Why or Why Not?

**[Day 02](class-02.md)**

- What’s the difference between PUT and PATCH?
- Provide links to 3 services or tools that allow you to “mock” an API for development like json-server?
- Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?
- Compare and contrast SOAP and ReST?

- Document the following Vocabulary Terms:

  - Web Server
  - Express
  - Routing
  - WRRC

**[Day 03](class-03.md)**

- Name 3 real world use cases where you’d want to change the request with custom middleware?
- True or false: The route handler is middleware?
- In what ways can a middleware function end the process and send data to the browser?
- At what point in the request lifecycle can you “inject” middleware?
- What can cause express to error with “Request headers sent twice, cannot start a second response”?

- Document the following Vocabulary Terms:

  - Term
  - Middleware
  - Request Object
  - Response Object
  - Application Middleware
  - Routing Middleware
  - Test Driven Development
  - Behavioral Testing

**[Day 04](class-04.md)**

- Name 3 advantages to Test Driven Development?
- In what case would you need to use beforeEach() or afterEach() in a test suite?
- What is one downside of Test Driven Development?
- What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
- Why REST?

- Document the following Vocabulary Terms:

  - functional programming
  - object-oriented programming (OOP)
  - class
  - super
  - this
  - Test Driven Development (TDD)
  - Jest
  - Continuous Integration (CI)
  - REST
  - Data Model

**[Day 05](/class-05/class-05.md)**

*[Quiz](/class-05/quiz-05.md)*

- <a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html">"Big O: Analysis of Algorithm Efficiency, through “Linear Complexity Growth”"</a>

- <a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html">"Linked LIsts"</a>

- <a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d">"What's a Linked List Anyway pt. 1"</a>

- <a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996">"What's a Linked List Anyway pt. 2"</a>

**[Day 06](class-06.md)**

- Explain what a “Singleton” is (in Computer Science terms)?
- Explain how the Singleton pattern can be used with Node modules, specifically with classes?
- If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

- Document the following Vocabulary Terms:

  - Router Middleware
  - Dynamic Module Loading
  - Singleton Pattern
  - CRUD -> REST Method Matches
  - Mock Testing

**[Day 07](class-07.md)**

- Write the following steps in the correct order:

  - Register your application to get a client_id and client_secret
  - Ask the client if they want to sign in via a third party
  - Make a request to a third-party API endpoint
  - Receive access token
  - Receive authorization code
  - Make a request to the access token endpoint
  - Redirect to a third party authentication endpoint

- What can you do with an authorization code?
- What can you do with an access token?
- What’s a benefit of using OAuth instead of your own basic authentication?

- Document the following Vocabulary Terms:

  - Client ID
  - Client Secret
  - Authentication Endpoint
  - Access Token Endpoint
  - API Endpoint
  - Authorization Code
  - Access Token

**[Day 08](class-08.md)**

- When is Basic Authorization used vs. Bearer Authorization?
- What does the JSON Web Token package do?
- What considerations should we make when creating and storing a SECRET?

- Document the following Vocabulary Terms:

  - encryption
  - token
  - bearer
  - secret
  - JSON Web Token

**[Day 09](class-09.md)**

- What header(s) are used in authentication and authorization?
- What is safe to put into a JWT?
- How are JWTs validated?

- Document the following Vocabulary Terms:

  - RBAC
  - User Roles
  - JWT Token

**[Day 10](/class-10/class-10.md)**

*[Quiz](/class-10/quiz-10.md)*

- Stacks and Queues

**[Day 11](class-11.md)**

- Why is access control important?
- Describe an application that would need access control?
- What is a role used for?
- Why is role based access control more scalable than discretionary or mandatory access control?

- Document the following Vocabulary Terms:

  - Authorization
  - Role Based Access Control
  - Capabilities

**[Day 12](class-12.md)**

- What is the benefit of transforming data into packets?
- UDP is often refereed to as a connectionless protocol. Why is this?
- Can a socket server application have multiple socket connections?
- Can a socket connection application be connected to multiple socket servers?
- Can an application be both a socket server and a socket connection?

- Document the following Vocabulary Terms:

  - Observer Pattern
  - Listener
  - Event Handler
  - Event Driven Programming
  - Event Loop
  - Event Queue
  - Call Stack
  - Emit/Raise/Trigger
  - Subscribe
  - Database

**[Day 13](class-13.md)**

- What does it mean that web sockets are bidirectional? Why is this useful?
- Does socket.io use HTTP? Why?
- What happens when a client emits an event?
- What happens when a server emits an event?
- What happens if a client “misses” an event?
- How can we mitigate this?

- Document the following Vocabulary Terms:

  - Socket
  - Web Socket
  - Socket.io
  - Client
  - Server
  - OSI Model
  - TCP Model
  - TCP
  - UDP
  - Packets

**[Day 14](class-14.md)**

- What’s the difference between a FIFO and a standard queue?
- How can the server be assured a message was properly received?
- What classic design pattern is best represented by event driven programming?
- How do you test an event driven system?

- Document the following Vocabulary Terms:

  - FIFO Queue
  - Pub/Sub

**[Day 15](/class-15/class-15.md)**

*[Quiz](/class-15/quiz-15.md)*

- Binary Trees, Binary Search Trees, & K-ary Trees.

**[Day 16](class-16.md)**

- Describe the Web-Request-Response-Cycle?
- Explain what a “server” is, as it relates to the WRRC?
- What does it mean to “deploy” an application?

- Document the following Vocabulary Terms:

  - Server
  - Pub/Sub
  - WRRC

**[Day 17](class-17.md)**

- Describe “The Cloud”?
- What is a container (as it relates to computers and servers)?
- What is auto-scaling?
- What is bandwidth?
- How do cloud providers compute service costs?

- Document the following Vocabulary Terms:

  - Server Instances
  - Containers
  - Cloud Services
  - Cloud Architecture
  - AWS
  - EC2/Beanstalk vs Heroku

**[Day 18](class-18)**

- Describe a use case for a serverless function?
- If you were to create a system that emulated Lambda functions, how would you do it?
- Describe how a CDN works?

- Document the following Vocabulary Terms:

  - Serverless Functions
  - Cloud Storage
  - CDN

**[Day 19](class-19.md)**

- Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server?
- List the AWS Database offerings and talk about the pros and cons of each?
- What’s the difference between a FIFO and a standard queue?
- How can the server be assured a message was properly received?

- Document the following Vocabulary Terms:

  - Serverless API
  - Triggers
  - Dynamo vs Mongo
  - Dynamoose vs Mongoose

**[Day 20](class-20.md)**

- Name 5 Javascript UI Frameworks (other than React)
- What’s the difference between a framework and a library?

- Document the following Vocabulary Terms:

  - Rendering
  - Templates
  - State

**[Day 21](class-21.md)**

- How does React differ from vanilla JS/HTML/CSS?
- What is the primary difference between a function component and a class component?

- Document the following Vocabulary Terms:

  - Functional Components
  - Children / Child Components

**[Day 22](class-22.md)**

- Why do we not need more .html pages in a multi-page React app?
- If we wanted a component to show up on every page, where would we put it and why?

  - Outside the `<BrowserRouter/>`?
  - Inside the `<BrowserRouter />`, outside a `<Route />`?
  - Inside a `<Route />`?

- What does routing do with the components that were rendered when a new route is requested?
- What does props.children contain?
- How do useState() and this.setState() differ?

- Document the following Vocabulary Terms:

  - State Hook
  - Mounting and Un-Mounting

**[Day 23](class-23.md)**

- How can we ensure that an effect hook runs only once?
- Can useState() update more than one state variable at the same time?
- Is useState() synchronous?

- Document the following Vocabulary Terms:

  - State Hook
  - Component Lifecycle

**[Day 24](/class-24/class-24.md)**

*[Quiz](/class-24/quiz-24.md)*

- <a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html">Intro to Hash Tables</a>

- <a href = "https://www.youtube.com/watch?v=MfhjkfocRR0">What is a Hash table?</a>

- <a href = "https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/">Basics of Hash Tables</a>

- <a href = "https://en.wikipedia.org/wiki/Hash_table">Hash Table Wiki</a>

**[Day 25](class-25.md)**

- Describe use cases useState() vs useReducer()
- Why do custom hooks need the use prefix?
- What do custom hooks usually do?
- Using any list of custom hooks, research and name one that you think will be useful in your applications?
- Describe how a hook that fetches API data might work?

- Document the following Vocabulary Terms:

  - reducer

**[Day 26](class-26.md)**

- When you have multiple contexts, what component type should you use (class/function) and why?
- What are some good use cases for using the Context API for global state?
- How can you best test context?

- Document the following Vocabulary Terms:

  - context
  - useContext()
  - static context

**[Day 27](class-27.md)**

- Why is the Context API useful?
- Can a component outside of a provider get its context?
- What are some common use cases for using the Context API?
- Describe “Context Hell”?

- Document the following Vocabulary Terms:

  - global state
  - global context
  - provider
  - consumer

**[Day 28](class-28.md)**

- How do bearer tokens work?
- Describe express middleware?
- What is a JWT?

- Document the following Vocabulary Terms:

  - role based access control
  - http cookies
  
**[Day 29](/class-29/class-29.md)**

*[Quiz](/class-29/quiz-29.md)*

**[Day 30](/class-30.md)**

- What are the advantages of storing tokens in “Cookies” vs “Local Storage”
- Explain 3rd party cookies.
- How do pixel tags work?

- Document the following Vocabulary Terms:

  - cookies
  - authorization
  - access control
  - conditional rendering

---
**<a href = "https://github.com/scottie-l/reading-notes">Back</a>**

---
<!-- EOF -->
