<b><a href = "https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa">"Functional Programming Concepts"</a>

1. What is functional programming? Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. — Wikipedia

2. What is a pure function and how do we know if something is a pure function? It returns the same result if given the same arguments (it is also referred as deterministic) & it does not cause any observable side effects.

3. What are the benefits of a pure function? Every function is isolated and unable to impact other parts of our system. Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen. The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts.

4. What is immutability? When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

5. What is Referential transparency? If a function consistently yields the same result for the same input, it is referentially transparent. Pure functions + Immutable data = Referential transparency.

<b><a href = "https://www.youtube.com/watch?v=xHLd36QoS4k">"Node JS Tutorial for Beginners #6 - Modules & Require()"</a>

1. What is a module? A small bit of code that has a certain bit of functionality.

2. What does the word ‘require’ do? Use the module in another application.

3. How do we bring another module into the file the we are working in? module.exports = functionName();

4. What do we have to do to make a module available? var functionName = require('./path);

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
