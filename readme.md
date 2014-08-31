# exit-hook [![Build Status](https://travis-ci.org/sindresorhus/exit-hook.svg?branch=master)](https://travis-ci.org/sindresorhus/exit-hook)

> Run some code when the process exits

The `process.on('exit')` event doesn't catch all the ways a process can exit.

Useful for cleaning up.


## Install

```sh
$ npm install --save exit-hook
```


## Usage

```js
var exitHook = require('exit-hook');

exitHook(function () {
	console.log('exiting');
});

throw new Error('unicorns');

//=> exiting
```


## License

MIT © [Sindre Sorhus](http://sindresorhus.com)
