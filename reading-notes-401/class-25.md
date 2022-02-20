# Notes - Day 25

1. Describe use cases useState() vs useReducer()? `useReducer` is usually preferable to `useState` when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. `useReducer` also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks. <a href = "https://reactjs.org/docs/hooks-reference.html#:~:text=useReducer%20is%20usually%20preferable%20to,dispatch%20down%20instead%20of%20callbacks.">"Source"</a>

2. Why do custom hooks need the use prefix? This is mainly to have an extra option for sharing state and logic between components. Custom hooks are normal JS functions, named with the prefix 'use', that can use hooks inside of it and contain a common stateful logic to be reused in other components. <a href = "https://betterprogramming.pub/quick-intro-to-react-hooks-6e8a44ae4aa6">"Source"</a>

3. What do custom hooks usually do? Share logic between other JavaScript functions other components, it allows you to reuse some piece of code in several parts of your app to create an event.  <a href = "https://dev.to/olenadrugalya/introduction-to-custom-hooks-2nmk">"Source"</a>

4. Using any list of custom hooks, research and name one that you think will be useful in your applications. <a href = "https://reactjs.org/docs/hooks-reference.html">"Source"</a> `useMemo`; Pass a “create” function and an array of dependencies. useMemo will only recompute the memoized value when one of the dependencies has changed. This optimization helps to avoid expensive calculations on every render. <a href = "https://reactjs.org/docs/hooks-reference.html#usememo">"Source"</a>

5. Describe how a hook that fetches API data might work? We put the fetchData function above in the useEffect hook and call it to get the response data. <a href = "https://designcode.io/react-hooks-handbook-fetch-data-from-an-api">"Source"</a>

6. Document the following Vocabulary Terms:

- *reducer:* A reducer is just a simple JS function which takes in two arguments — the current state and an action — and returns based on both arguments a new state. <a href = "https://medium.com/react-bootcamp/what-is-a-reducer-in-javascript-f4fd40f98324#:~:text=A%20reducer%20is%20a%20very,both%20arguments%20a%20new%20state.">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
