# Webpack

Webpack at it's core is just a bundling utility. All it needs to run is a entry and exit point. e.g.

```
webpack ./js/clientApp.jsx public/bundle.js
```

## Dependency Graph

When webpack processes your application, it starts from a list of modules defined on the command line or in its config file. Starting from these entry points, webpack recursively builds a dependency graph that includes every module your application needs, then packages all of those modules into a small number of bundles - often, just one - to be loaded by the browser.

## Hot Module Replacement

Update a particular component without a hard refresh. Great for development.

## Plugins

babel-loader: This package allows transpiling JavaScript files using Babel and webpack.

style-loader: Adds CSS to the DOM by injecting a `<style>` tag 

css-loader: The css-loader interprets @import and url() like import/require() and will resolve them. 

## Example Projects:

https://github.com/kentcdodds/es6-todomvc

### Awesome webpack

https://github.com/webpack-contrib/awesome-webpack
