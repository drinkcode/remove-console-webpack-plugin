# remove-console-webpack-plugin
A light webpack plugin to remove console.* in your JS code without any dependency.

## Example

**In**

```js
console.log("log test"); // by default
console.error("error test"); // need to configure
```

**Out**

```js
```

## Installation
```sh
npm install remove-console-webpack-plugin --save-dev
```

## Usage
```js
// webpack.config.js
const RemoveConsolePlugin = require('remove-console-webpack-plugin')

// demo1: remove console.log by default
module.exports = {
  // other code ...
  plugins: [
    new RemoveConsolePlugin({ include: ['log', 'warn', 'error'] })
  ]
}

// demo2: remove console.log, console.warn, console.error 
module.exports = {
  // other code ...
  plugins: [
    new RemoveConsolePlugin({ include: ['log', 'warn', 'error'] })
  ]
}

// demo3: don't remove console.*
module.exports = {
  // other code ...
  plugins: [
    new RemoveConsolePlugin({ include: [] })
  ]
}
```


## Options
| option | description | default |
| ------ | ----------- | ------- |
| include | An array of console methods that you want to remove. | ['log']|
