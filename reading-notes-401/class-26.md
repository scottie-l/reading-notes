# Notes - Day 26

1. When you have multiple contexts, what component type should you use (class/function) and why? You should use a function component, as the class component would need to change the entire class along with all it's children.

2. What are some good use cases for using the Context API for global state? When some data needs to be accessible by many components at different nesting levels.  <a href = "https://reactjs.org/docs/context.html">"Source"</a>

3. How can you best test context? The best way to test Context is to make our tests unaware of its existence and avoiding mocks. We want to test our components in the same way that developers would use them (behavioral testing) and mimic the way they would run in our applications (integration testing). <a href = "https://www.samdawson.dev/article/react-context-testing">"Source"</a>

4. Document the following Vocabulary Terms:

- <u>*Context:*</u> Refers to an object. Within an object, the keyword “this” refers to that object (i.e. “self”), and provides an interface to the properties and methods that are members of that object. When a function is executed, the keyword “this” refers to the object that the function is executed in. <a href = "https://blog.kevinchisholm.com/javascript/context-object-literals/#:~:text=In%20JavaScript%2C%20%E2%80%9Ccontext%E2%80%9D%20refers,the%20function%20is%20executed%20in.">"Source"</a>
- <u>*useContext():*</u> The `useContext` hook is used to create common data that can be accessed throughout the component hierarchy without passing the props down manually to each level. Context defined will be available to all the child components without involving “props”. <a href = "https://medium.com/technofunnel/usecontext-in-react-hooks-aa9a60b8a461#:~:text=%E2%80%9CuseContext%E2%80%9D%20hook%20is%20used%20to,components%20without%20involving%20%E2%80%9Cprops%E2%80%9D.">"Source"</a>
- <u>*Static Context:*</u> You can invoke static methods without creating an object. But static contexts(methods and blocks) don't have any instance, they belong to the class. In a simple sense, to use “this” the method should be invoked by an object, which is not always necessary with static methods. <a href = "https://www.tutorialspoint.com/is-it-possible-to-use-this-keyword-in-static-context-in-java#:~:text=You%20can%20invoke%20static%20methods%20without%20creating%20an%20object.&text=But%20static%20contexts(methods%20and,always%20necessary%20with%20static%20methods.">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
