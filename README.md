publisher.js
================================================================================

**Cross-cut your concerns with published authority.**

* [Read the guide][guide]
* [Read the really neat part of the guide][cool-part]
* [The guide on jsFiddle](http://jsfiddle.net/rpflorence/6QScG/)
* [Report an issue][issues]

`publisher.js` is a sophisticated mix of publish/subscribe (pub/sub) and
Aspect-Oriented Programming that facilitates autonomous JavaScript module
development.

In other words, your modules don't have to know about other modules, or the
application, or even the `publisher` object--they can be 100% self-contained.
The `publisher` object handles all of the cross-cutting concerns, connecting
your objects together.

Installation and Universal JavaScript Support
--------------------------------------------------------------------------------

`publisher` works as an AMD (RequireJS) module, a Node.js module, or a plain
object. If neither AMD nor Node.js environments are detected, the publisher
object is assigned to the global object (window).

### AMD (RequireJS) installation

Place `publisher.js` in your application and require it as usual.

```javascript
require(['path/to/publisher'], function (publisher) {
  /* Do stuff with publisher here */
});
```

### Node.js Installation

Install with npm

    npm install publisher

Include like everything else

```javascript
var publisher = require('publisher');
```

### Other browser usage

If neither AMD nor Node.js are detected, publisher is global with a
`noConflict` that restores the previous `publisher` definition and returns
the publisher object.

```javascript
publisher
publisher.noConflict();
```

License & Copyright
--------------------------------------------------------------------------------

Copyright (c) Ryan Florence

MIT-Style License

Contributing
--------------------------------------------------------------------------------

Fork, create a topic branch, send a pull request :D

### Development dependencies

While `publisher` has no dependencies, developing it does.

You'll need to install some stuff to run the tests and generate docs.  There's
a script in `bin` to help.  First make sure you've got Node.js, npm, and
Python installed, then simply run from the repository root:

    $ ./bin/setup-dev

### Running tests

    $ ./bin/run-tests
    # or
    $ tap test/test.js

### Generating docs

    $ ./bin/generate-docs

[guide]:http://ryanflorence.com/publisher.js/
[cool-part]:http://ryanflorence.com/publisher.js/#section-41
[issues]:https://github.com/rpflorence/publisher.js/issues/new
