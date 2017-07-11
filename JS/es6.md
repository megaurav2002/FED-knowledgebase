# ES6

## Arrow functions

### Variations

```
() => 3
x => 3
(...x) => 3
(x,y) => 3
x => {try {3; } catch (e) {} }
x => {DO_SOMETHING and return 3; }
x => ({ y:x }) // sticking () gives it an implicit return
const x = => 3 // proposed - headless arrow function
```

Arrow functions come with a lot of confusion and inconsistent syntax. https://github.com/getify/You-Dont-Know-JS/blob/master/es6%20&%20beyond/fig1.png

What makes arrow functions shine is that it doesn't have a `this`. So, when it encounters this, it automatically gets a lexical this.

## Block Scoping

