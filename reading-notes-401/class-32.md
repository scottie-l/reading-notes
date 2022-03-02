# Notes - Day 32

1. How granular should your reducers be? Recommend putting as much logic as possible into reducers. There are times when you may need some logic to help prepare what goes into the action, but reducers should do most of the work. <a href = "https://redux.js.org/faq/code-structure">"Source"</a>

2. Pro or Con – Multiple reducers can “fire” when a commonly named action is dispatched? Pro since we have to change multiple states in multiple components; Reducers can listen when an action is dispatched which can reduce a lot of work, and each reducer can provide a different logic to the same dispatcher. The downside is, now, you have no history of why the changes are happening, so debugging gets really difficult. <a href = "https://redux.ruanyifeng.com/faq/Actions.html#should-i-dispatch-multiple-actions-in-a-row-from-one-action-creator">"Source"</a>

3. Name a strategy for preventing the above? Make a reducer for each component affected by the dispatcher, then you're only targeting a specific instance of the state.

4. Document the following Vocabulary Terms:

- <u>*store:*</u> A store is basically just a plain JavaScript object that allows components to share state. In a way, we can think of a store as a database. On the most fundamental level, both constructs allow us to store data in some form or another. <a href = "https://learn.co/lessons/react-stores#:~:text=A%20store%20is%20basically%20just,in%20some%20form%20or%20another.">"Source"</a>
- <u>*combined reducers:*</u> The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore . The resulting reducer calls every child reducer, and gathers their results into a single state object. <a href = "https://redux.js.org/api/combinereducers#:~:text=The%20combineReducers%20helper%20function%20turns,into%20a%20single%20state%20object.">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
