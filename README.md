# The bindable middleware

The `bindable` middleware adds the `$bindable` method to elements, which can be used to make any element bindable.

- name: bindable
- middleware dependencies: [attributes](https://github.com/nx-js/attributes-middleware)
- all middleware dependencies: [observe](https://github.com/nx-js/observe-middleware), [attributes](https://github.com/nx-js/attributes-middleware)
- type: component or content middleware
- ignores: text nodes
- [docs](http://nx-framework.com/docs/middlewares/bind)

## Installation

`npm install @nx-js/bindable-middleware`

## Usage

```js
const component = require('@nx-js/core')
const observe = require('@nx-js/observe-middleware')
const attributes = require('@nx-js/attributes-middleware')
const style = require('@nx-js/bindable-middleware')

component()
  .use(observe)
  .use(attributes)
  .use(bindables)
  .use(elem => elem.$bindable({mode: 'two-way', on: 'input'}))
  .register('bindable-comp')
```

```html
<bindable-comp name="prop" bind></bindable-comp>
```
