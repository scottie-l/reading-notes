# Notes - Day 27

1. Why is the Context API useful? The Context API can be used to share data with multiple components, without having to pass data through props manually. For example, some use cases the Context API is ideal for: theming, user language, authentication, etc. <a href = "https://www.telerik.com/blogs/understand-react-context-api#:~:text=The%20Context%20API%20can%20be,user%20language%2C%20authentication%2C%20etc.">"Source"</a>

2. Can a component outside of a provider get its context? To access a React context outside of the render function, we can use the useContext hook. We create the UserContext by calling the React. createContext method with a default context value. Then in the Users component, we call the useContext hook with UserContext to accxess the current value of UserContext . <a href = "https://thewebdev.info/2021/05/28/how-to-access-a-react-context-outside-of-the-render-function/#:~:text=the%20render%20Function-,To%20access%20a%20React%20context%20outside%20of%20the%20render%20function,can%20use%20the%20useContext%20hook.&text=We%20create%20the%20UserContext%20by,the%20current%20value%20of%20UserContext%20.">"Source"</a>

3. What are some common use cases for using the Context API? Theming, translation, authentication <a href = "https://flexiple.com/react/provider-pattern-with-react-context-api/">"Source"</a>

4. Describe “Context Hell” Like the callback hell, usual when jQuery was used for everything, the React Context hell is the nasty code you get taking advantage of the React Context API. <a href = "https://dev.to/alfredosalzillo/the-react-context-hell-7p4">"Source"</a>

5. Document the following Vocabulary Terms:

- *global state:* In computer programming, a global variable is a variable with global scope, meaning that it is visible (hence accessible) throughout the program, unless shadowed. The set of all global variables is known as the global environment or global state. <a href = "https://en.wikipedia.org/wiki/Global_variable">"Source"</a>
- *global context:* The global context is the fallback context in JavaScript. If you run a function and no context is set (usually by an object) then the fallback is the global context. In Node. js, that means an object with information related to Node. <a href = "https://thinkster.io/tutorials/javascript-fundamentals-the-this-keyword/global-context">"Source"</a>
- *provider:* The provider() function allows us to create a configurable service where we can set input per application for the service created using the provider(). The provider() function allows us to create a configurable service where we can set input per application for the service created using the provider(). <a href = "https://dzone.com/articles/what-is-a-provider-in-angularjs">"Source"</a>
- *consumer:* All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes. They "consume the data passed down to them. <a href = "https://reactjs.org/docs/context.html">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
