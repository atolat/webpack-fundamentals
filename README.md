# webpack-fundamentals

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
  watch: true //enter watch mode
}
```
