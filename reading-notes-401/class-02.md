# Notes - Day 2

1. What’s the difference between PUT and PATCH? The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource but keeps the original. <a href = "https://en.wikipedia.org/wiki/Patch_verb">"Source"</a>

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

  - <a href = "https://www.postman.com/features/mock-api/">"Postman"</a>
  - <a href = "https://mocki.io/">"Mock API"</a>
  - <a href = "http://wiremock.org/">"WireMock"</a>

3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

- 100 Continue
- 101 Switching Protocols
- 102 Processing
- 103 Early Hints
- 200 OK
- 201 Created
- 202 Accepted
- 203 Non-Authoritative Information
- 204 No Content
- 205 Reset Content
- 206 Partial Content
- 207 Multi-Status
- 208 Already Reported
- 226 IM Used
- 300 Multiple Choice
- 301 Moved Permanently
- 302 Found
- 303 See Other
- 304 Not Modified
- 305 Use Proxy
- 306 unused
- 307 Temporary Redirect
- 308 Permanent Redirect
- 400 Bad Request
- 401 Unauthorized
- 402 Payment Required
- 403 Forbidden
- 404 Not Found
- 405 Method Not Allowed
- 406 Not Acceptable
- 407 Proxy Authentication Required
- 408 Request Timeout
- 409 Conflict
- 410 Gone
- 411 Length Required
- 412 Precondition Failed
- 413 Payload Too Large
- 414 URI Too Long
- 415 Unsupported Media Type
- 416 Range Not Satisfiable
- 417 Expectation Failed
- 418 I'm a teapot
- 421 Misdirected Request
- 422 Unprocessable Entity
- 423 Locked
- 424 Failed Dependency
- 425 Too Early
- 426 Upgrade Required
- 428 Precondition Required
- 429 Too Many Requests
- 431 Request Header Fields Too Large
- 451 Unavailable For Legal Reasons
- 500 Internal Server Error
- 501 Not Implemented
- 502 Bad Gateway
- 503 Service Unavailable
- 504 Gateway Timeout
- 505 HTTP Version Not Supported
- 506 Variant Also Negotiates
- 507 Insufficient Storage
- 508 Loop Detected
- 510 Not Extended
- 511 Network Authentication Required
- <a href = "https://developer.mozilla.org/en-US/docs/Web/HTTP/Status">"Source"</a>

4. Compare and contrast SOAP and ReST: The main difference is that SOAP is a protocol while REST is not. Typically, an API will adhere to either REST or SOAP, depending on the use case and preferences of the developer. REST is a set of guidelines that offers flexible implementation, whereas SOAP is a protocol with specific requirements like XML messaging.
<a href = "https://www.redhat.com/en/topics/integration/whats-the-difference-between-soap-rest">"Source"</a>

5. Document the following Vocabulary Terms:

- Web Server: The term web server can refer to hardware or software, or both of them working together. On the hardware side, a web server is a computer that stores web server software and a website's component files. A web server connects to the Internet and supports physical data interchange with other devices connected to the web.
On the software side, a web server includes several parts that control how web users access hosted files. At a minimum, this is an HTTP server. An HTTP server is software that understands URLs and HTTP. An HTTP server can be accessed through the domain names of the websites it stores, and it delivers the content of these hosted websites to the end user's device. <a href = "https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server">"Source"</a>

- Express: Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications. <a href = "https://expressjs.com/">"Source"</a>

- Routing: Routing is a way of organizing and managing application states. A routing framework in JavaScript helps you to change the state of the application--perhaps moving from one admin panel section to another--while maintaining application persistence. <a href = "https://stackoverflow.com/questions/10075507/what-does-javascript-routing-buy-you">"Source"</a>

- WRRC: Web Request & Response Cycle- The request/response cycle traces how a user’s request flows through the app. 1- A user opens his browser, types in a URL, and presses Enter.
2- When a user presses Enter, the browser makes a request for that URL. 3- The request hits the router. The router maps the URL to the correct controller and action to handle the request. 4- The action receives the request and passes it on to the view. 5- The view renders the page as HTML. 6- The controller sends the HTML back to the browser. The page loads and the user sees it. <a href = "https://www.codecademy.com/article/request-response-cycle-static">"Source"</a>

1. Which 3 things had you heard about previously and now have better clarity on?

- CRUD
- ReST
- Node.js

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- Test Driven Development
- CI/CD
- Supertest

3. What are you most excited about trying to implement or see how it works?

-TDD

---
**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**

---
