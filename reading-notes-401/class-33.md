# Notes - Day 33

1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application? The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount) of a Higher Order Component that wraps your app. <a href = "https://stackoverflow.com/questions/39356517/correct-way-to-pre-load-component-data-in-reactredux#:~:text=1%20Answer&text=The%20most%20'redux%2Dlike',Component%20that%20wraps%20your%20app.">"Source"</a>

2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer? Export the thunk/async function.

3. Document the following Vocabulary Terms

- <u>*middleware:*</u> A type of computer software that provides services to software applications beyond those available from the operating system. It can be described as "software glue". <a href = "https://en.wikipedia.org/wiki/Middleware">"Source"</a>
- <u>*thunk:*</u> a thunk is a subroutine used to inject a calculation into another subroutine. Thunks are primarily used to delay a calculation until its result is needed, or to insert operations at the beginning or end of the other subroutine. <a href = "https://en.wikipedia.org/wiki/Thunk">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
