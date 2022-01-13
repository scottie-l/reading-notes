# Notes - Day 3

1. Name 3 real world use cases where you’d want to change the request with custom middleware? User verification; Data normalization; Security(Malware i.e Log4j)

2. True or false: The route handler is middleware? False. It routes the info where to be processed and is at the start, not middle.

3. In what ways can a middleware function end the process and send data to the browser?  By using request, respond, next, the request will get a response, or trigger the next to move on to next function, or trigger an error.

4. At what point in the request lifecycle can you “inject” middleware? When it hits the server so it can be routed to correct path.

5. What can cause express to error with “Request headers sent twice, cannot start a second response” ? Error [ERR_HTTP_HEADERS_SENT] is an interesting error that is fired up when a server tries to send more than one response to a client. What this means is that for a given client request the server previously sent a response (either a success responsei with the resource requested or error response for a bad request) back to the client and now is unexpectedly trying to send another response. <a href = "https://www.codementor.io/@oparaprosper79/understanding-node-error-err_http_headers_sent-117mpk82z8">"Source"</a>

6. Document the following Vocabulary Terms:

- Middleware: Software that acts as a bridge between an operating system or database and applications, especially on a network.
- Request Object: The request object is the main entry point for an application to issue a request to the Library - all operations on a URL must use a Request object. The request object is application independent in that both servers and clients use the same Request class. <a href = "https://www.google.com/search?q=define+request+object&rlz=1C1CHZN_enUS962US962&sxsrf=AOaemvIYgLnfReLGJk8_ti0bmkSOcxsxWQ%3A1642051386796&ei=OrffYZCIMKjU1sQPj_eVgAc&oq=define+request+objext&gs_lcp=Cgdnd3Mtd2l6EAMYADIGCAAQDRAeMgUIABCGAzoHCAAQRxCwAzoHCAAQsAMQQzoECCMQJzoFCAAQkQI6BAgAEEM6CwgAEIAEELEDEIMBOggIABCABBCxAzoFCAAQgAQ6FQgAEIAEEIcCELEDEIMBEBQQRhD5AToICAAQsQMQkQI6CggAEIAEEIcCEBQ6BwgAEIAEEAo6BggAEBYQHkoECEEYAEoECEYYAFCTBljhLmD3PGgBcAJ4AIABgwGIAaUIkgEEMTMuMZgBAKABAcgBCsABAQ&sclient=gws-wiz">"Source"</a>
- Response Object: The Response() constructor creates a new Response object. An object defining a body for the response. <a href = "https://developer.mozilla.org/en-US/docs/Web/API/Response/Response">"Source"</a>
- Application Middleware: Middleware is software that provides common services and capabilities to applications outside of what's offered by the operating system. ... Middleware helps developers build applications more efficiently. <a href = "https://www.redhat.com/en/topics/middleware/what-is-middleware">"Source"</a>
- Routing Middleware: The term is composed of 2 words router and middleware. Middleware is a piece of code that comes in the middle of request and response . It kind of hijacks your request so that you can do anything that you want with your request or response eg: Modify the data or call the next middleware.<a href = "https://stackoverflow.com/questions/63106648/what-is-router-middleware-in-express">"Source"</a>
- Test Driven Development: (TDD) is a software development practice that focuses on creating unit test cases before developing the actual code. It is an iterative approach that combines programming, the creation of unit tests, and refactoring. <a href = "https://www.browserstack.com/guide/what-is-test-driven-development#:~:text=In%20layman's%20terms%2C%20Test%20Driven,of%20unit%20tests%2C%20and%20refactoring.">"Source"</a>
- Behavioral Testing: Behavioral testing checks the software behavior. By definition, it is almost always a functionality test, and can be automated to a certain degree. Test cases can be easily created due to the software specifications.<a href = "https://www.quora.com/What-is-the-difference-between-Behavioral-testing-and-Blackbox-testing">"Source"</a>

Which 3 things had you heard about previously and now have better clarity on?

- Hoisting
- Strict mode
- Next

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- Behavioral testing
- TDD
- Routers

What are you most excited about trying to implement or see how it works? Behavioral testing

<b><a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>
