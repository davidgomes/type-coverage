# type-coverage

A CLI tool to check type coverage for typescript code

This tool will check type of all identifiers, `the code coverage` = `the count of identifiers whose type is not any` / `the total count of identifiers`, the higher, the better. This count will include JavaScript files inside the same project structure (all the identifiers in these files are untyped). 

[![Dependency Status](https://david-dm.org/plantain-00/type-coverage.svg)](https://david-dm.org/plantain-00/type-coverage)
[![devDependency Status](https://david-dm.org/plantain-00/type-coverage/dev-status.svg)](https://david-dm.org/plantain-00/type-coverage#info=devDependencies)
[![Build Status: Linux](https://travis-ci.org/plantain-00/type-coverage.svg?branch=master)](https://travis-ci.org/plantain-00/type-coverage)
[![Build Status: Windows](https://ci.appveyor.com/api/projects/status/github/plantain-00/type-coverage?branch=master&svg=true)](https://ci.appveyor.com/project/plantain-00/type-coverage/branch/master)
[![npm version](https://badge.fury.io/js/type-coverage.svg)](https://badge.fury.io/js/type-coverage)
[![Downloads](https://img.shields.io/npm/dm/type-coverage.svg)](https://www.npmjs.com/package/type-coverage)
[![type-coverage](https://img.shields.io/badge/dynamic/json.svg?label=type-coverage&prefix=%E2%89%A5&suffix=%&query=$.typeCoverage.atLeast&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fplantain-00%2Ftype-coverage%2Fmaster%2Fpackage.json)](https://github.com/plantain-00/type-coverage)

## install

`yarn global add type-coverage`

## usage

run `type-coverage`

## arguments

name | type | description
--- | --- | ---
-p, --project | string? | show where is the `tsconfig.json`
--detail | boolean? | show detail
--at-least | number? | fail if coverage rate < this value
--debug | boolean? | show debug info

## config in package.json

```json
  "typeCoverage": {
    "atLeast": 99 // same as --at-least
  },
```

## vscode plugin

<https://marketplace.visualstudio.com/items?itemName=york-yao.vscode-type-coverage>

## add dynamic badges of type coverage

Use your own project url:

```md
[![type-coverage](https://img.shields.io/badge/dynamic/json.svg?label=type-coverage&prefix=%E2%89%A5&suffix=%&query=$.typeCoverage.atLeast&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fplantain-00%2Ftype-coverage%2Fmaster%2Fpackage.json)](https://github.com/plantain-00/type-coverage)
```

## FAQ

> Q: Does this count JavaScript files?

Yes, This package calls Typescript API, Typescript can parse Javascript file(with `allowJs`), then this package can too.
