# package-json-to-readme 0.0.0-development 

Generate a README.md from package.json contents

## Installation

This is a [Node.js](https://nodejs.org/) module available through:
- the [github repository](https://www.github.com/)
.

It can be installed using the 
[`npm`](https://docs.npmjs.com/getting-started/installing-npm-packages-locally)
or 
[`yarn`](https://yarnpkg.com/en/)
command line tools.

```sh
npm install git+https://github.com/cionz0/package-json-to-readme --global
```



## Usage

```sh
# Write to stdout
readme package.json

# Pipe output into a new file
readme package.json > README.md

# Add a Travis badge
readme package.json --travis

# Run tests and add their output
readme package.json --tests

# Do it all
readme package.json --tests --travis > README.md

# If your package has an example.sh or example.js file, it will be used to
# generate a usage section like this one.

# If your example.js has a require("./") statement, the relative path will be
# replaced with the package name.

```

## Tests

```sh
npm install
npm test
```

## Dependencies

- [github-url-to-object](https://ghub.io/github-url-to-object): Extract user, repo, and other interesting properties from GitHub URLs
- [hogan.js](https://ghub.io/hogan.js): A mustache compiler.
- [strip-ansi](https://ghub.io/strip-ansi): Strip ANSI escape codes
- [yargs](https://ghub.io/yargs): Light-weight option parsing with an argv hash. No optstrings attached.

## Dev Dependencies

- [mocha](https://ghub.io/mocha): simple, flexible, fun test framework
- [nixt](https://ghub.io/nixt): Simple and powerful testing for command-line apps
- [standard](https://ghub.io/standard): JavaScript Standard Style
- [semantic-release](https://ghub.io/semantic-release): Automated semver compliant package publishing

## License

MIT
