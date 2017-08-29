# webpack-fundamentals

Webpack+NPM == Grunt/Gulp

## CLI Basics
```
$ npm install webpack -g - Install webpack globally
$ webpack ./in.js out.js - Building a single file, build in.js --> out.js
$ webpack --watch - Run webpack in watch mode
$ webpack-dev-server - Starts local server, files served via http, scoped in an iframe in browser
$ webpack-dev-server --inline - Starts local server, files served directly to browser via http, no iframe, auto-reload works. 
```

## Config File - commonJS module
```
module.exports = {
  entry:"./in.js", //files that go into the build pipe
  output:{
    filename:"bundle.js" //build out file
  },
  modules:{
    preLoaders: [{ //These will process files before loaders, linters, static code analysers, etc...
      test: /\.js$/,
      exclude: 'node_modules',
      loader: 'jshint' //linter
    }]
    loaders: [{
      test: /\.es6$/, //regex patterns that match filenames that the loader must process
      exclude: /node_modules/, //regex for files to ignore/exclude
      loader: "babel-loader" //name of loader, must be installed via npm, present in package.json
    }]
  },
  resolve: {
    extensions:['','.es6','.js','.ts',...], //specify what type of files can be processed without specifying a file extension
  },
  watch: true //enter watch mode
}
```
