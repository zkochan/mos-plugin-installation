<!--@h1([pkg.name])-->
# mos-plugin-installation
<!--/@-->

<!--@blockquote([pkg.description])-->
> A mos plugin for creating installation section
<!--/@-->

<!--@shields.flatSquare('npm', 'travis', 'coveralls')-->
[![NPM version](https://img.shields.io/npm/v/mos-plugin-installation.svg?style=flat-square)](https://www.npmjs.com/package/mos-plugin-installation) [![Build status for master](https://img.shields.io/travis/zkochan/mos-plugin-installation/master.svg?style=flat-square)](https://travis-ci.org/zkochan/mos-plugin-installation) [![Test coverage for master](https://img.shields.io/coveralls/zkochan/mos-plugin-installation/master.svg?style=flat-square)](https://coveralls.io/r/zkochan/mos-plugin-installation?branch=master)
<!--/@-->

<!--@installation({useShortAlias: true})-->
## Installation

```sh
npm i -S mos-plugin-installation
```
<!--/@-->

## Usage

Add this code snippet to your `README.md`

```md
<!--@installation()-->
<!--/@-->
```

Run `mos` in the terminal.

You'll get an installation section in your README that will instruct how to install the package via npm.

The plugin will use information from the `package.json` in order to figure out what should the installation command look like.

- If there is a `preferGlobal: true` specified in the `package.json`, the generated command will be `npm install --global`
- If there is a `preferDev: true` specified in the `package.json`, the generated command will be `npm install --save-dev`
- If there is a `private: true`, the command instruction will suggest to clone the repo and install its dependencies
- Otherwise, the generated command will be `npm install --save`

If the package has `peerDependencies`, the installation command will suggest to install all the peer dependencies with the package.

## API

`installation(opts)`

- `opts.useShortAlias` - _Boolean_, false by default. If true, uses shorter aliases in the installation command. `i` instead of `install`, `-S` instead of `--save`, etc.

<!--@license()-->
## License

[MIT](./LICENSE) © [Zoltan Kochan](http://kochan.io)
<!--/@-->

* * *

<!--@dependencies({ shield: 'flat-square' })-->
## <a name="dependencies">Dependencies</a> [![Dependency status for master](https://img.shields.io/david/zkochan/mos-plugin-installation/master.svg?style=flat-square)](https://david-dm.org/zkochan/mos-plugin-installation/master)

- [markdownscript](https://github.com/zkochan/markdownscript): Creates markdown Abstract Syntax Tree

<!--/@-->

<!--@devDependencies({ shield: 'flat-square' })-->
## <a name="dev-dependencies">Dev Dependencies</a> [![devDependency status for master](https://img.shields.io/david/dev/zkochan/mos-plugin-installation/master.svg?style=flat-square)](https://david-dm.org/zkochan/mos-plugin-installation/master#info=devDependencies)

- [chai](https://github.com/chaijs/chai): BDD/TDD assertion library for node.js and the browser. Test framework agnostic.
- [cz-conventional-changelog](https://github.com/commitizen/cz-conventional-changelog): Commitizen adapter following the conventional-changelog format.
- [eslint](https://github.com/eslint/eslint): An AST-based pattern checker for JavaScript.
- [eslint-config-standard](https://github.com/feross/eslint-config-standard): JavaScript Standard Style - ESLint Shareable Config
- [eslint-plugin-promise](https://github.com/xjamundx/eslint-plugin-promise): Enforce best practices for JavaScript promises
- [eslint-plugin-standard](https://github.com/xjamundx/eslint-plugin-standard): ESlint Plugin for the Standard Linter
- [ghooks](https://github.com/gtramontina/ghooks): Simple git hooks
- [istanbul](https://github.com/gotwarlost/istanbul): Yet another JS code coverage tool that computes statement, line, function and branch coverage with module loader hooks to transparently add coverage when running tests. Supports all JS coverage use cases including unit tests, server side functional tests
- [mocha](https://github.com/mochajs/mocha): simple, flexible, fun test framework
- [mos](https://github.com/zkochan/mos): A pluggable module that injects content into your markdown files via hidden JavaScript snippets
- [semantic-release](https://github.com/semantic-release/semantic-release): automated semver compliant package publishing
- [validate-commit-msg](https://github.com/kentcdodds/validate-commit-msg): Script to validate a commit message follows the conventional changelog standard

<!--/@-->
