# Modules

Reusable piece of code whose existence does not unintentionally impact other code. Since JS did not have modules (prior to es6) Node introduced CommonJS modules.

Modules get converted to Function Expressions by Node before handing it over to V8 (to isolate scope) -
https://github.com/nodejs/node/blob/master/lib/module.js#L530

## Common Patterns

* Replace export obj
```
module.export = greet;
var greet = require('filename');
greet();
```

* Attach to export obj

```
module.export.greet = greet;
var greet = require('filename').greet;
greet();
```

* Return a function constructor
```
module.export.Greet = Greet;
var greet = require('filename').Greet;
var myGreet = new greet();
```

* Return a new obj (even though it's a new obj, only the same instance is always returned as node caches exports)
```
module.export.Greet = new Greet();
var greet = require('filename').Greet;
```
