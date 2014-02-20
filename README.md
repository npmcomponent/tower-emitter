*This repository is a mirror of the [component](http://component.io) module [tower/emitter](http://github.com/tower/emitter). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/tower-emitter`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# Tower Emitter

Event emitter component (started from component/emitter).

## Installation

node.js:

```bash
$ npm install tower-emitter
```

browser:

```bash
$ component install tower/emitter
```

## API

### Emitter(obj)

  The `Emitter` may also be used as a mixin. For example
  a "plain" object may become an emitter, or you may
  extend an existing prototype.

  As an `Emitter` instance:

```js
var Emitter = require('emitter');
var emitter = new Emitter;
emitter.emit('something');
```

  As a mixin:

```js
var Emitter = require('emitter');
var user = { name: 'tobi' };
Emitter(user);

user.emit('im a user');
```

  As a prototype mixin:

```js
var Emitter = require('emitter');
Emitter(User.prototype);
```
  
### Emitter#on(event, fn)

  Register an `event` handler `fn`.

### Emitter#once(event, fn)

  Register a single-shot `event` handler `fn`,
  removed immediately after it is invoked the
  first time.

### Emitter#off(event, fn)

  Remove `event` handler `fn`, or pass only the `event`
  name to remove all handlers for `event`.

### Emitter#emit(event, ...)

  Emit an `event` with variable option args.

### Emitter#listeners(event)

  Return an array of callbacks, or an empty array.

### Emitter#hasListeners(event)

  Check if this emitter has `event` handlers.

## Notes

- https://github.com/component/clone/blob/master/index.js

## Testing

Install testem:

```bash
$ npm install -g testem
```

Run tests:

```bash
$ testem
```

Then, open all the browsers you want to test by going to the outputted url defaulted to [http://localhost:7357](http://localhost:7357)

Tests will run on any open browser linked to the stated url and your current Node environment.

## Contributing

Before you send a pull request, make sure your code meets the style guidelines at [https://github.com/tower/style-guide](https://github.com/tower/style-guide) and all tests pass.

## License

MIT