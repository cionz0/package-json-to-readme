# {{name}} {{version}} {{#travis_url}} [![Build Status]({{travis_url}}.png?branch=master)]({{travis_url}}){{/travis_url}}

{{description}}

{{^private}}
## Installation

This is a [Node.js](https://nodejs.org/) module available through:
{{#npmregistry}}
- the [npm registry](https://www.npmjs.com/)
{{/npmregistry}}
{{#install_from_git}}
- the [github repository](https://www.github.com/)
{{/install_from_git}}.

It can be installed using the 
[`npm`](https://docs.npmjs.com/getting-started/installing-npm-packages-locally)
or 
[`yarn`](https://yarnpkg.com/en/)
command line tools.

```sh
{{#npmregistry}}
{{#preferGlobal}}
npm install {{name}} --global
{{/preferGlobal}}
{{^preferGlobal}}
npm install {{name}} --save
{{/preferGlobal}}
{{/npmregistry}}
{{#install_from_git}}
{{#preferGlobal}}
npm install git+{{repository}} --global
{{/preferGlobal}}
{{^preferGlobal}}
npm install git+{{repository}} --save
{{/preferGlobal}}
{{/install_from_git}}
```


{{/private}}
{{#usage}}

## Usage

```{{language}}
{{{content}}}
```
{{/usage}}
{{#scripts.test}}

## Tests

```sh
npm install
npm test
```
{{/scripts.test}}
{{#testOutput}}
```
{{{testOutput}}}
```
{{/testOutput}}

## Dependencies

{{#depDetails}}
- [{{name}}]({{repository}}): {{description}}
{{/depDetails}}
{{^depDetails}}
None
{{/depDetails}}

## Dev Dependencies

{{#devDepDetails}}
- [{{name}}]({{repository}}): {{description}}
{{/devDepDetails}}
{{^devDepDetails}}
None
{{/devDepDetails}}

{{#license}}
## License

{{license}}
{{/license}}
