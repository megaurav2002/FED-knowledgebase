# React Component State

A component can have state and only it can modify it.

Always use this.setState to modify state. We never do this.state.x='blah' as react is not watching it and it will not trigger re-render. Calling setState is also optimised as react batches these.