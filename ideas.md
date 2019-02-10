
State machine modeled on a component like API.
```javascript
import {State, Machine} from 'state-machine';

const on = new State({
  actions: {
    power: () => {}
  }
});

const off = new State({
  actions: {
    power: () => {}
  }
});

const m = new Machine({
  initial: on,
  states: {
    on,
    off
  },
  transition: [
    ['on', 'power', 'off'],
    ['off', 'power', 'on'],
  ]
});

```