# exenv

React's ExecutionEnvironment module extracted for use in other packages &amp; components.

## Why?

Because a lot of packages and components use React's private ExecutionEnvironment lib to detect the environment, e.g

```
canUseDOM = require('react/lib/ExecutionEnvironment').canUseDOM;
```

It is bad practice to use React internals and this is likely to be broken / disabled in the future. Use this package instead.

## Usage

```
npm install exenv --save
```

```js
var ExecutionEnvironment = require('exenv');

// You now have...
ExecutionEnvironment.canUseDOM             // is the DOM available? i.e window document etc. 
ExecutionEnvironment.canUseWorkers         // are Web Workers available?
ExecutionEnvironment.canUseEventListeners  // are Events available? i.e addEventListener etc.
ExecutionEnvironment.canUseViewport        // is there a viewport? i.e window.screen
```