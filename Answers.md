1. What problem does the context API help solve?

In your typical react application state is passed top-down (parent to child) via props, but this can become very cumbersome quickly, especially when those props are required by many components across your application. However with the introduction of reacts Context API you no longer have to pass props down from component to component. We can now store data on a context object, and retrieve that data in the necessary components from the context object, not props!

1. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

reducers:update the state in a immutable way
actions:dispatch a action to reducers to update the state
store:provide the data to the app

1. What is the difference between Application state and Component state? When would be a good time to use one over the other?

Application state is global, white component state is local. Redux, use what it calls "stores" to hold application state. That means any component, anywhere in the app can access it (kind of like a database) so long as they hook into it.

Component state however, lives within that specific component. As such, it can only be updated within that component and passed down to its children via props.

1. Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

It’s a special name for a function that’s returned by another.When an action creator is called, redux-thunk will intercept and look at what is returned. If the thing returned is an action, it will forward the action through to the reducer. But, if the thing returned is a function, aka a thunk (a function returned from a function), then it will invoke that function and pass in the dispatch function as an argument to it.

1. What is your favorite state management system you've learned and this sprint? Please explain why!

Redux. It makes state management more predictable, centralized and organized
