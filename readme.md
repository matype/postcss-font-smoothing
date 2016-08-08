# postcss-font-smoothing [![Build Status](https://travis-ci.org/morishitter/postcss-font-smoothing.svg)](https://travis-ci.org/morishitter/postcss-font-smoothing)

PostCSS plugin to fallback font-smoothing property

## Installation

```shell
$ npm install postcss-font-smoothing
```

## Example

input:

```css
.font {
  font-smoothing: antialiased;
}
```

output:
```css
.font {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
```

## Usage

```js
// dependencies
var fs = require("fs")
var postcss = require("postcss")
var fontSmoothing = require("postcss-font-smoothing")

// css to be processed
var css = fs.readFileSync("input.css", "utf8")

// process css
var output = postcss()
  .use(fontSmoothing())
  .process(css)
  .css
```

## License

The MIT License (MIT)

Copyright (c) 2016 Masaaki Morishita
