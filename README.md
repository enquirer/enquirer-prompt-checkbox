# enquirer-prompt-checkbox [![NPM version](https://img.shields.io/npm/v/enquirer-prompt-checkbox.svg?style=flat)](https://www.npmjs.com/package/enquirer-prompt-checkbox) [![NPM downloads](https://img.shields.io/npm/dm/enquirer-prompt-checkbox.svg?style=flat)](https://npmjs.org/package/enquirer-prompt-checkbox)

> Adds multiple-choice/checkbox prompt support to Enquirer.

![checkbox prompt example](https://raw.githubusercontent.com/enquirer/enquirer-prompt-checkbox/master/example.gif)

## Usage

```js
var Enquirer = require('enquirer');
var enquirer = new Enquirer();

enquirer.register('checkbox', require('enquirer-prompt-checkbox'));
```

## Example

[Enquirer](https://github.com/jonschlinkert/enquirer) supports both the declarative inquirer-style question format and a functional format using the `.question` method:

**.question**

Functional style questions.

```js
var Enquirer = require('enquirer');
var enquirer = new Enquirer();

enquirer.register('checkbox', require('enquirer-prompt-checkbox'));
enquirer.question('color', 'What is your favorite color?', {
  type: 'checkbox',
  default: 'blue',
  choices: ['red', 'yellow', 'blue']
});

enquirer.ask('color')
  .then(function(answers) {
    console.log(answers)
  });
```

**Inquirer-style questions**

Declarative questions format.

```js
var Enquirer = require('enquirer');
var enquirer = new Enquirer();

enquirer.register('checkbox', require('enquirer-prompt-checkbox'));

var questions = [
  {
    name: 'color',
    message: 'What is your favorite color?',
    type: 'checkbox',
    default: 'blue',
    choices: ['red', 'yellow', 'blue']
  }
];

enquirer.ask(questions)
  .then(function(answers) {
    console.log(answers)
  });
```

## Attribution

Based on the `checkbox` prompt in inquirer.

## About

### Related projects

* [enquirer-prompt](https://www.npmjs.com/package/enquirer-prompt): Base prompt module used for creating custom prompt types for Enquirer. | [homepage](https://github.com/enquirer/enquirer-prompt "Base prompt module used for creating custom prompt types for Enquirer.")
* [enquirer-question](https://www.npmjs.com/package/enquirer-question): Question object, used by Enquirer and prompt plugins. | [homepage](https://github.com/enquirer/enquirer-question "Question object, used by Enquirer and prompt plugins.")
* [enquirer](https://www.npmjs.com/package/enquirer): Plugin-based prompt system for node.js | [homepage](https://github.com/jonschlinkert/enquirer "Plugin-based prompt system for node.js")

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

### License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/enquirer/enquirer-prompt-checkbox/blob/master/LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.1.30, on August 29, 2016._