## Const Keyword

Const does not mean the value is unchangeable. It just means the bindings is immutable for e.g.

```
const myArray = [1,2,3];
myArray = 10 // invalid
myArray[0] = 100; // valid
```
To achieve the above behavior, you are better off with Object.freeze

