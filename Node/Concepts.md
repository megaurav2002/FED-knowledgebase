# Concepts

NodeJS is a c++ program with V8 embedded and whole bunch of c++ functions to add additional functionality to JS. Some of these additional functionalities are

* Way to deal with files (organising code)
* Talking to DB
* Accepting/sending requests
* Ability to deal with work that takes a long time

## V8

V8 is google's open source javaScript engine and is used in Google Chrome and Node. V8 can be used as a standalone program or can be embedded to a c++ application. V8 can be extended by writting c++ function and linking V8 to it. 

## Events

In Node, we actually talk about 2 different type of events.

* System Events - Events raised from c++ core e.g. some network event, finish reading a file etc. These are in libuv library.

* Custom Events - Events raised from Javascript core. Come from Event Emitter.


### Bit of history

io.js was forked off node as there was a disagreement on how often node should be updated. Few years later a consensus was reached and io.js was merged back into node. 

### Links

https://github.com/v8/v8