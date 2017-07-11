## Const

Const enforces block level scoping. Const does not mean the value is unchangeable. It just means the bindings/assignment is immutable for e.g.

```
const myArray = [1,2,3];
myArray = 10 // invalid
myArray[0] = 100; // valid
```
To achieve the above behavior, you are better off with Object.freeze. It's a shallow operation i.e. if it was array of arrays, freeze will not be able to ensure that the inner array is not getting changed.


## Let

Let Keyword enforces block level scoping i.e. if statement
