# Babel

### Presets
Presets just means include a group of plugins. for e.g. each ES6 transformation is a plugin by itself, we don't want to include them individually, so we just include `presets:["es2015"]`

## Babel-core
Babel-core is the compiler itself. 

The compiler can be broken down into 3 parts:

* The parser: babylon (moved to a separate repo and versioned independently)
* The transformer[s]: All the plugins/presets. These all use babel-traverse to traverse through the AST
* The generator: babel-generator

```
The flow goes like this:

input string -> babylon parser -> AST -> transformer[s] -> AST -> babel-generator -> output string
```

## Tips

* Using `presets:["es2015"]` has some disadvantages. What we are saying here is transform the complete es6 syntax. While our browser may already support some natively. Instead of this we can use `env` config that wil direct babel to do transformation for only last 2 browsers. e.g.
```
"presets": [
        // "es2015",
        [  
            "env", {
                "targets": {
                    "browsers": "last 2 versions"
                }
            },
            "modules": false
        ]
    ]
```

* Set `"modules": false` in example above, leaves transformation of es6 modules to webpack. we want babel to leave modules alone so that webpack can do the tree shaking magic.