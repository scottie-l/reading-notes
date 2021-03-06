# Notes - Day 6

1. Explain what a “Singleton” is (in Computer Science terms): A software design pattern that restricts the instantiation of a class to one "single" instance. <a href = "https://en.wikipedia.org/wiki/Singleton_pattern">"Source"</a>

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes? A singleton represents a single instance of an object. Only one can be created, no matter how many times the object is instantiated. If there’s already an instance, the singleton will create a new one. <a href = "https://medium.com/@maheshkumawat_83392/node-js-design-patterns-singleton-pattern-series-1-1e0ab71e3edf">"Source"</a>

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it? I'd create a class in a file and then export that class to all children who would need to instantiate it.

4. Document the following Vocabulary Terms:

- <u>*Router Middleware:*</u> The term is composed of 2 words router and middleware. Middleware. It is a piece of code that comes in the middle of request and response . It kind of hijacks your request so that you can do anything that you want with your request or response eg: Modify the data or call the next middleware. <a href = "https://stackoverflow.com/questions/63106648/what-is-router-middleware-in-express">"Source"</a>
- <u>*Dynamic Module Loading:*</u> Dynamic loading is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. <a href = "https://en.wikipedia.org/wiki/Dynamic_loading">"Source"</a>
- <u>*Singleton Pattern:*</u> In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. <a href = "https://en.wikipedia.org/wiki/Singleton_pattern">"Source"</a>. This pattern involves a single class which is responsible to create an object while making sure that only single object gets created. This class provides a way to access its only object which can be accessed directly without need to instantiate the object of the class. <a href = "https://www.tutorialspoint.com/design_pattern/singleton_pattern.htm">"Source"</a>
- <u>*CRUD -> REST Method Matches:*</u> Create = POST(Create new data) or PATCH(Selected amount of data only); Read = GET(no change to data); Update = PUT(overwrite entire file) or PATCH(overwrite a select amount in file) or POST(create new data); delete = DELETE(remove data). <a href = "https://medium.com/@ritika.atal.work/crud-mapping-to-http-verbs-354a3c0009f5">"Source"</a>
- <u>*Mock Testing:*</u> Mocking means creating a fake version of an external or internal service that can stand in for the real one, helping your tests run more quickly and more reliably. When your implementation interacts with an object's properties, rather than its function or behavior, a mock can be used. <a href = "https://circleci.com/blog/how-to-test-software-part-i-mocking-stubbing-and-contract-testing/#:~:text=What%20is%20mock%20testing%3F,a%20mock%20can%20be%20used.">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">**Back**</a>

---
