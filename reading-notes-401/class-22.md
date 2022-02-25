# Notes - Day 22

1. Why do we not need more .html pages in a multi-page React app? Because the page is updated dynamically from supplied state data to render.

2. If we wanted a component to show up on every page, where would we put it and why?
    - Inside the `<BrowserRouter />`, outside a `<Route />`? It will have access to our components to render the page.

3. What does routing do with the components that were rendered when a new route is requested? It re-renders the page with the new component.

4. What does props.children contain? Whatever you include between the opening and closing tags when invoking a component. <a href = "https://stackoverflow.com/questions/49706823/what-is-this-props-children-and-when-you-should-use-it#:~:text=of%20what%20this.-,props.,tags%20when%20invoking%20a%20component.&text=This%20component%20contains%20an%20%3Cimg,children%7D%20.">"Source"</a>

5. How do `useState()` and `this.setState()` differ? `useState` allows react components can receive dynamic information from props, or set their dynamic data with state. Props are passed down by parents components, whereas state is created and maintained by the component itself. You can use `this.state()` in constructor method and use it in `render()`, and then updated with `this.setState()`. React class components can change their state with `this.setState`. `this.setState()` should always be used instead of directly modifying the `this.state` object. `this.setState()` takes an object which it merges with the component’s current state. <a href = "https://discuss.codecademy.com/t/usestate-vs-setstate/561632">"Source"</a>

6. Document the following Vocabulary Terms:

- <u>*State Hook:*</u> Allows you to have state variables in functional components. You pass the initial state to this function and it returns a variable with the current state value and another function to update this value. <a href = "https://blog.logrocket.com/a-guide-to-usestate-in-react-ecb9952e406c/">"Source"</a>
- <u>*Mounting:*</u> The mount command mounts a storage device or filesystem, making it accessible and attaching it to an existing directory structure.
- <u>*Un-Mounting:*</u> The un-mount command "unmounts" a mounted filesystem, informing the system to complete any pending read or write operations, and safely detaching it. <a href = "https://www.computerhope.com/unix/umount.htm#:~:text=The%20mount%20command%20mounts%20a,operations%2C%20and%20safely%20detaching%20it.">"Source"</a>

---
**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>**

---
