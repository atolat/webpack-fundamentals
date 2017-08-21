# webpack-fundamentals

## CLI Basics
```
$ npm install webpack -g - Install webpack globally
$ webpack ./in.js out.js - Building a single file, build in.js --> out.js
$ webpack --watch - Run webpack in watch mode
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
