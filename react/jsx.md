# JSX

* JSX gets compiled to react create element. It's just a easier way to write mark up.
* Use className instead of class as class is a reserved JS keyword. className itself is a valid choice because that's how you call DOM api to retrieve for class names of an element. ``` x.className ```

* Object Spread
Similar to array spread in JS. The two components below are equivalent
```
function App1() {
  return <Greeting firstName="Ben" lastName="Hector" />;
}

function App2() {
  const props = {firstName: 'Ben', lastName: 'Hector'};
  return <Greeting {...props} />;
}
```
This should be used sparingly as you may end up passing lot of irrelevant props to components

