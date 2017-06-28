# React Internals

## How does react render method work?

## How does react translate JSX?

## what happens when setState is called?

### setState Implementation

1. https://github.com/facebook/react/blob/5c6a496d98b80d19d851c2ec3a56d760b7118a50/src/isomorphic/modern/class/ReactBaseClasses.js#L59

`ReactComponent.prototype.setState = function(partialState, callback)`

* partialState -  Next partial state or function to produce next partial state to be merged with current state

* callback Called after state is updated.

2. https://github.com/facebook/react/blob/767a5d60e8a67148dc8831de521ce636374016f1/src/renderers/shared/fiber/ReactFiberClassComponent.js#L68

```
addUpdate(fiber, partialState, callback, priorityLevel);
scheduleUpdate(fiber, priorityLevel);
```
      
ReactFiber.addUpdate - https://github.com/facebook/react/blob/master/src/renderers/shared/fiber/ReactFiberUpdateQueue.js#L299 >> insertUpdate(fiber, update)