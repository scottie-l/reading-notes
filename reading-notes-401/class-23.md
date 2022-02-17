# Notes - Day 23

1. How can we ensure that an effect hook runs only once? The trick is that useEffect takes a second parameter. That will ensure the useEffect only runs once. Note from the docs: If you use this optimization, make sure the array includes all values from the component scope (such as props and state) that change over time and that are used by the effect. <a href = "https://www.google.com/search?q=How+can+we+ensure+that+an+effect+hook+runs+only+once%3F+&rlz=1C1CHZN_enUS962US962&sxsrf=APq-WBtxgyzUlhMDz6i9qDGJTyXpyNCAbw%3A1645080920415&ei=WPENYozhGJm_0PEPxpuC-A8&ved=0ahUKEwiM7Yz_k4b2AhWZHzQIHcaNAP8Q4dUDCA8&uact=5&oq=How+can+we+ensure+that+an+effect+hook+runs+only+once%3F+&gs_lcp=Cgdnd3Mtd2l6EANKBAhBGABKBAhGGABQAFgAYKoHaABwAXgAgAFwiAFwkgEDMC4xmAEAoAECoAEBwAEB&sclient=gws-wiz">"Source"</a>

2. Can useState() update more than one state variable at the same time? You could combine the loading state and data state into one state object and then you could do one setState call and there will only be one render. Note: Unlike the setState in class components, the setState returned from useState doesn't merge objects with existing state, it replaces the object entirely. <a href = "https://stackoverflow.com/questions/53574614/multiple-calls-to-state-updater-from-usestate-in-component-causes-multiple-re-re">"Source"</a>

3. Is useState() synchronous? useState and setState both are asynchronous. They do not update the state immediately but have queues that are used to update the state object. This is done to improve the performance of the rendering of React components. <a href = "https://www.linkedin.com/pulse/provide-callback-usestate-hook-like-setstate-saransh-kataria/">"Source"</a>

4. Document the following Vocabulary Terms:

- *State Hook:* The React useState Hook allows us to track state in a function component. State generally refers to data or properites that need to be tracking in an application. <a href = "https://www.w3schools.com/react/react_usestate.asp">"Source"</a>
- *Component Lifecycle:* Every React Component has a lifecycle of its own, lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component's existence. <a href = "https://www.geeksforgeeks.org/reactjs-lifecycle-components/#:~:text=Every%20React%20Component%20has%20a,stages%20of%20the%20component's%20existence.">"Source"</a>

---
**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**
