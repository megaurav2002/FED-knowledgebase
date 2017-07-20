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

## Default Values for functions

Sets the default value of 42 if X below is undefined, in every other case including null the value of X will not be set to 42.  

```
function foo(x = 42) {
 // do something
}
```

## Rest/Spread/Gather operator

Accept all the function parameters passed in to an array called args. 
```
function (...args) {
}
```

The other usage of this operator is called spread operator
```
bar(...args)
```
will pass multiple params(equal to array length) to bar()

This would work on anything that has iterator built in for e.g. es6 arrays, strings. 

``` This is valid
var myString = "Hello";
foo(...myString) // 5 params passed
```

## Array Destructuring

```
function foo() {
    return [1, 2, 3];
}
var [a, b, c] = foo();
// a=1, b=2, c=3 
```

this can also be done for object keys destructuring

```
var obj = {};
[obj.a, obj.b, obj.c] = foo();
```

## Object Destructuring

```
function foo() {
    return { a:1, b:2, c:3};
}

var {
    a = 10,
    b: X = 42,
    c
}
```

For a, we have a default value of 10
For b, we have specified a target variable X with a default value
For c, get value of c in variable called c with no defaults

## Symbol

A way of putting special/meta property on an object. 

## Iterator

It's an simple way of stepping through data from a datasource. For e.g. resultSet.next().. consume one at a time.

for of loop can iterate over any iterable e.g. array

## Generators

Its a function that is not immediately executed. It returns an iterator. In essence, it's a function that can be started and stopped many times.

```
function *main() {
    console.log("helloworld")
}

var it = main();
it.next() // prints helloworld and returns {value:undefined, done:true} as it is finished.
```

yield can be used to pause a generator function (optionally send a value out) and will be unpaused only on it.next()

```
function *main() {
    console.log("hello")
    yield 9; 
    console.log("world");
    return 10; 
}
var it = main();
it.next(); // {value: 9, done: false}
it.next(); // {value: 10, done: true}
```
