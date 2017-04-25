# npmdoc-backoff

#### basic api documentation for  [backoff (v2.5.0)](https://github.com/MathieuTurcotte/node-backoff#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-backoff.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-backoff) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-backoff.svg)](https://travis-ci.org/npmdoc/node-npmdoc-backoff)

#### Fibonacci and exponential backoffs.

[![NPM](https://nodei.co/npm/backoff.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/backoff)

- [https://npmdoc.github.io/node-npmdoc-backoff/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-backoff/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-backoff/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-backoff/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-backoff/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-backoff/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mathieu Turcotte"
    },
    "bugs": {
        "url": "https://github.com/MathieuTurcotte/node-backoff/issues"
    },
    "dependencies": {
        "precond": "0.2"
    },
    "description": "Fibonacci and exponential backoffs.",
    "devDependencies": {
        "nodeunit": "0.9",
        "sinon": "1.10"
    },
    "directories": {},
    "dist": {
        "shasum": "f616eda9d3e4b66b8ca7fca79f695722c5f8e26f",
        "tarball": "https://registry.npmjs.org/backoff/-/backoff-2.5.0.tgz"
    },
    "engines": {
        "node": ">= 0.6"
    },
    "files": [
        "index.js",
        "lib",
        "tests"
    ],
    "gitHead": "811118fd1f89e9ca4e6b67292b9ef5da6c4f60e9",
    "homepage": "https://github.com/MathieuTurcotte/node-backoff#readme",
    "keywords": [
        "backoff",
        "retry",
        "fibonacci",
        "exponential"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "mathieu"
        }
    ],
    "name": "backoff",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/MathieuTurcotte/node-backoff.git"
    },
    "scripts": {
        "docco": "docco lib/*.js lib/strategy/* index.js",
        "pretest": "jshint lib/ tests/ examples/ index.js",
        "test": "node_modules/nodeunit/bin/nodeunit tests/"
    },
    "version": "2.5.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
