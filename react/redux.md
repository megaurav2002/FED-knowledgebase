# Redux

It's a state management tool. It is just a tree of data and each part of the application can subscribe to one part of the tree. You would use redux to manage state when you have tons of react components that share the same state.

user action handler >> dispatch event (action creator) >> reducer modifies state >> react (subscriber) >> re-render

## Principles of Redux

- Everything that changes in your application including data and UI state are stored in a single state tree
- State tree is read only. the only way to change it is dispatching an action 
- Reducer functions have to be pure i.e. they cannot modify the passed in state. they are not slow however, as the new state inner props can be a reference to the earlier state's prop.
- `Store` - current state (getState), dispatch actions to change state of application (dispatch), listen to state changes (subscribe)

## Reducers

Reducer is just a function that takes a state and an action as a paramter and returns another state. This is great as everything is reproducible and makes everything extremely testable.


### Links

https://egghead.io/courses/getting-started-with-redux by Dan Ambrov

