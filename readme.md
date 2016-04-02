# eslint-bom-test

This module simply for diagnostic purposes to help demonstrates the problems listed in the following issues:

ESLint Issue [#5766](https://github.com/eslint/eslint/issues/5766)
XO Issue [#96](https://github.com/sindresorhus/xo/issues/95)

## Install 

```
$ git clone https://github.com/radiovisual/eslint-bom-test.git
$ cd eslint-bom-test
$ npm install
```

## Recreate the Problem

1. The following command yields **no results:**
```
$ npm run test
```

2. The following command yields **3 errors:**
```
$ xo
```

## The Problem?

The problem is that both commands `$ npm run test` and `$ xo` should return the same results, **and** XO should be ignoring 
 the Unicode BOM, because [ESLint strips the Unicode BOM from files before linting](https://github.com/eslint/eslint/issues/4878).
   
## Notes

The contained file `utf8-bom.js` has an intentional UTF8 BOM character at the beginning of the file.

