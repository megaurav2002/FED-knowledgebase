# Webpack

Webpack at it's core is just a bundling utility. All it needs to run is a entry and exit point. e.g.

```
webpack ./js/clientApp.jsx public/bundle.js
```

## Dependency Graph

When webpack processes your application, it starts from a list of modules defined on the command line or in its config file. Starting from these entry points, webpack recursively builds a dependency graph that includes every module your application needs, then packages all of those modules into a small number of bundles - often, just one - to be loaded by the browser.

## Hot Module Replacement

Update a particular component without a hard refresh. Great for development.

## Loaders

```
module: {
    rules: [
        {
            test: /\.js$/,
            use: "babel-loader"
        }
    ]

}
```
Test - only perform this loader if it matches this rule

Loader functionally transform them from right to left

e.g.

```
{
    test: /\.scss$/,
    loader: ['style-loader', 'css-loader', 'sass-loader'],
}
```

### Popular loaders

babel-loader: This package allows transpiling JavaScript files using Babel and webpack.

style-loader: Adds CSS to the DOM by injecting a `<style>` tag 

css-loader: The css-loader interprets @import and url() like import/require() and will resolve them. 


## Plugins

A plugin can perform any of the functionality that loaders couldn't. Loaders are constrained to perform transformations on single file right before it is added to dependency graph. You need plugin for minifying your code, bundling etc. Plugins is a class and you can pass arguments/config to the constructor.

```
 plugins: [
    new webpack.DefinePlugin({
      'process.env': {
        NODE_ENV: JSON.stringify(env.prod ? 'production' : 'development'),
      },
    }),
  ],
```

## Example Projects:

https://github.com/kentcdodds/es6-todomvc

### Awesome webpack

https://github.com/webpack-contrib/awesome-webpack

### Tutorial

Excellent tutorial by Sean Larkin - https://webpack.academy/

https://survivejs.com/webpack/what-is-webpack/
