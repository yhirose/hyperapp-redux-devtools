# hyperapp-redux-devtools
hyperapp mixin to utilize redux-devtools-extension from hyperapp

* NOTE: hyperapp >= 0.11 requires version 1.0.5 of this package

```js
import { h, app } from 'hyperapp';
import devtools from 'hyperapp-redux-devtools';

app({
  state: { count: 0},
  view: (state, actions) => {
    return (
      <div>
        <button onclick={actions.increment}>Click</button>
        <span>{state.count}</span>
      </div>
    );
  },
  actions: {
    increment: (state) => Object.assign({}, state, { count: state.count + 1 })
  },
  mixins: [devtools()]
});

```
