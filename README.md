# vue-viewports

> define your custom viewports and use them in your components

## Status

[![Build Status](https://travis-ci.org/scaccogatto/vue-viewports.svg?branch=master)](https://travis-ci.org/scaccogatto/vue-viewports)

## Features

- Uses [requestAnimationFrame](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame)
- Exposes a fully updated viewport name
- Exposes the event name fired by requestAnimationFrame

## Installation

### npm
```
$ npm install vue-viewports --save-dev
```

### Vue's main.js
```js
import VueViewports from 'vue-viewports'

Vue.use(VueViewports, { 0: 'sub-mobile', 420: 'mobile', 768: 'tablet', 1024: 'desktop', 1920: 'hd-desktop', 2560: 'qhd-desktop', 3840: 'uhd-desktop' })
```
### Arguments
- options [optional]: object defining a set of `{ key: value }` where 'key' is the number value (px) where the viewport starts (included) and the 'value' is the viewport's name, **defaults** on previous example

## Example
```js
{
  if (this.$currentViewport.label === 'mobile') {
    // mobile viewport
  } else {
    // more than mobile
  }
}
```

## API

## Variables
- `$currentViewport`: the current viewport object, defined by `label`, `value` and a private `_windowWidth` for testing purposes
- `$viewportsUpdateEventName`: the event name, called on window (you can catch it if needed)

## Testing
This software uses [mocha](https://mochajs.org/) as testing framework

- Clone this repository
- `cd vue-viewports`
- `npm install`
- `npm test`

*Feel free to contribute and ask questions*
