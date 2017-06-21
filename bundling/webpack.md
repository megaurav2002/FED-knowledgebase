# Webpack

Webpack at it's core is just a bundling utility. All it needs to run is a entry and exit point. e.g.

```
webpack ./js/clientApp.jsx public/bundle.js
```

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
