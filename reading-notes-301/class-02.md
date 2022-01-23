# Notes - Day 2

_<a href = "https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093">"React Lifecycle"</a>_

1. what happens 1st, the render or the componenetDidMount? The render function happens first, while the componentDidMount happens in the commit phase.

2. What's the very 1st thing to happen in the lifecycle of React? Mounting. Left to right, top to bottom.

3. Put following in order: 1.constructor, 2.React Updates, 3.render, 4.componentDidMount, 5. componentWillUnmount.

4. What's componentDidMount do? Used to load anything using network request or initialize DOM. Also a good place to set up any subscriptions.

3 phases of component lifecycle: Mounting, Updating, & Unmounting.

Mounting: When instance of component is being created and inserted into DOM, it occurs during Mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount occur in this order when mounting.

Updating: Anytime component is updated, it's re-rendered. These lifecycle events happen during updating in this order: static getDerivedStateFromProps, shouldComponentUpdate, render, getSnapshotBeforeUpdate, componentDidUpdate, UNSAFE_componentWillUpdate, UNSAFE_componentWillReceiveProps.

Unmounting: Final phase of lifecycle, if called, when a component is being removed from DOM. componentWillUnmount is the only lifecycle event during this phase.

Constructor() for a React component is called before it's mounted. If component is subclass you should call super(props), or props will be undefined. Constructors can be used to assign state using this.state or to bind event handle methods to an instance.

static getDerivedStateFromProps() This method exists for rare cases where state relies on changes in props over time.

Render() is the only required method in class component. Will examine this.props and this.state when called. Render() should not modify the component state because it would cause a  bugs by changing state every time it re-renders. Also should not directly interact with browser. Render will not be invoked if shouldComponentUpdate() returns false.

ComponentDidMount() method is invoked immediately after a component is mounted. If you need to load anything using network request or initialize DOM, it should go here. This is a good place to set up any subscriptions. Don’t forget to unsubscribe in componentWillUnmount() if you do subscribe.

SetState() can be called, but it should be used sparingly, because it will cause a re-render.

The default behavior in react is to re-render after every state change. Setting shouldComponentUpdate() to false allows you to prevent this from happening.

ShouldComponentUpdate() If you want to use this method, it may be better to use PureComponent instead, which performs a shallow comparison of props and state. If you do use this method, be sure to check the previous props and state with current props and state. If shouldComponentUpdate() returns false, then UNSAFE_componentWillUpdate(), render(), and componentDidUpdate() will not be invoked.

GetSnapshotBeforeUpdate() Another rarely used method that allows to capture picture of DOM to check out before actually changing anything on DOM.

componentDidUpdate() Method is useful for performing network requests after change has occurred.

componentWillUnmount() Method allows you to clean up DOM and network requests/subscriptions.

UNSAFE Lifecycle Events: React 17 these will no longer be able to be used without the UNSAFE tag in front of them.

UNSAFE_componentWillMount(), instead of componentWillMount, use ComponentDidMount.

UNSAFE_componentWillUpdate(), instead of componentWillUpdate, use getSnapshotBeforeUpdate.

UNSAFE_componentWillReceiveProps(), instead of componentWillReceiveProps, use static getDerivedStateFromProps.

_<a href = "https://www.youtube.com/watch?v=IYvD9oBCuJI">"React state Vs Props"</a>_

1. What types of things can you pass in the props? Things you would pass to a function, like your initialized counter or how you'd like it to render.

2. What's the difference between props and state? State is inside component and changes inside component, props are handled outside and changed outside, usually static.

3. When do we re-render our app? When state changes, or props is passed new state.

4. What are some ex. of things that we could store in state? Things to display something to user.  

_<a href = "https://reactjs.org/docs/state-and-lifecycle.html">"React Docs - State and Lifecycle"</a>_

When `<Clock />` is passed to ReactDOM.render(), React calls the constructor of the Clock component. Since Clock needs to display the current time, it initializes this.state with an object including the current time. We will later update this state.

React then calls the Clock component’s render() method. This is how React learns what should be displayed on the screen. React then updates the DOM to match the Clock’s render output.

When the Clock output is inserted in the DOM, React calls the componentDidMount() lifecycle method. Inside it, the Clock component asks the browser to set up a timer to call the component’s tick() method once a second.

Every second the browser calls the tick() method. Inside it, the Clock component schedules a UI update by calling setState() with an object containing the current time. Thanks to the setState() call, React knows the state has changed, and calls the render() method again to learn what should be on the screen. This time, this.state.date in the render() method will be different, and so the render output will include the updated time. React updates the DOM accordingly.

If the Clock component is ever removed from the DOM, React calls the componentWillUnmount() lifecycle method so the timer is stopped.

The only place where you can assign this.state is the constructor.

_<a href = "https://reactjs.org/docs/handling-events.html">"React Docs - Handling Events"</a>_

_<a href = "https://reactjs.org/tutorial/tutorial.html">"React Docs - Tutorial through Dev tools"</a>_

**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>**
