# Notes - Day 1

1. Describe what `Array.map()` does: The Array.map() method allows you to iterate over an array and modify its elements using a callback function. The callback function will then be executed on each of the array's elements. <a href = "https://www.freecodecamp.org/news/javascript-map-how-to-use-the-js-map-function-array-method/">"Source"</a>

2. Describe what `Array.reduce()` does: The arr.reduce() method in JavaScript is used to reduce the array to a single value and executes a provided function for each value of the array (from left-to-right) and the return value of the function is stored in an accumulator. <a href = "https://www.geeksforgeeks.org/javascript-array-reduce-method/">"Source"</a>

3. Provide code snippets showing how to use `superagent()` to fetch data from a URL and log the result:

~~~js
`request`
  `.post('/api/pet')`
  `.send({ name: 'Manny', species: 'cat' })`
  `.set('X-API-Key', 'foobar')`
  `.set('Accept', 'application/json')`
  `.then(res => {`
     `alert('yay got ' + JSON.stringify(res.body));`
   `});`
~~~

<a href = "https://visionmedia.github.io/superagent/">"Source"</a>

- With normal Promise .then() syntax:

~~~js
`request`
  `.get('/search')`
  `.then(res => {`
     `// res.body, res.headers, res.status`
  `})`
  `.catch(err => {`
     `// err.message, err.response`
  `});`
~~~

<a href = "https://visionmedia.github.io/superagent/">"Source"</a>  

- Again with async / await syntax:

~~~js
`async function loginUser(user, request) {`
  `let auth;`
  `await request`
    `.post('/users/login')`
    `.send(credentials)`
    `.expect(200)`
    `.end(onResponse);`

 `function onResponse(err, res) {`
    `auth.token = res.body.token;`
  `}`
  `return auth;`
`}`
~~~

<a href = "https://stackoverflow.com/questions/51438903/superagent-supertest-with-async-await">"Source"</a>

4. Explain promises as though you were mentoring a Code 301 level student: A Promise is an object that represents the eventual completion (or failure) of an asynchronous operation, and its resulting value. <a href = "https://www.freecodecamp.org/news/javascript-promises-explained/">"Source"</a>

5. Are all callback functions considered to be Asynchronous? Why or Why Not? Callbacks that you call yourself are regular function calls, which are always synchronous. Certain native APIs are asynchronous and will execute their callbacks later in the event loop. If you call a callback synchronously from within an async callback, it will end up being async too. <a href = "https://stackoverflow.com/questions/19083357/are-all-javascript-callbacks-asynchronous-if-not-how-do-i-know-which-are">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">**Back**</a>

---
