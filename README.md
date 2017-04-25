# npmtest-tweetnacl

#### basic test coverage for  [tweetnacl (v0.14.5)](https://tweetnacl.js.org)  [![npm package](https://img.shields.io/npm/v/npmtest-tweetnacl.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-tweetnacl) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-tweetnacl.svg)](https://travis-ci.org/npmtest/node-npmtest-tweetnacl)

#### Port of TweetNaCl cryptographic library to JavaScript

[![NPM](https://nodei.co/npm/tweetnacl.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/tweetnacl)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-tweetnacl/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-tweetnacl/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-tweetnacl/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-tweetnacl/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-tweetnacl/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-tweetnacl/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-tweetnacl/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-tweetnacl/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-tweetnacl/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-tweetnacl/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-tweetnacl/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-tweetnacl/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-tweetnacl/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-tweetnacl/build/test-report.html](https://npmtest.github.io/node-npmtest-tweetnacl/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-tweetnacl/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-tweetnacl/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-tweetnacl/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-tweetnacl/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tweetnacl/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tweetnacl/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-tweetnacl/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-tweetnacl/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "TweetNaCl-js contributors"
    },
    "browser": {
        "buffer": false,
        "crypto": false
    },
    "bugs": {
        "url": "https://github.com/dchest/tweetnacl-js/issues"
    },
    "dependencies": {},
    "description": "Port of TweetNaCl cryptographic library to JavaScript",
    "devDependencies": {
        "browserify": "^13.0.0",
        "eslint": "^2.2.0",
        "faucet": "^0.0.1",
        "tap-browser-color": "^0.1.2",
        "tape": "^4.4.0",
        "tape-run": "^2.1.3",
        "tweetnacl-util": "^0.13.3",
        "uglify-js": "^2.6.1"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "5ae68177f192d4456269d108afa93ff8743f4f64",
        "tarball": "https://registry.npmjs.org/tweetnacl/-/tweetnacl-0.14.5.tgz"
    },
    "gitHead": "cce829e473b1ae299a9373b5140c713ee88f577f",
    "homepage": "https://tweetnacl.js.org",
    "keywords": [
        "crypto",
        "cryptography",
        "curve25519",
        "ed25519",
        "encrypt",
        "hash",
        "key",
        "nacl",
        "poly1305",
        "public",
        "salsa20",
        "signatures"
    ],
    "license": "Unlicense",
    "main": "nacl-fast.js",
    "maintainers": [
        {
            "name": "dchest"
        }
    ],
    "name": "tweetnacl",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dchest/tweetnacl-js.git"
    },
    "scripts": {
        "bench": "node test/benchmark/bench.js",
        "build": "uglifyjs nacl.js -c -m -o nacl.min.js && uglifyjs nacl-fast.js -c -m -o nacl-fast.min.js",
        "build-test-browser": "browserify test/browser/init.js test/*.js | uglifyjs -c -m -o test/browser/_bundle.js 2>/dev/null && browserify test/browser/init.js test/*.quick.js | uglifyjs -c -m -o test/browser/_bundle-quick.js 2>/dev/null",
        "lint": "eslint nacl.js nacl-fast.js test/*.js test/benchmark/*.js",
        "test": "npm run test-node-all && npm run test-browser",
        "test-browser": "NACL_SRC=${NACL_SRC:='nacl.min.js'} && npm run build-test-browser && cat $NACL_SRC test/browser/_bundle.js | tape-run | faucet",
        "test-node": "tape test/*.js | faucet",
        "test-node-all": "make -C test/c && tape test/*.js test/c/*.js | faucet"
    },
    "types": "nacl.d.ts",
    "version": "0.14.5",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
