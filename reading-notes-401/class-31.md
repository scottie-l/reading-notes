# Notes - Day 31

1. Why choose Redux instead of the Context API for global state? Redux is an Open Source Library which provides a central store, and actions to modify the store. <a href = "https://dev.to/ruppysuppy/redux-vs-context-api-when-to-use-them-4k3p">"Source"</a>

2. What is the purpose of a reducer? In Redux, a reducer is a pure function that takes an action and the previous state of the application and returns the new state. The action describes what happened and it is the reducer's job to return the new state based on that action. <a href = "https://www.pluralsight.com/guides/how-to-write-redux-reducer">"Source"</a>

3. What does an action contain? Actions have a type field that tells what kind of action to perform and all other fields contain information or data. And there is one other term called Action Creators, these are the function that creates actions. So actions are the information (Objects) and action creator are functions that return these actions. <a href = "https://www.geeksforgeeks.org/introduction-to-redux-action-reducers-and-store/">"Source"</a>

4. Why do we need to copy the state in a reducer? If the new state is different, the reducer must create new object, and making a copy is a way to describe the unchanged part. <a href = "https://stackoverflow.com/questions/39521868/why-does-redux-need-to-make-a-copy-of-the-data-each-time-it-changes#:~:text=If%20the%20new%20state%20is,to%20describe%20the%20unchanged%20part.">"Source"</a>

5. Document the following Vocabulary Terms:

- <u>*immutable state:*</u> Immutable state means its value cannot be changed once it's created. <a href = "https://medium.com/@mateuszsokola/understanding-immutable-state-with-immutable-js-and-typescript-91a9ba648fe5#:~:text=Immutable%20state%20means%20its%20value%20cannot%20be%20changed%20once%20it's%20created.">"Source"</a>
- <u>*time travel in redux:*</u> Time travel is the ability to move back and forth among the previous states of an application and view the results in real time. <a href = "https://blog.scottlogic.com/2017/03/09/relogic-2.html#:~:text=Time%20travel%20is%20the%20ability,is%20always%20exactly%20the%20same.">"Source"</a>
- <u>*action creator:*</u> An action creator is a function that literally creates an action object. <a href = "https://www.educative.io/courses/building-teslas-battery-range-calculator-with-react-and-redux/7nVVPYOGVPr">"Source"</a>
- <u>*reducer:*</u> A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. <a href = "https://css-tricks.com/understanding-how-reducers-are-used-in-redux/">"Source"</a>
- <u>*dispatch:*</u> dispatch is a function of the Redux store. You call store. dispatch to dispatch an action. This is the only way to trigger a state change. <a href = "https://react-redux.js.org/using-react-redux/connect-mapdispatch#:~:text=dispatch%20is%20a%20function%20of,connect%20does%20it%20for%20you.">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
