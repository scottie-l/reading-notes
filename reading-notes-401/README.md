# Code 401 Reading-notes

### All reading notes can be navigated to from here for code 401

## ***Table of Contents***

**Daily Readings**

0. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/Prep.md">**Day 0**</a>

- <a href = "https://simpleprogrammer.com/solving-problems-breaking-it-down/">"How to Solve Programming Problems"</a>
- <a href = "https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2/">"How to think like a programmer"</a>
- <a href = "https://www.mindtools.com/pages/article/newTMC_5W.htm">"The 5 Whys"</a>

1. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-01.md">**Day 1**</a>

- Describe what `Array.map()`, `Array.reduce()` does?
- Code snippets showing how to use superagent() to fetch data from a URL and log the result.
        - With normal Promise .then() syntax?
        - Again with async / await syntax?
- Explain promises as though you were mentoring a Code 301 level student?
- Are all callback functions considered to be Asynchronous? Why or Why Not?

2. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-02.md">**Day 2**</a>

- What’s the difference between PUT and PATCH?
- Provide links to 3 services or tools that allow you to “mock” an API for development like json-server?
- Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?
- Compare and contrast SOAP and ReST?

Document the following Vocabulary Terms:

- Web Server
- Express
- Routing
- WRRC

3. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-03.md">**Day 3**</a>

- Name 3 real world use cases where you’d want to change the request with custom middleware?
- True or false: The route handler is middleware?
- In what ways can a middleware function end the process and send data to the browser?
- At what point in the request lifecycle can you “inject” middleware?
- What can cause express to error with “Request headers sent twice, cannot start a second response”?

Document the following Vocabulary Terms:

- Term
- Middleware
- Request Object
- Response Object
- Application Middleware
- Routing Middleware
- Test Driven Development
- Behavioral Testing

4. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-04.md">**Day 4**</a>

- Name 3 advantages to Test Driven Development?
- In what case would you need to use beforeEach() or afterEach() in a test suite?
- What is one downside of Test Driven Development?
- What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
- Why REST?

Document the following Vocabulary Terms:

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

5. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-05.md">**Day 5**</a>

<a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-05.md">Quiz</a>

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html">"Big O: Analysis of Algorithm Efficiency, through “Linear Complexity Growth”"</a>

<a href = "https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html">"Linked LIsts"</a>

<a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d">"What's a Linked List Anyway pt. 1"</a>

<a href = "https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996">"What's a Linked List Anyway pt. 2"</a>

6. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-06.md">**Day 6**</a>

- Explain what a “Singleton” is (in Computer Science terms)?
- Explain how the Singleton pattern can be used with Node modules, specifically with classes?
- If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

Document the following Vocabulary Terms:

- Router Middleware
- Dynamic Module Loading
- Singleton Pattern
- CRUD -> REST Method Matches
- Mock Testing

7. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-07.md">**Day 7**</a>

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

Document the following Vocabulary Terms:

- Client ID
- Client Secret
- Authentication Endpoint
- Access Token Endpoint
- API Endpoint
- Authorization Code
- Access Token

8. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-08.md">**Day 8**</a>

- When is Basic Authorization used vs. Bearer Authorization?
- What does the JSON Web Token package do?
- What considerations should we make when creating and storing a SECRET?

Document the following Vocabulary Terms:

- encryption
- token
- bearer
- secret
- JSON Web Token

9. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-09.md">**Day 9**</a>

- What header(s) are used in authentication and authorization?
- What is safe to put into a JWT?
- How are JWTs validated?

Document the following Vocabulary Terms:

- RBAC
- User Roles
- JWT Token

10. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-10.md">**Day 10**</a>

- <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-10.md">Quiz</a>
- Stacks and Queues

11. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-11.md">**Day 11**</a>

- Why is access control important?
- Describe an application that would need access control?
- What is a role used for?
- Why is role based access control more scalable than discretionary or mandatory access control?

Document the following Vocabulary Terms:

- Authorization
- Role Based Access Control
- Capabilities

12. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-12.md">**Day 12**</a>

- What is the benefit of transforming data into packets?
- UDP is often refereed to as a connectionless protocol. Why is this?
- Can a socket server application have multiple socket connections?
- Can a socket connection application be connected to multiple socket servers?
- Can an application be both a socket server and a socket connection?

Document the following Vocabulary Terms:

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

13. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-13.md">**Day 13**</a>

- What does it mean that web sockets are bidirectional? Why is this useful?
- Does socket.io use HTTP? Why?
- What happens when a client emits an event?
- What happens when a server emits an event?
- What happens if a client “misses” an event?
- How can we mitigate this?

Document the following Vocabulary Terms:

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

14. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-14.md">**Day 14**</a>

- What’s the difference between a FIFO and a standard queue?
- How can the server be assured a message was properly received?
- What classic design pattern is best represented by event driven programming?
- How do you test an event driven system?

- Document the following Vocabulary Terms:

- FIFO Queue
- Pub/Sub

15. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-15.md">**Day 15**</a>

[Quiz](class-15.md)

- Binary Trees, Binary Search Trees, & K-ary Trees.

16. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-16.md">**Day 16**</a>

- Describe the Web-Request-Response-Cycle?
- Explain what a “server” is, as it relates to the WRRC?
- What does it mean to “deploy” an application?

- Document the following Vocabulary Terms:

- Server
- Pub/Sub
- WRRC

17. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-17.md">**Day 17**</a>

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

18. <a href="https://github.com/scottie-l/reading-notes/blob/main/reading-notes-401/class-18.md">**Day 18**</a>

- Describe a use case for a serverless function?
- If you were to create a system that emulated Lambda functions, how would you do it?
- Describe how a CDN works?

- Document the following Vocabulary Terms:

- Serverless Functions
- Cloud Storage
- CDN

<a href = "https://github.com/scottie-l/reading-notes">**Back**</a>
