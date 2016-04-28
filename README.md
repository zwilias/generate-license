# generate-license [![NPM version](https://img.shields.io/npm/v/generate-license.svg?style=flat)](https://www.npmjs.com/package/generate-license) [![NPM downloads](https://img.shields.io/npm/dm/generate-license.svg?style=flat)](https://npmjs.org/package/generate-license) [![Build Status](https://img.shields.io/travis/generate/generate-license.svg?style=flat)](https://travis-ci.org/generate/generate-license)

Generate a license file for a GitHub project.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install generate-license --save
```

## CLI

Run the `license` generator from the command line:

```sh
$ gen license
```

## Tasks

### [default](generator.js#L27)

Alias for the [mit](#mit) task.

**Example**

```sh
$ gen git
```

### [license](generator.js#L39)

Alias for the [mit](#mit) task.

**Example**

```sh
$ gen git:license
```

### [mit](generator.js#L51)

Initialize a git repository, including `git add` and first commit.

**Example**

```sh
$ gen git:mit
```

## API

To use this generator programmatically, as a plugin or sub-generator, you must first install the generator locally.

### Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install generate-license
```

### Usage

Then use in your project:

```js
var license = require('generate-license');
```

**Use as a plugin**

In your [generate](https://github.com/generate/generate) project:

```js
var generate = require('generate');
var app = generate();

app.use(license());
```

**Use as a generator plugin**

In your [generate](https://github.com/generate/generate) generator:

```js
module.exports = function(app) {
  app.use(license());
};
```

**Use as a sub-generator**

In your [generate](https://github.com/generate/generate) generator:

```js
module.exports = function(app) {
  // name the sub-generator whatever you want
  app.register('foo', require('generate-license'));
};
```

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/generate/generate-license/issues/new).

## Building docs

Generate readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install verb && npm run docs
```

Or, if [verb](https://github.com/verbose/verb) is installed globally:

```sh
$ verb
```

## Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/generate/generate-license/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on April 28, 2016._