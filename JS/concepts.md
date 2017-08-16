# Concepts

## Closure
closure is when a function "remembers" the variables around it even when the function is executed elsewhere.

## Currying
Briefly, currying is a way of constructing functions that allows partial application of a function’s arguments. What this means is that you can pass all of the arguments a function is expecting and get the result, or pass a subset of those arguments and get a function back that’s waiting for the rest of the arguments.

## SetTimeout(0)
while it seems like the code entered in here should execute immediately, it only executes once the current callstack has been completed.  When setTimeout is called, the code wrapped in this gets pushed to webapi (browser - outside of JS current stack) where it waits for 0 milliseconds which is nothing. So it immediately, gets pushed to event loop from where it will get picked by JS runtime when the current callstack has been cleared. 

similar concepts, apply to ajax calls.

stack >> browser >> event loop >> stack 
