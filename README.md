# npmdoc-json-rpc2

#### api documentation for  [json-rpc2 (v1.0.2)](https://github.com/pocesar/node-jsonrpc2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-json-rpc2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-json-rpc2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-json-rpc2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-json-rpc2)

#### JSON-RPC 2.0 server and client library, with HTTP, TCP and Websocket endpoints

[![NPM](https://nodei.co/npm/json-rpc2.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/json-rpc2)

- [https://npmdoc.github.io/node-npmdoc-json-rpc2/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Eric Florenzano",
        "url": "eflorenzano.com"
    },
    "bugs": {
        "url": "https://github.com/pocesar/node-jsonrpc2/issues"
    },
    "contributors": [
        {
            "name": "Bill Casarin",
            "url": "jb55.com"
        },
        {
            "name": "Stefan Thomas",
            "url": "justmoon.net"
        },
        {
            "name": "Paulo Cesar",
            "url": "github.com/pocesar"
        }
    ],
    "dependencies": {
        "debug": "2.x.x",
        "es5class": "2.x.x",
        "eventemitter3": "1.x.x",
        "faye-websocket": "0.x.x",
        "jsonparse": "1.x.x",
        "lodash": "3.x.x",
        "object-assign": "4.x"
    },
    "description": "JSON-RPC 2.0 server and client library, with HTTP, TCP and Websocket endpoints",
    "devDependencies": {
        "expect.js": "0.x.x",
        "istanbul": "0.x.x",
        "jshint": "2.x.x",
        "mocha": "2.x.x"
    },
    "directories": {},
    "dist": {
        "shasum": "eb77bd27b1df606c23702c4e35d4afc54742ae8d",
        "tarball": "https://registry.npmjs.org/json-rpc2/-/json-rpc2-1.0.2.tgz"
    },
    "engines": {
        "node": "0.10.x || 0.12.x"
    },
    "gitHead": "4c0d49021728d2c32fa07ae4cde8f0fe8ccb044f",
    "homepage": "https://github.com/pocesar/node-jsonrpc2#readme",
    "keywords": [
        "json",
        "rpc",
        "rpc2",
        "json-rpc",
        "json-rpc2",
        "jsonrpc",
        "jsonrpc2",
        "server",
        "client",
        "tcp",
        "websocket",
        "http"
    ],
    "license": "MIT",
    "main": "./src/jsonrpc.js",
    "maintainers": [
        {
            "name": "pocesar"
        }
    ],
    "name": "json-rpc2",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/pocesar/node-jsonrpc2.git"
    },
    "scripts": {
        "coverage": "node ./node_modules/istanbul/lib/cli.js cover ./node_modules/mocha/bin/_mocha -- -t 5000 test/jsonrpc-test.js",
        "test": "jshint examples src test && mocha test/*.js"
    },
    "version": "1.0.2",
    "warnings": [
        {
            "code": "ENOTSUP",
            "required": {
                "node": "0.10.x || 0.12.x"
            },
            "pkgid": "json-rpc2@1.0.2"
        },
        {
            "code": "ENOTSUP",
            "required": {
                "node": "0.10.x || 0.12.x"
            },
            "pkgid": "json-rpc2@1.0.2"
        }
    ]
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
