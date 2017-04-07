# api documentation for  [json-rpc2 (v1.0.2)](https://github.com/pocesar/node-jsonrpc2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-json-rpc2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-json-rpc2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-json-rpc2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-json-rpc2)
#### JSON-RPC 2.0 server and client library, with HTTP, TCP and Websocket endpoints

[![NPM](https://nodei.co/npm/json-rpc2.png?downloads=true)](https://www.npmjs.com/package/json-rpc2)

[![apidoc](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-json-rpc2_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-json-rpc2/build/apidoc.html)

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
            "email": "bill@casarin.ca",
            "url": "jb55.com"
        },
        {
            "name": "Stefan Thomas",
            "email": "justmoon@members.fsf.org",
            "url": "justmoon.net"
        },
        {
            "name": "Paulo Cesar",
            "email": "email@pocesar.e4ward.com",
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
            "name": "pocesar",
            "email": "email@pocesar.e4ward.com"
        }
    ],
    "name": "json-rpc2",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module json-rpc2](#apidoc.module.json-rpc2)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Client ()](#apidoc.element.json-rpc2.Client)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Connection ()](#apidoc.element.json-rpc2.Connection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>ES5Class ()](#apidoc.element.json-rpc2.ES5Class)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Endpoint ()](#apidoc.element.json-rpc2.Endpoint)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Error.AbstractError ()](#apidoc.element.json-rpc2.Error.AbstractError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>EventEmitter ()](#apidoc.element.json-rpc2.EventEmitter)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>HttpServerConnection ()](#apidoc.element.json-rpc2.HttpServerConnection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Server ()](#apidoc.element.json-rpc2.Server)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>SocketConnection ()](#apidoc.element.json-rpc2.SocketConnection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>WebSocketConnection ()](#apidoc.element.json-rpc2.WebSocketConnection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket (request, socket, body, protocols, options)](#apidoc.element.json-rpc2.Websocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.Client (_url, protocols, options)](#apidoc.element.json-rpc2.Websocket.Client)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.EventSource (request, response, options)](#apidoc.element.json-rpc2.Websocket.EventSource)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.super_ (options)](#apidoc.element.json-rpc2.Websocket.super_)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_ (value)](#apidoc.element.json-rpc2._)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.bind ()](#apidoc.element.json-rpc2._.bind)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.bindKey ()](#apidoc.element.json-rpc2._.bindKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.curry (func, arity, guard)](#apidoc.element.json-rpc2._.curry)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.curryRight (func, arity, guard)](#apidoc.element.json-rpc2._.curryRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.memoize (func, resolver)](#apidoc.element.json-rpc2._.memoize)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.partial ()](#apidoc.element.json-rpc2._.partial)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_.partialRight ()](#apidoc.element.json-rpc2._.partialRight)
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Client.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Connection.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>ES5Class.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Endpoint.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Error
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Error.AbstractError.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>EventEmitter.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>HttpServerConnection.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Server.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>SocketConnection.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>WebSocketConnection.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.Client.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.EventSource.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.super_.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>_.memoize.Cache.prototype
1.  object <span class="apidocSignatureSpan">json-rpc2.</span>_.prototype

#### [module json-rpc2.Client](#apidoc.module.json-rpc2.Client)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Client ()](#apidoc.element.json-rpc2.Client.Client)

#### [module json-rpc2.Client.prototype](#apidoc.module.json-rpc2.Client.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>_authHeader (headers)](#apidoc.element.json-rpc2.Client.prototype._authHeader)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>call (method, params, opts, callback)](#apidoc.element.json-rpc2.Client.prototype.call)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>connectHttp (method, params, opts, callback)](#apidoc.element.json-rpc2.Client.prototype.connectHttp)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>connectSocket (callback)](#apidoc.element.json-rpc2.Client.prototype.connectSocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>connectWebsocket (callback)](#apidoc.element.json-rpc2.Client.prototype.connectWebsocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>construct ()](#apidoc.element.json-rpc2.Client.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>stream (method, params, opts, callback)](#apidoc.element.json-rpc2.Client.prototype.stream)

#### [module json-rpc2.Connection](#apidoc.module.json-rpc2.Connection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Connection ()](#apidoc.element.json-rpc2.Connection.Connection)

#### [module json-rpc2.Connection.prototype](#apidoc.module.json-rpc2.Connection.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>call (method, params, callback)](#apidoc.element.json-rpc2.Connection.prototype.call)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>construct ()](#apidoc.element.json-rpc2.Connection.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>handleMessage (msg)](#apidoc.element.json-rpc2.Connection.prototype.handleMessage)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>sendReply (err, result, id)](#apidoc.element.json-rpc2.Connection.prototype.sendReply)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>stream (onend)](#apidoc.element.json-rpc2.Connection.prototype.stream)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>write ()](#apidoc.element.json-rpc2.Connection.prototype.write)

#### [module json-rpc2.ES5Class](#apidoc.module.json-rpc2.ES5Class)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>ES5Class ()](#apidoc.element.json-rpc2.ES5Class.ES5Class)

#### [module json-rpc2.ES5Class.prototype](#apidoc.module.json-rpc2.ES5Class.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.ES5Class.prototype.</span>construct ()](#apidoc.element.json-rpc2.ES5Class.prototype.construct)

#### [module json-rpc2.Endpoint](#apidoc.module.json-rpc2.Endpoint)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Endpoint ()](#apidoc.element.json-rpc2.Endpoint.Endpoint)

#### [module json-rpc2.Endpoint.prototype](#apidoc.module.json-rpc2.Endpoint.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Endpoint.prototype.</span>construct ()](#apidoc.element.json-rpc2.Endpoint.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Endpoint.prototype.</span>expose (name, func, scope)](#apidoc.element.json-rpc2.Endpoint.prototype.expose)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Endpoint.prototype.</span>handleCall (decoded, conn, callback)](#apidoc.element.json-rpc2.Endpoint.prototype.handleCall)

#### [module json-rpc2.Error](#apidoc.module.json-rpc2.Error)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>AbstractError ()](#apidoc.element.json-rpc2.Error.AbstractError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>InternalError ()](#apidoc.element.json-rpc2.Error.InternalError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>InvalidParams ()](#apidoc.element.json-rpc2.Error.InvalidParams)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>InvalidRequest ()](#apidoc.element.json-rpc2.Error.InvalidRequest)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>MethodNotFound ()](#apidoc.element.json-rpc2.Error.MethodNotFound)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>ParseError ()](#apidoc.element.json-rpc2.Error.ParseError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>ServerError ()](#apidoc.element.json-rpc2.Error.ServerError)

#### [module json-rpc2.Error.AbstractError](#apidoc.module.json-rpc2.Error.AbstractError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.</span>AbstractError ()](#apidoc.element.json-rpc2.Error.AbstractError.AbstractError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.</span>captureStackTrace ()](#apidoc.element.json-rpc2.Error.AbstractError.captureStackTrace)
1.  number <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.</span>stackTraceLimit

#### [module json-rpc2.Error.AbstractError.prototype](#apidoc.module.json-rpc2.Error.AbstractError.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.prototype.</span>construct (message, extra)](#apidoc.element.json-rpc2.Error.AbstractError.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.prototype.</span>toString ()](#apidoc.element.json-rpc2.Error.AbstractError.prototype.toString)

#### [module json-rpc2.EventEmitter](#apidoc.module.json-rpc2.EventEmitter)
1.  boolean <span class="apidocSignatureSpan">json-rpc2.EventEmitter.</span>prefixed
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>EventEmitter ()](#apidoc.element.json-rpc2.EventEmitter.EventEmitter)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.</span>hasId (request)](#apidoc.element.json-rpc2.EventEmitter.hasId)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.</span>trace (direction, message)](#apidoc.element.json-rpc2.EventEmitter.trace)

#### [module json-rpc2.EventEmitter.prototype](#apidoc.module.json-rpc2.EventEmitter.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>addListener (event, fn, context)](#apidoc.element.json-rpc2.EventEmitter.prototype.addListener)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>emit (event, a1, a2, a3, a4, a5)](#apidoc.element.json-rpc2.EventEmitter.prototype.emit)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>eventNames ()](#apidoc.element.json-rpc2.EventEmitter.prototype.eventNames)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>listeners (event, exists)](#apidoc.element.json-rpc2.EventEmitter.prototype.listeners)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>off (event, fn, context, once)](#apidoc.element.json-rpc2.EventEmitter.prototype.off)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>on (event, fn, context)](#apidoc.element.json-rpc2.EventEmitter.prototype.on)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>once (event, fn, context)](#apidoc.element.json-rpc2.EventEmitter.prototype.once)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>removeAllListeners (event)](#apidoc.element.json-rpc2.EventEmitter.prototype.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>removeListener (event, fn, context, once)](#apidoc.element.json-rpc2.EventEmitter.prototype.removeListener)
1.  [function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>setMaxListeners ()](#apidoc.element.json-rpc2.EventEmitter.prototype.setMaxListeners)

#### [module json-rpc2.HttpServerConnection](#apidoc.module.json-rpc2.HttpServerConnection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>HttpServerConnection ()](#apidoc.element.json-rpc2.HttpServerConnection.HttpServerConnection)

#### [module json-rpc2.HttpServerConnection.prototype](#apidoc.module.json-rpc2.HttpServerConnection.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.HttpServerConnection.prototype.</span>construct ()](#apidoc.element.json-rpc2.HttpServerConnection.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.HttpServerConnection.prototype.</span>stream ()](#apidoc.element.json-rpc2.HttpServerConnection.prototype.stream)
1.  [function <span class="apidocSignatureSpan">json-rpc2.HttpServerConnection.prototype.</span>write (data)](#apidoc.element.json-rpc2.HttpServerConnection.prototype.write)

#### [module json-rpc2.Server](#apidoc.module.json-rpc2.Server)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Server ()](#apidoc.element.json-rpc2.Server.Server)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.</span>handleHttpError (req, res, error, custom_headers)](#apidoc.element.json-rpc2.Server.handleHttpError)

#### [module json-rpc2.Server.prototype](#apidoc.module.json-rpc2.Server.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>_checkAuth (req, res)](#apidoc.element.json-rpc2.Server.prototype._checkAuth)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>construct ()](#apidoc.element.json-rpc2.Server.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>enableAuth (handler, password)](#apidoc.element.json-rpc2.Server.prototype.enableAuth)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleHttp (req, res)](#apidoc.element.json-rpc2.Server.prototype.handleHttp)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleHybrid (httpServer, socket)](#apidoc.element.json-rpc2.Server.prototype.handleHybrid)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleRaw (socket)](#apidoc.element.json-rpc2.Server.prototype.handleRaw)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleWebsocket (request, socket, body)](#apidoc.element.json-rpc2.Server.prototype.handleWebsocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>listen (port, host)](#apidoc.element.json-rpc2.Server.prototype.listen)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>listenHybrid (port, host)](#apidoc.element.json-rpc2.Server.prototype.listenHybrid)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>listenRaw (port, host)](#apidoc.element.json-rpc2.Server.prototype.listenRaw)

#### [module json-rpc2.SocketConnection](#apidoc.module.json-rpc2.SocketConnection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>SocketConnection ()](#apidoc.element.json-rpc2.SocketConnection.SocketConnection)

#### [module json-rpc2.SocketConnection.prototype](#apidoc.module.json-rpc2.SocketConnection.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>construct ()](#apidoc.element.json-rpc2.SocketConnection.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>end ()](#apidoc.element.json-rpc2.SocketConnection.prototype.end)
1.  [function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>reconnect ()](#apidoc.element.json-rpc2.SocketConnection.prototype.reconnect)
1.  [function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>write (data)](#apidoc.element.json-rpc2.SocketConnection.prototype.write)

#### [module json-rpc2.WebSocketConnection](#apidoc.module.json-rpc2.WebSocketConnection)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>WebSocketConnection ()](#apidoc.element.json-rpc2.WebSocketConnection.WebSocketConnection)

#### [module json-rpc2.WebSocketConnection.prototype](#apidoc.module.json-rpc2.WebSocketConnection.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.WebSocketConnection.prototype.</span>construct ()](#apidoc.element.json-rpc2.WebSocketConnection.prototype.construct)
1.  [function <span class="apidocSignatureSpan">json-rpc2.WebSocketConnection.prototype.</span>end ()](#apidoc.element.json-rpc2.WebSocketConnection.prototype.end)
1.  [function <span class="apidocSignatureSpan">json-rpc2.WebSocketConnection.prototype.</span>write (data)](#apidoc.element.json-rpc2.WebSocketConnection.prototype.write)

#### [module json-rpc2.Websocket](#apidoc.module.json-rpc2.Websocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket (request, socket, body, protocols, options)](#apidoc.element.json-rpc2.Websocket.Websocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>Client (_url, protocols, options)](#apidoc.element.json-rpc2.Websocket.Client)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>EventSource (request, response, options)](#apidoc.element.json-rpc2.Websocket.EventSource)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>WebSocket (request, socket, body, protocols, options)](#apidoc.element.json-rpc2.Websocket.WebSocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>isWebSocket (request)](#apidoc.element.json-rpc2.Websocket.isWebSocket)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>super_ (options)](#apidoc.element.json-rpc2.Websocket.super_)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>validateOptions (options, validKeys)](#apidoc.element.json-rpc2.Websocket.validateOptions)

#### [module json-rpc2.Websocket.Client](#apidoc.module.json-rpc2.Websocket.Client)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>Client (_url, protocols, options)](#apidoc.element.json-rpc2.Websocket.Client.Client)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.Client.</span>super_ (options)](#apidoc.element.json-rpc2.Websocket.Client.super_)

#### [module json-rpc2.Websocket.Client.prototype](#apidoc.module.json-rpc2.Websocket.Client.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.Client.prototype.</span>_configureProxy (proxy, originTLS)](#apidoc.element.json-rpc2.Websocket.Client.prototype._configureProxy)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.Client.prototype.</span>_onConnect ()](#apidoc.element.json-rpc2.Websocket.Client.prototype._onConnect)

#### [module json-rpc2.Websocket.EventSource](#apidoc.module.json-rpc2.Websocket.EventSource)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>EventSource (request, response, options)](#apidoc.element.json-rpc2.Websocket.EventSource.EventSource)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.</span>isEventSource (request)](#apidoc.element.json-rpc2.Websocket.EventSource.isEventSource)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.</span>super_ ()](#apidoc.element.json-rpc2.Websocket.EventSource.super_)

#### [module json-rpc2.Websocket.EventSource.prototype](#apidoc.module.json-rpc2.Websocket.EventSource.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>_open ()](#apidoc.element.json-rpc2.Websocket.EventSource.prototype._open)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>_write (chunk)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype._write)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>addEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.addEventListener)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>close ()](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.close)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>dispatchEvent (event)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.dispatchEvent)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>end (message)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.end)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>ping ()](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.ping)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>removeEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.removeEventListener)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>send (message, options)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.send)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>write (message)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.write)
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>DEFAULT_PING
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>DEFAULT_RETRY
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>onclose
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>onerror
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>onmessage
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>onopen

#### [module json-rpc2.Websocket.super_](#apidoc.module.json-rpc2.Websocket.super_)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>super_ ()](#apidoc.element.json-rpc2.Websocket.super_.super_)
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.</span>CLOSED
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.</span>CLOSE_TIMEOUT
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.</span>CLOSING
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.</span>CONNECTING
1.  number <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.</span>OPEN

#### [module json-rpc2.Websocket.super_.prototype](#apidoc.module.json-rpc2.Websocket.super_.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_beginClose (reason, code)](#apidoc.element.json-rpc2.Websocket.super_.prototype._beginClose)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_configureStream ()](#apidoc.element.json-rpc2.Websocket.super_.prototype._configureStream)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_emitError (message)](#apidoc.element.json-rpc2.Websocket.super_.prototype._emitError)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_finalizeClose ()](#apidoc.element.json-rpc2.Websocket.super_.prototype._finalizeClose)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_open ()](#apidoc.element.json-rpc2.Websocket.super_.prototype._open)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_receiveMessage (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype._receiveMessage)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>addEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.super_.prototype.addEventListener)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>close (code, reason)](#apidoc.element.json-rpc2.Websocket.super_.prototype.close)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>dispatchEvent (event)](#apidoc.element.json-rpc2.Websocket.super_.prototype.dispatchEvent)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>end (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype.end)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>pause ()](#apidoc.element.json-rpc2.Websocket.super_.prototype.pause)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>ping (message, callback)](#apidoc.element.json-rpc2.Websocket.super_.prototype.ping)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>removeEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.super_.prototype.removeEventListener)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>resume ()](#apidoc.element.json-rpc2.Websocket.super_.prototype.resume)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>send (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype.send)
1.  [function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>write (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype.write)
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>onclose
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>onerror
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>onmessage
1.  object <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>onopen

#### [module json-rpc2._](#apidoc.module.json-rpc2._)
1.  [function <span class="apidocSignatureSpan">json-rpc2.</span>_ (value)](#apidoc.element.json-rpc2._._)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>add (augend, addend)](#apidoc.element.json-rpc2._.add)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>after (n, func)](#apidoc.element.json-rpc2._.after)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>all (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.all)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>any (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.any)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>ary (func, n, guard)](#apidoc.element.json-rpc2._.ary)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>assign ()](#apidoc.element.json-rpc2._.assign)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>at ()](#apidoc.element.json-rpc2._.at)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>attempt ()](#apidoc.element.json-rpc2._.attempt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>backflow ()](#apidoc.element.json-rpc2._.backflow)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>before (n, func)](#apidoc.element.json-rpc2._.before)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>bind ()](#apidoc.element.json-rpc2._.bind)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>bindAll ()](#apidoc.element.json-rpc2._.bindAll)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>bindKey ()](#apidoc.element.json-rpc2._.bindKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>callback (func, thisArg, guard)](#apidoc.element.json-rpc2._.callback)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>camelCase (string)](#apidoc.element.json-rpc2._.camelCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>capitalize (string)](#apidoc.element.json-rpc2._.capitalize)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>ceil (number, precision)](#apidoc.element.json-rpc2._.ceil)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>chain (value)](#apidoc.element.json-rpc2._.chain)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>chunk (array, size, guard)](#apidoc.element.json-rpc2._.chunk)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>clone (value, isDeep, customizer, thisArg)](#apidoc.element.json-rpc2._.clone)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>cloneDeep (value, customizer, thisArg)](#apidoc.element.json-rpc2._.cloneDeep)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>collect (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.collect)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>compact (array)](#apidoc.element.json-rpc2._.compact)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>compose ()](#apidoc.element.json-rpc2._.compose)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>constant (value)](#apidoc.element.json-rpc2._.constant)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>contains (collection, target, fromIndex, guard)](#apidoc.element.json-rpc2._.contains)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>countBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.countBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>create (prototype, properties, guard)](#apidoc.element.json-rpc2._.create)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>curry (func, arity, guard)](#apidoc.element.json-rpc2._.curry)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>curryRight (func, arity, guard)](#apidoc.element.json-rpc2._.curryRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>debounce (func, wait, options)](#apidoc.element.json-rpc2._.debounce)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>deburr (string)](#apidoc.element.json-rpc2._.deburr)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>defaults ()](#apidoc.element.json-rpc2._.defaults)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>defaultsDeep ()](#apidoc.element.json-rpc2._.defaultsDeep)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>defer ()](#apidoc.element.json-rpc2._.defer)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>delay ()](#apidoc.element.json-rpc2._.delay)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>detect (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.detect)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>difference ()](#apidoc.element.json-rpc2._.difference)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>drop (array, n, guard)](#apidoc.element.json-rpc2._.drop)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>dropRight (array, n, guard)](#apidoc.element.json-rpc2._.dropRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>dropRightWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.dropRightWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>dropWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.dropWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>each (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.each)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>eachRight (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.eachRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>endsWith (string, target, position)](#apidoc.element.json-rpc2._.endsWith)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>eq (value, other, customizer, thisArg)](#apidoc.element.json-rpc2._.eq)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>escape (string)](#apidoc.element.json-rpc2._.escape)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>escapeRegExp (string)](#apidoc.element.json-rpc2._.escapeRegExp)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>every (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.every)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>extend ()](#apidoc.element.json-rpc2._.extend)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>fill (array, value, start, end)](#apidoc.element.json-rpc2._.fill)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>filter (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.filter)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>find (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.find)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>findIndex (array, predicate, thisArg)](#apidoc.element.json-rpc2._.findIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>findKey (object, predicate, thisArg)](#apidoc.element.json-rpc2._.findKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>findLast (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.findLast)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>findLastIndex (array, predicate, thisArg)](#apidoc.element.json-rpc2._.findLastIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>findLastKey (object, predicate, thisArg)](#apidoc.element.json-rpc2._.findLastKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>findWhere (collection, source)](#apidoc.element.json-rpc2._.findWhere)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>first (array)](#apidoc.element.json-rpc2._.first)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>flatten (array, isDeep, guard)](#apidoc.element.json-rpc2._.flatten)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>flattenDeep (array)](#apidoc.element.json-rpc2._.flattenDeep)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>floor (number, precision)](#apidoc.element.json-rpc2._.floor)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>flow ()](#apidoc.element.json-rpc2._.flow)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>flowRight ()](#apidoc.element.json-rpc2._.flowRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>foldl (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.foldl)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>foldr (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.foldr)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>forEach (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.forEach)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>forEachRight (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.forEachRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>forIn (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forIn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>forInRight (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forInRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>forOwn (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forOwn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>forOwnRight (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forOwnRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>functions (object)](#apidoc.element.json-rpc2._.functions)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>get (object, path, defaultValue)](#apidoc.element.json-rpc2._.get)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>groupBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.groupBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>gt (value, other)](#apidoc.element.json-rpc2._.gt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>gte (value, other)](#apidoc.element.json-rpc2._.gte)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>has (object, path)](#apidoc.element.json-rpc2._.has)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>head (array)](#apidoc.element.json-rpc2._.head)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>identity (value)](#apidoc.element.json-rpc2._.identity)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>inRange (value, start, end)](#apidoc.element.json-rpc2._.inRange)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>include (collection, target, fromIndex, guard)](#apidoc.element.json-rpc2._.include)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>includes (collection, target, fromIndex, guard)](#apidoc.element.json-rpc2._.includes)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>indexBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.indexBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>indexOf (array, value, fromIndex)](#apidoc.element.json-rpc2._.indexOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>initial (array)](#apidoc.element.json-rpc2._.initial)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>inject (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.inject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>intersection ()](#apidoc.element.json-rpc2._.intersection)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>invert (object, multiValue, guard)](#apidoc.element.json-rpc2._.invert)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>invoke ()](#apidoc.element.json-rpc2._.invoke)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isArguments (value)](#apidoc.element.json-rpc2._.isArguments)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isArray ()](#apidoc.element.json-rpc2._.isArray)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isBoolean (value)](#apidoc.element.json-rpc2._.isBoolean)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isDate (value)](#apidoc.element.json-rpc2._.isDate)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isElement (value)](#apidoc.element.json-rpc2._.isElement)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isEmpty (value)](#apidoc.element.json-rpc2._.isEmpty)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isEqual (value, other, customizer, thisArg)](#apidoc.element.json-rpc2._.isEqual)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isError (value)](#apidoc.element.json-rpc2._.isError)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isFinite (value)](#apidoc.element.json-rpc2._.isFinite)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isFunction (value)](#apidoc.element.json-rpc2._.isFunction)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isMatch (object, source, customizer, thisArg)](#apidoc.element.json-rpc2._.isMatch)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isNaN (value)](#apidoc.element.json-rpc2._.isNaN)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isNative (value)](#apidoc.element.json-rpc2._.isNative)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isNull (value)](#apidoc.element.json-rpc2._.isNull)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isNumber (value)](#apidoc.element.json-rpc2._.isNumber)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isObject (value)](#apidoc.element.json-rpc2._.isObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isPlainObject (value)](#apidoc.element.json-rpc2._.isPlainObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isRegExp (value)](#apidoc.element.json-rpc2._.isRegExp)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isString (value)](#apidoc.element.json-rpc2._.isString)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isTypedArray (value)](#apidoc.element.json-rpc2._.isTypedArray)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>isUndefined (value)](#apidoc.element.json-rpc2._.isUndefined)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>iteratee (func, thisArg, guard)](#apidoc.element.json-rpc2._.iteratee)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>kebabCase (string)](#apidoc.element.json-rpc2._.kebabCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>keys (object)](#apidoc.element.json-rpc2._.keys)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>keysIn (object)](#apidoc.element.json-rpc2._.keysIn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>last (array)](#apidoc.element.json-rpc2._.last)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>lastIndexOf (array, value, fromIndex)](#apidoc.element.json-rpc2._.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>lt (value, other)](#apidoc.element.json-rpc2._.lt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>lte (value, other)](#apidoc.element.json-rpc2._.lte)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>map (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.map)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>mapKeys (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.mapKeys)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>mapValues (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.mapValues)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>matches (source)](#apidoc.element.json-rpc2._.matches)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>matchesProperty (path, srcValue)](#apidoc.element.json-rpc2._.matchesProperty)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>max (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.max)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>memoize (func, resolver)](#apidoc.element.json-rpc2._.memoize)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>merge ()](#apidoc.element.json-rpc2._.merge)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>method ()](#apidoc.element.json-rpc2._.method)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>methodOf ()](#apidoc.element.json-rpc2._.methodOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>methods (object)](#apidoc.element.json-rpc2._.methods)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>min (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.min)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>mixin (object, source, options)](#apidoc.element.json-rpc2._.mixin)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>modArgs ()](#apidoc.element.json-rpc2._.modArgs)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>negate (predicate)](#apidoc.element.json-rpc2._.negate)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>noConflict ()](#apidoc.element.json-rpc2._.noConflict)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>noop ()](#apidoc.element.json-rpc2._.noop)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>now ()](#apidoc.element.json-rpc2._.now)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>object (props, values)](#apidoc.element.json-rpc2._.object)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>omit ()](#apidoc.element.json-rpc2._.omit)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>once (func)](#apidoc.element.json-rpc2._.once)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>pad (string, length, chars)](#apidoc.element.json-rpc2._.pad)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>padLeft (string, length, chars)](#apidoc.element.json-rpc2._.padLeft)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>padRight (string, length, chars)](#apidoc.element.json-rpc2._.padRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>pairs (object)](#apidoc.element.json-rpc2._.pairs)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>parseInt (string, radix, guard)](#apidoc.element.json-rpc2._.parseInt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>partial ()](#apidoc.element.json-rpc2._.partial)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>partialRight ()](#apidoc.element.json-rpc2._.partialRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>partition (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.partition)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>pick ()](#apidoc.element.json-rpc2._.pick)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>pluck (collection, path)](#apidoc.element.json-rpc2._.pluck)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>property (path)](#apidoc.element.json-rpc2._.property)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>propertyOf (object)](#apidoc.element.json-rpc2._.propertyOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>pull ()](#apidoc.element.json-rpc2._.pull)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>pullAt ()](#apidoc.element.json-rpc2._.pullAt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>random (min, max, floating)](#apidoc.element.json-rpc2._.random)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>range (start, end, step)](#apidoc.element.json-rpc2._.range)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>rearg ()](#apidoc.element.json-rpc2._.rearg)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>reduce (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.reduce)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>reduceRight (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.reduceRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>reject (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.reject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>remove (array, predicate, thisArg)](#apidoc.element.json-rpc2._.remove)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>repeat (string, n)](#apidoc.element.json-rpc2._.repeat)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>rest (array)](#apidoc.element.json-rpc2._.rest)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>restParam (func, start)](#apidoc.element.json-rpc2._.restParam)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>result (object, path, defaultValue)](#apidoc.element.json-rpc2._.result)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>round (number, precision)](#apidoc.element.json-rpc2._.round)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>runInContext (context)](#apidoc.element.json-rpc2._.runInContext)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sample (collection, n, guard)](#apidoc.element.json-rpc2._.sample)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>select (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.select)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>set (object, path, value)](#apidoc.element.json-rpc2._.set)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>shuffle (collection)](#apidoc.element.json-rpc2._.shuffle)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>size (collection)](#apidoc.element.json-rpc2._.size)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>slice (array, start, end)](#apidoc.element.json-rpc2._.slice)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>snakeCase (string)](#apidoc.element.json-rpc2._.snakeCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>some (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.some)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sortBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.sortBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sortByAll ()](#apidoc.element.json-rpc2._.sortByAll)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sortByOrder (collection, iteratees, orders, guard)](#apidoc.element.json-rpc2._.sortByOrder)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sortedIndex (array, value, iteratee, thisArg)](#apidoc.element.json-rpc2._.sortedIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sortedLastIndex (array, value, iteratee, thisArg)](#apidoc.element.json-rpc2._.sortedLastIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>spread (func)](#apidoc.element.json-rpc2._.spread)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>startCase (string)](#apidoc.element.json-rpc2._.startCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>startsWith (string, target, position)](#apidoc.element.json-rpc2._.startsWith)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>sum (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.sum)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>tail (array)](#apidoc.element.json-rpc2._.tail)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>take (array, n, guard)](#apidoc.element.json-rpc2._.take)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>takeRight (array, n, guard)](#apidoc.element.json-rpc2._.takeRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>takeRightWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.takeRightWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>takeWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.takeWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>tap (value, interceptor, thisArg)](#apidoc.element.json-rpc2._.tap)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>template (string, options, otherOptions)](#apidoc.element.json-rpc2._.template)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>throttle (func, wait, options)](#apidoc.element.json-rpc2._.throttle)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>thru (value, interceptor, thisArg)](#apidoc.element.json-rpc2._.thru)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>times (n, iteratee, thisArg)](#apidoc.element.json-rpc2._.times)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>toArray (value)](#apidoc.element.json-rpc2._.toArray)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>toPlainObject (value)](#apidoc.element.json-rpc2._.toPlainObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>transform (object, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.transform)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>trim (string, chars, guard)](#apidoc.element.json-rpc2._.trim)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>trimLeft (string, chars, guard)](#apidoc.element.json-rpc2._.trimLeft)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>trimRight (string, chars, guard)](#apidoc.element.json-rpc2._.trimRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>trunc (string, options, guard)](#apidoc.element.json-rpc2._.trunc)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>unescape (string)](#apidoc.element.json-rpc2._.unescape)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>union ()](#apidoc.element.json-rpc2._.union)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>uniq (array, isSorted, iteratee, thisArg)](#apidoc.element.json-rpc2._.uniq)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>unique (array, isSorted, iteratee, thisArg)](#apidoc.element.json-rpc2._.unique)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>uniqueId (prefix)](#apidoc.element.json-rpc2._.uniqueId)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>unzip (array)](#apidoc.element.json-rpc2._.unzip)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>unzipWith (array, iteratee, thisArg)](#apidoc.element.json-rpc2._.unzipWith)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>values (object)](#apidoc.element.json-rpc2._.values)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>valuesIn (object)](#apidoc.element.json-rpc2._.valuesIn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>where (collection, source)](#apidoc.element.json-rpc2._.where)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>without ()](#apidoc.element.json-rpc2._.without)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>words (string, pattern, guard)](#apidoc.element.json-rpc2._.words)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>wrap (value, wrapper)](#apidoc.element.json-rpc2._.wrap)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>xor ()](#apidoc.element.json-rpc2._.xor)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>zip ()](#apidoc.element.json-rpc2._.zip)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>zipObject (props, values)](#apidoc.element.json-rpc2._.zipObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>zipWith ()](#apidoc.element.json-rpc2._.zipWith)
1.  object <span class="apidocSignatureSpan">json-rpc2._.</span>support
1.  object <span class="apidocSignatureSpan">json-rpc2._.</span>templateSettings
1.  string <span class="apidocSignatureSpan">json-rpc2._.</span>VERSION

#### [module json-rpc2._.bind](#apidoc.module.json-rpc2._.bind)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>bind ()](#apidoc.element.json-rpc2._.bind.bind)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.bind.</span>placeholder (value)](#apidoc.element.json-rpc2._.bind.placeholder)

#### [module json-rpc2._.bindKey](#apidoc.module.json-rpc2._.bindKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>bindKey ()](#apidoc.element.json-rpc2._.bindKey.bindKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.bindKey.</span>placeholder (value)](#apidoc.element.json-rpc2._.bindKey.placeholder)

#### [module json-rpc2._.curry](#apidoc.module.json-rpc2._.curry)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>curry (func, arity, guard)](#apidoc.element.json-rpc2._.curry.curry)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.curry.</span>placeholder (value)](#apidoc.element.json-rpc2._.curry.placeholder)

#### [module json-rpc2._.curryRight](#apidoc.module.json-rpc2._.curryRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>curryRight (func, arity, guard)](#apidoc.element.json-rpc2._.curryRight.curryRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.curryRight.</span>placeholder (value)](#apidoc.element.json-rpc2._.curryRight.placeholder)

#### [module json-rpc2._.memoize](#apidoc.module.json-rpc2._.memoize)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>memoize (func, resolver)](#apidoc.element.json-rpc2._.memoize.memoize)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.memoize.</span>Cache ()](#apidoc.element.json-rpc2._.memoize.Cache)

#### [module json-rpc2._.memoize.Cache.prototype](#apidoc.module.json-rpc2._.memoize.Cache.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>delete (key)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.delete)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>get (key)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.get)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>has (key)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.has)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>set (key, value)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.set)

#### [module json-rpc2._.partial](#apidoc.module.json-rpc2._.partial)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>partial ()](#apidoc.element.json-rpc2._.partial.partial)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.partial.</span>placeholder (value)](#apidoc.element.json-rpc2._.partial.placeholder)

#### [module json-rpc2._.partialRight](#apidoc.module.json-rpc2._.partialRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.</span>partialRight ()](#apidoc.element.json-rpc2._.partialRight.partialRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.partialRight.</span>placeholder (value)](#apidoc.element.json-rpc2._.partialRight.placeholder)

#### [module json-rpc2._.prototype](#apidoc.module.json-rpc2._.prototype)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>add ()](#apidoc.element.json-rpc2._.prototype.add)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>after ()](#apidoc.element.json-rpc2._.prototype.after)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>all ()](#apidoc.element.json-rpc2._.prototype.all)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>any ()](#apidoc.element.json-rpc2._.prototype.any)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>ary ()](#apidoc.element.json-rpc2._.prototype.ary)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>assign ()](#apidoc.element.json-rpc2._.prototype.assign)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>at ()](#apidoc.element.json-rpc2._.prototype.at)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>attempt ()](#apidoc.element.json-rpc2._.prototype.attempt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>backflow ()](#apidoc.element.json-rpc2._.prototype.backflow)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>before ()](#apidoc.element.json-rpc2._.prototype.before)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>bind ()](#apidoc.element.json-rpc2._.prototype.bind)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>bindAll ()](#apidoc.element.json-rpc2._.prototype.bindAll)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>bindKey ()](#apidoc.element.json-rpc2._.prototype.bindKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>callback ()](#apidoc.element.json-rpc2._.prototype.callback)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>camelCase ()](#apidoc.element.json-rpc2._.prototype.camelCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>capitalize ()](#apidoc.element.json-rpc2._.prototype.capitalize)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>ceil ()](#apidoc.element.json-rpc2._.prototype.ceil)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>chain ()](#apidoc.element.json-rpc2._.prototype.chain)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>chunk ()](#apidoc.element.json-rpc2._.prototype.chunk)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>clone ()](#apidoc.element.json-rpc2._.prototype.clone)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>cloneDeep ()](#apidoc.element.json-rpc2._.prototype.cloneDeep)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>collect ()](#apidoc.element.json-rpc2._.prototype.collect)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>commit ()](#apidoc.element.json-rpc2._.prototype.commit)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>compact ()](#apidoc.element.json-rpc2._.prototype.compact)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>compose ()](#apidoc.element.json-rpc2._.prototype.compose)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>concat ()](#apidoc.element.json-rpc2._.prototype.concat)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>constant ()](#apidoc.element.json-rpc2._.prototype.constant)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>contains ()](#apidoc.element.json-rpc2._.prototype.contains)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>countBy ()](#apidoc.element.json-rpc2._.prototype.countBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>create ()](#apidoc.element.json-rpc2._.prototype.create)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>curry ()](#apidoc.element.json-rpc2._.prototype.curry)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>curryRight ()](#apidoc.element.json-rpc2._.prototype.curryRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>debounce ()](#apidoc.element.json-rpc2._.prototype.debounce)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>deburr ()](#apidoc.element.json-rpc2._.prototype.deburr)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>defaults ()](#apidoc.element.json-rpc2._.prototype.defaults)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>defaultsDeep ()](#apidoc.element.json-rpc2._.prototype.defaultsDeep)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>defer ()](#apidoc.element.json-rpc2._.prototype.defer)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>delay ()](#apidoc.element.json-rpc2._.prototype.delay)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>detect ()](#apidoc.element.json-rpc2._.prototype.detect)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>difference ()](#apidoc.element.json-rpc2._.prototype.difference)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>drop ()](#apidoc.element.json-rpc2._.prototype.drop)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>dropRight ()](#apidoc.element.json-rpc2._.prototype.dropRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>dropRightWhile ()](#apidoc.element.json-rpc2._.prototype.dropRightWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>dropWhile ()](#apidoc.element.json-rpc2._.prototype.dropWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>each ()](#apidoc.element.json-rpc2._.prototype.each)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>eachRight ()](#apidoc.element.json-rpc2._.prototype.eachRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>endsWith ()](#apidoc.element.json-rpc2._.prototype.endsWith)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>eq ()](#apidoc.element.json-rpc2._.prototype.eq)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>escape ()](#apidoc.element.json-rpc2._.prototype.escape)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>escapeRegExp ()](#apidoc.element.json-rpc2._.prototype.escapeRegExp)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>every ()](#apidoc.element.json-rpc2._.prototype.every)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>extend ()](#apidoc.element.json-rpc2._.prototype.extend)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>fill ()](#apidoc.element.json-rpc2._.prototype.fill)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>filter ()](#apidoc.element.json-rpc2._.prototype.filter)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>find ()](#apidoc.element.json-rpc2._.prototype.find)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findIndex ()](#apidoc.element.json-rpc2._.prototype.findIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findKey ()](#apidoc.element.json-rpc2._.prototype.findKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findLast ()](#apidoc.element.json-rpc2._.prototype.findLast)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findLastIndex ()](#apidoc.element.json-rpc2._.prototype.findLastIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findLastKey ()](#apidoc.element.json-rpc2._.prototype.findLastKey)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findWhere ()](#apidoc.element.json-rpc2._.prototype.findWhere)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>first ()](#apidoc.element.json-rpc2._.prototype.first)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flatten ()](#apidoc.element.json-rpc2._.prototype.flatten)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flattenDeep ()](#apidoc.element.json-rpc2._.prototype.flattenDeep)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>floor ()](#apidoc.element.json-rpc2._.prototype.floor)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flow ()](#apidoc.element.json-rpc2._.prototype.flow)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flowRight ()](#apidoc.element.json-rpc2._.prototype.flowRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>foldl ()](#apidoc.element.json-rpc2._.prototype.foldl)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>foldr ()](#apidoc.element.json-rpc2._.prototype.foldr)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forEach ()](#apidoc.element.json-rpc2._.prototype.forEach)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forEachRight ()](#apidoc.element.json-rpc2._.prototype.forEachRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forIn ()](#apidoc.element.json-rpc2._.prototype.forIn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forInRight ()](#apidoc.element.json-rpc2._.prototype.forInRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forOwn ()](#apidoc.element.json-rpc2._.prototype.forOwn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forOwnRight ()](#apidoc.element.json-rpc2._.prototype.forOwnRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>functions ()](#apidoc.element.json-rpc2._.prototype.functions)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>get ()](#apidoc.element.json-rpc2._.prototype.get)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>groupBy ()](#apidoc.element.json-rpc2._.prototype.groupBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>gt ()](#apidoc.element.json-rpc2._.prototype.gt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>gte ()](#apidoc.element.json-rpc2._.prototype.gte)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>has ()](#apidoc.element.json-rpc2._.prototype.has)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>head ()](#apidoc.element.json-rpc2._.prototype.head)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>identity ()](#apidoc.element.json-rpc2._.prototype.identity)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>inRange ()](#apidoc.element.json-rpc2._.prototype.inRange)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>include ()](#apidoc.element.json-rpc2._.prototype.include)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>includes ()](#apidoc.element.json-rpc2._.prototype.includes)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>indexBy ()](#apidoc.element.json-rpc2._.prototype.indexBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>indexOf ()](#apidoc.element.json-rpc2._.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>initial ()](#apidoc.element.json-rpc2._.prototype.initial)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>inject ()](#apidoc.element.json-rpc2._.prototype.inject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>intersection ()](#apidoc.element.json-rpc2._.prototype.intersection)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>invert ()](#apidoc.element.json-rpc2._.prototype.invert)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>invoke ()](#apidoc.element.json-rpc2._.prototype.invoke)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isArguments ()](#apidoc.element.json-rpc2._.prototype.isArguments)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isArray ()](#apidoc.element.json-rpc2._.prototype.isArray)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isBoolean ()](#apidoc.element.json-rpc2._.prototype.isBoolean)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isDate ()](#apidoc.element.json-rpc2._.prototype.isDate)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isElement ()](#apidoc.element.json-rpc2._.prototype.isElement)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isEmpty ()](#apidoc.element.json-rpc2._.prototype.isEmpty)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isEqual ()](#apidoc.element.json-rpc2._.prototype.isEqual)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isError ()](#apidoc.element.json-rpc2._.prototype.isError)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isFinite ()](#apidoc.element.json-rpc2._.prototype.isFinite)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isFunction ()](#apidoc.element.json-rpc2._.prototype.isFunction)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isMatch ()](#apidoc.element.json-rpc2._.prototype.isMatch)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNaN ()](#apidoc.element.json-rpc2._.prototype.isNaN)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNative ()](#apidoc.element.json-rpc2._.prototype.isNative)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNull ()](#apidoc.element.json-rpc2._.prototype.isNull)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNumber ()](#apidoc.element.json-rpc2._.prototype.isNumber)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isObject ()](#apidoc.element.json-rpc2._.prototype.isObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isPlainObject ()](#apidoc.element.json-rpc2._.prototype.isPlainObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isRegExp ()](#apidoc.element.json-rpc2._.prototype.isRegExp)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isString ()](#apidoc.element.json-rpc2._.prototype.isString)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isTypedArray ()](#apidoc.element.json-rpc2._.prototype.isTypedArray)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isUndefined ()](#apidoc.element.json-rpc2._.prototype.isUndefined)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>iteratee ()](#apidoc.element.json-rpc2._.prototype.iteratee)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>join ()](#apidoc.element.json-rpc2._.prototype.join)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>kebabCase ()](#apidoc.element.json-rpc2._.prototype.kebabCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>keys ()](#apidoc.element.json-rpc2._.prototype.keys)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>keysIn ()](#apidoc.element.json-rpc2._.prototype.keysIn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>last ()](#apidoc.element.json-rpc2._.prototype.last)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>lastIndexOf ()](#apidoc.element.json-rpc2._.prototype.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>lt ()](#apidoc.element.json-rpc2._.prototype.lt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>lte ()](#apidoc.element.json-rpc2._.prototype.lte)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>map ()](#apidoc.element.json-rpc2._.prototype.map)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>mapKeys ()](#apidoc.element.json-rpc2._.prototype.mapKeys)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>mapValues ()](#apidoc.element.json-rpc2._.prototype.mapValues)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>matches ()](#apidoc.element.json-rpc2._.prototype.matches)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>matchesProperty ()](#apidoc.element.json-rpc2._.prototype.matchesProperty)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>max ()](#apidoc.element.json-rpc2._.prototype.max)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>memoize ()](#apidoc.element.json-rpc2._.prototype.memoize)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>merge ()](#apidoc.element.json-rpc2._.prototype.merge)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>method ()](#apidoc.element.json-rpc2._.prototype.method)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>methodOf ()](#apidoc.element.json-rpc2._.prototype.methodOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>methods ()](#apidoc.element.json-rpc2._.prototype.methods)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>min ()](#apidoc.element.json-rpc2._.prototype.min)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>mixin ()](#apidoc.element.json-rpc2._.prototype.mixin)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>modArgs ()](#apidoc.element.json-rpc2._.prototype.modArgs)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>negate ()](#apidoc.element.json-rpc2._.prototype.negate)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>noConflict ()](#apidoc.element.json-rpc2._.prototype.noConflict)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>noop ()](#apidoc.element.json-rpc2._.prototype.noop)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>now ()](#apidoc.element.json-rpc2._.prototype.now)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>object ()](#apidoc.element.json-rpc2._.prototype.object)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>omit ()](#apidoc.element.json-rpc2._.prototype.omit)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>once ()](#apidoc.element.json-rpc2._.prototype.once)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pad ()](#apidoc.element.json-rpc2._.prototype.pad)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>padLeft ()](#apidoc.element.json-rpc2._.prototype.padLeft)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>padRight ()](#apidoc.element.json-rpc2._.prototype.padRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pairs ()](#apidoc.element.json-rpc2._.prototype.pairs)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>parseInt ()](#apidoc.element.json-rpc2._.prototype.parseInt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>partial ()](#apidoc.element.json-rpc2._.prototype.partial)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>partialRight ()](#apidoc.element.json-rpc2._.prototype.partialRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>partition ()](#apidoc.element.json-rpc2._.prototype.partition)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pick ()](#apidoc.element.json-rpc2._.prototype.pick)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>plant (value)](#apidoc.element.json-rpc2._.prototype.plant)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pluck ()](#apidoc.element.json-rpc2._.prototype.pluck)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pop ()](#apidoc.element.json-rpc2._.prototype.pop)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>property ()](#apidoc.element.json-rpc2._.prototype.property)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>propertyOf ()](#apidoc.element.json-rpc2._.prototype.propertyOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pull ()](#apidoc.element.json-rpc2._.prototype.pull)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pullAt ()](#apidoc.element.json-rpc2._.prototype.pullAt)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>push ()](#apidoc.element.json-rpc2._.prototype.push)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>random ()](#apidoc.element.json-rpc2._.prototype.random)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>range ()](#apidoc.element.json-rpc2._.prototype.range)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>rearg ()](#apidoc.element.json-rpc2._.prototype.rearg)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reduce ()](#apidoc.element.json-rpc2._.prototype.reduce)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reduceRight ()](#apidoc.element.json-rpc2._.prototype.reduceRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reject ()](#apidoc.element.json-rpc2._.prototype.reject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>remove ()](#apidoc.element.json-rpc2._.prototype.remove)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>repeat ()](#apidoc.element.json-rpc2._.prototype.repeat)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>replace ()](#apidoc.element.json-rpc2._.prototype.replace)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>rest ()](#apidoc.element.json-rpc2._.prototype.rest)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>restParam ()](#apidoc.element.json-rpc2._.prototype.restParam)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>result ()](#apidoc.element.json-rpc2._.prototype.result)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reverse ()](#apidoc.element.json-rpc2._.prototype.reverse)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>round ()](#apidoc.element.json-rpc2._.prototype.round)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>run ()](#apidoc.element.json-rpc2._.prototype.run)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>runInContext ()](#apidoc.element.json-rpc2._.prototype.runInContext)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sample (n)](#apidoc.element.json-rpc2._.prototype.sample)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>select ()](#apidoc.element.json-rpc2._.prototype.select)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>set ()](#apidoc.element.json-rpc2._.prototype.set)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>shift ()](#apidoc.element.json-rpc2._.prototype.shift)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>shuffle ()](#apidoc.element.json-rpc2._.prototype.shuffle)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>size ()](#apidoc.element.json-rpc2._.prototype.size)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>slice ()](#apidoc.element.json-rpc2._.prototype.slice)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>snakeCase ()](#apidoc.element.json-rpc2._.prototype.snakeCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>some ()](#apidoc.element.json-rpc2._.prototype.some)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sort ()](#apidoc.element.json-rpc2._.prototype.sort)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortBy ()](#apidoc.element.json-rpc2._.prototype.sortBy)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortByAll ()](#apidoc.element.json-rpc2._.prototype.sortByAll)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortByOrder ()](#apidoc.element.json-rpc2._.prototype.sortByOrder)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortedIndex ()](#apidoc.element.json-rpc2._.prototype.sortedIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortedLastIndex ()](#apidoc.element.json-rpc2._.prototype.sortedLastIndex)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>splice ()](#apidoc.element.json-rpc2._.prototype.splice)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>split ()](#apidoc.element.json-rpc2._.prototype.split)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>spread ()](#apidoc.element.json-rpc2._.prototype.spread)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>startCase ()](#apidoc.element.json-rpc2._.prototype.startCase)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>startsWith ()](#apidoc.element.json-rpc2._.prototype.startsWith)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sum ()](#apidoc.element.json-rpc2._.prototype.sum)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>tail ()](#apidoc.element.json-rpc2._.prototype.tail)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>take ()](#apidoc.element.json-rpc2._.prototype.take)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>takeRight ()](#apidoc.element.json-rpc2._.prototype.takeRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>takeRightWhile ()](#apidoc.element.json-rpc2._.prototype.takeRightWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>takeWhile ()](#apidoc.element.json-rpc2._.prototype.takeWhile)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>tap ()](#apidoc.element.json-rpc2._.prototype.tap)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>template ()](#apidoc.element.json-rpc2._.prototype.template)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>throttle ()](#apidoc.element.json-rpc2._.prototype.throttle)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>thru ()](#apidoc.element.json-rpc2._.prototype.thru)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>times ()](#apidoc.element.json-rpc2._.prototype.times)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toArray ()](#apidoc.element.json-rpc2._.prototype.toArray)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toJSON ()](#apidoc.element.json-rpc2._.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toPlainObject ()](#apidoc.element.json-rpc2._.prototype.toPlainObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toString ()](#apidoc.element.json-rpc2._.prototype.toString)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>transform ()](#apidoc.element.json-rpc2._.prototype.transform)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trim ()](#apidoc.element.json-rpc2._.prototype.trim)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trimLeft ()](#apidoc.element.json-rpc2._.prototype.trimLeft)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trimRight ()](#apidoc.element.json-rpc2._.prototype.trimRight)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trunc ()](#apidoc.element.json-rpc2._.prototype.trunc)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unescape ()](#apidoc.element.json-rpc2._.prototype.unescape)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>union ()](#apidoc.element.json-rpc2._.prototype.union)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>uniq ()](#apidoc.element.json-rpc2._.prototype.uniq)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unique ()](#apidoc.element.json-rpc2._.prototype.unique)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>uniqueId ()](#apidoc.element.json-rpc2._.prototype.uniqueId)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unshift ()](#apidoc.element.json-rpc2._.prototype.unshift)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unzip ()](#apidoc.element.json-rpc2._.prototype.unzip)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unzipWith ()](#apidoc.element.json-rpc2._.prototype.unzipWith)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>value ()](#apidoc.element.json-rpc2._.prototype.value)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>valueOf ()](#apidoc.element.json-rpc2._.prototype.valueOf)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>values ()](#apidoc.element.json-rpc2._.prototype.values)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>valuesIn ()](#apidoc.element.json-rpc2._.prototype.valuesIn)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>where ()](#apidoc.element.json-rpc2._.prototype.where)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>without ()](#apidoc.element.json-rpc2._.prototype.without)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>words ()](#apidoc.element.json-rpc2._.prototype.words)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>wrap ()](#apidoc.element.json-rpc2._.prototype.wrap)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>xor ()](#apidoc.element.json-rpc2._.prototype.xor)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>zip ()](#apidoc.element.json-rpc2._.prototype.zip)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>zipObject ()](#apidoc.element.json-rpc2._.prototype.zipObject)
1.  [function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>zipWith ()](#apidoc.element.json-rpc2._.prototype.zipWith)



# <a name="apidoc.module.json-rpc2"></a>[module json-rpc2](#apidoc.module.json-rpc2)

#### <a name="apidoc.element.json-rpc2.Client"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Client ()](#apidoc.element.json-rpc2.Client)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...

if (!/^wss?:\/\//i.test(self.host)) {
  self.host = 'ws://' + self.host + ':' + self.port + '/';
}

this._authHeader(headers);

socket = new WebSocket.Client(self.host, null, {headers: headers});

conn = new WebSocketConnection(self, socket);

parser = new JsonParser();

parser.onValue = function parseOnValue(decoded){
  if (this.stack.length) {
...
```

#### <a name="apidoc.element.json-rpc2.Connection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Connection ()](#apidoc.element.json-rpc2.Connection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.ES5Class"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>ES5Class ()](#apidoc.element.json-rpc2.ES5Class)
- description and source-code
```javascript
function ES5Class(){ }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Endpoint"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Endpoint ()](#apidoc.element.json-rpc2.Endpoint)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Error.AbstractError"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Error.AbstractError ()](#apidoc.element.json-rpc2.Error.AbstractError)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>EventEmitter ()](#apidoc.element.json-rpc2.EventEmitter)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.HttpServerConnection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>HttpServerConnection ()](#apidoc.element.json-rpc2.HttpServerConnection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      response.id = decoded.id;
      reply(response);
    } else {
      reply();
    }
  };

  var conn = new classes.HttpServerConnection(self, req, res);

  self.handleCall(decoded, conn, callback);
}; // function handle(buf)

req.on('data', function requestData(chunk) {
  buffer = buffer + chunk;
});
...
```

#### <a name="apidoc.element.json-rpc2.Server"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Server ()](#apidoc.element.json-rpc2.Server)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.SocketConnection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>SocketConnection ()](#apidoc.element.json-rpc2.SocketConnection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      },

      handleRaw: function (socket) {
var self = this, conn, parser, requireAuth;

Endpoint.trace('<--', 'Accepted socket connection');

conn = new classes.SocketConnection(self, socket);
parser = new JsonParser();
requireAuth = !!this.authHandler;

parser.onValue = function (decoded) {
  if (this.stack.length) {
    return;
  }
...
```

#### <a name="apidoc.element.json-rpc2.WebSocketConnection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>WebSocketConnection ()](#apidoc.element.json-rpc2.WebSocketConnection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      handleWebsocket: function (request, socket, body) {
var self = this, conn, parser;

socket = new WebSocket(request, socket, body);

Endpoint.trace('<--', 'Accepted Websocket connection');

conn = new classes.WebSocketConnection(self, socket);
parser = new JsonParser();

parser.onValue = function (decoded) {
  if (this.stack.length) {
    return;
  }
...
```

#### <a name="apidoc.element.json-rpc2.Websocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket (request, socket, body, protocols, options)](#apidoc.element.json-rpc2.Websocket)
- description and source-code
```javascript
Websocket = function (request, socket, body, protocols, options) {
  options = options || {};

  this._stream = socket;
  this._driver = driver.http(request, {maxLength: options.maxLength, protocols: protocols});

  var self = this;
  if (!this._stream || !this._stream.writable) return;
  if (!this._stream.readable) return this._stream.end();

  var catchup = function() { self._stream.removeListener('data', catchup) };
  this._stream.on('data', catchup);

  API.call(this, options);

  process.nextTick(function() {
    self._driver.start();
    self._driver.io.write(body);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.Client"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.Client (_url, protocols, options)](#apidoc.element.json-rpc2.Websocket.Client)
- description and source-code
```javascript
Websocket.Client = function (_url, protocols, options) {
  options = options || {};

  this.url     = _url;
  this._driver = driver.client(this.url, {maxLength: options.maxLength, protocols: protocols});

  ['open', 'error'].forEach(function(event) {
    this._driver.on(event, function() {
      self.headers    = self._driver.headers;
      self.statusCode = self._driver.statusCode;
    });
  }, this);

  var proxy      = options.proxy || {},
      endpoint   = url.parse(proxy.origin || this.url),
      port       = endpoint.port || DEFAULT_PORTS[endpoint.protocol],
      secure     = SECURE_PROTOCOLS.indexOf(endpoint.protocol) >= 0,
      onConnect  = function() { self._onConnect() },
      netOptions = options.net || {},
      originTLS  = options.tls || {},
      socketTLS  = proxy.origin ? (proxy.tls || {}) : originTLS,
      self       = this;

  netOptions.host = socketTLS.host = endpoint.hostname;
  netOptions.port = socketTLS.port = port;

  originTLS.ca = originTLS.ca || options.ca;
  socketTLS.servername = socketTLS.servername || endpoint.hostname;

  this._stream = secure
               ? tls.connect(socketTLS, onConnect)
               : net.connect(netOptions, onConnect);

  if (proxy.origin) this._configureProxy(proxy, originTLS);

  API.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.EventSource (request, response, options)](#apidoc.element.json-rpc2.Websocket.EventSource)
- description and source-code
```javascript
Websocket.EventSource = function (request, response, options) {
  this.writable = true;
  options = options || {};

  this._stream = response.socket;
  this._ping   = options.ping  || this.DEFAULT_PING;
  this._retry  = options.retry || this.DEFAULT_RETRY;

  var scheme       = driver.isSecureRequest(request) ? 'https:' : 'http:';
  this.url         = scheme + '//' + request.headers.host + request.url;
  this.lastEventId = request.headers['last-event-id'] || '';
  this.readyState  = API.CONNECTING;

  var headers = new Headers(),
      self    = this;

  if (options.headers) {
    for (var key in options.headers) headers.set(key, options.headers[key]);
  }

  if (!this._stream || !this._stream.writable) return;
  process.nextTick(function() { self._open() });

  this._stream.setTimeout(0);
  this._stream.setNoDelay(true);

  var handshake = 'HTTP/1.1 200 OK\r\n' +
                  'Content-Type: text/event-stream\r\n' +
                  'Cache-Control: no-cache, no-store\r\n' +
                  'Connection: close\r\n' +
                  headers.toString() +
                  '\r\n' +
                  'retry: ' + Math.floor(this._retry * 1000) + '\r\n\r\n';

  this._write(handshake);

  this._stream.on('drain', function() { self.emit('drain') });

  if (this._ping)
    this._pingTimer = setInterval(function() { self.ping() }, this._ping * 1000);

  ['error', 'end'].forEach(function(event) {
    self._stream.on(event, function() { self.close() });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket.super_ (options)](#apidoc.element.json-rpc2.Websocket.super_)
- description and source-code
```javascript
Websocket.super_ = function (options) {
  options = options || {};
  driver.validateOptions(options, ['headers', 'extensions', 'maxLength', 'ping', 'proxy', 'tls', 'ca']);

  this.readable = this.writable = true;

  var headers = options.headers;
  if (headers) {
    for (var name in headers) this._driver.setHeader(name, headers[name]);
  }

  var extensions = options.extensions;
  if (extensions) {
    [].concat(extensions).forEach(this._driver.addExtension, this._driver);
  }

  this._ping          = options.ping;
  this._pingId        = 0;
  this.readyState     = API.CONNECTING;
  this.bufferedAmount = 0;
  this.protocol       = '';
  this.url            = this._driver.url;
  this.version        = this._driver.version;

  var self = this;

  this._driver.on('open',    function(e) { self._open() });
  this._driver.on('message', function(e) { self._receiveMessage(e.data) });
  this._driver.on('close',   function(e) { self._beginClose(e.reason, e.code) });

  this._driver.on('error', function(error) {
    self._emitError(error.message);
  });
  this.on('error', function() {});

  this._driver.messages.on('drain', function() {
    self.emit('drain');
  });

  if (this._ping)
    this._pingTimer = setInterval(function() {
      self._pingId += 1;
      self.ping(self._pingId.toString());
    }, this._ping * 1000);

  this._configureStream();

  if (!this._proxy) {
    this._stream.pipe(this._driver.io);
    this._driver.io.pipe(this._stream);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_ (value)](#apidoc.element.json-rpc2._)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bind"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.bind ()](#apidoc.element.json-rpc2._.bind)
- description and source-code
```javascript
_.bind = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bindKey"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.bindKey ()](#apidoc.element.json-rpc2._.bindKey)
- description and source-code
```javascript
_.bindKey = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.curry"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.curry (func, arity, guard)](#apidoc.element.json-rpc2._.curry)
- description and source-code
```javascript
function curryFunc(func, arity, guard) {
  if (guard && isIterateeCall(func, arity, guard)) {
    arity = undefined;
  }
  var result = createWrapper(func, flag, undefined, undefined, undefined, undefined, undefined, arity);
  result.placeholder = curryFunc.placeholder;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.curryRight"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.curryRight (func, arity, guard)](#apidoc.element.json-rpc2._.curryRight)
- description and source-code
```javascript
function curryFunc(func, arity, guard) {
  if (guard && isIterateeCall(func, arity, guard)) {
    arity = undefined;
  }
  var result = createWrapper(func, flag, undefined, undefined, undefined, undefined, undefined, arity);
  result.placeholder = curryFunc.placeholder;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.memoize"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.memoize (func, resolver)](#apidoc.element.json-rpc2._.memoize)
- description and source-code
```javascript
function memoize(func, resolver) {
  if (typeof func != 'function' || (resolver && typeof resolver != 'function')) {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  var memoized = function() {
    var args = arguments,
        key = resolver ? resolver.apply(this, args) : args[0],
        cache = memoized.cache;

    if (cache.has(key)) {
      return cache.get(key);
    }
    var result = func.apply(this, args);
    memoized.cache = cache.set(key, result);
    return result;
  };
  memoized.cache = new memoize.Cache;
  return memoized;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partial"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.partial ()](#apidoc.element.json-rpc2._.partial)
- description and source-code
```javascript
_.partial = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partialRight"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_.partialRight ()](#apidoc.element.json-rpc2._.partialRight)
- description and source-code
```javascript
_.partialRight = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Client"></a>[module json-rpc2.Client](#apidoc.module.json-rpc2.Client)

#### <a name="apidoc.element.json-rpc2.Client.Client"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Client ()](#apidoc.element.json-rpc2.Client.Client)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...

if (!/^wss?:\/\//i.test(self.host)) {
  self.host = 'ws://' + self.host + ':' + self.port + '/';
}

this._authHeader(headers);

socket = new WebSocket.Client(self.host, null, {headers: headers});

conn = new WebSocketConnection(self, socket);

parser = new JsonParser();

parser.onValue = function parseOnValue(decoded){
  if (this.stack.length) {
...
```



# <a name="apidoc.module.json-rpc2.Client.prototype"></a>[module json-rpc2.Client.prototype](#apidoc.module.json-rpc2.Client.prototype)

#### <a name="apidoc.element.json-rpc2.Client.prototype._authHeader"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>_authHeader (headers)](#apidoc.element.json-rpc2.Client.prototype._authHeader)
- description and source-code
```javascript
_authHeader = function (headers){
  if (this.user && this.password) {
    var buff = new Buffer(this.user + ':' + this.password).toString('base64');
    headers['Authorization'] = 'Basic ' + buff;
  }
}
```
- example usage
```shell
...
  'method' : method,
  'params' : params,
  'jsonrpc': '2.0'
});

var headers = {};

this._authHeader(headers);

// Then we build some basic headers.
headers['Host'] = this.host;
headers['Content-Length'] = Buffer.byteLength(requestJSON, 'utf8');

// Now we'll make a request to the server
var options = {
...
```

#### <a name="apidoc.element.json-rpc2.Client.prototype.call"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>call (method, params, opts, callback)](#apidoc.element.json-rpc2.Client.prototype.call)
- description and source-code
```javascript
call = function (method, params, opts, callback){
  if (_.isFunction(opts)) {
    callback = opts;
    opts = {};
  }
  opts = opts || {};
  EventEmitter.trace('-->', 'Http call (method ' + method + '): ' + JSON.stringify(params));

  this.connectHttp(method, params, opts, function connectHttp(id, request, response){
    // Check if response object exists.
    if (!response) {
      callback(new Error('Have no response object'));
      return;
    }

    var data = '';

    response.on('data', function responseData(chunk){
      data += chunk;
    });

    response.on('end', function responseEnd(){
      if (response.statusCode !== 200) {
        callback(new Error('"' + response.statusCode + '"' + data))
        ;
        return;
      }
      var decoded = JSON.parse(data);
      if (_.isFunction(callback)) {
        if (!decoded.error) {
          decoded.error = null;
        }
        callback(decoded.error, decoded.result);
      }
    });
  });
}
```
- example usage
```shell
...
'''js
var rpc = require('json-rpc2');

var client = rpc.Client.$create(8000, 'localhost');

// Call add function on the server

client.call('add', [1, 2], function(err, result) {
    console.log('1 + 2 = ' + result);
});
'''

Create a raw (socket) server using:

'''js
...
```

#### <a name="apidoc.element.json-rpc2.Client.prototype.connectHttp"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>connectHttp (method, params, opts, callback)](#apidoc.element.json-rpc2.Client.prototype.connectHttp)
- description and source-code
```javascript
connectHttp = function (method, params, opts, callback){
  if (_.isFunction(opts)) {
    callback = opts;
    opts = {};
  }
  opts = opts || {};

  var id = 1, self = this;

  // First we encode the request into JSON
  var requestJSON = JSON.stringify({
    'id'     : id,
    'method' : method,
    'params' : params,
    'jsonrpc': '2.0'
  });

  var headers = {};

  this._authHeader(headers);

  // Then we build some basic headers.
  headers['Host'] = this.host;
  headers['Content-Length'] = Buffer.byteLength(requestJSON, 'utf8');

  // Now we'll make a request to the server
  var options = {
    hostname: this.host,
    port    : this.port,
    path    : opts.path || '/',
    method  : 'POST',
    headers : headers
  };
  var request;
  if(opts.https === true) {
    if(opts.rejectUnauthorized !== undefined) {
      options.rejectUnauthorized = opts.rejectUnauthorized;
    }
    request = https.request(options);
  } else {
    request = http.request(options);
  }


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
}
```
- example usage
```shell
...
      stream       : function (method, params, opts, callback){
        if (_.isFunction(opts)) {
          callback = opts;
          opts = {};
        }
        opts = opts || {};

        this.connectHttp(method, params, opts, function connectHttp(id, request, response){
          if (_.isFunction(callback)) {
var connection = new EventEmitter();

connection.id = id;
connection.req = request;
connection.res = response;
...
```

#### <a name="apidoc.element.json-rpc2.Client.prototype.connectSocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>connectSocket (callback)](#apidoc.element.json-rpc2.Client.prototype.connectSocket)
- description and source-code
```javascript
connectSocket = function (callback){
  var self = this, socket, conn, parser;

  socket = net.connect(this.port, this.host, function netConnect(){
    // Submit non-standard 'auth' message for raw sockets.
    if (!_.isEmpty(self.user) && !_.isEmpty(self.password)) {
      conn.call('auth', [self.user, self.password], function connectionAuth(err){
        if (err) {
          callback(err);
        } else {
          callback(null, conn);
        }
      });
      return;
    }

    if (_.isFunction(callback)) {
      callback(null, conn);
    }
  });

  conn = new SocketConnection(self, socket);
  parser = new JsonParser();

  parser.onValue = function parseOnValue(decoded){
    if (this.stack.length) {
      return;
    }

    conn.handleMessage(decoded);
  };

  socket.on('data', function socketData(chunk){
    try {
      parser.write(chunk);
    } catch (err) {
      EventEmitter.trace('<--', err.toString());
    }
  });

  return conn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Client.prototype.connectWebsocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>connectWebsocket (callback)](#apidoc.element.json-rpc2.Client.prototype.connectWebsocket)
- description and source-code
```javascript
connectWebsocket = function (callback){
  var self = this, conn, socket, parser, headers = {};

  if (!/^wss?:\/\//i.test(self.host)) {
    self.host = 'ws://' + self.host + ':' + self.port + '/';
  }

  this._authHeader(headers);

  socket = new WebSocket.Client(self.host, null, {headers: headers});

  conn = new WebSocketConnection(self, socket);

  parser = new JsonParser();

  parser.onValue = function parseOnValue(decoded){
    if (this.stack.length) {
      return;
    }

    conn.handleMessage(decoded);
  };

  socket.on('error', function socketError(event){
    callback(event.reason);
  });

  socket.on('open', function socketOpen(){
    callback(null, conn);
  });

  socket.on('message', function socketMessage(event){
    try {
      parser.write(event.data);
    } catch (err) {
      EventEmitter.trace('<--', err.toString());
    }
  });

  return conn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Client.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>construct ()](#apidoc.element.json-rpc2.Client.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Client.prototype.stream"></a>[function <span class="apidocSignatureSpan">json-rpc2.Client.prototype.</span>stream (method, params, opts, callback)](#apidoc.element.json-rpc2.Client.prototype.stream)
- description and source-code
```javascript
stream = function (method, params, opts, callback){
  if (_.isFunction(opts)) {
    callback = opts;
    opts = {};
  }
  opts = opts || {};

  this.connectHttp(method, params, opts, function connectHttp(id, request, response){
    if (_.isFunction(callback)) {
      var connection = new EventEmitter();

      connection.id = id;
      connection.req = request;
      connection.res = response;

      connection.expose = function connectionExpose(method, callback){
        connection.on('call:' + method, function connectionCall(data){
          callback.call(null, data.params || []);
        });
      };

      connection.end = function connectionEnd(){
        this.req.connection.end();
      };

      // We need to buffer the response chunks in a nonblocking way.
      var parser = new JsonParser();
      parser.onValue = function (decoded){
        if (this.stack.length) {
          return;
        }

        connection.emit('data', decoded);
        if (
          decoded.hasOwnProperty('result') ||
            decoded.hasOwnProperty('error') &&
              decoded.id === id && _.isFunction(callback)
          ) {
          connection.emit('result', decoded);
        }
        else if (decoded.hasOwnProperty('method')) {
          connection.emit('call:' + decoded.method, decoded);
        }
      };

      if (response) {
        // Handle headers
        connection.res.once('data', function connectionOnce(data){
          if (connection.res.statusCode === 200) {
            callback(null, connection);
          } else {
            callback(new Error('"' + connection.res.statusCode + '"' + data));
          }
        });

        connection.res.on('data', function connectionData(chunk){
          try {
            parser.write(chunk);
          } catch (err) {
            // TODO: Is ignoring invalid data the right thing to do?
          }
        });

        connection.res.on('end', function connectionEnd(){
          // TODO: Issue an error if there has been no valid response message
        });
      }
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Connection"></a>[module json-rpc2.Connection](#apidoc.module.json-rpc2.Connection)

#### <a name="apidoc.element.json-rpc2.Connection.Connection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Connection ()](#apidoc.element.json-rpc2.Connection.Connection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Connection.prototype"></a>[module json-rpc2.Connection.prototype](#apidoc.module.json-rpc2.Connection.prototype)

#### <a name="apidoc.element.json-rpc2.Connection.prototype.call"></a>[function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>call (method, params, callback)](#apidoc.element.json-rpc2.Connection.prototype.call)
- description and source-code
```javascript
call = function (method, params, callback){
  if (!_.isArray(params)) {
    params = [params];
  }

  var id = null;
  if (_.isFunction(callback)) {
    id = ++this.latestId;
    this.callbacks[id] = callback;
  }

  EventEmitter.trace('-->', 'Connection call (method ' + method + '): ' + JSON.stringify(params));

  var data = JSON.stringify({
    jsonrpc: '2.0',
    method : method,
    params : params,
    id     : id
  });
  this.write(data);
}
```
- example usage
```shell
...
'''js
var rpc = require('json-rpc2');

var client = rpc.Client.$create(8000, 'localhost');

// Call add function on the server

client.call('add', [1, 2], function(err, result) {
    console.log('1 + 2 = ' + result);
});
'''

Create a raw (socket) server using:

'''js
...
```

#### <a name="apidoc.element.json-rpc2.Connection.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>construct ()](#apidoc.element.json-rpc2.Connection.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Connection.prototype.handleMessage"></a>[function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>handleMessage (msg)](#apidoc.element.json-rpc2.Connection.prototype.handleMessage)
- description and source-code
```javascript
handleMessage = function (msg){
  var self = this;

  if (msg) {
    if (
        (msg.hasOwnProperty('result') || msg.hasOwnProperty('error')) &&
        msg.hasOwnProperty('id')
      ) {
      // Are we in the client?
      try {
        this.callbacks[msg.id](msg.error, msg.result);
        delete this.callbacks[msg.id];
      } catch (err) {
        EventEmitter.trace('<---', 'Callback not found ' + msg.id + ': ' + (err.stack ? err.stack : err.toString()));
      }
    } else if (msg.hasOwnProperty('method')) {
      // Are we in the server?
      this.endpoint.handleCall(msg, this, function handleCall(err, result){
        if (err) {
          self.emit('error', err);

          EventEmitter.trace('-->',
            'Failure ' + (EventEmitter.hasId(msg) ? '(id ' + msg.id + ')' : '') + ': ' +
              (err.stack ? err.stack : err.toString())
          );
        }

        // Return if it's just a notification (no id)
        if (!EventEmitter.hasId(msg)) {
          return;
        }

        if (err) {
          err = err.toString();
          result = null;
        } else {
          EventEmitter.trace('-->', 'Response (id ' + msg.id + '): ' +
            JSON.stringify(result));
          err = null;
        }

        self.sendReply(err, result, msg.id);
      });
    }
  }
}
```
- example usage
```shell
...
parser = new JsonParser();

parser.onValue = function parseOnValue(decoded){
  if (this.stack.length) {
    return;
  }

  conn.handleMessage(decoded);
};

socket.on('error', function socketError(event){
  callback(event.reason);
});

socket.on('open', function socketOpen(){
...
```

#### <a name="apidoc.element.json-rpc2.Connection.prototype.sendReply"></a>[function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>sendReply (err, result, id)](#apidoc.element.json-rpc2.Connection.prototype.sendReply)
- description and source-code
```javascript
sendReply = function (err, result, id){
  var data = JSON.stringify({
    jsonrpc: '2.0',
    result : result,
    error  : err,
    id     : id
  });

  this.write(data);
}
```
- example usage
```shell
...
          result = null;
        } else {
          EventEmitter.trace('-->', 'Response (id ' + msg.id + '): ' +
            JSON.stringify(result));
          err = null;
        }

        self.sendReply(err, result, msg.id);
      });
    }
  }
},

sendReply: function (err, result, id){
  var data = JSON.stringify({
...
```

#### <a name="apidoc.element.json-rpc2.Connection.prototype.stream"></a>[function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>stream (onend)](#apidoc.element.json-rpc2.Connection.prototype.stream)
- description and source-code
```javascript
stream = function (onend){
  if (_.isFunction(onend)) {
    this.on('end', function(){
      onend();
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Connection.prototype.write"></a>[function <span class="apidocSignatureSpan">json-rpc2.Connection.prototype.</span>write ()](#apidoc.element.json-rpc2.Connection.prototype.write)
- description and source-code
```javascript
write = function (){
  throw new Error('Tried to write data on unsupported connection type.');
}
```
- example usage
```shell
...


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
connectWebsocket: function(callback){
  var self = this, conn, socket, parser, headers = {};
...
```



# <a name="apidoc.module.json-rpc2.ES5Class"></a>[module json-rpc2.ES5Class](#apidoc.module.json-rpc2.ES5Class)

#### <a name="apidoc.element.json-rpc2.ES5Class.ES5Class"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>ES5Class ()](#apidoc.element.json-rpc2.ES5Class.ES5Class)
- description and source-code
```javascript
function ES5Class(){ }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.ES5Class.prototype"></a>[module json-rpc2.ES5Class.prototype](#apidoc.module.json-rpc2.ES5Class.prototype)

#### <a name="apidoc.element.json-rpc2.ES5Class.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.ES5Class.prototype.</span>construct ()](#apidoc.element.json-rpc2.ES5Class.prototype.construct)
- description and source-code
```javascript
function noop(){}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Endpoint"></a>[module json-rpc2.Endpoint](#apidoc.module.json-rpc2.Endpoint)

#### <a name="apidoc.element.json-rpc2.Endpoint.Endpoint"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Endpoint ()](#apidoc.element.json-rpc2.Endpoint.Endpoint)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Endpoint.prototype"></a>[module json-rpc2.Endpoint.prototype](#apidoc.module.json-rpc2.Endpoint.prototype)

#### <a name="apidoc.element.json-rpc2.Endpoint.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.Endpoint.prototype.</span>construct ()](#apidoc.element.json-rpc2.Endpoint.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Endpoint.prototype.expose"></a>[function <span class="apidocSignatureSpan">json-rpc2.Endpoint.prototype.</span>expose (name, func, scope)](#apidoc.element.json-rpc2.Endpoint.prototype.expose)
- description and source-code
```javascript
expose = function (name, func, scope){
  if (_.isFunction(func)) {
    EventEmitter.trace('***', 'exposing: ' + name);
    this.functions[name] = func;

    if (scope) {
      this.scopes[name] = scope;
    }
  } else {
    var funcs = [];

    for (var funcName in func) {
      if (Object.prototype.hasOwnProperty.call(func, funcName)) {
        var funcObj = func[funcName];
        if (_.isFunction(funcObj)) {
          this.functions[name + '.' + funcName] = funcObj;
          funcs.push(funcName);

          if (scope) {
            this.scopes[name + '.' + funcName] = scope;
          }
        }
      }
    }

    EventEmitter.trace('***', 'exposing module: ' + name + ' [funs: ' + funcs.join(', ') + ']');
  }
  return func;
}
```
- example usage
```shell
...
}
});

function add(args, opt, callback) {
  callback(null, args[0] + args[1]);
}

server.expose('add', add);

// you can expose an entire object as well:

server.expose('namespace', {
'function1': function(){},
'function2': function(){},
'function3': function(){}
...
```

#### <a name="apidoc.element.json-rpc2.Endpoint.prototype.handleCall"></a>[function <span class="apidocSignatureSpan">json-rpc2.Endpoint.prototype.</span>handleCall (decoded, conn, callback)](#apidoc.element.json-rpc2.Endpoint.prototype.handleCall)
- description and source-code
```javascript
handleCall = function (decoded, conn, callback){
  EventEmitter.trace('<--', 'Request (id ' + decoded.id + '): ' +
    decoded.method + '(' + JSON.stringify(decoded.params) + ')');

  if (!this.functions.hasOwnProperty(decoded.method)) {
    callback(new Error.MethodNotFound('Unknown RPC call "' + decoded.method + '"'));
    return;
  }

  var method = this.functions[decoded.method];
  var scope = this.scopes[decoded.method] || this.defaultScope;

  // Try to call the method, but intercept errors and call our
  // error handler.
  try {
    method.call(scope, decoded.params, conn, callback);
  } catch (err) {
    callback(err);
  }
}
```
- example usage
```shell
...
              this.callbacks[msg.id](msg.error, msg.result);
              delete this.callbacks[msg.id];
            } catch (err) {
              EventEmitter.trace('<---', 'Callback not found ' + msg.id + ': ' + (err.stack ? err.stack : err.toString()));
            }
          } else if (msg.hasOwnProperty('method')) {
            // Are we in the server?
            this.endpoint.handleCall(msg, this, function handleCall(err, result){
              if (err) {
self.emit('error', err);

EventEmitter.trace('-->',
  'Failure ' + (EventEmitter.hasId(msg) ? '(id ' + msg.id + ')' : '') + ': ' +
    (err.stack ? err.stack : err.toString())
);
...
```



# <a name="apidoc.module.json-rpc2.Error"></a>[module json-rpc2.Error](#apidoc.module.json-rpc2.Error)

#### <a name="apidoc.element.json-rpc2.Error.AbstractError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>AbstractError ()](#apidoc.element.json-rpc2.Error.AbstractError)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Error.InternalError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>InternalError ()](#apidoc.element.json-rpc2.Error.InternalError)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...

Endpoint.trace('-->', 'Failure (id ' + decoded.id + '): ' +
  (err.stack ? err.stack : err.toString()));

result = null;

if (!(err instanceof Error.AbstractError)) {
  err = new Error.InternalError(err.toString());
}

response = {
  'jsonrpc': '2.0',
  'error': {code: err.code, message: err.message }
};
...
```

#### <a name="apidoc.element.json-rpc2.Error.InvalidParams"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>InvalidParams ()](#apidoc.element.json-rpc2.Error.InvalidParams)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      parts = auth.split(/:/), // split on colon
      username = parts[0],
      password = parts[1];

    if (!this.authHandler(username, password)) {
      if (res) {
        classes.EventEmitter.trace('<--', 'Unauthorized request');
        Server.handleHttpError(req, res, new Error.InvalidParams(UNAUTHORIZED), self.opts.headers);
      }
      return false;
    }
  }
  return true;
},
/**
...
```

#### <a name="apidoc.element.json-rpc2.Error.InvalidRequest"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>InvalidRequest ()](#apidoc.element.json-rpc2.Error.InvalidRequest)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
if (!self._checkAuth(req, res)) {
  return;
}

Endpoint.trace('<--', 'Accepted http request');

if (req.method !== 'POST') {
  Server.handleHttpError(req, res, new Error.InvalidRequest(METHOD_NOT_ALLOWED), self.opts.headers);
  return;
}

var handle = function handle(buf) {
  // Check if json is valid JSON document
  var decoded;
...
```

#### <a name="apidoc.element.json-rpc2.Error.MethodNotFound"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>MethodNotFound ()](#apidoc.element.json-rpc2.Error.MethodNotFound)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
return func;
      },
      handleCall: function (decoded, conn, callback){
EventEmitter.trace('<--', 'Request (id ' + decoded.id + '): ' +
  decoded.method + '(' + JSON.stringify(decoded.params) + ')');

if (!this.functions.hasOwnProperty(decoded.method)) {
  callback(new Error.MethodNotFound('Unknown RPC call "' + decoded.method + '"'));
  return;
}

var method = this.functions[decoded.method];
var scope = this.scopes[decoded.method] || this.defaultScope;

// Try to call the method, but intercept errors and call our
...
```

#### <a name="apidoc.element.json-rpc2.Error.ParseError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>ParseError ()](#apidoc.element.json-rpc2.Error.ParseError)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
        var handle = function handle(buf) {
// Check if json is valid JSON document
var decoded;

try {
  decoded = JSON.parse(buf);
} catch (error) {
  Server.handleHttpError(req, res, new Error.ParseError(INVALID_REQUEST), self.opts.headers);
  return;
}

// Check for the required fields, and if they aren't there, then
// dispatch to the handleHttpError function.
if (!decoded.method || !decoded.params) {
  Endpoint.trace('-->', 'Response (invalid request)');
...
```

#### <a name="apidoc.element.json-rpc2.Error.ServerError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>ServerError ()](#apidoc.element.json-rpc2.Error.ServerError)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Error.AbstractError"></a>[module json-rpc2.Error.AbstractError](#apidoc.module.json-rpc2.Error.AbstractError)

#### <a name="apidoc.element.json-rpc2.Error.AbstractError.AbstractError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.</span>AbstractError ()](#apidoc.element.json-rpc2.Error.AbstractError.AbstractError)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Error.AbstractError.captureStackTrace"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.</span>captureStackTrace ()](#apidoc.element.json-rpc2.Error.AbstractError.captureStackTrace)
- description and source-code
```javascript
function captureStackTrace() { [native code] }
```
- example usage
```shell
...

Errors.AbstractError = classes.ES5Class.$define('AbstractError', {
  construct: function(message, extra){
    this.name = this.$className;
    this.extra = extra || {};
    this.message = message || this.$className;

    Error.captureStackTrace(this, this.$class);
  },
  toString: function(){
    return this.message;
  }
}).$inherit(Error, []);

Errors.ParseError = Errors.AbstractError.$define('ParseError', {
...
```



# <a name="apidoc.module.json-rpc2.Error.AbstractError.prototype"></a>[module json-rpc2.Error.AbstractError.prototype](#apidoc.module.json-rpc2.Error.AbstractError.prototype)

#### <a name="apidoc.element.json-rpc2.Error.AbstractError.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.prototype.</span>construct (message, extra)](#apidoc.element.json-rpc2.Error.AbstractError.prototype.construct)
- description and source-code
```javascript
construct = function (message, extra){
  this.name = this.$className;
  this.extra = extra || {};
  this.message = message || this.$className;

  Error.captureStackTrace(this, this.$class);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Error.AbstractError.prototype.toString"></a>[function <span class="apidocSignatureSpan">json-rpc2.Error.AbstractError.prototype.</span>toString ()](#apidoc.element.json-rpc2.Error.AbstractError.prototype.toString)
- description and source-code
```javascript
toString = function (){
  return this.message;
}
```
- example usage
```shell
...
  this.port = port;
  this.host = host;
  this.user = user;
  this.password = password;
},
_authHeader: function(headers){
  if (this.user && this.password) {
    var buff = new Buffer(this.user + ':' + this.password).toString('base64');
    headers['Authorization'] = 'Basic ' + buff;
  }
},
/**
 * Make HTTP connection/request.
 *
 * In HTTP mode, we get to submit exactly one message and receive up to n
...
```



# <a name="apidoc.module.json-rpc2.EventEmitter"></a>[module json-rpc2.EventEmitter](#apidoc.module.json-rpc2.EventEmitter)

#### <a name="apidoc.element.json-rpc2.EventEmitter.EventEmitter"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>EventEmitter ()](#apidoc.element.json-rpc2.EventEmitter.EventEmitter)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.hasId"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.</span>hasId (request)](#apidoc.element.json-rpc2.EventEmitter.hasId)
- description and source-code
```javascript
hasId = function (request) {
  return request && typeof request['id'] !== 'undefined' &&
  (
    (typeof(request['id']) === 'number' && /^\-?\d+$/.test(request['id'])) ||
    (typeof(request['id']) === 'string') || (request['id'] === null)
  );
}
```
- example usage
```shell
...
          } else if (msg.hasOwnProperty('method')) {
            // Are we in the server?
            this.endpoint.handleCall(msg, this, function handleCall(err, result){
if (err) {
  self.emit('error', err);

  EventEmitter.trace('-->',
    'Failure ' + (EventEmitter.hasId(msg) ? '(id ' + msg.id + ')' : '') + ': ' +
      (err.stack ? err.stack : err.toString())
  );
}

// Return if it's just a notification (no id)
if (!EventEmitter.hasId(msg)) {
  return;
...
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.trace"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.</span>trace (direction, message)](#apidoc.element.json-rpc2.EventEmitter.trace)
- description and source-code
```javascript
trace = function (direction, message){
  var msg = '   ' + direction + '   ' + message;
  debug(msg);
  return msg;
}
```
- example usage
```shell
...
    callback(null, conn);
  });

  socket.on('message', function socketMessage(event){
    try {
      parser.write(event.data);
    } catch (err) {
      EventEmitter.trace('<--', err.toString());
    }
  });

  return conn;
},
/**
 * Make Socket connection.
...
```



# <a name="apidoc.module.json-rpc2.EventEmitter.prototype"></a>[module json-rpc2.EventEmitter.prototype](#apidoc.module.json-rpc2.EventEmitter.prototype)

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.addListener"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>addListener (event, fn, context)](#apidoc.element.json-rpc2.EventEmitter.prototype.addListener)
- description and source-code
```javascript
function on(event, fn, context) {
  var listener = new EE(fn, context || this)
    , evt = prefix ? prefix + event : event;

  if (!this._events) this._events = prefix ? {} : Object.create(null);
  if (!this._events[evt]) this._events[evt] = listener;
  else {
    if (!this._events[evt].fn) this._events[evt].push(listener);
    else this._events[evt] = [
      this._events[evt], listener
    ];
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.emit"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>emit (event, a1, a2, a3, a4, a5)](#apidoc.element.json-rpc2.EventEmitter.prototype.emit)
- description and source-code
```javascript
function emit(event, a1, a2, a3, a4, a5) {
  var evt = prefix ? prefix + event : event;

  if (!this._events || !this._events[evt]) return false;

  var listeners = this._events[evt]
    , len = arguments.length
    , args
    , i;

  if ('function' === typeof listeners.fn) {
    if (listeners.once) this.removeListener(event, listeners.fn, undefined, true);

    switch (len) {
      case 1: return listeners.fn.call(listeners.context), true;
      case 2: return listeners.fn.call(listeners.context, a1), true;
      case 3: return listeners.fn.call(listeners.context, a1, a2), true;
      case 4: return listeners.fn.call(listeners.context, a1, a2, a3), true;
      case 5: return listeners.fn.call(listeners.context, a1, a2, a3, a4), true;
      case 6: return listeners.fn.call(listeners.context, a1, a2, a3, a4, a5), true;
    }

    for (i = 1, args = new Array(len -1); i < len; i++) {
      args[i - 1] = arguments[i];
    }

    listeners.fn.apply(listeners.context, args);
  } else {
    var length = listeners.length
      , j;

    for (i = 0; i < length; i++) {
      if (listeners[i].once) this.removeListener(event, listeners[i].fn, undefined, true);

      switch (len) {
        case 1: listeners[i].fn.call(listeners[i].context); break;
        case 2: listeners[i].fn.call(listeners[i].context, a1); break;
        case 3: listeners[i].fn.call(listeners[i].context, a1, a2); break;
        default:
          if (!args) for (j = 1, args = new Array(len -1); j < len; j++) {
            args[j - 1] = arguments[j];
          }

          listeners[i].fn.apply(listeners[i].context, args);
      }
    }
  }

  return true;
}
```
- example usage
```shell
...
            // We need to buffer the response chunks in a nonblocking way.
            var parser = new JsonParser();
            parser.onValue = function (decoded){
if (this.stack.length) {
  return;
}

connection.emit('data', decoded);
if (
  decoded.hasOwnProperty('result') ||
    decoded.hasOwnProperty('error') &&
      decoded.id === id && _.isFunction(callback)
  ) {
  connection.emit('result', decoded);
}
...
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.eventNames"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>eventNames ()](#apidoc.element.json-rpc2.EventEmitter.prototype.eventNames)
- description and source-code
```javascript
function eventNames() {
  var events = this._events
    , names = []
    , name;

  if (!events) return names;

  for (name in events) {
    if (has.call(events, name)) names.push(prefix ? name.slice(1) : name);
  }

  if (Object.getOwnPropertySymbols) {
    return names.concat(Object.getOwnPropertySymbols(events));
  }

  return names;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.listeners"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>listeners (event, exists)](#apidoc.element.json-rpc2.EventEmitter.prototype.listeners)
- description and source-code
```javascript
function listeners(event, exists) {
  var evt = prefix ? prefix + event : event
    , available = this._events && this._events[evt];

  if (exists) return !!available;
  if (!available) return [];
  if (available.fn) return [available.fn];

  for (var i = 0, l = available.length, ee = new Array(l); i < l; i++) {
    ee[i] = available[i].fn;
  }

  return ee;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.off"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>off (event, fn, context, once)](#apidoc.element.json-rpc2.EventEmitter.prototype.off)
- description and source-code
```javascript
function removeListener(event, fn, context, once) {
  var evt = prefix ? prefix + event : event;

  if (!this._events || !this._events[evt]) return this;

  var listeners = this._events[evt]
    , events = [];

  if (fn) {
    if (listeners.fn) {
      if (
           listeners.fn !== fn
        || (once && !listeners.once)
        || (context && listeners.context !== context)
      ) {
        events.push(listeners);
      }
    } else {
      for (var i = 0, length = listeners.length; i < length; i++) {
        if (
             listeners[i].fn !== fn
          || (once && !listeners[i].once)
          || (context && listeners[i].context !== context)
        ) {
          events.push(listeners[i]);
        }
      }
    }
  }

  //
  // Reset the array, or remove it completely if we have no more listeners.
  //
  if (events.length) {
    this._events[evt] = events.length === 1 ? events[0] : events;
  } else {
    delete this._events[evt];
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.on"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>on (event, fn, context)](#apidoc.element.json-rpc2.EventEmitter.prototype.on)
- description and source-code
```javascript
function on(event, fn, context) {
  var listener = new EE(fn, context || this)
    , evt = prefix ? prefix + event : event;

  if (!this._events) this._events = prefix ? {} : Object.create(null);
  if (!this._events[evt]) this._events[evt] = listener;
  else {
    if (!this._events[evt].fn) this._events[evt].push(listener);
    else this._events[evt] = [
      this._events[evt], listener
    ];
  }

  return this;
}
```
- example usage
```shell
...
  } else {
    request = http.request(options);
  }


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
...
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.once"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>once (event, fn, context)](#apidoc.element.json-rpc2.EventEmitter.prototype.once)
- description and source-code
```javascript
function once(event, fn, context) {
  var listener = new EE(fn, context || this, true)
    , evt = prefix ? prefix + event : event;

  if (!this._events) this._events = prefix ? {} : Object.create(null);
  if (!this._events[evt]) this._events[evt] = listener;
  else {
    if (!this._events[evt].fn) this._events[evt].push(listener);
    else this._events[evt] = [
      this._events[evt], listener
    ];
  }

  return this;
}
```
- example usage
```shell
...
  else if (decoded.hasOwnProperty('method')) {
    connection.emit('call:' + decoded.method, decoded);
  }
};

if (response) {
  // Handle headers
  connection.res.once('data', function connectionOnce(data){
    if (connection.res.statusCode === 200) {
      callback(null, connection);
    } else {
      callback(new Error('"' + connection.res.statusCode + '"' + data));
    }
  });
...
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.removeAllListeners"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>removeAllListeners (event)](#apidoc.element.json-rpc2.EventEmitter.prototype.removeAllListeners)
- description and source-code
```javascript
function removeAllListeners(event) {
  if (!this._events) return this;

  if (event) delete this._events[prefix ? prefix + event : event];
  else this._events = prefix ? {} : Object.create(null);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.removeListener"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>removeListener (event, fn, context, once)](#apidoc.element.json-rpc2.EventEmitter.prototype.removeListener)
- description and source-code
```javascript
function removeListener(event, fn, context, once) {
  var evt = prefix ? prefix + event : event;

  if (!this._events || !this._events[evt]) return this;

  var listeners = this._events[evt]
    , events = [];

  if (fn) {
    if (listeners.fn) {
      if (
           listeners.fn !== fn
        || (once && !listeners.once)
        || (context && listeners.context !== context)
      ) {
        events.push(listeners);
      }
    } else {
      for (var i = 0, length = listeners.length; i < length; i++) {
        if (
             listeners[i].fn !== fn
          || (once && !listeners[i].once)
          || (context && listeners[i].context !== context)
        ) {
          events.push(listeners[i]);
        }
      }
    }
  }

  //
  // Reset the array, or remove it completely if we have no more listeners.
  //
  if (events.length) {
    this._events[evt] = events.length === 1 ? events[0] : events;
  } else {
    delete this._events[evt];
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.EventEmitter.prototype.setMaxListeners"></a>[function <span class="apidocSignatureSpan">json-rpc2.EventEmitter.prototype.</span>setMaxListeners ()](#apidoc.element.json-rpc2.EventEmitter.prototype.setMaxListeners)
- description and source-code
```javascript
function setMaxListeners() {
  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.HttpServerConnection"></a>[module json-rpc2.HttpServerConnection](#apidoc.module.json-rpc2.HttpServerConnection)

#### <a name="apidoc.element.json-rpc2.HttpServerConnection.HttpServerConnection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>HttpServerConnection ()](#apidoc.element.json-rpc2.HttpServerConnection.HttpServerConnection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      response.id = decoded.id;
      reply(response);
    } else {
      reply();
    }
  };

  var conn = new classes.HttpServerConnection(self, req, res);

  self.handleCall(decoded, conn, callback);
}; // function handle(buf)

req.on('data', function requestData(chunk) {
  buffer = buffer + chunk;
});
...
```



# <a name="apidoc.module.json-rpc2.HttpServerConnection.prototype"></a>[module json-rpc2.HttpServerConnection.prototype](#apidoc.module.json-rpc2.HttpServerConnection.prototype)

#### <a name="apidoc.element.json-rpc2.HttpServerConnection.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.HttpServerConnection.prototype.</span>construct ()](#apidoc.element.json-rpc2.HttpServerConnection.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.HttpServerConnection.prototype.stream"></a>[function <span class="apidocSignatureSpan">json-rpc2.HttpServerConnection.prototype.</span>stream ()](#apidoc.element.json-rpc2.HttpServerConnection.prototype.stream)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.HttpServerConnection.prototype.write"></a>[function <span class="apidocSignatureSpan">json-rpc2.HttpServerConnection.prototype.</span>write (data)](#apidoc.element.json-rpc2.HttpServerConnection.prototype.write)
- description and source-code
```javascript
write = function (data){
  if (!this.isStreaming) {
    throw new Error('Cannot send extra messages via non - streaming HTTP');
  }

  if (!this.res.connection.writable) {
    // Client disconnected, we'll quietly fail
    return;
  }

  this.res.write(data);
}
```
- example usage
```shell
...


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
connectWebsocket: function(callback){
  var self = this, conn, socket, parser, headers = {};
...
```



# <a name="apidoc.module.json-rpc2.Server"></a>[module json-rpc2.Server](#apidoc.module.json-rpc2.Server)

#### <a name="apidoc.element.json-rpc2.Server.Server"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Server ()](#apidoc.element.json-rpc2.Server.Server)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Server.handleHttpError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.</span>handleHttpError (req, res, error, custom_headers)](#apidoc.element.json-rpc2.Server.handleHttpError)
- description and source-code
```javascript
handleHttpError = function (req, res, error, custom_headers) {
  var message = JSON.stringify({
    'jsonrpc': '2.0',
    'error': {code: error.code, message: error.message},
    'id': null
  });
  custom_headers = custom_headers || {};
  var headers = extend({
      'Content-Type': 'application/json',
      'Content-Length': Buffer.byteLength(message),
      'Access-Control-Allow-Headers': 'Content-Type',
      'Allow': 'POST'
  }, custom_headers);

<span class="apidocCodeCommentSpan">  /*if (code === 401) {
   headers['WWW-Authenticate'] = 'Basic realm=' + 'JSON-RPC' + '';
   }*/
</span>
  if (res.writeHead) {
    res.writeHead(200, headers);
    res.write(message);
  } else {
    headers['Content-Length'] += 3;
    res.write(headers + '\n\n' + message + '\n');
  }
  res.end();
}
```
- example usage
```shell
...
      parts = auth.split(/:/), // split on colon
      username = parts[0],
      password = parts[1];

    if (!this.authHandler(username, password)) {
      if (res) {
        classes.EventEmitter.trace('<--', 'Unauthorized request');
        Server.handleHttpError(req, res, new Error.InvalidParams(UNAUTHORIZED), self.opts.headers);
      }
      return false;
    }
  }
  return true;
},
/**
...
```



# <a name="apidoc.module.json-rpc2.Server.prototype"></a>[module json-rpc2.Server.prototype](#apidoc.module.json-rpc2.Server.prototype)

#### <a name="apidoc.element.json-rpc2.Server.prototype._checkAuth"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>_checkAuth (req, res)](#apidoc.element.json-rpc2.Server.prototype._checkAuth)
- description and source-code
```javascript
_checkAuth = function (req, res) {
  var self = this;

  if (self.authHandler) {
    var
      authHeader = req.headers['authorization'] || '', // get the header
      authToken = authHeader.split(/\s+/).pop() || '', // get the token
      auth = new Buffer(authToken, 'base64').toString(), // base64 -> string
      parts = auth.split(/:/), // split on colon
      username = parts[0],
      password = parts[1];

    if (!this.authHandler(username, password)) {
      if (res) {
        classes.EventEmitter.trace('<--', 'Unauthorized request');
        Server.handleHttpError(req, res, new Error.InvalidParams(UNAUTHORIZED), self.opts.headers);
      }
      return false;
    }
  }
  return true;
}
```
- example usage
```shell
...
  Endpoint.trace('***', 'Server listening on http://' +
    (host || '127.0.0.1') + ':' + port + '/');
}

if (this.opts.websocket === true) {
  server.on('upgrade', function onUpgrade(req, socket, body) {
    if (WebSocket.isWebSocket(req)) {
      if (self._checkAuth(req, socket)) {
        self.handleWebsocket(req, socket, body);
      }
    }
  });
}

return server;
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>construct ()](#apidoc.element.json-rpc2.Server.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.enableAuth"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>enableAuth (handler, password)](#apidoc.element.json-rpc2.Server.prototype.enableAuth)
- description and source-code
```javascript
enableAuth = function (handler, password) {
  if (!_.isFunction(handler)) {
    var user = '' + handler;
    password = '' + password;

    handler = function checkAuth(suppliedUser, suppliedPassword) {
      return user === suppliedUser && password === suppliedPassword;
    };
  }

  this.authHandler = handler;
}
```
- example usage
```shell
...

'''js
var rpc = require('json-rpc2');

var server = rpc.Server.$create();

// non-standard auth for RPC, when using this module using both client and server, works out-of-the-box
server.enableAuth('user', 'pass');

// Listen on socket
server.listenRaw(8080, 'localhost');
'''

## Extend, overwrite, overload
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.handleHttp"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleHttp (req, res)](#apidoc.element.json-rpc2.Server.prototype.handleHttp)
- description and source-code
```javascript
handleHttp = function (req, res) {
  var buffer = '', self = this;
  var headers;

  if (req.method === 'OPTIONS') {
    headers = {
      'Content-Length': 0,
      'Access-Control-Allow-Headers': 'Accept, Authorization, Content-Type'
    };
    headers = extend({}, headers, self.opts.headers);
    res.writeHead(200, headers);
    res.end();
    return;
  }

  if (!self._checkAuth(req, res)) {
    return;
  }

  Endpoint.trace('<--', 'Accepted http request');

  if (req.method !== 'POST') {
    Server.handleHttpError(req, res, new Error.InvalidRequest(METHOD_NOT_ALLOWED), self.opts.headers);
    return;
  }

  var handle = function handle(buf) {
    // Check if json is valid JSON document
    var decoded;

    try {
      decoded = JSON.parse(buf);
    } catch (error) {
      Server.handleHttpError(req, res, new Error.ParseError(INVALID_REQUEST), self.opts.headers);
      return;
    }

    // Check for the required fields, and if they aren't there, then
    // dispatch to the handleHttpError function.
    if (!decoded.method || !decoded.params) {
      Endpoint.trace('-->', 'Response (invalid request)');
      Server.handleHttpError(req, res, new Error.InvalidRequest(INVALID_REQUEST), self.opts.headers);
      return;
    }

    var reply = function reply(json) {
      var encoded;
      headers = {
        'Content-Type': 'application/json'
      };

      if (json) {
        encoded = JSON.stringify(json);
        headers['Content-Length'] = Buffer.byteLength(encoded, 'utf-8');
      } else {
        encoded = '';
        headers['Content-Length'] = 0;
      }

      headers = extend({}, headers, self.opts.headers);

      if (!conn.isStreaming) {
        res.writeHead(200, headers);
        res.write(encoded);
        res.end();
      } else {
        res.writeHead(200, headers);
        res.write(encoded);
        // Keep connection open
      }
    };

    var callback = function callback(err, result) {
      var response;
      if (err) {

        self.emit('error', err);

        Endpoint.trace('-->', 'Failure (id ' + decoded.id + '): ' +
          (err.stack ? err.stack : err.toString()));

        result = null;

        if (!(err instanceof Error.AbstractError)) {
          err = new Error.InternalError(err.toString());
        }

        response = {
          'jsonrpc': '2.0',
          'error': {code: err.code, message: err.message }
        };

      } else {
        Endpoint.trace('-->', 'Response (id ' + decoded.id + '): ' +
          JSON.stringify(result));

        response = {
          'jsonrpc': '2.0',
          'result': typeof(result) === 'undefined' ? null : result
        };
      }

      // Don't return a message if it doesn't have an ID
      if (Endpoint.hasId(decoded)) {
        response.id = decoded.id;
        reply(response);
      } else {
        reply();
      }
    };

    var conn = new classes.HttpServerConnection(self, req, res);

    self.handleCall(decoded, conn, callback);
  }; // function handle(buf)

  req.on('data', function requestData(chunk) {
    buffer = buffer + chunk;
  });

  req.on('end', function requestEnd() {
    handle(buffer);
  });
}
```
- example usage
```shell
...
       */
      listen: function (port, host) {
var
  self = this,
  server = http.createServer();

server.on('request', function onRequest(req, res) {
  self.handleHttp(req, res);
});

if (port) {
  server.listen(port, host);
  Endpoint.trace('***', 'Server listening on http://' +
    (host || '127.0.0.1') + ':' + port + '/');
}
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.handleHybrid"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleHybrid (httpServer, socket)](#apidoc.element.json-rpc2.Server.prototype.handleHybrid)
- description and source-code
```javascript
handleHybrid = function (httpServer, socket) {
  var self = this;

  socket.once('data', function (chunk) {
    // If first byte is a capital letter, treat connection as HTTP
    if (chunk[0] >= 65 && chunk[0] <= 90) {
      // TODO: need to find a better way to do this
      http._connectionListener.call(httpServer, socket);
      socket.ondata(chunk, 0, chunk.length);
    } else {
      self.handleRaw(socket);
      // Re-emit first chunk
      socket.emit('data', chunk);
    }
  });
}
```
- example usage
```shell
...
      },

      listenHybrid: function (port, host) {
var
  self = this,
  httpServer = self.listen(),
  server = net.createServer(function createServer(socket) {
    self.handleHybrid(httpServer, socket);
  });

server.listen(port, host);

Endpoint.trace('***', 'Server (hybrid) listening on http+tcp://' +
  (host || '127.0.0.1') + ':' + port + '/');
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.handleRaw"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleRaw (socket)](#apidoc.element.json-rpc2.Server.prototype.handleRaw)
- description and source-code
```javascript
handleRaw = function (socket) {
  var self = this, conn, parser, requireAuth;

  Endpoint.trace('<--', 'Accepted socket connection');

  conn = new classes.SocketConnection(self, socket);
  parser = new JsonParser();
  requireAuth = !!this.authHandler;

  parser.onValue = function (decoded) {
    if (this.stack.length) {
      return;
    }

    // We're on a raw TCP socket. To enable authentication we implement a simple
    // authentication scheme that is non-standard, but is easy to call from any
    // client library.
    //
    // The authentication message is to be sent as follows:
    //   {'method': 'auth', 'params': ['myuser', 'mypass'], id: 0}
    if (requireAuth) {
      if (decoded.method !== 'auth') {
        // Try to notify client about failure to authenticate
        if (Endpoint.hasId(decoded)) {
          conn.sendReply('Error: Unauthorized', null, decoded.id);
        }
      } else {
        // Handle 'auth' message
        if (_.isArray(decoded.params) &&
          decoded.params.length === 2 &&
          self.authHandler(decoded.params[0], decoded.params[1])) {
          // Authorization completed
          requireAuth = false;

          // Notify client about success
          if (Endpoint.hasId(decoded)) {
            conn.sendReply(null, true, decoded.id);
          }
        } else {
          if (Endpoint.hasId(decoded)) {
            conn.sendReply('Error: Invalid credentials', null, decoded.id);
          }
        }
      }
      // Make sure we explicitly return here - the client was not yet auth'd.
      return;
    } else {
      conn.handleMessage(decoded);
    }
  };

  socket.on('data', function (chunk) {
    try {
      parser.write(chunk);
    } catch (err) {
      // TODO: Is ignoring invalid data the right thing to do?
    }
  });
}
```
- example usage
```shell
...
return server;
      },

      listenRaw: function (port, host) {
var
  self = this,
  server = net.createServer(function createServer(socket) {
    self.handleRaw(socket);
  });

server.listen(port, host);

Endpoint.trace('***', 'Server listening on tcp://' +
  (host || '127.0.0.1') + ':' + port + '/');
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.handleWebsocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>handleWebsocket (request, socket, body)](#apidoc.element.json-rpc2.Server.prototype.handleWebsocket)
- description and source-code
```javascript
handleWebsocket = function (request, socket, body) {
  var self = this, conn, parser;

  socket = new WebSocket(request, socket, body);

  Endpoint.trace('<--', 'Accepted Websocket connection');

  conn = new classes.WebSocketConnection(self, socket);
  parser = new JsonParser();

  parser.onValue = function (decoded) {
    if (this.stack.length) {
      return;
    }

    conn.handleMessage(decoded);
  };

  socket.on('message', function (event) {
    try {
      parser.write(event.data);
    } catch (err) {
      // TODO: Is ignoring invalid data the right thing to do?
    }
  });
}
```
- example usage
```shell
...
      (host || '127.0.0.1') + ':' + port + '/');
  }

  if (this.opts.websocket === true) {
    server.on('upgrade', function onUpgrade(req, socket, body) {
      if (WebSocket.isWebSocket(req)) {
        if (self._checkAuth(req, socket)) {
          self.handleWebsocket(req, socket, body);
        }
      }
    });
  }

  return server;
},
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.listen"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>listen (port, host)](#apidoc.element.json-rpc2.Server.prototype.listen)
- description and source-code
```javascript
listen = function (port, host) {
  var
    self = this,
    server = http.createServer();

  server.on('request', function onRequest(req, res) {
    self.handleHttp(req, res);
  });

  if (port) {
    server.listen(port, host);
    Endpoint.trace('***', 'Server listening on http://' +
      (host || '127.0.0.1') + ':' + port + '/');
  }

  if (this.opts.websocket === true) {
    server.on('upgrade', function onUpgrade(req, socket, body) {
      if (WebSocket.isWebSocket(req)) {
        if (self._checkAuth(req, socket)) {
          self.handleWebsocket(req, socket, body);
        }
      }
    });
  }

  return server;
}
```
- example usage
```shell
...
    'function1': function(){},
    'function2': function(){},
    'function3': function(){}
});
// expects calls to be namespace.function1, namespace.function2 and namespace.function3

// listen creates an HTTP server on localhost only
server.listen(8000, 'localhost');
'''

And creating a client to speak to that server is easy too:

'''js
var rpc = require('json-rpc2');
...
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.listenHybrid"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>listenHybrid (port, host)](#apidoc.element.json-rpc2.Server.prototype.listenHybrid)
- description and source-code
```javascript
listenHybrid = function (port, host) {
  var
    self = this,
    httpServer = self.listen(),
    server = net.createServer(function createServer(socket) {
      self.handleHybrid(httpServer, socket);
    });

  server.listen(port, host);

  Endpoint.trace('***', 'Server (hybrid) listening on http+tcp://' +
    (host || '127.0.0.1') + ':' + port + '/');

  return server;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Server.prototype.listenRaw"></a>[function <span class="apidocSignatureSpan">json-rpc2.Server.prototype.</span>listenRaw (port, host)](#apidoc.element.json-rpc2.Server.prototype.listenRaw)
- description and source-code
```javascript
listenRaw = function (port, host) {
  var
    self = this,
    server = net.createServer(function createServer(socket) {
      self.handleRaw(socket);
    });

  server.listen(port, host);

  Endpoint.trace('***', 'Server listening on tcp://' +
    (host || '127.0.0.1') + ':' + port + '/');

  return server;
}
```
- example usage
```shell
...

var server = rpc.Server.$create();

// non-standard auth for RPC, when using this module using both client and server, works out-of-the-box
server.enableAuth('user', 'pass');

// Listen on socket
server.listenRaw(8080, 'localhost');
'''

## Extend, overwrite, overload

Any class can be extended, or used as a mixin for new classes, since it uses [ES5Class](http://github.com/pocesar/ES5-Class) module
.

For example, you may extend the 'Endpoint' class, that automatically extends 'Client' and 'Server' classes.
...
```



# <a name="apidoc.module.json-rpc2.SocketConnection"></a>[module json-rpc2.SocketConnection](#apidoc.module.json-rpc2.SocketConnection)

#### <a name="apidoc.element.json-rpc2.SocketConnection.SocketConnection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>SocketConnection ()](#apidoc.element.json-rpc2.SocketConnection.SocketConnection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      },

      handleRaw: function (socket) {
var self = this, conn, parser, requireAuth;

Endpoint.trace('<--', 'Accepted socket connection');

conn = new classes.SocketConnection(self, socket);
parser = new JsonParser();
requireAuth = !!this.authHandler;

parser.onValue = function (decoded) {
  if (this.stack.length) {
    return;
  }
...
```



# <a name="apidoc.module.json-rpc2.SocketConnection.prototype"></a>[module json-rpc2.SocketConnection.prototype](#apidoc.module.json-rpc2.SocketConnection.prototype)

#### <a name="apidoc.element.json-rpc2.SocketConnection.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>construct ()](#apidoc.element.json-rpc2.SocketConnection.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.SocketConnection.prototype.end"></a>[function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>end ()](#apidoc.element.json-rpc2.SocketConnection.prototype.end)
- description and source-code
```javascript
end = function (){
  this.ended = true;
  this.conn.end();
}
```
- example usage
```shell
...
connection.expose = function connectionExpose(method, callback){
  connection.on('call:' + method, function connectionCall(data){
    callback.call(null, data.params || []);
  });
};

connection.end = function connectionEnd(){
  this.req.connection.end();
};

// We need to buffer the response chunks in a nonblocking way.
var parser = new JsonParser();
parser.onValue = function (decoded){
  if (this.stack.length) {
    return;
...
```

#### <a name="apidoc.element.json-rpc2.SocketConnection.prototype.reconnect"></a>[function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>reconnect ()](#apidoc.element.json-rpc2.SocketConnection.prototype.reconnect)
- description and source-code
```javascript
reconnect = function (){
  this.ended = false;
  if (this.endpoint.$className === 'Client') {
    this.conn.connect(this.endpoint.port, this.endpoint.host);
  } else {
    throw new Error('Cannot reconnect a connection from the server-side.');
  }
}
```
- example usage
```shell
...
    if (
      self.endpoint.$className === 'Client' &&
        self.autoReconnect && !self.ended
      ) {
      if (hadError) {
        // If there was an error, we'll wait a moment before retrying
        setTimeout(function reconnectTimeout(){
          self.reconnect();
        }, 200);
      } else {
        self.reconnect();
      }
    }
  });
},
...
```

#### <a name="apidoc.element.json-rpc2.SocketConnection.prototype.write"></a>[function <span class="apidocSignatureSpan">json-rpc2.SocketConnection.prototype.</span>write (data)](#apidoc.element.json-rpc2.SocketConnection.prototype.write)
- description and source-code
```javascript
write = function (data){
  if (!this.conn.writable) {
    // Other side disconnected, we'll quietly fail
    return;
  }

  this.conn.write(data);
}
```
- example usage
```shell
...


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
connectWebsocket: function(callback){
  var self = this, conn, socket, parser, headers = {};
...
```



# <a name="apidoc.module.json-rpc2.WebSocketConnection"></a>[module json-rpc2.WebSocketConnection](#apidoc.module.json-rpc2.WebSocketConnection)

#### <a name="apidoc.element.json-rpc2.WebSocketConnection.WebSocketConnection"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>WebSocketConnection ()](#apidoc.element.json-rpc2.WebSocketConnection.WebSocketConnection)
- description and source-code
```javascript
function Constructor(){
  var args = BetterCurry.flatten(arguments);

  if (!(this instanceof Constructor)) {
    // auto instantiation
    return splat(Constructor, '$create', args);
  }

  if (superApply(this, Constructor, args)) {
    spo(this, Constructor.prototype); // always need to restore prototype after superApply
  }

  // old school new operator, call the constructor
  if (this.construct && this.construct !== noop) {
    splat(this, 'construct', args);
    copyArgs(this, args);
  }

  return this;
}
```
- example usage
```shell
...
      handleWebsocket: function (request, socket, body) {
var self = this, conn, parser;

socket = new WebSocket(request, socket, body);

Endpoint.trace('<--', 'Accepted Websocket connection');

conn = new classes.WebSocketConnection(self, socket);
parser = new JsonParser();

parser.onValue = function (decoded) {
  if (this.stack.length) {
    return;
  }
...
```



# <a name="apidoc.module.json-rpc2.WebSocketConnection.prototype"></a>[module json-rpc2.WebSocketConnection.prototype](#apidoc.module.json-rpc2.WebSocketConnection.prototype)

#### <a name="apidoc.element.json-rpc2.WebSocketConnection.prototype.construct"></a>[function <span class="apidocSignatureSpan">json-rpc2.WebSocketConnection.prototype.</span>construct ()](#apidoc.element.json-rpc2.WebSocketConnection.prototype.construct)
- description and source-code
```javascript
function wrapped(){
  var self = this;

  if (fn.$currentContext !== self) {
    fn = BetterCurry.wrap(superFn, self, fn.__length || obj[key].length, true);
    fn.$currentContext = self;
  }

  if (arguments.length) {
    return obj[key].apply(self, BetterCurry.flatten([fn], arguments));
  } else {
    return obj[key].call(self, fn);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.WebSocketConnection.prototype.end"></a>[function <span class="apidocSignatureSpan">json-rpc2.WebSocketConnection.prototype.</span>end ()](#apidoc.element.json-rpc2.WebSocketConnection.prototype.end)
- description and source-code
```javascript
end = function (){
  this.conn.close();
  this.ended = true;
}
```
- example usage
```shell
...
connection.expose = function connectionExpose(method, callback){
  connection.on('call:' + method, function connectionCall(data){
    callback.call(null, data.params || []);
  });
};

connection.end = function connectionEnd(){
  this.req.connection.end();
};

// We need to buffer the response chunks in a nonblocking way.
var parser = new JsonParser();
parser.onValue = function (decoded){
  if (this.stack.length) {
    return;
...
```

#### <a name="apidoc.element.json-rpc2.WebSocketConnection.prototype.write"></a>[function <span class="apidocSignatureSpan">json-rpc2.WebSocketConnection.prototype.</span>write (data)](#apidoc.element.json-rpc2.WebSocketConnection.prototype.write)
- description and source-code
```javascript
write = function (data){
  if (!this.conn.writable) {
    // Other side disconnected, we'll quietly fail
    return;
  }

  this.conn.write(data);
}
```
- example usage
```shell
...


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
connectWebsocket: function(callback){
  var self = this, conn, socket, parser, headers = {};
...
```



# <a name="apidoc.module.json-rpc2.Websocket"></a>[module json-rpc2.Websocket](#apidoc.module.json-rpc2.Websocket)

#### <a name="apidoc.element.json-rpc2.Websocket.Websocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>Websocket (request, socket, body, protocols, options)](#apidoc.element.json-rpc2.Websocket.Websocket)
- description and source-code
```javascript
Websocket = function (request, socket, body, protocols, options) {
  options = options || {};

  this._stream = socket;
  this._driver = driver.http(request, {maxLength: options.maxLength, protocols: protocols});

  var self = this;
  if (!this._stream || !this._stream.writable) return;
  if (!this._stream.readable) return this._stream.end();

  var catchup = function() { self._stream.removeListener('data', catchup) };
  this._stream.on('data', catchup);

  API.call(this, options);

  process.nextTick(function() {
    self._driver.start();
    self._driver.io.write(body);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.Client"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>Client (_url, protocols, options)](#apidoc.element.json-rpc2.Websocket.Client)
- description and source-code
```javascript
Client = function (_url, protocols, options) {
  options = options || {};

  this.url     = _url;
  this._driver = driver.client(this.url, {maxLength: options.maxLength, protocols: protocols});

  ['open', 'error'].forEach(function(event) {
    this._driver.on(event, function() {
      self.headers    = self._driver.headers;
      self.statusCode = self._driver.statusCode;
    });
  }, this);

  var proxy      = options.proxy || {},
      endpoint   = url.parse(proxy.origin || this.url),
      port       = endpoint.port || DEFAULT_PORTS[endpoint.protocol],
      secure     = SECURE_PROTOCOLS.indexOf(endpoint.protocol) >= 0,
      onConnect  = function() { self._onConnect() },
      netOptions = options.net || {},
      originTLS  = options.tls || {},
      socketTLS  = proxy.origin ? (proxy.tls || {}) : originTLS,
      self       = this;

  netOptions.host = socketTLS.host = endpoint.hostname;
  netOptions.port = socketTLS.port = port;

  originTLS.ca = originTLS.ca || options.ca;
  socketTLS.servername = socketTLS.servername || endpoint.hostname;

  this._stream = secure
               ? tls.connect(socketTLS, onConnect)
               : net.connect(netOptions, onConnect);

  if (proxy.origin) this._configureProxy(proxy, originTLS);

  API.call(this, options);
}
```
- example usage
```shell
...

if (!/^wss?:\/\//i.test(self.host)) {
  self.host = 'ws://' + self.host + ':' + self.port + '/';
}

this._authHeader(headers);

socket = new WebSocket.Client(self.host, null, {headers: headers});

conn = new WebSocketConnection(self, socket);

parser = new JsonParser();

parser.onValue = function parseOnValue(decoded){
  if (this.stack.length) {
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>EventSource (request, response, options)](#apidoc.element.json-rpc2.Websocket.EventSource)
- description and source-code
```javascript
EventSource = function (request, response, options) {
  this.writable = true;
  options = options || {};

  this._stream = response.socket;
  this._ping   = options.ping  || this.DEFAULT_PING;
  this._retry  = options.retry || this.DEFAULT_RETRY;

  var scheme       = driver.isSecureRequest(request) ? 'https:' : 'http:';
  this.url         = scheme + '//' + request.headers.host + request.url;
  this.lastEventId = request.headers['last-event-id'] || '';
  this.readyState  = API.CONNECTING;

  var headers = new Headers(),
      self    = this;

  if (options.headers) {
    for (var key in options.headers) headers.set(key, options.headers[key]);
  }

  if (!this._stream || !this._stream.writable) return;
  process.nextTick(function() { self._open() });

  this._stream.setTimeout(0);
  this._stream.setNoDelay(true);

  var handshake = 'HTTP/1.1 200 OK\r\n' +
                  'Content-Type: text/event-stream\r\n' +
                  'Cache-Control: no-cache, no-store\r\n' +
                  'Connection: close\r\n' +
                  headers.toString() +
                  '\r\n' +
                  'retry: ' + Math.floor(this._retry * 1000) + '\r\n\r\n';

  this._write(handshake);

  this._stream.on('drain', function() { self.emit('drain') });

  if (this._ping)
    this._pingTimer = setInterval(function() { self.ping() }, this._ping * 1000);

  ['error', 'end'].forEach(function(event) {
    self._stream.on(event, function() { self.close() });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.WebSocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>WebSocket (request, socket, body, protocols, options)](#apidoc.element.json-rpc2.Websocket.WebSocket)
- description and source-code
```javascript
WebSocket = function (request, socket, body, protocols, options) {
  options = options || {};

  this._stream = socket;
  this._driver = driver.http(request, {maxLength: options.maxLength, protocols: protocols});

  var self = this;
  if (!this._stream || !this._stream.writable) return;
  if (!this._stream.readable) return this._stream.end();

  var catchup = function() { self._stream.removeListener('data', catchup) };
  this._stream.on('data', catchup);

  API.call(this, options);

  process.nextTick(function() {
    self._driver.start();
    self._driver.io.write(body);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.isWebSocket"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>isWebSocket (request)](#apidoc.element.json-rpc2.Websocket.isWebSocket)
- description and source-code
```javascript
isWebSocket = function (request) {
  return driver.isWebSocket(request);
}
```
- example usage
```shell
...
  server.listen(port, host);
  Endpoint.trace('***', 'Server listening on http://' +
    (host || '127.0.0.1') + ':' + port + '/');
}

if (this.opts.websocket === true) {
  server.on('upgrade', function onUpgrade(req, socket, body) {
    if (WebSocket.isWebSocket(req)) {
      if (self._checkAuth(req, socket)) {
        self.handleWebsocket(req, socket, body);
      }
    }
  });
}
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>super_ (options)](#apidoc.element.json-rpc2.Websocket.super_)
- description and source-code
```javascript
super_ = function (options) {
  options = options || {};
  driver.validateOptions(options, ['headers', 'extensions', 'maxLength', 'ping', 'proxy', 'tls', 'ca']);

  this.readable = this.writable = true;

  var headers = options.headers;
  if (headers) {
    for (var name in headers) this._driver.setHeader(name, headers[name]);
  }

  var extensions = options.extensions;
  if (extensions) {
    [].concat(extensions).forEach(this._driver.addExtension, this._driver);
  }

  this._ping          = options.ping;
  this._pingId        = 0;
  this.readyState     = API.CONNECTING;
  this.bufferedAmount = 0;
  this.protocol       = '';
  this.url            = this._driver.url;
  this.version        = this._driver.version;

  var self = this;

  this._driver.on('open',    function(e) { self._open() });
  this._driver.on('message', function(e) { self._receiveMessage(e.data) });
  this._driver.on('close',   function(e) { self._beginClose(e.reason, e.code) });

  this._driver.on('error', function(error) {
    self._emitError(error.message);
  });
  this.on('error', function() {});

  this._driver.messages.on('drain', function() {
    self.emit('drain');
  });

  if (this._ping)
    this._pingTimer = setInterval(function() {
      self._pingId += 1;
      self.ping(self._pingId.toString());
    }, this._ping * 1000);

  this._configureStream();

  if (!this._proxy) {
    this._stream.pipe(this._driver.io);
    this._driver.io.pipe(this._stream);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.validateOptions"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>validateOptions (options, validKeys)](#apidoc.element.json-rpc2.Websocket.validateOptions)
- description and source-code
```javascript
validateOptions = function (options, validKeys) {
  driver.validateOptions(options, validKeys);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Websocket.Client"></a>[module json-rpc2.Websocket.Client](#apidoc.module.json-rpc2.Websocket.Client)

#### <a name="apidoc.element.json-rpc2.Websocket.Client.Client"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>Client (_url, protocols, options)](#apidoc.element.json-rpc2.Websocket.Client.Client)
- description and source-code
```javascript
Client = function (_url, protocols, options) {
  options = options || {};

  this.url     = _url;
  this._driver = driver.client(this.url, {maxLength: options.maxLength, protocols: protocols});

  ['open', 'error'].forEach(function(event) {
    this._driver.on(event, function() {
      self.headers    = self._driver.headers;
      self.statusCode = self._driver.statusCode;
    });
  }, this);

  var proxy      = options.proxy || {},
      endpoint   = url.parse(proxy.origin || this.url),
      port       = endpoint.port || DEFAULT_PORTS[endpoint.protocol],
      secure     = SECURE_PROTOCOLS.indexOf(endpoint.protocol) >= 0,
      onConnect  = function() { self._onConnect() },
      netOptions = options.net || {},
      originTLS  = options.tls || {},
      socketTLS  = proxy.origin ? (proxy.tls || {}) : originTLS,
      self       = this;

  netOptions.host = socketTLS.host = endpoint.hostname;
  netOptions.port = socketTLS.port = port;

  originTLS.ca = originTLS.ca || options.ca;
  socketTLS.servername = socketTLS.servername || endpoint.hostname;

  this._stream = secure
               ? tls.connect(socketTLS, onConnect)
               : net.connect(netOptions, onConnect);

  if (proxy.origin) this._configureProxy(proxy, originTLS);

  API.call(this, options);
}
```
- example usage
```shell
...

if (!/^wss?:\/\//i.test(self.host)) {
  self.host = 'ws://' + self.host + ':' + self.port + '/';
}

this._authHeader(headers);

socket = new WebSocket.Client(self.host, null, {headers: headers});

conn = new WebSocketConnection(self, socket);

parser = new JsonParser();

parser.onValue = function parseOnValue(decoded){
  if (this.stack.length) {
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.Client.super_"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.Client.</span>super_ (options)](#apidoc.element.json-rpc2.Websocket.Client.super_)
- description and source-code
```javascript
super_ = function (options) {
  options = options || {};
  driver.validateOptions(options, ['headers', 'extensions', 'maxLength', 'ping', 'proxy', 'tls', 'ca']);

  this.readable = this.writable = true;

  var headers = options.headers;
  if (headers) {
    for (var name in headers) this._driver.setHeader(name, headers[name]);
  }

  var extensions = options.extensions;
  if (extensions) {
    [].concat(extensions).forEach(this._driver.addExtension, this._driver);
  }

  this._ping          = options.ping;
  this._pingId        = 0;
  this.readyState     = API.CONNECTING;
  this.bufferedAmount = 0;
  this.protocol       = '';
  this.url            = this._driver.url;
  this.version        = this._driver.version;

  var self = this;

  this._driver.on('open',    function(e) { self._open() });
  this._driver.on('message', function(e) { self._receiveMessage(e.data) });
  this._driver.on('close',   function(e) { self._beginClose(e.reason, e.code) });

  this._driver.on('error', function(error) {
    self._emitError(error.message);
  });
  this.on('error', function() {});

  this._driver.messages.on('drain', function() {
    self.emit('drain');
  });

  if (this._ping)
    this._pingTimer = setInterval(function() {
      self._pingId += 1;
      self.ping(self._pingId.toString());
    }, this._ping * 1000);

  this._configureStream();

  if (!this._proxy) {
    this._stream.pipe(this._driver.io);
    this._driver.io.pipe(this._stream);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Websocket.Client.prototype"></a>[module json-rpc2.Websocket.Client.prototype](#apidoc.module.json-rpc2.Websocket.Client.prototype)

#### <a name="apidoc.element.json-rpc2.Websocket.Client.prototype._configureProxy"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.Client.prototype.</span>_configureProxy (proxy, originTLS)](#apidoc.element.json-rpc2.Websocket.Client.prototype._configureProxy)
- description and source-code
```javascript
_configureProxy = function (proxy, originTLS) {
  var uri    = url.parse(this.url),
      secure = SECURE_PROTOCOLS.indexOf(uri.protocol) >= 0,
      self   = this,
      name;

  this._proxy = this._driver.proxy(proxy.origin);

  if (proxy.headers) {
    for (name in proxy.headers) this._proxy.setHeader(name, proxy.headers[name]);
  }

  this._proxy.pipe(this._stream, {end: false});
  this._stream.pipe(this._proxy);

  this._proxy.on('connect', function() {
    if (secure) {
      var options = {socket: self._stream, servername: uri.hostname};
      for (name in originTLS) options[name] = originTLS[name];
      self._stream = tls.connect(options);
      self._configureStream();
    }
    self._driver.io.pipe(self._stream);
    self._stream.pipe(self._driver.io);
    self._driver.start();
  });

  this._proxy.on('error', function(error) {
    self._driver.emit('error', error);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.Client.prototype._onConnect"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.Client.prototype.</span>_onConnect ()](#apidoc.element.json-rpc2.Websocket.Client.prototype._onConnect)
- description and source-code
```javascript
_onConnect = function () {
  var worker = this._proxy || this._driver;
  worker.start();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Websocket.EventSource"></a>[module json-rpc2.Websocket.EventSource](#apidoc.module.json-rpc2.Websocket.EventSource)

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.EventSource"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>EventSource (request, response, options)](#apidoc.element.json-rpc2.Websocket.EventSource.EventSource)
- description and source-code
```javascript
EventSource = function (request, response, options) {
  this.writable = true;
  options = options || {};

  this._stream = response.socket;
  this._ping   = options.ping  || this.DEFAULT_PING;
  this._retry  = options.retry || this.DEFAULT_RETRY;

  var scheme       = driver.isSecureRequest(request) ? 'https:' : 'http:';
  this.url         = scheme + '//' + request.headers.host + request.url;
  this.lastEventId = request.headers['last-event-id'] || '';
  this.readyState  = API.CONNECTING;

  var headers = new Headers(),
      self    = this;

  if (options.headers) {
    for (var key in options.headers) headers.set(key, options.headers[key]);
  }

  if (!this._stream || !this._stream.writable) return;
  process.nextTick(function() { self._open() });

  this._stream.setTimeout(0);
  this._stream.setNoDelay(true);

  var handshake = 'HTTP/1.1 200 OK\r\n' +
                  'Content-Type: text/event-stream\r\n' +
                  'Cache-Control: no-cache, no-store\r\n' +
                  'Connection: close\r\n' +
                  headers.toString() +
                  '\r\n' +
                  'retry: ' + Math.floor(this._retry * 1000) + '\r\n\r\n';

  this._write(handshake);

  this._stream.on('drain', function() { self.emit('drain') });

  if (this._ping)
    this._pingTimer = setInterval(function() { self.ping() }, this._ping * 1000);

  ['error', 'end'].forEach(function(event) {
    self._stream.on(event, function() { self.close() });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.isEventSource"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.</span>isEventSource (request)](#apidoc.element.json-rpc2.Websocket.EventSource.isEventSource)
- description and source-code
```javascript
isEventSource = function (request) {
  if (request.method !== 'GET') return false;
  var accept = (request.headers.accept || '').split(/\s*,\s*/);
  return accept.indexOf('text/event-stream') >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.super_"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.</span>super_ ()](#apidoc.element.json-rpc2.Websocket.EventSource.super_)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Websocket.EventSource.prototype"></a>[module json-rpc2.Websocket.EventSource.prototype](#apidoc.module.json-rpc2.Websocket.EventSource.prototype)

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype._open"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>_open ()](#apidoc.element.json-rpc2.Websocket.EventSource.prototype._open)
- description and source-code
```javascript
_open = function () {
  if (this.readyState !== API.CONNECTING) return;

  this.readyState = API.OPEN;

  var event = new Event('open');
  event.initEvent('open', false, false);
  this.dispatchEvent(event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype._write"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>_write (chunk)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype._write)
- description and source-code
```javascript
_write = function (chunk) {
  if (!this.writable) return false;
  try {
    return this._stream.write(chunk, 'utf8');
  } catch (e) {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.addEventListener"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>addEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.addEventListener)
- description and source-code
```javascript
addEventListener = function (eventType, listener, useCapture) {
  this.on(eventType, listener);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.close"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>close ()](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.close)
- description and source-code
```javascript
close = function () {
  if (this.readyState > API.OPEN) return false;

  this.readyState = API.CLOSED;
  this.writable = false;
  if (this._pingTimer) clearInterval(this._pingTimer);
  if (this._stream) this._stream.end();

  var event = new Event('close');
  event.initEvent('close', false, false);
  this.dispatchEvent(event);

  return true;
}
```
- example usage
```shell
...
          // Other side disconnected, we'll quietly fail
          return;
        }

        this.conn.write(data);
      },
      end: function(){
        this.conn.close();
        this.ended = true;
      }
    });

  return WebSocketConnection;
};
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.dispatchEvent"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>dispatchEvent (event)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.dispatchEvent)
- description and source-code
```javascript
dispatchEvent = function (event) {
  event.target = event.currentTarget = this;
  event.eventPhase = Event.AT_TARGET;

  if (this['on' + event.type])
    this['on' + event.type](event);

  this.emit(event.type, event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.end"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>end (message)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.end)
- description and source-code
```javascript
end = function (message) {
  if (message !== undefined) this.write(message);
  this.close();
}
```
- example usage
```shell
...
connection.expose = function connectionExpose(method, callback){
  connection.on('call:' + method, function connectionCall(data){
    callback.call(null, data.params || []);
  });
};

connection.end = function connectionEnd(){
  this.req.connection.end();
};

// We need to buffer the response chunks in a nonblocking way.
var parser = new JsonParser();
parser.onValue = function (decoded){
  if (this.stack.length) {
    return;
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.ping"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>ping ()](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.ping)
- description and source-code
```javascript
ping = function () {
  return this._write(':\r\n\r\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.removeEventListener"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>removeEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.removeEventListener)
- description and source-code
```javascript
removeEventListener = function (eventType, listener, useCapture) {
  this.removeListener(eventType, listener);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.send"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>send (message, options)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.send)
- description and source-code
```javascript
send = function (message, options) {
  if (this.readyState > API.OPEN) return false;

  message = String(message).replace(/(\r\n|\r|\n)/g, '$1data: ');
  options = options || {};

  var frame = '';
  if (options.event) frame += 'event: ' + options.event + '\r\n';
  if (options.id)    frame += 'id: '    + options.id    + '\r\n';
  frame += 'data: ' + message + '\r\n\r\n';

  return this._write(frame);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.EventSource.prototype.write"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.EventSource.prototype.</span>write (message)](#apidoc.element.json-rpc2.Websocket.EventSource.prototype.write)
- description and source-code
```javascript
write = function (message) {
  return this.send(message);
}
```
- example usage
```shell
...


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
connectWebsocket: function(callback){
  var self = this, conn, socket, parser, headers = {};
...
```



# <a name="apidoc.module.json-rpc2.Websocket.super_"></a>[module json-rpc2.Websocket.super_](#apidoc.module.json-rpc2.Websocket.super_)

#### <a name="apidoc.element.json-rpc2.Websocket.super_.super_"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.</span>super_ ()](#apidoc.element.json-rpc2.Websocket.super_.super_)
- description and source-code
```javascript
function Stream() {
  EE.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2.Websocket.super_.prototype"></a>[module json-rpc2.Websocket.super_.prototype](#apidoc.module.json-rpc2.Websocket.super_.prototype)

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype._beginClose"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_beginClose (reason, code)](#apidoc.element.json-rpc2.Websocket.super_.prototype._beginClose)
- description and source-code
```javascript
_beginClose = function (reason, code) {
  if (this.readyState === API.CLOSED) return;
  this.readyState = API.CLOSING;
  this._closeParams = [reason, code];

  if (this._stream) {
    this._stream.destroy();
    if (!this._stream.readable) this._finalizeClose();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype._configureStream"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_configureStream ()](#apidoc.element.json-rpc2.Websocket.super_.prototype._configureStream)
- description and source-code
```javascript
_configureStream = function () {
  var self = this;

  this._stream.setTimeout(0);
  this._stream.setNoDelay(true);

  ['close', 'end'].forEach(function(event) {
    this._stream.on(event, function() { self._finalizeClose() });
  }, this);

  this._stream.on('error', function(error) {
    self._emitError('Network error: ' + self.url + ': ' + error.message);
    self._finalizeClose();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype._emitError"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_emitError (message)](#apidoc.element.json-rpc2.Websocket.super_.prototype._emitError)
- description and source-code
```javascript
_emitError = function (message) {
  if (this.readyState >= API.CLOSING) return;

  var event = new Event('error', {message: message});
  event.initEvent('error', false, false);
  this.dispatchEvent(event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype._finalizeClose"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_finalizeClose ()](#apidoc.element.json-rpc2.Websocket.super_.prototype._finalizeClose)
- description and source-code
```javascript
_finalizeClose = function () {
  if (this.readyState === API.CLOSED) return;
  this.readyState = API.CLOSED;

  if (this._closeTimer) clearTimeout(this._closeTimer);
  if (this._pingTimer) clearInterval(this._pingTimer);
  if (this._stream) this._stream.end();

  if (this.readable) this.emit('end');
  this.readable = this.writable = false;

  var reason = this._closeParams ? this._closeParams[0] : '',
      code   = this._closeParams ? this._closeParams[1] : 1006;

  var event = new Event('close', {code: code, reason: reason});
  event.initEvent('close', false, false);
  this.dispatchEvent(event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype._open"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_open ()](#apidoc.element.json-rpc2.Websocket.super_.prototype._open)
- description and source-code
```javascript
_open = function () {
  if (this.readyState !== API.CONNECTING) return;

  this.readyState = API.OPEN;
  this.protocol = this._driver.protocol || '';

  var event = new Event('open');
  event.initEvent('open', false, false);
  this.dispatchEvent(event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype._receiveMessage"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>_receiveMessage (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype._receiveMessage)
- description and source-code
```javascript
_receiveMessage = function (data) {
  if (this.readyState > API.OPEN) return false;

  if (this.readable) this.emit('data', data);

  var event = new Event('message', {data: data});
  event.initEvent('message', false, false);
  this.dispatchEvent(event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.addEventListener"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>addEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.super_.prototype.addEventListener)
- description and source-code
```javascript
addEventListener = function (eventType, listener, useCapture) {
  this.on(eventType, listener);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.close"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>close (code, reason)](#apidoc.element.json-rpc2.Websocket.super_.prototype.close)
- description and source-code
```javascript
close = function (code, reason) {
  if (code === undefined) code = 1000;
  if (reason === undefined) reason = '';

  if (code !== 1000 && (code < 3000 || code > 4999))
    throw new Error("Failed to execute 'close' on WebSocket: " +
                    "The code must be either 1000, or between 3000 and 4999. " +
                    code + " is neither.");

  if (this.readyState !== API.CLOSED) this.readyState = API.CLOSING;
  this._driver.close(reason, code);

  var self = this;

  this._closeTimer = setTimeout(function() {
    self._beginClose('', 1006);
  }, API.CLOSE_TIMEOUT);
}
```
- example usage
```shell
...
          // Other side disconnected, we'll quietly fail
          return;
        }

        this.conn.write(data);
      },
      end: function(){
        this.conn.close();
        this.ended = true;
      }
    });

  return WebSocketConnection;
};
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.dispatchEvent"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>dispatchEvent (event)](#apidoc.element.json-rpc2.Websocket.super_.prototype.dispatchEvent)
- description and source-code
```javascript
dispatchEvent = function (event) {
  event.target = event.currentTarget = this;
  event.eventPhase = Event.AT_TARGET;

  if (this['on' + event.type])
    this['on' + event.type](event);

  this.emit(event.type, event);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.end"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>end (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype.end)
- description and source-code
```javascript
end = function (data) {
  if (data !== undefined) this.send(data);
  this.close();
}
```
- example usage
```shell
...
connection.expose = function connectionExpose(method, callback){
  connection.on('call:' + method, function connectionCall(data){
    callback.call(null, data.params || []);
  });
};

connection.end = function connectionEnd(){
  this.req.connection.end();
};

// We need to buffer the response chunks in a nonblocking way.
var parser = new JsonParser();
parser.onValue = function (decoded){
  if (this.stack.length) {
    return;
...
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.pause"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>pause ()](#apidoc.element.json-rpc2.Websocket.super_.prototype.pause)
- description and source-code
```javascript
pause = function () {
  return this._driver.messages.pause();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.ping"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>ping (message, callback)](#apidoc.element.json-rpc2.Websocket.super_.prototype.ping)
- description and source-code
```javascript
ping = function (message, callback) {
  if (this.readyState > API.OPEN) return false;
  return this._driver.ping(message, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.removeEventListener"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>removeEventListener (eventType, listener, useCapture)](#apidoc.element.json-rpc2.Websocket.super_.prototype.removeEventListener)
- description and source-code
```javascript
removeEventListener = function (eventType, listener, useCapture) {
  this.removeListener(eventType, listener);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.resume"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>resume ()](#apidoc.element.json-rpc2.Websocket.super_.prototype.resume)
- description and source-code
```javascript
resume = function () {
  return this._driver.messages.resume();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.send"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>send (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype.send)
- description and source-code
```javascript
send = function (data) {
  if (this.readyState > API.OPEN) return false;
  if (!(data instanceof Buffer)) data = String(data);
  return this._driver.messages.write(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2.Websocket.super_.prototype.write"></a>[function <span class="apidocSignatureSpan">json-rpc2.Websocket.super_.prototype.</span>write (data)](#apidoc.element.json-rpc2.Websocket.super_.prototype.write)
- description and source-code
```javascript
write = function (data) {
  return this.send(data);
}
```
- example usage
```shell
...


  // Report errors from the http client. This also prevents crashes since
  // an exception is thrown if we don't handle this event.
  request.on('error', function requestError(err){
    callback(err);
  });
  request.write(requestJSON);
  request.on('response', function requestResponse(response){
    callback.call(self, id, request, response);
  });
},
connectWebsocket: function(callback){
  var self = this, conn, socket, parser, headers = {};
...
```



# <a name="apidoc.module.json-rpc2._"></a>[module json-rpc2._](#apidoc.module.json-rpc2._)

#### <a name="apidoc.element.json-rpc2._._"></a>[function <span class="apidocSignatureSpan">json-rpc2.</span>_ (value)](#apidoc.element.json-rpc2._._)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.add"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>add (augend, addend)](#apidoc.element.json-rpc2._.add)
- description and source-code
```javascript
function add(augend, addend) {
  return (+augend || 0) + (+addend || 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.after"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>after (n, func)](#apidoc.element.json-rpc2._.after)
- description and source-code
```javascript
function after(n, func) {
  if (typeof func != 'function') {
    if (typeof n == 'function') {
      var temp = n;
      n = func;
      func = temp;
    } else {
      throw new TypeError(FUNC_ERROR_TEXT);
    }
  }
  n = nativeIsFinite(n = +n) ? n : 0;
  return function() {
    if (--n < 1) {
      return func.apply(this, arguments);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.all"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>all (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.all)
- description and source-code
```javascript
function every(collection, predicate, thisArg) {
  var func = isArray(collection) ? arrayEvery : baseEvery;
  if (thisArg && isIterateeCall(collection, predicate, thisArg)) {
    predicate = undefined;
  }
  if (typeof predicate != 'function' || thisArg !== undefined) {
    predicate = getCallback(predicate, thisArg, 3);
  }
  return func(collection, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.any"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>any (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.any)
- description and source-code
```javascript
function some(collection, predicate, thisArg) {
  var func = isArray(collection) ? arraySome : baseSome;
  if (thisArg && isIterateeCall(collection, predicate, thisArg)) {
    predicate = undefined;
  }
  if (typeof predicate != 'function' || thisArg !== undefined) {
    predicate = getCallback(predicate, thisArg, 3);
  }
  return func(collection, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.ary"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>ary (func, n, guard)](#apidoc.element.json-rpc2._.ary)
- description and source-code
```javascript
function ary(func, n, guard) {
  if (guard && isIterateeCall(func, n, guard)) {
    n = undefined;
  }
  n = (func && n == null) ? func.length : nativeMax(+n || 0, 0);
  return createWrapper(func, ARY_FLAG, undefined, undefined, undefined, undefined, n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.assign"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>assign ()](#apidoc.element.json-rpc2._.assign)
- description and source-code
```javascript
assign = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.at"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>at ()](#apidoc.element.json-rpc2._.at)
- description and source-code
```javascript
at = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.attempt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>attempt ()](#apidoc.element.json-rpc2._.attempt)
- description and source-code
```javascript
attempt = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.backflow"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>backflow ()](#apidoc.element.json-rpc2._.backflow)
- description and source-code
```javascript
backflow = function () {
  var wrapper,
      length = arguments.length,
      index = fromRight ? length : -1,
      leftIndex = 0,
      funcs = Array(length);

  while ((fromRight ? index-- : ++index < length)) {
    var func = funcs[leftIndex++] = arguments[index];
    if (typeof func != 'function') {
      throw new TypeError(FUNC_ERROR_TEXT);
    }
    if (!wrapper && LodashWrapper.prototype.thru && getFuncName(func) == 'wrapper') {
      wrapper = new LodashWrapper([], true);
    }
  }
  index = wrapper ? -1 : length;
  while (++index < length) {
    func = funcs[index];

    var funcName = getFuncName(func),
        data = funcName == 'wrapper' ? getData(func) : undefined;

    if (data && isLaziable(data[0]) && data[1] == (ARY_FLAG | CURRY_FLAG | PARTIAL_FLAG | REARG_FLAG) && !data[4].length && data
[9] == 1) {
      wrapper = wrapper[getFuncName(data[0])].apply(wrapper, data[3]);
    } else {
      wrapper = (func.length == 1 && isLaziable(func)) ? wrapper[funcName]() : wrapper.thru(func);
    }
  }
  return function() {
    var args = arguments,
        value = args[0];

    if (wrapper && args.length == 1 && isArray(value) && value.length >= LARGE_ARRAY_SIZE) {
      return wrapper.plant(value).value();
    }
    var index = 0,
        result = length ? funcs[index].apply(this, args) : value;

    while (++index < length) {
      result = funcs[index].call(this, result);
    }
    return result;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.before"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>before (n, func)](#apidoc.element.json-rpc2._.before)
- description and source-code
```javascript
function before(n, func) {
  var result;
  if (typeof func != 'function') {
    if (typeof n == 'function') {
      var temp = n;
      n = func;
      func = temp;
    } else {
      throw new TypeError(FUNC_ERROR_TEXT);
    }
  }
  return function() {
    if (--n > 0) {
      result = func.apply(this, arguments);
    }
    if (n <= 1) {
      func = undefined;
    }
    return result;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bind"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>bind ()](#apidoc.element.json-rpc2._.bind)
- description and source-code
```javascript
bind = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bindAll"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>bindAll ()](#apidoc.element.json-rpc2._.bindAll)
- description and source-code
```javascript
bindAll = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bindKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>bindKey ()](#apidoc.element.json-rpc2._.bindKey)
- description and source-code
```javascript
bindKey = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.callback"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>callback (func, thisArg, guard)](#apidoc.element.json-rpc2._.callback)
- description and source-code
```javascript
function callback(func, thisArg, guard) {
  if (guard && isIterateeCall(func, thisArg, guard)) {
    thisArg = undefined;
  }
  return isObjectLike(func)
    ? matches(func)
    : baseCallback(func, thisArg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.camelCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>camelCase (string)](#apidoc.element.json-rpc2._.camelCase)
- description and source-code
```javascript
camelCase = function (string) {
  var index = -1,
      array = words(deburr(string)),
      length = array.length,
      result = '';

  while (++index < length) {
    result = callback(result, array[index], index);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.capitalize"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>capitalize (string)](#apidoc.element.json-rpc2._.capitalize)
- description and source-code
```javascript
function capitalize(string) {
  string = baseToString(string);
  return string && (string.charAt(0).toUpperCase() + string.slice(1));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.ceil"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>ceil (number, precision)](#apidoc.element.json-rpc2._.ceil)
- description and source-code
```javascript
ceil = function (number, precision) {
  precision = precision === undefined ? 0 : (+precision || 0);
  if (precision) {
    precision = pow(10, precision);
    return func(number * precision) / precision;
  }
  return func(number);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.chain"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>chain (value)](#apidoc.element.json-rpc2._.chain)
- description and source-code
```javascript
function chain(value) {
  var result = lodash(value);
  result.__chain__ = true;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.chunk"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>chunk (array, size, guard)](#apidoc.element.json-rpc2._.chunk)
- description and source-code
```javascript
function chunk(array, size, guard) {
  if (guard ? isIterateeCall(array, size, guard) : size == null) {
    size = 1;
  } else {
    size = nativeMax(nativeFloor(size) || 1, 1);
  }
  var index = 0,
      length = array ? array.length : 0,
      resIndex = -1,
      result = Array(nativeCeil(length / size));

  while (index < length) {
    result[++resIndex] = baseSlice(array, index, (index += size));
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.clone"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>clone (value, isDeep, customizer, thisArg)](#apidoc.element.json-rpc2._.clone)
- description and source-code
```javascript
function clone(value, isDeep, customizer, thisArg) {
  if (isDeep && typeof isDeep != 'boolean' && isIterateeCall(value, isDeep, customizer)) {
    isDeep = false;
  }
  else if (typeof isDeep == 'function') {
    thisArg = customizer;
    customizer = isDeep;
    isDeep = false;
  }
  return typeof customizer == 'function'
    ? baseClone(value, isDeep, bindCallback(customizer, thisArg, 1))
    : baseClone(value, isDeep);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.cloneDeep"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>cloneDeep (value, customizer, thisArg)](#apidoc.element.json-rpc2._.cloneDeep)
- description and source-code
```javascript
function cloneDeep(value, customizer, thisArg) {
  return typeof customizer == 'function'
    ? baseClone(value, true, bindCallback(customizer, thisArg, 1))
    : baseClone(value, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.collect"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>collect (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.collect)
- description and source-code
```javascript
function map(collection, iteratee, thisArg) {
  var func = isArray(collection) ? arrayMap : baseMap;
  iteratee = getCallback(iteratee, thisArg, 3);
  return func(collection, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.compact"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>compact (array)](#apidoc.element.json-rpc2._.compact)
- description and source-code
```javascript
function compact(array) {
  var index = -1,
      length = array ? array.length : 0,
      resIndex = -1,
      result = [];

  while (++index < length) {
    var value = array[index];
    if (value) {
      result[++resIndex] = value;
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.compose"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>compose ()](#apidoc.element.json-rpc2._.compose)
- description and source-code
```javascript
compose = function () {
  var wrapper,
      length = arguments.length,
      index = fromRight ? length : -1,
      leftIndex = 0,
      funcs = Array(length);

  while ((fromRight ? index-- : ++index < length)) {
    var func = funcs[leftIndex++] = arguments[index];
    if (typeof func != 'function') {
      throw new TypeError(FUNC_ERROR_TEXT);
    }
    if (!wrapper && LodashWrapper.prototype.thru && getFuncName(func) == 'wrapper') {
      wrapper = new LodashWrapper([], true);
    }
  }
  index = wrapper ? -1 : length;
  while (++index < length) {
    func = funcs[index];

    var funcName = getFuncName(func),
        data = funcName == 'wrapper' ? getData(func) : undefined;

    if (data && isLaziable(data[0]) && data[1] == (ARY_FLAG | CURRY_FLAG | PARTIAL_FLAG | REARG_FLAG) && !data[4].length && data
[9] == 1) {
      wrapper = wrapper[getFuncName(data[0])].apply(wrapper, data[3]);
    } else {
      wrapper = (func.length == 1 && isLaziable(func)) ? wrapper[funcName]() : wrapper.thru(func);
    }
  }
  return function() {
    var args = arguments,
        value = args[0];

    if (wrapper && args.length == 1 && isArray(value) && value.length >= LARGE_ARRAY_SIZE) {
      return wrapper.plant(value).value();
    }
    var index = 0,
        result = length ? funcs[index].apply(this, args) : value;

    while (++index < length) {
      result = funcs[index].call(this, result);
    }
    return result;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.constant"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>constant (value)](#apidoc.element.json-rpc2._.constant)
- description and source-code
```javascript
function constant(value) {
  return function() {
    return value;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.contains"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>contains (collection, target, fromIndex, guard)](#apidoc.element.json-rpc2._.contains)
- description and source-code
```javascript
function includes(collection, target, fromIndex, guard) {
  var length = collection ? getLength(collection) : 0;
  if (!isLength(length)) {
    collection = values(collection);
    length = collection.length;
  }
  if (typeof fromIndex != 'number' || (guard && isIterateeCall(target, fromIndex, guard))) {
    fromIndex = 0;
  } else {
    fromIndex = fromIndex < 0 ? nativeMax(length + fromIndex, 0) : (fromIndex || 0);
  }
  return (typeof collection == 'string' || !isArray(collection) && isString(collection))
    ? (fromIndex <= length && collection.indexOf(target, fromIndex) > -1)
    : (!!length && getIndexOf(collection, target, fromIndex) > -1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.countBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>countBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.countBy)
- description and source-code
```javascript
countBy = function (collection, iteratee, thisArg) {
  var result = initializer ? initializer() : {};
  iteratee = getCallback(iteratee, thisArg, 3);

  if (isArray(collection)) {
    var index = -1,
        length = collection.length;

    while (++index < length) {
      var value = collection[index];
      setter(result, value, iteratee(value, index, collection), collection);
    }
  } else {
    baseEach(collection, function(value, key, collection) {
      setter(result, value, iteratee(value, key, collection), collection);
    });
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.create"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>create (prototype, properties, guard)](#apidoc.element.json-rpc2._.create)
- description and source-code
```javascript
function create(prototype, properties, guard) {
  var result = baseCreate(prototype);
  if (guard && isIterateeCall(prototype, properties, guard)) {
    properties = undefined;
  }
  return properties ? baseAssign(result, properties) : result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.curry"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>curry (func, arity, guard)](#apidoc.element.json-rpc2._.curry)
- description and source-code
```javascript
function curryFunc(func, arity, guard) {
  if (guard && isIterateeCall(func, arity, guard)) {
    arity = undefined;
  }
  var result = createWrapper(func, flag, undefined, undefined, undefined, undefined, undefined, arity);
  result.placeholder = curryFunc.placeholder;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.curryRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>curryRight (func, arity, guard)](#apidoc.element.json-rpc2._.curryRight)
- description and source-code
```javascript
function curryFunc(func, arity, guard) {
  if (guard && isIterateeCall(func, arity, guard)) {
    arity = undefined;
  }
  var result = createWrapper(func, flag, undefined, undefined, undefined, undefined, undefined, arity);
  result.placeholder = curryFunc.placeholder;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.debounce"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>debounce (func, wait, options)](#apidoc.element.json-rpc2._.debounce)
- description and source-code
```javascript
function debounce(func, wait, options) {
  var args,
      maxTimeoutId,
      result,
      stamp,
      thisArg,
      timeoutId,
      trailingCall,
      lastCalled = 0,
      maxWait = false,
      trailing = true;

  if (typeof func != 'function') {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  wait = wait < 0 ? 0 : (+wait || 0);
  if (options === true) {
    var leading = true;
    trailing = false;
  } else if (isObject(options)) {
    leading = !!options.leading;
    maxWait = 'maxWait' in options && nativeMax(+options.maxWait || 0, wait);
    trailing = 'trailing' in options ? !!options.trailing : trailing;
  }

  function cancel() {
    if (timeoutId) {
      clearTimeout(timeoutId);
    }
    if (maxTimeoutId) {
      clearTimeout(maxTimeoutId);
    }
    lastCalled = 0;
    maxTimeoutId = timeoutId = trailingCall = undefined;
  }

  function complete(isCalled, id) {
    if (id) {
      clearTimeout(id);
    }
    maxTimeoutId = timeoutId = trailingCall = undefined;
    if (isCalled) {
      lastCalled = now();
      result = func.apply(thisArg, args);
      if (!timeoutId && !maxTimeoutId) {
        args = thisArg = undefined;
      }
    }
  }

  function delayed() {
    var remaining = wait - (now() - stamp);
    if (remaining <= 0 || remaining > wait) {
      complete(trailingCall, maxTimeoutId);
    } else {
      timeoutId = setTimeout(delayed, remaining);
    }
  }

  function maxDelayed() {
    complete(trailing, timeoutId);
  }

  function debounced() {
    args = arguments;
    stamp = now();
    thisArg = this;
    trailingCall = trailing && (timeoutId || !leading);

    if (maxWait === false) {
      var leadingCall = leading && !timeoutId;
    } else {
      if (!maxTimeoutId && !leading) {
        lastCalled = stamp;
      }
      var remaining = maxWait - (stamp - lastCalled),
          isCalled = remaining <= 0 || remaining > maxWait;

      if (isCalled) {
        if (maxTimeoutId) {
          maxTimeoutId = clearTimeout(maxTimeoutId);
        }
        lastCalled = stamp;
        result = func.apply(thisArg, args);
      }
      else if (!maxTimeoutId) {
        maxTimeoutId = setTimeout(maxDelayed, remaining);
      }
    }
    if (isCalled && timeoutId) {
      timeoutId = clearTimeout(timeoutId);
    }
    else if (!timeoutId && wait !== maxWait) {
      timeoutId = setTimeout(delayed, wait);
    }
    if (leadingCall) {
      isCalled = true;
      result = func.apply(thisArg, args);
    }
    if (isCalled && !timeoutId && !maxTimeoutId) {
      args = thisArg = undefined;
    }
    return result;
  }
  debounced.cancel = cancel;
  return debounced;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.deburr"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>deburr (string)](#apidoc.element.json-rpc2._.deburr)
- description and source-code
```javascript
function deburr(string) {
  string = baseToString(string);
  return string && string.replace(reLatin1, deburrLetter).replace(reComboMark, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.defaults"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>defaults ()](#apidoc.element.json-rpc2._.defaults)
- description and source-code
```javascript
defaults = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.defaultsDeep"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>defaultsDeep ()](#apidoc.element.json-rpc2._.defaultsDeep)
- description and source-code
```javascript
defaultsDeep = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.defer"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>defer ()](#apidoc.element.json-rpc2._.defer)
- description and source-code
```javascript
defer = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.delay"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>delay ()](#apidoc.element.json-rpc2._.delay)
- description and source-code
```javascript
delay = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.detect"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>detect (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.detect)
- description and source-code
```javascript
detect = function (collection, predicate, thisArg) {
  predicate = getCallback(predicate, thisArg, 3);
  if (isArray(collection)) {
    var index = baseFindIndex(collection, predicate, fromRight);
    return index > -1 ? collection[index] : undefined;
  }
  return baseFind(collection, predicate, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.difference"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>difference ()](#apidoc.element.json-rpc2._.difference)
- description and source-code
```javascript
difference = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.drop"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>drop (array, n, guard)](#apidoc.element.json-rpc2._.drop)
- description and source-code
```javascript
function drop(array, n, guard) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (guard ? isIterateeCall(array, n, guard) : n == null) {
    n = 1;
  }
  return baseSlice(array, n < 0 ? 0 : n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.dropRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>dropRight (array, n, guard)](#apidoc.element.json-rpc2._.dropRight)
- description and source-code
```javascript
function dropRight(array, n, guard) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (guard ? isIterateeCall(array, n, guard) : n == null) {
    n = 1;
  }
  n = length - (+n || 0);
  return baseSlice(array, 0, n < 0 ? 0 : n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.dropRightWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>dropRightWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.dropRightWhile)
- description and source-code
```javascript
function dropRightWhile(array, predicate, thisArg) {
  return (array && array.length)
    ? baseWhile(array, getCallback(predicate, thisArg, 3), true, true)
    : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.dropWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>dropWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.dropWhile)
- description and source-code
```javascript
function dropWhile(array, predicate, thisArg) {
  return (array && array.length)
    ? baseWhile(array, getCallback(predicate, thisArg, 3), true)
    : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.each"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>each (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.each)
- description and source-code
```javascript
each = function (collection, iteratee, thisArg) {
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee)
    : eachFunc(collection, bindCallback(iteratee, thisArg, 3));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.eachRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>eachRight (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.eachRight)
- description and source-code
```javascript
eachRight = function (collection, iteratee, thisArg) {
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee)
    : eachFunc(collection, bindCallback(iteratee, thisArg, 3));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.endsWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>endsWith (string, target, position)](#apidoc.element.json-rpc2._.endsWith)
- description and source-code
```javascript
function endsWith(string, target, position) {
  string = baseToString(string);
  target = (target + '');

  var length = string.length;
  position = position === undefined
    ? length
    : nativeMin(position < 0 ? 0 : (+position || 0), length);

  position -= target.length;
  return position >= 0 && string.indexOf(target, position) == position;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.eq"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>eq (value, other, customizer, thisArg)](#apidoc.element.json-rpc2._.eq)
- description and source-code
```javascript
function isEqual(value, other, customizer, thisArg) {
  customizer = typeof customizer == 'function' ? bindCallback(customizer, thisArg, 3) : undefined;
  var result = customizer ? customizer(value, other) : undefined;
  return  result === undefined ? baseIsEqual(value, other, customizer) : !!result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.escape"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>escape (string)](#apidoc.element.json-rpc2._.escape)
- description and source-code
```javascript
function escape(string) {
  // Reset 'lastIndex' because in IE < 9 'String#replace' does not.
  string = baseToString(string);
  return (string && reHasUnescapedHtml.test(string))
    ? string.replace(reUnescapedHtml, escapeHtmlChar)
    : string;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.escapeRegExp"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>escapeRegExp (string)](#apidoc.element.json-rpc2._.escapeRegExp)
- description and source-code
```javascript
function escapeRegExp(string) {
  string = baseToString(string);
  return (string && reHasRegExpChars.test(string))
    ? string.replace(reRegExpChars, escapeRegExpChar)
    : (string || '(?:)');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.every"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>every (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.every)
- description and source-code
```javascript
function every(collection, predicate, thisArg) {
  var func = isArray(collection) ? arrayEvery : baseEvery;
  if (thisArg && isIterateeCall(collection, predicate, thisArg)) {
    predicate = undefined;
  }
  if (typeof predicate != 'function' || thisArg !== undefined) {
    predicate = getCallback(predicate, thisArg, 3);
  }
  return func(collection, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.extend"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>extend ()](#apidoc.element.json-rpc2._.extend)
- description and source-code
```javascript
extend = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.fill"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>fill (array, value, start, end)](#apidoc.element.json-rpc2._.fill)
- description and source-code
```javascript
function fill(array, value, start, end) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (start && typeof start != 'number' && isIterateeCall(array, value, start)) {
    start = 0;
    end = length;
  }
  return baseFill(array, value, start, end);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.filter"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>filter (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.filter)
- description and source-code
```javascript
function filter(collection, predicate, thisArg) {
  var func = isArray(collection) ? arrayFilter : baseFilter;
  predicate = getCallback(predicate, thisArg, 3);
  return func(collection, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.find"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>find (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.find)
- description and source-code
```javascript
find = function (collection, predicate, thisArg) {
  predicate = getCallback(predicate, thisArg, 3);
  if (isArray(collection)) {
    var index = baseFindIndex(collection, predicate, fromRight);
    return index > -1 ? collection[index] : undefined;
  }
  return baseFind(collection, predicate, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.findIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>findIndex (array, predicate, thisArg)](#apidoc.element.json-rpc2._.findIndex)
- description and source-code
```javascript
findIndex = function (array, predicate, thisArg) {
  if (!(array && array.length)) {
    return -1;
  }
  predicate = getCallback(predicate, thisArg, 3);
  return baseFindIndex(array, predicate, fromRight);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.findKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>findKey (object, predicate, thisArg)](#apidoc.element.json-rpc2._.findKey)
- description and source-code
```javascript
findKey = function (object, predicate, thisArg) {
  predicate = getCallback(predicate, thisArg, 3);
  return baseFind(object, predicate, objectFunc, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.findLast"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>findLast (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.findLast)
- description and source-code
```javascript
findLast = function (collection, predicate, thisArg) {
  predicate = getCallback(predicate, thisArg, 3);
  if (isArray(collection)) {
    var index = baseFindIndex(collection, predicate, fromRight);
    return index > -1 ? collection[index] : undefined;
  }
  return baseFind(collection, predicate, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.findLastIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>findLastIndex (array, predicate, thisArg)](#apidoc.element.json-rpc2._.findLastIndex)
- description and source-code
```javascript
findLastIndex = function (array, predicate, thisArg) {
  if (!(array && array.length)) {
    return -1;
  }
  predicate = getCallback(predicate, thisArg, 3);
  return baseFindIndex(array, predicate, fromRight);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.findLastKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>findLastKey (object, predicate, thisArg)](#apidoc.element.json-rpc2._.findLastKey)
- description and source-code
```javascript
findLastKey = function (object, predicate, thisArg) {
  predicate = getCallback(predicate, thisArg, 3);
  return baseFind(object, predicate, objectFunc, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.findWhere"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>findWhere (collection, source)](#apidoc.element.json-rpc2._.findWhere)
- description and source-code
```javascript
function findWhere(collection, source) {
  return find(collection, baseMatches(source));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.first"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>first (array)](#apidoc.element.json-rpc2._.first)
- description and source-code
```javascript
function first(array) {
  return array ? array[0] : undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.flatten"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>flatten (array, isDeep, guard)](#apidoc.element.json-rpc2._.flatten)
- description and source-code
```javascript
function flatten(array, isDeep, guard) {
  var length = array ? array.length : 0;
  if (guard && isIterateeCall(array, isDeep, guard)) {
    isDeep = false;
  }
  return length ? baseFlatten(array, isDeep) : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.flattenDeep"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>flattenDeep (array)](#apidoc.element.json-rpc2._.flattenDeep)
- description and source-code
```javascript
function flattenDeep(array) {
  var length = array ? array.length : 0;
  return length ? baseFlatten(array, true) : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.floor"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>floor (number, precision)](#apidoc.element.json-rpc2._.floor)
- description and source-code
```javascript
floor = function (number, precision) {
  precision = precision === undefined ? 0 : (+precision || 0);
  if (precision) {
    precision = pow(10, precision);
    return func(number * precision) / precision;
  }
  return func(number);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.flow"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>flow ()](#apidoc.element.json-rpc2._.flow)
- description and source-code
```javascript
flow = function () {
  var wrapper,
      length = arguments.length,
      index = fromRight ? length : -1,
      leftIndex = 0,
      funcs = Array(length);

  while ((fromRight ? index-- : ++index < length)) {
    var func = funcs[leftIndex++] = arguments[index];
    if (typeof func != 'function') {
      throw new TypeError(FUNC_ERROR_TEXT);
    }
    if (!wrapper && LodashWrapper.prototype.thru && getFuncName(func) == 'wrapper') {
      wrapper = new LodashWrapper([], true);
    }
  }
  index = wrapper ? -1 : length;
  while (++index < length) {
    func = funcs[index];

    var funcName = getFuncName(func),
        data = funcName == 'wrapper' ? getData(func) : undefined;

    if (data && isLaziable(data[0]) && data[1] == (ARY_FLAG | CURRY_FLAG | PARTIAL_FLAG | REARG_FLAG) && !data[4].length && data
[9] == 1) {
      wrapper = wrapper[getFuncName(data[0])].apply(wrapper, data[3]);
    } else {
      wrapper = (func.length == 1 && isLaziable(func)) ? wrapper[funcName]() : wrapper.thru(func);
    }
  }
  return function() {
    var args = arguments,
        value = args[0];

    if (wrapper && args.length == 1 && isArray(value) && value.length >= LARGE_ARRAY_SIZE) {
      return wrapper.plant(value).value();
    }
    var index = 0,
        result = length ? funcs[index].apply(this, args) : value;

    while (++index < length) {
      result = funcs[index].call(this, result);
    }
    return result;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.flowRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>flowRight ()](#apidoc.element.json-rpc2._.flowRight)
- description and source-code
```javascript
flowRight = function () {
  var wrapper,
      length = arguments.length,
      index = fromRight ? length : -1,
      leftIndex = 0,
      funcs = Array(length);

  while ((fromRight ? index-- : ++index < length)) {
    var func = funcs[leftIndex++] = arguments[index];
    if (typeof func != 'function') {
      throw new TypeError(FUNC_ERROR_TEXT);
    }
    if (!wrapper && LodashWrapper.prototype.thru && getFuncName(func) == 'wrapper') {
      wrapper = new LodashWrapper([], true);
    }
  }
  index = wrapper ? -1 : length;
  while (++index < length) {
    func = funcs[index];

    var funcName = getFuncName(func),
        data = funcName == 'wrapper' ? getData(func) : undefined;

    if (data && isLaziable(data[0]) && data[1] == (ARY_FLAG | CURRY_FLAG | PARTIAL_FLAG | REARG_FLAG) && !data[4].length && data
[9] == 1) {
      wrapper = wrapper[getFuncName(data[0])].apply(wrapper, data[3]);
    } else {
      wrapper = (func.length == 1 && isLaziable(func)) ? wrapper[funcName]() : wrapper.thru(func);
    }
  }
  return function() {
    var args = arguments,
        value = args[0];

    if (wrapper && args.length == 1 && isArray(value) && value.length >= LARGE_ARRAY_SIZE) {
      return wrapper.plant(value).value();
    }
    var index = 0,
        result = length ? funcs[index].apply(this, args) : value;

    while (++index < length) {
      result = funcs[index].call(this, result);
    }
    return result;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.foldl"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>foldl (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.foldl)
- description and source-code
```javascript
foldl = function (collection, iteratee, accumulator, thisArg) {
  var initFromArray = arguments.length < 3;
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee, accumulator, initFromArray)
    : baseReduce(collection, getCallback(iteratee, thisArg, 4), accumulator, initFromArray, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.foldr"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>foldr (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.foldr)
- description and source-code
```javascript
foldr = function (collection, iteratee, accumulator, thisArg) {
  var initFromArray = arguments.length < 3;
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee, accumulator, initFromArray)
    : baseReduce(collection, getCallback(iteratee, thisArg, 4), accumulator, initFromArray, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.forEach"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>forEach (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.forEach)
- description and source-code
```javascript
forEach = function (collection, iteratee, thisArg) {
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee)
    : eachFunc(collection, bindCallback(iteratee, thisArg, 3));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.forEachRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>forEachRight (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.forEachRight)
- description and source-code
```javascript
forEachRight = function (collection, iteratee, thisArg) {
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee)
    : eachFunc(collection, bindCallback(iteratee, thisArg, 3));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.forIn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>forIn (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forIn)
- description and source-code
```javascript
forIn = function (object, iteratee, thisArg) {
  if (typeof iteratee != 'function' || thisArg !== undefined) {
    iteratee = bindCallback(iteratee, thisArg, 3);
  }
  return objectFunc(object, iteratee, keysIn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.forInRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>forInRight (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forInRight)
- description and source-code
```javascript
forInRight = function (object, iteratee, thisArg) {
  if (typeof iteratee != 'function' || thisArg !== undefined) {
    iteratee = bindCallback(iteratee, thisArg, 3);
  }
  return objectFunc(object, iteratee, keysIn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.forOwn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>forOwn (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forOwn)
- description and source-code
```javascript
forOwn = function (object, iteratee, thisArg) {
  if (typeof iteratee != 'function' || thisArg !== undefined) {
    iteratee = bindCallback(iteratee, thisArg, 3);
  }
  return objectFunc(object, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.forOwnRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>forOwnRight (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.forOwnRight)
- description and source-code
```javascript
forOwnRight = function (object, iteratee, thisArg) {
  if (typeof iteratee != 'function' || thisArg !== undefined) {
    iteratee = bindCallback(iteratee, thisArg, 3);
  }
  return objectFunc(object, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.functions"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>functions (object)](#apidoc.element.json-rpc2._.functions)
- description and source-code
```javascript
function functions(object) {
  return baseFunctions(object, keysIn(object));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.get"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>get (object, path, defaultValue)](#apidoc.element.json-rpc2._.get)
- description and source-code
```javascript
function get(object, path, defaultValue) {
  var result = object == null ? undefined : baseGet(object, toPath(path), path + '');
  return result === undefined ? defaultValue : result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.groupBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>groupBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.groupBy)
- description and source-code
```javascript
groupBy = function (collection, iteratee, thisArg) {
  var result = initializer ? initializer() : {};
  iteratee = getCallback(iteratee, thisArg, 3);

  if (isArray(collection)) {
    var index = -1,
        length = collection.length;

    while (++index < length) {
      var value = collection[index];
      setter(result, value, iteratee(value, index, collection), collection);
    }
  } else {
    baseEach(collection, function(value, key, collection) {
      setter(result, value, iteratee(value, key, collection), collection);
    });
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.gt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>gt (value, other)](#apidoc.element.json-rpc2._.gt)
- description and source-code
```javascript
function gt(value, other) {
  return value > other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.gte"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>gte (value, other)](#apidoc.element.json-rpc2._.gte)
- description and source-code
```javascript
function gte(value, other) {
  return value >= other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.has"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>has (object, path)](#apidoc.element.json-rpc2._.has)
- description and source-code
```javascript
function has(object, path) {
  if (object == null) {
    return false;
  }
  var result = hasOwnProperty.call(object, path);
  if (!result && !isKey(path)) {
    path = toPath(path);
    object = path.length == 1 ? object : baseGet(object, baseSlice(path, 0, -1));
    if (object == null) {
      return false;
    }
    path = last(path);
    result = hasOwnProperty.call(object, path);
  }
  return result || (isLength(object.length) && isIndex(path, object.length) &&
    (isArray(object) || isArguments(object)));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.head"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>head (array)](#apidoc.element.json-rpc2._.head)
- description and source-code
```javascript
function first(array) {
  return array ? array[0] : undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.identity"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>identity (value)](#apidoc.element.json-rpc2._.identity)
- description and source-code
```javascript
function identity(value) {
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.inRange"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>inRange (value, start, end)](#apidoc.element.json-rpc2._.inRange)
- description and source-code
```javascript
function inRange(value, start, end) {
  start = +start || 0;
  if (end === undefined) {
    end = start;
    start = 0;
  } else {
    end = +end || 0;
  }
  return value >= nativeMin(start, end) && value < nativeMax(start, end);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.include"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>include (collection, target, fromIndex, guard)](#apidoc.element.json-rpc2._.include)
- description and source-code
```javascript
function includes(collection, target, fromIndex, guard) {
  var length = collection ? getLength(collection) : 0;
  if (!isLength(length)) {
    collection = values(collection);
    length = collection.length;
  }
  if (typeof fromIndex != 'number' || (guard && isIterateeCall(target, fromIndex, guard))) {
    fromIndex = 0;
  } else {
    fromIndex = fromIndex < 0 ? nativeMax(length + fromIndex, 0) : (fromIndex || 0);
  }
  return (typeof collection == 'string' || !isArray(collection) && isString(collection))
    ? (fromIndex <= length && collection.indexOf(target, fromIndex) > -1)
    : (!!length && getIndexOf(collection, target, fromIndex) > -1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.includes"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>includes (collection, target, fromIndex, guard)](#apidoc.element.json-rpc2._.includes)
- description and source-code
```javascript
function includes(collection, target, fromIndex, guard) {
  var length = collection ? getLength(collection) : 0;
  if (!isLength(length)) {
    collection = values(collection);
    length = collection.length;
  }
  if (typeof fromIndex != 'number' || (guard && isIterateeCall(target, fromIndex, guard))) {
    fromIndex = 0;
  } else {
    fromIndex = fromIndex < 0 ? nativeMax(length + fromIndex, 0) : (fromIndex || 0);
  }
  return (typeof collection == 'string' || !isArray(collection) && isString(collection))
    ? (fromIndex <= length && collection.indexOf(target, fromIndex) > -1)
    : (!!length && getIndexOf(collection, target, fromIndex) > -1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.indexBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>indexBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.indexBy)
- description and source-code
```javascript
indexBy = function (collection, iteratee, thisArg) {
  var result = initializer ? initializer() : {};
  iteratee = getCallback(iteratee, thisArg, 3);

  if (isArray(collection)) {
    var index = -1,
        length = collection.length;

    while (++index < length) {
      var value = collection[index];
      setter(result, value, iteratee(value, index, collection), collection);
    }
  } else {
    baseEach(collection, function(value, key, collection) {
      setter(result, value, iteratee(value, key, collection), collection);
    });
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.indexOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>indexOf (array, value, fromIndex)](#apidoc.element.json-rpc2._.indexOf)
- description and source-code
```javascript
function indexOf(array, value, fromIndex) {
  var length = array ? array.length : 0;
  if (!length) {
    return -1;
  }
  if (typeof fromIndex == 'number') {
    fromIndex = fromIndex < 0 ? nativeMax(length + fromIndex, 0) : fromIndex;
  } else if (fromIndex) {
    var index = binaryIndex(array, value);
    if (index < length &&
        (value === value ? (value === array[index]) : (array[index] !== array[index]))) {
      return index;
    }
    return -1;
  }
  return baseIndexOf(array, value, fromIndex || 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.initial"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>initial (array)](#apidoc.element.json-rpc2._.initial)
- description and source-code
```javascript
function initial(array) {
  return dropRight(array, 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.inject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>inject (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.inject)
- description and source-code
```javascript
inject = function (collection, iteratee, accumulator, thisArg) {
  var initFromArray = arguments.length < 3;
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee, accumulator, initFromArray)
    : baseReduce(collection, getCallback(iteratee, thisArg, 4), accumulator, initFromArray, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.intersection"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>intersection ()](#apidoc.element.json-rpc2._.intersection)
- description and source-code
```javascript
intersection = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.invert"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>invert (object, multiValue, guard)](#apidoc.element.json-rpc2._.invert)
- description and source-code
```javascript
function invert(object, multiValue, guard) {
  if (guard && isIterateeCall(object, multiValue, guard)) {
    multiValue = undefined;
  }
  var index = -1,
      props = keys(object),
      length = props.length,
      result = {};

  while (++index < length) {
    var key = props[index],
        value = object[key];

    if (multiValue) {
      if (hasOwnProperty.call(result, value)) {
        result[value].push(key);
      } else {
        result[value] = [key];
      }
    }
    else {
      result[value] = key;
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.invoke"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>invoke ()](#apidoc.element.json-rpc2._.invoke)
- description and source-code
```javascript
invoke = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isArguments"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isArguments (value)](#apidoc.element.json-rpc2._.isArguments)
- description and source-code
```javascript
function isArguments(value) {
  return isObjectLike(value) && isArrayLike(value) &&
    hasOwnProperty.call(value, 'callee') && !propertyIsEnumerable.call(value, 'callee');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isArray"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isArray ()](#apidoc.element.json-rpc2._.isArray)
- description and source-code
```javascript
function isArray() { [native code] }
```
- example usage
```shell
...
      /**
       * Make a standard RPC call to the other endpoint.
       *
       * Note that some ways to make RPC calls bypass this method, for example HTTP
       * calls and responses are done in other places.
       */
      call     : function (method, params, callback){
if (!_.isArray(params)) {
  params = [params];
}

var id = null;
if (_.isFunction(callback)) {
  id = ++this.latestId;
  this.callbacks[id] = callback;
...
```

#### <a name="apidoc.element.json-rpc2._.isBoolean"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isBoolean (value)](#apidoc.element.json-rpc2._.isBoolean)
- description and source-code
```javascript
function isBoolean(value) {
  return value === true || value === false || (isObjectLike(value) && objToString.call(value) == boolTag);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isDate"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isDate (value)](#apidoc.element.json-rpc2._.isDate)
- description and source-code
```javascript
function isDate(value) {
  return isObjectLike(value) && objToString.call(value) == dateTag;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isElement"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isElement (value)](#apidoc.element.json-rpc2._.isElement)
- description and source-code
```javascript
function isElement(value) {
  return !!value && value.nodeType === 1 && isObjectLike(value) && !isPlainObject(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isEmpty"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isEmpty (value)](#apidoc.element.json-rpc2._.isEmpty)
- description and source-code
```javascript
function isEmpty(value) {
  if (value == null) {
    return true;
  }
  if (isArrayLike(value) && (isArray(value) || isString(value) || isArguments(value) ||
      (isObjectLike(value) && isFunction(value.splice)))) {
    return !value.length;
  }
  return !keys(value).length;
}
```
- example usage
```shell
...
       * receive as many messages as we like once the socket is established.
       */
      connectSocket: function (callback){
var self = this, socket, conn, parser;

socket = net.connect(this.port, this.host, function netConnect(){
  // Submit non-standard 'auth' message for raw sockets.
  if (!_.isEmpty(self.user) && !_.isEmpty(self.password)) {
    conn.call('auth', [self.user, self.password], function connectionAuth(err){
      if (err) {
        callback(err);
      } else {
        callback(null, conn);
      }
    });
...
```

#### <a name="apidoc.element.json-rpc2._.isEqual"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isEqual (value, other, customizer, thisArg)](#apidoc.element.json-rpc2._.isEqual)
- description and source-code
```javascript
function isEqual(value, other, customizer, thisArg) {
  customizer = typeof customizer == 'function' ? bindCallback(customizer, thisArg, 3) : undefined;
  var result = customizer ? customizer(value, other) : undefined;
  return  result === undefined ? baseIsEqual(value, other, customizer) : !!result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isError"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isError (value)](#apidoc.element.json-rpc2._.isError)
- description and source-code
```javascript
function isError(value) {
  return isObjectLike(value) && typeof value.message == 'string' && objToString.call(value) == errorTag;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isFinite"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isFinite (value)](#apidoc.element.json-rpc2._.isFinite)
- description and source-code
```javascript
function isFinite(value) {
  return typeof value == 'number' && nativeIsFinite(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isFunction"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isFunction (value)](#apidoc.element.json-rpc2._.isFunction)
- description and source-code
```javascript
function isFunction(value) {
  // The use of 'Object#toString' avoids issues with the 'typeof' operator
  // in older versions of Chrome and Safari which return 'function' for regexes
  // and Safari 8 equivalents which return 'object' for typed array constructors.
  return isObject(value) && objToString.call(value) == funcTag;
}
```
- example usage
```shell
...
      /**
       * Make HTTP connection/request.
       *
       * In HTTP mode, we get to submit exactly one message and receive up to n
       * messages.
       */
      connectHttp  : function (method, params, opts, callback){
if (_.isFunction(opts)) {
  callback = opts;
  opts = {};
}
opts = opts || {};

var id = 1, self = this;
...
```

#### <a name="apidoc.element.json-rpc2._.isMatch"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isMatch (object, source, customizer, thisArg)](#apidoc.element.json-rpc2._.isMatch)
- description and source-code
```javascript
function isMatch(object, source, customizer, thisArg) {
  customizer = typeof customizer == 'function' ? bindCallback(customizer, thisArg, 3) : undefined;
  return baseIsMatch(object, getMatchData(source), customizer);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isNaN"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isNaN (value)](#apidoc.element.json-rpc2._.isNaN)
- description and source-code
```javascript
function isNaN(value) {
  // An 'NaN' primitive is the only value that is not equal to itself.
  // Perform the 'toStringTag' check first to avoid errors with some host objects in IE.
  return isNumber(value) && value != +value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isNative"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isNative (value)](#apidoc.element.json-rpc2._.isNative)
- description and source-code
```javascript
function isNative(value) {
  if (value == null) {
    return false;
  }
  if (isFunction(value)) {
    return reIsNative.test(fnToString.call(value));
  }
  return isObjectLike(value) && reIsHostCtor.test(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isNull"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isNull (value)](#apidoc.element.json-rpc2._.isNull)
- description and source-code
```javascript
function isNull(value) {
  return value === null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isNumber"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isNumber (value)](#apidoc.element.json-rpc2._.isNumber)
- description and source-code
```javascript
function isNumber(value) {
  return typeof value == 'number' || (isObjectLike(value) && objToString.call(value) == numberTag);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isObject (value)](#apidoc.element.json-rpc2._.isObject)
- description and source-code
```javascript
function isObject(value) {
  // Avoid a V8 JIT bug in Chrome 19-20.
  // See https://code.google.com/p/v8/issues/detail?id=2291 for more details.
  var type = typeof value;
  return !!value && (type == 'object' || type == 'function');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isPlainObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isPlainObject (value)](#apidoc.element.json-rpc2._.isPlainObject)
- description and source-code
```javascript
function isPlainObject(value) {
  var Ctor;

  // Exit early for non 'Object' objects.
  if (!(isObjectLike(value) && objToString.call(value) == objectTag && !isArguments(value)) ||
      (!hasOwnProperty.call(value, 'constructor') && (Ctor = value.constructor, typeof Ctor == 'function' && !(Ctor instanceof Ctor
)))) {
    return false;
  }
  // IE < 9 iterates inherited properties before own properties. If the first
  // iterated property is an object's own property then there are no inherited
  // enumerable properties.
  var result;
  // In most environments an object's own properties are iterated before
  // its inherited properties. If the last iterated property is an object's
  // own property then there are no inherited enumerable properties.
  baseForIn(value, function(subValue, key) {
    result = key;
  });
  return result === undefined || hasOwnProperty.call(value, result);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isRegExp"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isRegExp (value)](#apidoc.element.json-rpc2._.isRegExp)
- description and source-code
```javascript
function isRegExp(value) {
  return isObject(value) && objToString.call(value) == regexpTag;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isString"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isString (value)](#apidoc.element.json-rpc2._.isString)
- description and source-code
```javascript
function isString(value) {
  return typeof value == 'string' || (isObjectLike(value) && objToString.call(value) == stringTag);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isTypedArray"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isTypedArray (value)](#apidoc.element.json-rpc2._.isTypedArray)
- description and source-code
```javascript
function isTypedArray(value) {
  return isObjectLike(value) && isLength(value.length) && !!typedArrayTags[objToString.call(value)];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.isUndefined"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>isUndefined (value)](#apidoc.element.json-rpc2._.isUndefined)
- description and source-code
```javascript
function isUndefined(value) {
  return value === undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.iteratee"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>iteratee (func, thisArg, guard)](#apidoc.element.json-rpc2._.iteratee)
- description and source-code
```javascript
function callback(func, thisArg, guard) {
  if (guard && isIterateeCall(func, thisArg, guard)) {
    thisArg = undefined;
  }
  return isObjectLike(func)
    ? matches(func)
    : baseCallback(func, thisArg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.kebabCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>kebabCase (string)](#apidoc.element.json-rpc2._.kebabCase)
- description and source-code
```javascript
kebabCase = function (string) {
  var index = -1,
      array = words(deburr(string)),
      length = array.length,
      result = '';

  while (++index < length) {
    result = callback(result, array[index], index);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.keys"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>keys (object)](#apidoc.element.json-rpc2._.keys)
- description and source-code
```javascript
keys = function (object) {
  var Ctor = object == null ? undefined : object.constructor;
  if ((typeof Ctor == 'function' && Ctor.prototype === object) ||
      (typeof object != 'function' && isArrayLike(object))) {
    return shimKeys(object);
  }
  return isObject(object) ? nativeKeys(object) : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.keysIn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>keysIn (object)](#apidoc.element.json-rpc2._.keysIn)
- description and source-code
```javascript
function keysIn(object) {
  if (object == null) {
    return [];
  }
  if (!isObject(object)) {
    object = Object(object);
  }
  var length = object.length;
  length = (length && isLength(length) &&
    (isArray(object) || isArguments(object)) && length) || 0;

  var Ctor = object.constructor,
      index = -1,
      isProto = typeof Ctor == 'function' && Ctor.prototype === object,
      result = Array(length),
      skipIndexes = length > 0;

  while (++index < length) {
    result[index] = (index + '');
  }
  for (var key in object) {
    if (!(skipIndexes && isIndex(key, length)) &&
        !(key == 'constructor' && (isProto || !hasOwnProperty.call(object, key)))) {
      result.push(key);
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.last"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>last (array)](#apidoc.element.json-rpc2._.last)
- description and source-code
```javascript
function last(array) {
  var length = array ? array.length : 0;
  return length ? array[length - 1] : undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.lastIndexOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>lastIndexOf (array, value, fromIndex)](#apidoc.element.json-rpc2._.lastIndexOf)
- description and source-code
```javascript
function lastIndexOf(array, value, fromIndex) {
  var length = array ? array.length : 0;
  if (!length) {
    return -1;
  }
  var index = length;
  if (typeof fromIndex == 'number') {
    index = (fromIndex < 0 ? nativeMax(length + fromIndex, 0) : nativeMin(fromIndex || 0, length - 1)) + 1;
  } else if (fromIndex) {
    index = binaryIndex(array, value, true) - 1;
    var other = array[index];
    if (value === value ? (value === other) : (other !== other)) {
      return index;
    }
    return -1;
  }
  if (value !== value) {
    return indexOfNaN(array, index, true);
  }
  while (index--) {
    if (array[index] === value) {
      return index;
    }
  }
  return -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.lt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>lt (value, other)](#apidoc.element.json-rpc2._.lt)
- description and source-code
```javascript
function lt(value, other) {
  return value < other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.lte"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>lte (value, other)](#apidoc.element.json-rpc2._.lte)
- description and source-code
```javascript
function lte(value, other) {
  return value <= other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.map"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>map (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.map)
- description and source-code
```javascript
function map(collection, iteratee, thisArg) {
  var func = isArray(collection) ? arrayMap : baseMap;
  iteratee = getCallback(iteratee, thisArg, 3);
  return func(collection, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.mapKeys"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>mapKeys (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.mapKeys)
- description and source-code
```javascript
mapKeys = function (object, iteratee, thisArg) {
  var result = {};
  iteratee = getCallback(iteratee, thisArg, 3);

  baseForOwn(object, function(value, key, object) {
    var mapped = iteratee(value, key, object);
    key = isMapKeys ? mapped : key;
    value = isMapKeys ? value : mapped;
    result[key] = value;
  });
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.mapValues"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>mapValues (object, iteratee, thisArg)](#apidoc.element.json-rpc2._.mapValues)
- description and source-code
```javascript
mapValues = function (object, iteratee, thisArg) {
  var result = {};
  iteratee = getCallback(iteratee, thisArg, 3);

  baseForOwn(object, function(value, key, object) {
    var mapped = iteratee(value, key, object);
    key = isMapKeys ? mapped : key;
    value = isMapKeys ? value : mapped;
    result[key] = value;
  });
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.matches"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>matches (source)](#apidoc.element.json-rpc2._.matches)
- description and source-code
```javascript
function matches(source) {
  return baseMatches(baseClone(source, true));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.matchesProperty"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>matchesProperty (path, srcValue)](#apidoc.element.json-rpc2._.matchesProperty)
- description and source-code
```javascript
function matchesProperty(path, srcValue) {
  return baseMatchesProperty(path, baseClone(srcValue, true));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.max"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>max (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.max)
- description and source-code
```javascript
max = function (collection, iteratee, thisArg) {
  if (thisArg && isIterateeCall(collection, iteratee, thisArg)) {
    iteratee = undefined;
  }
  iteratee = getCallback(iteratee, thisArg, 3);
  if (iteratee.length == 1) {
    collection = isArray(collection) ? collection : toIterable(collection);
    var result = arrayExtremum(collection, iteratee, comparator, exValue);
    if (!(collection.length && result === exValue)) {
      return result;
    }
  }
  return baseExtremum(collection, iteratee, comparator, exValue);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.memoize"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>memoize (func, resolver)](#apidoc.element.json-rpc2._.memoize)
- description and source-code
```javascript
function memoize(func, resolver) {
  if (typeof func != 'function' || (resolver && typeof resolver != 'function')) {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  var memoized = function() {
    var args = arguments,
        key = resolver ? resolver.apply(this, args) : args[0],
        cache = memoized.cache;

    if (cache.has(key)) {
      return cache.get(key);
    }
    var result = func.apply(this, args);
    memoized.cache = cache.set(key, result);
    return result;
  };
  memoized.cache = new memoize.Cache;
  return memoized;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.merge"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>merge ()](#apidoc.element.json-rpc2._.merge)
- description and source-code
```javascript
merge = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.method"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>method ()](#apidoc.element.json-rpc2._.method)
- description and source-code
```javascript
method = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.methodOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>methodOf ()](#apidoc.element.json-rpc2._.methodOf)
- description and source-code
```javascript
methodOf = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.methods"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>methods (object)](#apidoc.element.json-rpc2._.methods)
- description and source-code
```javascript
function functions(object) {
  return baseFunctions(object, keysIn(object));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.min"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>min (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.min)
- description and source-code
```javascript
min = function (collection, iteratee, thisArg) {
  if (thisArg && isIterateeCall(collection, iteratee, thisArg)) {
    iteratee = undefined;
  }
  iteratee = getCallback(iteratee, thisArg, 3);
  if (iteratee.length == 1) {
    collection = isArray(collection) ? collection : toIterable(collection);
    var result = arrayExtremum(collection, iteratee, comparator, exValue);
    if (!(collection.length && result === exValue)) {
      return result;
    }
  }
  return baseExtremum(collection, iteratee, comparator, exValue);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.mixin"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>mixin (object, source, options)](#apidoc.element.json-rpc2._.mixin)
- description and source-code
```javascript
function mixin(object, source, options) {
  if (options == null) {
    var isObj = isObject(source),
        props = isObj ? keys(source) : undefined,
        methodNames = (props && props.length) ? baseFunctions(source, props) : undefined;

    if (!(methodNames ? methodNames.length : isObj)) {
      methodNames = false;
      options = source;
      source = object;
      object = this;
    }
  }
  if (!methodNames) {
    methodNames = baseFunctions(source, keys(source));
  }
  var chain = true,
      index = -1,
      isFunc = isFunction(object),
      length = methodNames.length;

  if (options === false) {
    chain = false;
  } else if (isObject(options) && 'chain' in options) {
    chain = options.chain;
  }
  while (++index < length) {
    var methodName = methodNames[index],
        func = source[methodName];

    object[methodName] = func;
    if (isFunc) {
      object.prototype[methodName] = (function(func) {
        return function() {
          var chainAll = this.__chain__;
          if (chain || chainAll) {
            var result = object(this.__wrapped__),
                actions = result.__actions__ = arrayCopy(this.__actions__);

            actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
            result.__chain__ = chainAll;
            return result;
          }
          return func.apply(object, arrayPush([this.value()], arguments));
        };
      }(func));
    }
  }
  return object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.modArgs"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>modArgs ()](#apidoc.element.json-rpc2._.modArgs)
- description and source-code
```javascript
modArgs = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.negate"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>negate (predicate)](#apidoc.element.json-rpc2._.negate)
- description and source-code
```javascript
function negate(predicate) {
  if (typeof predicate != 'function') {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  return function() {
    return !predicate.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.noConflict"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>noConflict ()](#apidoc.element.json-rpc2._.noConflict)
- description and source-code
```javascript
function noConflict() {
  root._ = oldDash;
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.noop"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>noop ()](#apidoc.element.json-rpc2._.noop)
- description and source-code
```javascript
function noop() {
  // No operation performed.
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.now"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>now ()](#apidoc.element.json-rpc2._.now)
- description and source-code
```javascript
function now() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.object"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>object (props, values)](#apidoc.element.json-rpc2._.object)
- description and source-code
```javascript
function zipObject(props, values) {
  var index = -1,
      length = props ? props.length : 0,
      result = {};

  if (length && !values && !isArray(props[0])) {
    values = [];
  }
  while (++index < length) {
    var key = props[index];
    if (values) {
      result[key] = values[index];
    } else if (key) {
      result[key[0]] = key[1];
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.omit"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>omit ()](#apidoc.element.json-rpc2._.omit)
- description and source-code
```javascript
omit = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.once"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>once (func)](#apidoc.element.json-rpc2._.once)
- description and source-code
```javascript
function once(func) {
  return before(2, func);
}
```
- example usage
```shell
...
  else if (decoded.hasOwnProperty('method')) {
    connection.emit('call:' + decoded.method, decoded);
  }
};

if (response) {
  // Handle headers
  connection.res.once('data', function connectionOnce(data){
    if (connection.res.statusCode === 200) {
      callback(null, connection);
    } else {
      callback(new Error('"' + connection.res.statusCode + '"' + data));
    }
  });
...
```

#### <a name="apidoc.element.json-rpc2._.pad"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>pad (string, length, chars)](#apidoc.element.json-rpc2._.pad)
- description and source-code
```javascript
function pad(string, length, chars) {
  string = baseToString(string);
  length = +length;

  var strLength = string.length;
  if (strLength >= length || !nativeIsFinite(length)) {
    return string;
  }
  var mid = (length - strLength) / 2,
      leftLength = nativeFloor(mid),
      rightLength = nativeCeil(mid);

  chars = createPadding('', rightLength, chars);
  return chars.slice(0, leftLength) + string + chars;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.padLeft"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>padLeft (string, length, chars)](#apidoc.element.json-rpc2._.padLeft)
- description and source-code
```javascript
padLeft = function (string, length, chars) {
  string = baseToString(string);
  return (fromRight ? string : '') + createPadding(string, length, chars) + (fromRight ? '' : string);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.padRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>padRight (string, length, chars)](#apidoc.element.json-rpc2._.padRight)
- description and source-code
```javascript
padRight = function (string, length, chars) {
  string = baseToString(string);
  return (fromRight ? string : '') + createPadding(string, length, chars) + (fromRight ? '' : string);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.pairs"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>pairs (object)](#apidoc.element.json-rpc2._.pairs)
- description and source-code
```javascript
function pairs(object) {
  object = toObject(object);

  var index = -1,
      props = keys(object),
      length = props.length,
      result = Array(length);

  while (++index < length) {
    var key = props[index];
    result[index] = [key, object[key]];
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.parseInt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>parseInt (string, radix, guard)](#apidoc.element.json-rpc2._.parseInt)
- description and source-code
```javascript
function parseInt(string, radix, guard) {
  // Firefox < 21 and Opera < 15 follow ES3 for 'parseInt'.
  // Chrome fails to trim leading <BOM> whitespace characters.
  // See https://code.google.com/p/v8/issues/detail?id=3109 for more details.
  if (guard ? isIterateeCall(string, radix, guard) : radix == null) {
    radix = 0;
  } else if (radix) {
    radix = +radix;
  }
  string = trim(string);
  return nativeParseInt(string, radix || (reHasHexPrefix.test(string) ? 16 : 10));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partial"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>partial ()](#apidoc.element.json-rpc2._.partial)
- description and source-code
```javascript
partial = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partialRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>partialRight ()](#apidoc.element.json-rpc2._.partialRight)
- description and source-code
```javascript
partialRight = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partition"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>partition (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.partition)
- description and source-code
```javascript
partition = function (collection, iteratee, thisArg) {
  var result = initializer ? initializer() : {};
  iteratee = getCallback(iteratee, thisArg, 3);

  if (isArray(collection)) {
    var index = -1,
        length = collection.length;

    while (++index < length) {
      var value = collection[index];
      setter(result, value, iteratee(value, index, collection), collection);
    }
  } else {
    baseEach(collection, function(value, key, collection) {
      setter(result, value, iteratee(value, key, collection), collection);
    });
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.pick"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>pick ()](#apidoc.element.json-rpc2._.pick)
- description and source-code
```javascript
pick = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.pluck"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>pluck (collection, path)](#apidoc.element.json-rpc2._.pluck)
- description and source-code
```javascript
function pluck(collection, path) {
  return map(collection, property(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.property"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>property (path)](#apidoc.element.json-rpc2._.property)
- description and source-code
```javascript
function property(path) {
  return isKey(path) ? baseProperty(path) : basePropertyDeep(path);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.propertyOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>propertyOf (object)](#apidoc.element.json-rpc2._.propertyOf)
- description and source-code
```javascript
function propertyOf(object) {
  return function(path) {
    return baseGet(object, toPath(path), path + '');
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.pull"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>pull ()](#apidoc.element.json-rpc2._.pull)
- description and source-code
```javascript
function pull() {
  var args = arguments,
      array = args[0];

  if (!(array && array.length)) {
    return array;
  }
  var index = 0,
      indexOf = getIndexOf(),
      length = args.length;

  while (++index < length) {
    var fromIndex = 0,
        value = args[index];

    while ((fromIndex = indexOf(array, value, fromIndex)) > -1) {
      splice.call(array, fromIndex, 1);
    }
  }
  return array;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.pullAt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>pullAt ()](#apidoc.element.json-rpc2._.pullAt)
- description and source-code
```javascript
pullAt = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.random"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>random (min, max, floating)](#apidoc.element.json-rpc2._.random)
- description and source-code
```javascript
function random(min, max, floating) {
  if (floating && isIterateeCall(min, max, floating)) {
    max = floating = undefined;
  }
  var noMin = min == null,
      noMax = max == null;

  if (floating == null) {
    if (noMax && typeof min == 'boolean') {
      floating = min;
      min = 1;
    }
    else if (typeof max == 'boolean') {
      floating = max;
      noMax = true;
    }
  }
  if (noMin && noMax) {
    max = 1;
    noMax = false;
  }
  min = +min || 0;
  if (noMax) {
    max = min;
    min = 0;
  } else {
    max = +max || 0;
  }
  if (floating || min % 1 || max % 1) {
    var rand = nativeRandom();
    return nativeMin(min + (rand * (max - min + parseFloat('1e-' + ((rand + '').length - 1)))), max);
  }
  return baseRandom(min, max);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.range"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>range (start, end, step)](#apidoc.element.json-rpc2._.range)
- description and source-code
```javascript
function range(start, end, step) {
  if (step && isIterateeCall(start, end, step)) {
    end = step = undefined;
  }
  start = +start || 0;
  step = step == null ? 1 : (+step || 0);

  if (end == null) {
    end = start;
    start = 0;
  } else {
    end = +end || 0;
  }
  // Use 'Array(length)' so engines like Chakra and V8 avoid slower modes.
  // See https://youtu.be/XAqIpGU8ZZk#t=17m25s for more details.
  var index = -1,
      length = nativeMax(nativeCeil((end - start) / (step || 1)), 0),
      result = Array(length);

  while (++index < length) {
    result[index] = start;
    start += step;
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.rearg"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>rearg ()](#apidoc.element.json-rpc2._.rearg)
- description and source-code
```javascript
rearg = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.reduce"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>reduce (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.reduce)
- description and source-code
```javascript
reduce = function (collection, iteratee, accumulator, thisArg) {
  var initFromArray = arguments.length < 3;
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee, accumulator, initFromArray)
    : baseReduce(collection, getCallback(iteratee, thisArg, 4), accumulator, initFromArray, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.reduceRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>reduceRight (collection, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.reduceRight)
- description and source-code
```javascript
reduceRight = function (collection, iteratee, accumulator, thisArg) {
  var initFromArray = arguments.length < 3;
  return (typeof iteratee == 'function' && thisArg === undefined && isArray(collection))
    ? arrayFunc(collection, iteratee, accumulator, initFromArray)
    : baseReduce(collection, getCallback(iteratee, thisArg, 4), accumulator, initFromArray, eachFunc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.reject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>reject (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.reject)
- description and source-code
```javascript
function reject(collection, predicate, thisArg) {
  var func = isArray(collection) ? arrayFilter : baseFilter;
  predicate = getCallback(predicate, thisArg, 3);
  return func(collection, function(value, index, collection) {
    return !predicate(value, index, collection);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.remove"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>remove (array, predicate, thisArg)](#apidoc.element.json-rpc2._.remove)
- description and source-code
```javascript
function remove(array, predicate, thisArg) {
  var result = [];
  if (!(array && array.length)) {
    return result;
  }
  var index = -1,
      indexes = [],
      length = array.length;

  predicate = getCallback(predicate, thisArg, 3);
  while (++index < length) {
    var value = array[index];
    if (predicate(value, index, array)) {
      result.push(value);
      indexes.push(index);
    }
  }
  basePullAt(array, indexes);
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.repeat"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>repeat (string, n)](#apidoc.element.json-rpc2._.repeat)
- description and source-code
```javascript
function repeat(string, n) {
  var result = '';
  string = baseToString(string);
  n = +n;
  if (n < 1 || !string || !nativeIsFinite(n)) {
    return result;
  }
  // Leverage the exponentiation by squaring algorithm for a faster repeat.
  // See https://en.wikipedia.org/wiki/Exponentiation_by_squaring for more details.
  do {
    if (n % 2) {
      result += string;
    }
    n = nativeFloor(n / 2);
    string += string;
  } while (n);

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.rest"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>rest (array)](#apidoc.element.json-rpc2._.rest)
- description and source-code
```javascript
function rest(array) {
  return drop(array, 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.restParam"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>restParam (func, start)](#apidoc.element.json-rpc2._.restParam)
- description and source-code
```javascript
function restParam(func, start) {
  if (typeof func != 'function') {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  start = nativeMax(start === undefined ? (func.length - 1) : (+start || 0), 0);
  return function() {
    var args = arguments,
        index = -1,
        length = nativeMax(args.length - start, 0),
        rest = Array(length);

    while (++index < length) {
      rest[index] = args[start + index];
    }
    switch (start) {
      case 0: return func.call(this, rest);
      case 1: return func.call(this, args[0], rest);
      case 2: return func.call(this, args[0], args[1], rest);
    }
    var otherArgs = Array(start + 1);
    index = -1;
    while (++index < start) {
      otherArgs[index] = args[index];
    }
    otherArgs[start] = rest;
    return func.apply(this, otherArgs);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.result"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>result (object, path, defaultValue)](#apidoc.element.json-rpc2._.result)
- description and source-code
```javascript
function result(object, path, defaultValue) {
  var result = object == null ? undefined : object[path];
  if (result === undefined) {
    if (object != null && !isKey(path, object)) {
      path = toPath(path);
      object = path.length == 1 ? object : baseGet(object, baseSlice(path, 0, -1));
      result = object == null ? undefined : object[last(path)];
    }
    result = result === undefined ? defaultValue : result;
  }
  return isFunction(result) ? result.call(object) : result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.round"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>round (number, precision)](#apidoc.element.json-rpc2._.round)
- description and source-code
```javascript
round = function (number, precision) {
  precision = precision === undefined ? 0 : (+precision || 0);
  if (precision) {
    precision = pow(10, precision);
    return func(number * precision) / precision;
  }
  return func(number);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.runInContext"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>runInContext (context)](#apidoc.element.json-rpc2._.runInContext)
- description and source-code
```javascript
function runInContext(context) {
  // Avoid issues with some ES3 environments that attempt to use values, named
  // after built-in constructors like 'Object', for the creation of literals.
  // ES5 clears this up by stating that literals must use built-in constructors.
  // See https://es5.github.io/#x11.1.5 for more details.
  context = context ? _.defaults(root.Object(), context, _.pick(root, contextProps)) : root;

<span class="apidocCodeCommentSpan">  /** Native constructor references. */
</span>  var Array = context.Array,
      Date = context.Date,
      Error = context.Error,
      Function = context.Function,
      Math = context.Math,
      Number = context.Number,
      Object = context.Object,
      RegExp = context.RegExp,
      String = context.String,
      TypeError = context.TypeError;

  /** Used for native method references. */
  var arrayProto = Array.prototype,
      objectProto = Object.prototype,
      stringProto = String.prototype;

  /** Used to resolve the decompiled source of functions. */
  var fnToString = Function.prototype.toString;

  /** Used to check objects for own properties. */
  var hasOwnProperty = objectProto.hasOwnProperty;

  /** Used to generate unique IDs. */
  var idCounter = 0;

  /**
   * Used to resolve the ['toStringTag'](http://ecma-international.org/ecma-262/6.0/#sec-object.prototype.tostring)
   * of values.
   */
  var objToString = objectProto.toString;

  /** Used to restore the original '_' reference in '_.noConflict'. */
  var oldDash = root._;

  /** Used to detect if a method is native. */
  var reIsNative = RegExp('^' +
    fnToString.call(hasOwnProperty).replace(/[\\^$.*+?()[\]{}|]/g, '\\$&')
    .replace(/hasOwnProperty|(function).*?(?=\\\()| for .+?(?=\\\])/g, '$1.*?') + '$'
  );

  /** Native method references. */
  var ArrayBuffer = context.ArrayBuffer,
      clearTimeout = context.clearTimeout,
      parseFloat = context.parseFloat,
      pow = Math.pow,
      propertyIsEnumerable = objectProto.propertyIsEnumerable,
      Set = getNative(context, 'Set'),
      setTimeout = context.setTimeout,
      splice = arrayProto.splice,
      Uint8Array = context.Uint8Array,
      WeakMap = getNative(context, 'WeakMap');

  /* Native method references for those with the same name as other 'lodash' methods. */
  var nativeCeil = Math.ceil,
      nativeCreate = getNative(Object, 'create'),
      nativeFloor = Math.floor,
      nativeIsArray = getNative(Array, 'isArray'),
      nativeIsFinite = context.isFinite,
      nativeKeys = getNative(Object, 'keys'),
      nativeMax = Math.max,
      nativeMin = Math.min,
      nativeNow = getNative(Date, 'now'),
      nativeParseInt = context.parseInt,
      nativeRandom = Math.random;

  /** Used as references for '-Infinity' and 'Infinity'. */
  var NEGATIVE_INFINITY = Number.NEGATIVE_INFINITY,
      POSITIVE_INFINITY = Number.POSITIVE_INFINITY;

  /** Used as references for the maximum length and index of an array. */
  var MAX_ARRAY_LENGTH = 4294967295,
      MAX_ARRAY_INDEX = MAX_ARRAY_LENGTH - 1,
      HALF_MAX_ARRAY_LENGTH = MAX_ARRAY_LENGTH >>> 1;

  /**
   * Used as the [maximum length](http://ecma-international.org/ecma-262/6.0/#sec-number.max_safe_integer)
   * of an array-like value.
   */
  var MAX_SAFE_INTEGER = 9007199254740991;

  /** Used to store function metadata. */
  var metaMap = WeakMap && new WeakMap;

  /** Used to lookup unminified function names. */
  var realNames = {};

  /*------------------------------------------------------------------------*/

  /**
   * Creates a 'lodash' object which wraps 'value' to enable implicit chaining.
   * Methods that operate on and return arrays, collections, and functions can
   * be chained together. Methods that retrieve a single value or may return a
   * primitive value will automatically end the chain returning the unwrapped
   * value. Explicit chaining may be enabled using '_.chain'. The execution of
   * chained methods is lazy, that is, execution is deferred until '_#value'
   * is implicitly or explicitly called.
   *
   * Lazy evaluation allows several methods to support shortcut fusion. Shortcut ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sample"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sample (collection, n, guard)](#apidoc.element.json-rpc2._.sample)
- description and source-code
```javascript
function sample(collection, n, guard) {
  if (guard ? isIterateeCall(collection, n, guard) : n == null) {
    collection = toIterable(collection);
    var length = collection.length;
    return length > 0 ? collection[baseRandom(0, length - 1)] : undefined;
  }
  var index = -1,
      result = toArray(collection),
      length = result.length,
      lastIndex = length - 1;

  n = nativeMin(n < 0 ? 0 : (+n || 0), length);
  while (++index < n) {
    var rand = baseRandom(index, lastIndex),
        value = result[rand];

    result[rand] = result[index];
    result[index] = value;
  }
  result.length = n;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.select"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>select (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.select)
- description and source-code
```javascript
function filter(collection, predicate, thisArg) {
  var func = isArray(collection) ? arrayFilter : baseFilter;
  predicate = getCallback(predicate, thisArg, 3);
  return func(collection, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.set"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>set (object, path, value)](#apidoc.element.json-rpc2._.set)
- description and source-code
```javascript
function set(object, path, value) {
  if (object == null) {
    return object;
  }
  var pathKey = (path + '');
  path = (object[pathKey] != null || isKey(path, object)) ? [pathKey] : toPath(path);

  var index = -1,
      length = path.length,
      lastIndex = length - 1,
      nested = object;

  while (nested != null && ++index < length) {
    var key = path[index];
    if (isObject(nested)) {
      if (index == lastIndex) {
        nested[key] = value;
      } else if (nested[key] == null) {
        nested[key] = isIndex(path[index + 1]) ? [] : {};
      }
    }
    nested = nested[key];
  }
  return object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.shuffle"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>shuffle (collection)](#apidoc.element.json-rpc2._.shuffle)
- description and source-code
```javascript
function shuffle(collection) {
  return sample(collection, POSITIVE_INFINITY);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.size"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>size (collection)](#apidoc.element.json-rpc2._.size)
- description and source-code
```javascript
function size(collection) {
  var length = collection ? getLength(collection) : 0;
  return isLength(length) ? length : keys(collection).length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.slice"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>slice (array, start, end)](#apidoc.element.json-rpc2._.slice)
- description and source-code
```javascript
function slice(array, start, end) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (end && typeof end != 'number' && isIterateeCall(array, start, end)) {
    start = 0;
    end = length;
  }
  return baseSlice(array, start, end);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.snakeCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>snakeCase (string)](#apidoc.element.json-rpc2._.snakeCase)
- description and source-code
```javascript
snakeCase = function (string) {
  var index = -1,
      array = words(deburr(string)),
      length = array.length,
      result = '';

  while (++index < length) {
    result = callback(result, array[index], index);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.some"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>some (collection, predicate, thisArg)](#apidoc.element.json-rpc2._.some)
- description and source-code
```javascript
function some(collection, predicate, thisArg) {
  var func = isArray(collection) ? arraySome : baseSome;
  if (thisArg && isIterateeCall(collection, predicate, thisArg)) {
    predicate = undefined;
  }
  if (typeof predicate != 'function' || thisArg !== undefined) {
    predicate = getCallback(predicate, thisArg, 3);
  }
  return func(collection, predicate);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sortBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sortBy (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.sortBy)
- description and source-code
```javascript
function sortBy(collection, iteratee, thisArg) {
  if (collection == null) {
    return [];
  }
  if (thisArg && isIterateeCall(collection, iteratee, thisArg)) {
    iteratee = undefined;
  }
  var index = -1;
  iteratee = getCallback(iteratee, thisArg, 3);

  var result = baseMap(collection, function(value, key, collection) {
    return { 'criteria': iteratee(value, key, collection), 'index': ++index, 'value': value };
  });
  return baseSortBy(result, compareAscending);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sortByAll"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sortByAll ()](#apidoc.element.json-rpc2._.sortByAll)
- description and source-code
```javascript
sortByAll = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sortByOrder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sortByOrder (collection, iteratees, orders, guard)](#apidoc.element.json-rpc2._.sortByOrder)
- description and source-code
```javascript
function sortByOrder(collection, iteratees, orders, guard) {
  if (collection == null) {
    return [];
  }
  if (guard && isIterateeCall(iteratees, orders, guard)) {
    orders = undefined;
  }
  if (!isArray(iteratees)) {
    iteratees = iteratees == null ? [] : [iteratees];
  }
  if (!isArray(orders)) {
    orders = orders == null ? [] : [orders];
  }
  return baseSortByOrder(collection, iteratees, orders);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sortedIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sortedIndex (array, value, iteratee, thisArg)](#apidoc.element.json-rpc2._.sortedIndex)
- description and source-code
```javascript
sortedIndex = function (array, value, iteratee, thisArg) {
  var callback = getCallback(iteratee);
  return (iteratee == null && callback === baseCallback)
    ? binaryIndex(array, value, retHighest)
    : binaryIndexBy(array, value, callback(iteratee, thisArg, 1), retHighest);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sortedLastIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sortedLastIndex (array, value, iteratee, thisArg)](#apidoc.element.json-rpc2._.sortedLastIndex)
- description and source-code
```javascript
sortedLastIndex = function (array, value, iteratee, thisArg) {
  var callback = getCallback(iteratee);
  return (iteratee == null && callback === baseCallback)
    ? binaryIndex(array, value, retHighest)
    : binaryIndexBy(array, value, callback(iteratee, thisArg, 1), retHighest);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.spread"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>spread (func)](#apidoc.element.json-rpc2._.spread)
- description and source-code
```javascript
function spread(func) {
  if (typeof func != 'function') {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  return function(array) {
    return func.apply(this, array);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.startCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>startCase (string)](#apidoc.element.json-rpc2._.startCase)
- description and source-code
```javascript
startCase = function (string) {
  var index = -1,
      array = words(deburr(string)),
      length = array.length,
      result = '';

  while (++index < length) {
    result = callback(result, array[index], index);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.startsWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>startsWith (string, target, position)](#apidoc.element.json-rpc2._.startsWith)
- description and source-code
```javascript
function startsWith(string, target, position) {
  string = baseToString(string);
  position = position == null
    ? 0
    : nativeMin(position < 0 ? 0 : (+position || 0), string.length);

  return string.lastIndexOf(target, position) == position;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.sum"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>sum (collection, iteratee, thisArg)](#apidoc.element.json-rpc2._.sum)
- description and source-code
```javascript
function sum(collection, iteratee, thisArg) {
  if (thisArg && isIterateeCall(collection, iteratee, thisArg)) {
    iteratee = undefined;
  }
  iteratee = getCallback(iteratee, thisArg, 3);
  return iteratee.length == 1
    ? arraySum(isArray(collection) ? collection : toIterable(collection), iteratee)
    : baseSum(collection, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.tail"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>tail (array)](#apidoc.element.json-rpc2._.tail)
- description and source-code
```javascript
function rest(array) {
  return drop(array, 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.take"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>take (array, n, guard)](#apidoc.element.json-rpc2._.take)
- description and source-code
```javascript
function take(array, n, guard) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (guard ? isIterateeCall(array, n, guard) : n == null) {
    n = 1;
  }
  return baseSlice(array, 0, n < 0 ? 0 : n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.takeRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>takeRight (array, n, guard)](#apidoc.element.json-rpc2._.takeRight)
- description and source-code
```javascript
function takeRight(array, n, guard) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (guard ? isIterateeCall(array, n, guard) : n == null) {
    n = 1;
  }
  n = length - (+n || 0);
  return baseSlice(array, n < 0 ? 0 : n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.takeRightWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>takeRightWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.takeRightWhile)
- description and source-code
```javascript
function takeRightWhile(array, predicate, thisArg) {
  return (array && array.length)
    ? baseWhile(array, getCallback(predicate, thisArg, 3), false, true)
    : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.takeWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>takeWhile (array, predicate, thisArg)](#apidoc.element.json-rpc2._.takeWhile)
- description and source-code
```javascript
function takeWhile(array, predicate, thisArg) {
  return (array && array.length)
    ? baseWhile(array, getCallback(predicate, thisArg, 3))
    : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.tap"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>tap (value, interceptor, thisArg)](#apidoc.element.json-rpc2._.tap)
- description and source-code
```javascript
function tap(value, interceptor, thisArg) {
  interceptor.call(thisArg, value);
  return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.template"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>template (string, options, otherOptions)](#apidoc.element.json-rpc2._.template)
- description and source-code
```javascript
function template(string, options, otherOptions) {
  // Based on John Resig's 'tmpl' implementation (http://ejohn.org/blog/javascript-micro-templating/)
  // and Laura Doktorova's doT.js (https://github.com/olado/doT).
  var settings = lodash.templateSettings;

  if (otherOptions && isIterateeCall(string, options, otherOptions)) {
    options = otherOptions = undefined;
  }
  string = baseToString(string);
  options = assignWith(baseAssign({}, otherOptions || options), settings, assignOwnDefaults);

  var imports = assignWith(baseAssign({}, options.imports), settings.imports, assignOwnDefaults),
      importsKeys = keys(imports),
      importsValues = baseValues(imports, importsKeys);

  var isEscaping,
      isEvaluating,
      index = 0,
      interpolate = options.interpolate || reNoMatch,
      source = "__p += '";

  // Compile the regexp to match each delimiter.
  var reDelimiters = RegExp(
    (options.escape || reNoMatch).source + '|' +
    interpolate.source + '|' +
    (interpolate === reInterpolate ? reEsTemplate : reNoMatch).source + '|' +
    (options.evaluate || reNoMatch).source + '|$'
  , 'g');

  // Use a sourceURL for easier debugging.
  var sourceURL = '//# sourceURL=' +
    ('sourceURL' in options
      ? options.sourceURL
      : ('lodash.templateSources[' + (++templateCounter) + ']')
    ) + '\n';

  string.replace(reDelimiters, function(match, escapeValue, interpolateValue, esTemplateValue, evaluateValue, offset) {
    interpolateValue || (interpolateValue = esTemplateValue);

    // Escape characters that can't be included in string literals.
    source += string.slice(index, offset).replace(reUnescapedString, escapeStringChar);

    // Replace delimiters with snippets.
    if (escapeValue) {
      isEscaping = true;
      source += "' +\n__e(" + escapeValue + ") +\n'";
    }
    if (evaluateValue) {
      isEvaluating = true;
      source += "';\n" + evaluateValue + ";\n__p += '";
    }
    if (interpolateValue) {
      source += "' +\n((__t = (" + interpolateValue + ")) == null ? '' : __t) +\n'";
    }
    index = offset + match.length;

    // The JS engine embedded in Adobe products requires returning the 'match'
    // string in order to produce the correct 'offset' value.
    return match;
  });

  source += "';\n";

  // If 'variable' is not specified wrap a with-statement around the generated
  // code to add the data object to the top of the scope chain.
  var variable = options.variable;
  if (!variable) {
    source = 'with (obj) {\n' + source + '\n}\n';
  }
  // Cleanup code by stripping empty strings.
  source = (isEvaluating ? source.replace(reEmptyStringLeading, '') : source)
    .replace(reEmptyStringMiddle, '$1')
    .replace(reEmptyStringTrailing, '$1;');

  // Frame code as the function body.
  source = 'function(' + (variable || 'obj') + ') {\n' +
    (variable
      ? ''
      : 'obj || (obj = {});\n'
    ) +
    "var __t, __p = ''" +
    (isEscaping
       ? ', __e = _.escape'
       : ''
    ) +
    (isEvaluating
      ? ', __j = Array.prototype.join;\n' +
        "function print() { __p += __j.call(arguments, '') }\n"
      : ';\n'
    ) +
    source +
    'return __p\n}';

  var result = attempt(function() {
    return Function(importsKeys, sourceURL + 'return ' + source).apply(undefined, importsValues);
  });

  // Provide the compiled function's source by its 'toString' method or
  // the 'source' property as a convenience for inlining compiled templates.
  result.source = source;
  if (isError(result)) {
    throw result;
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.throttle"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>throttle (func, wait, options)](#apidoc.element.json-rpc2._.throttle)
- description and source-code
```javascript
function throttle(func, wait, options) {
  var leading = true,
      trailing = true;

  if (typeof func != 'function') {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  if (options === false) {
    leading = false;
  } else if (isObject(options)) {
    leading = 'leading' in options ? !!options.leading : leading;
    trailing = 'trailing' in options ? !!options.trailing : trailing;
  }
  return debounce(func, wait, { 'leading': leading, 'maxWait': +wait, 'trailing': trailing });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.thru"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>thru (value, interceptor, thisArg)](#apidoc.element.json-rpc2._.thru)
- description and source-code
```javascript
function thru(value, interceptor, thisArg) {
  return interceptor.call(thisArg, value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.times"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>times (n, iteratee, thisArg)](#apidoc.element.json-rpc2._.times)
- description and source-code
```javascript
function times(n, iteratee, thisArg) {
  n = nativeFloor(n);

  // Exit early to avoid a JSC JIT bug in Safari 8
  // where 'Array(0)' is treated as 'Array(1)'.
  if (n < 1 || !nativeIsFinite(n)) {
    return [];
  }
  var index = -1,
      result = Array(nativeMin(n, MAX_ARRAY_LENGTH));

  iteratee = bindCallback(iteratee, thisArg, 1);
  while (++index < n) {
    if (index < MAX_ARRAY_LENGTH) {
      result[index] = iteratee(index);
    } else {
      iteratee(index);
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.toArray"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>toArray (value)](#apidoc.element.json-rpc2._.toArray)
- description and source-code
```javascript
function toArray(value) {
  var length = value ? getLength(value) : 0;
  if (!isLength(length)) {
    return values(value);
  }
  if (!length) {
    return [];
  }
  return arrayCopy(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.toPlainObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>toPlainObject (value)](#apidoc.element.json-rpc2._.toPlainObject)
- description and source-code
```javascript
function toPlainObject(value) {
  return baseCopy(value, keysIn(value));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.transform"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>transform (object, iteratee, accumulator, thisArg)](#apidoc.element.json-rpc2._.transform)
- description and source-code
```javascript
function transform(object, iteratee, accumulator, thisArg) {
  var isArr = isArray(object) || isTypedArray(object);
  iteratee = getCallback(iteratee, thisArg, 4);

  if (accumulator == null) {
    if (isArr || isObject(object)) {
      var Ctor = object.constructor;
      if (isArr) {
        accumulator = isArray(object) ? new Ctor : [];
      } else {
        accumulator = baseCreate(isFunction(Ctor) ? Ctor.prototype : undefined);
      }
    } else {
      accumulator = {};
    }
  }
  (isArr ? arrayEach : baseForOwn)(object, function(value, index, object) {
    return iteratee(accumulator, value, index, object);
  });
  return accumulator;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.trim"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>trim (string, chars, guard)](#apidoc.element.json-rpc2._.trim)
- description and source-code
```javascript
function trim(string, chars, guard) {
  var value = string;
  string = baseToString(string);
  if (!string) {
    return string;
  }
  if (guard ? isIterateeCall(value, chars, guard) : chars == null) {
    return string.slice(trimmedLeftIndex(string), trimmedRightIndex(string) + 1);
  }
  chars = (chars + '');
  return string.slice(charsLeftIndex(string, chars), charsRightIndex(string, chars) + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.trimLeft"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>trimLeft (string, chars, guard)](#apidoc.element.json-rpc2._.trimLeft)
- description and source-code
```javascript
function trimLeft(string, chars, guard) {
  var value = string;
  string = baseToString(string);
  if (!string) {
    return string;
  }
  if (guard ? isIterateeCall(value, chars, guard) : chars == null) {
    return string.slice(trimmedLeftIndex(string));
  }
  return string.slice(charsLeftIndex(string, (chars + '')));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.trimRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>trimRight (string, chars, guard)](#apidoc.element.json-rpc2._.trimRight)
- description and source-code
```javascript
function trimRight(string, chars, guard) {
  var value = string;
  string = baseToString(string);
  if (!string) {
    return string;
  }
  if (guard ? isIterateeCall(value, chars, guard) : chars == null) {
    return string.slice(0, trimmedRightIndex(string) + 1);
  }
  return string.slice(0, charsRightIndex(string, (chars + '')) + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.trunc"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>trunc (string, options, guard)](#apidoc.element.json-rpc2._.trunc)
- description and source-code
```javascript
function trunc(string, options, guard) {
  if (guard && isIterateeCall(string, options, guard)) {
    options = undefined;
  }
  var length = DEFAULT_TRUNC_LENGTH,
      omission = DEFAULT_TRUNC_OMISSION;

  if (options != null) {
    if (isObject(options)) {
      var separator = 'separator' in options ? options.separator : separator;
      length = 'length' in options ? (+options.length || 0) : length;
      omission = 'omission' in options ? baseToString(options.omission) : omission;
    } else {
      length = +options || 0;
    }
  }
  string = baseToString(string);
  if (length >= string.length) {
    return string;
  }
  var end = length - omission.length;
  if (end < 1) {
    return omission;
  }
  var result = string.slice(0, end);
  if (separator == null) {
    return result + omission;
  }
  if (isRegExp(separator)) {
    if (string.slice(end).search(separator)) {
      var match,
          newEnd,
          substring = string.slice(0, end);

      if (!separator.global) {
        separator = RegExp(separator.source, (reFlags.exec(separator) || '') + 'g');
      }
      separator.lastIndex = 0;
      while ((match = separator.exec(substring))) {
        newEnd = match.index;
      }
      result = result.slice(0, newEnd == null ? end : newEnd);
    }
  } else if (string.indexOf(separator, end) != end) {
    var index = result.lastIndexOf(separator);
    if (index > -1) {
      result = result.slice(0, index);
    }
  }
  return result + omission;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.unescape"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>unescape (string)](#apidoc.element.json-rpc2._.unescape)
- description and source-code
```javascript
function unescape(string) {
  string = baseToString(string);
  return (string && reHasEscapedHtml.test(string))
    ? string.replace(reEscapedHtml, unescapeHtmlChar)
    : string;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.union"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>union ()](#apidoc.element.json-rpc2._.union)
- description and source-code
```javascript
union = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.uniq"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>uniq (array, isSorted, iteratee, thisArg)](#apidoc.element.json-rpc2._.uniq)
- description and source-code
```javascript
function uniq(array, isSorted, iteratee, thisArg) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (isSorted != null && typeof isSorted != 'boolean') {
    thisArg = iteratee;
    iteratee = isIterateeCall(array, isSorted, thisArg) ? undefined : isSorted;
    isSorted = false;
  }
  var callback = getCallback();
  if (!(iteratee == null && callback === baseCallback)) {
    iteratee = callback(iteratee, thisArg, 3);
  }
  return (isSorted && getIndexOf() == baseIndexOf)
    ? sortedUniq(array, iteratee)
    : baseUniq(array, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.unique"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>unique (array, isSorted, iteratee, thisArg)](#apidoc.element.json-rpc2._.unique)
- description and source-code
```javascript
function uniq(array, isSorted, iteratee, thisArg) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  if (isSorted != null && typeof isSorted != 'boolean') {
    thisArg = iteratee;
    iteratee = isIterateeCall(array, isSorted, thisArg) ? undefined : isSorted;
    isSorted = false;
  }
  var callback = getCallback();
  if (!(iteratee == null && callback === baseCallback)) {
    iteratee = callback(iteratee, thisArg, 3);
  }
  return (isSorted && getIndexOf() == baseIndexOf)
    ? sortedUniq(array, iteratee)
    : baseUniq(array, iteratee);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.uniqueId"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>uniqueId (prefix)](#apidoc.element.json-rpc2._.uniqueId)
- description and source-code
```javascript
function uniqueId(prefix) {
  var id = ++idCounter;
  return baseToString(prefix) + id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.unzip"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>unzip (array)](#apidoc.element.json-rpc2._.unzip)
- description and source-code
```javascript
function unzip(array) {
  if (!(array && array.length)) {
    return [];
  }
  var index = -1,
      length = 0;

  array = arrayFilter(array, function(group) {
    if (isArrayLike(group)) {
      length = nativeMax(group.length, length);
      return true;
    }
  });
  var result = Array(length);
  while (++index < length) {
    result[index] = arrayMap(array, baseProperty(index));
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.unzipWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>unzipWith (array, iteratee, thisArg)](#apidoc.element.json-rpc2._.unzipWith)
- description and source-code
```javascript
function unzipWith(array, iteratee, thisArg) {
  var length = array ? array.length : 0;
  if (!length) {
    return [];
  }
  var result = unzip(array);
  if (iteratee == null) {
    return result;
  }
  iteratee = bindCallback(iteratee, thisArg, 4);
  return arrayMap(result, function(group) {
    return arrayReduce(group, iteratee, undefined, true);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.values"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>values (object)](#apidoc.element.json-rpc2._.values)
- description and source-code
```javascript
function values(object) {
  return baseValues(object, keys(object));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.valuesIn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>valuesIn (object)](#apidoc.element.json-rpc2._.valuesIn)
- description and source-code
```javascript
function valuesIn(object) {
  return baseValues(object, keysIn(object));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.where"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>where (collection, source)](#apidoc.element.json-rpc2._.where)
- description and source-code
```javascript
function where(collection, source) {
  return filter(collection, baseMatches(source));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.without"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>without ()](#apidoc.element.json-rpc2._.without)
- description and source-code
```javascript
without = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.words"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>words (string, pattern, guard)](#apidoc.element.json-rpc2._.words)
- description and source-code
```javascript
function words(string, pattern, guard) {
  if (guard && isIterateeCall(string, pattern, guard)) {
    pattern = undefined;
  }
  string = baseToString(string);
  return string.match(pattern || reWords) || [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.wrap"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>wrap (value, wrapper)](#apidoc.element.json-rpc2._.wrap)
- description and source-code
```javascript
function wrap(value, wrapper) {
  wrapper = wrapper == null ? identity : wrapper;
  return createWrapper(wrapper, PARTIAL_FLAG, undefined, [value], []);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.xor"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>xor ()](#apidoc.element.json-rpc2._.xor)
- description and source-code
```javascript
function xor() {
  var index = -1,
      length = arguments.length;

  while (++index < length) {
    var array = arguments[index];
    if (isArrayLike(array)) {
      var result = result
        ? arrayPush(baseDifference(result, array), baseDifference(array, result))
        : array;
    }
  }
  return result ? baseUniq(result) : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.zip"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>zip ()](#apidoc.element.json-rpc2._.zip)
- description and source-code
```javascript
zip = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.zipObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>zipObject (props, values)](#apidoc.element.json-rpc2._.zipObject)
- description and source-code
```javascript
function zipObject(props, values) {
  var index = -1,
      length = props ? props.length : 0,
      result = {};

  if (length && !values && !isArray(props[0])) {
    values = [];
  }
  while (++index < length) {
    var key = props[index];
    if (values) {
      result[key] = values[index];
    } else if (key) {
      result[key[0]] = key[1];
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.zipWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>zipWith ()](#apidoc.element.json-rpc2._.zipWith)
- description and source-code
```javascript
zipWith = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.bind"></a>[module json-rpc2._.bind](#apidoc.module.json-rpc2._.bind)

#### <a name="apidoc.element.json-rpc2._.bind.bind"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>bind ()](#apidoc.element.json-rpc2._.bind.bind)
- description and source-code
```javascript
function bind() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bind.placeholder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.bind.</span>placeholder (value)](#apidoc.element.json-rpc2._.bind.placeholder)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.bindKey"></a>[module json-rpc2._.bindKey](#apidoc.module.json-rpc2._.bindKey)

#### <a name="apidoc.element.json-rpc2._.bindKey.bindKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>bindKey ()](#apidoc.element.json-rpc2._.bindKey.bindKey)
- description and source-code
```javascript
bindKey = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.bindKey.placeholder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.bindKey.</span>placeholder (value)](#apidoc.element.json-rpc2._.bindKey.placeholder)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.curry"></a>[module json-rpc2._.curry](#apidoc.module.json-rpc2._.curry)

#### <a name="apidoc.element.json-rpc2._.curry.curry"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>curry (func, arity, guard)](#apidoc.element.json-rpc2._.curry.curry)
- description and source-code
```javascript
function curryFunc(func, arity, guard) {
  if (guard && isIterateeCall(func, arity, guard)) {
    arity = undefined;
  }
  var result = createWrapper(func, flag, undefined, undefined, undefined, undefined, undefined, arity);
  result.placeholder = curryFunc.placeholder;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.curry.placeholder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.curry.</span>placeholder (value)](#apidoc.element.json-rpc2._.curry.placeholder)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.curryRight"></a>[module json-rpc2._.curryRight](#apidoc.module.json-rpc2._.curryRight)

#### <a name="apidoc.element.json-rpc2._.curryRight.curryRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>curryRight (func, arity, guard)](#apidoc.element.json-rpc2._.curryRight.curryRight)
- description and source-code
```javascript
function curryFunc(func, arity, guard) {
  if (guard && isIterateeCall(func, arity, guard)) {
    arity = undefined;
  }
  var result = createWrapper(func, flag, undefined, undefined, undefined, undefined, undefined, arity);
  result.placeholder = curryFunc.placeholder;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.curryRight.placeholder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.curryRight.</span>placeholder (value)](#apidoc.element.json-rpc2._.curryRight.placeholder)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.memoize"></a>[module json-rpc2._.memoize](#apidoc.module.json-rpc2._.memoize)

#### <a name="apidoc.element.json-rpc2._.memoize.memoize"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>memoize (func, resolver)](#apidoc.element.json-rpc2._.memoize.memoize)
- description and source-code
```javascript
function memoize(func, resolver) {
  if (typeof func != 'function' || (resolver && typeof resolver != 'function')) {
    throw new TypeError(FUNC_ERROR_TEXT);
  }
  var memoized = function() {
    var args = arguments,
        key = resolver ? resolver.apply(this, args) : args[0],
        cache = memoized.cache;

    if (cache.has(key)) {
      return cache.get(key);
    }
    var result = func.apply(this, args);
    memoized.cache = cache.set(key, result);
    return result;
  };
  memoized.cache = new memoize.Cache;
  return memoized;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.memoize.Cache"></a>[function <span class="apidocSignatureSpan">json-rpc2._.memoize.</span>Cache ()](#apidoc.element.json-rpc2._.memoize.Cache)
- description and source-code
```javascript
function MapCache() {
  this.__data__ = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.memoize.Cache.prototype"></a>[module json-rpc2._.memoize.Cache.prototype](#apidoc.module.json-rpc2._.memoize.Cache.prototype)

#### <a name="apidoc.element.json-rpc2._.memoize.Cache.prototype.delete"></a>[function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>delete (key)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.delete)
- description and source-code
```javascript
function mapDelete(key) {
  return this.has(key) && delete this.__data__[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.memoize.Cache.prototype.get"></a>[function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>get (key)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.get)
- description and source-code
```javascript
function mapGet(key) {
  return key == '__proto__' ? undefined : this.__data__[key];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.memoize.Cache.prototype.has"></a>[function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>has (key)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.has)
- description and source-code
```javascript
function mapHas(key) {
  return key != '__proto__' && hasOwnProperty.call(this.__data__, key);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.memoize.Cache.prototype.set"></a>[function <span class="apidocSignatureSpan">json-rpc2._.memoize.Cache.prototype.</span>set (key, value)](#apidoc.element.json-rpc2._.memoize.Cache.prototype.set)
- description and source-code
```javascript
function mapSet(key, value) {
  if (key != '__proto__') {
    this.__data__[key] = value;
  }
  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.partial"></a>[module json-rpc2._.partial](#apidoc.module.json-rpc2._.partial)

#### <a name="apidoc.element.json-rpc2._.partial.partial"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>partial ()](#apidoc.element.json-rpc2._.partial.partial)
- description and source-code
```javascript
partial = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partial.placeholder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.partial.</span>placeholder (value)](#apidoc.element.json-rpc2._.partial.placeholder)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.partialRight"></a>[module json-rpc2._.partialRight](#apidoc.module.json-rpc2._.partialRight)

#### <a name="apidoc.element.json-rpc2._.partialRight.partialRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.</span>partialRight ()](#apidoc.element.json-rpc2._.partialRight.partialRight)
- description and source-code
```javascript
partialRight = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.partialRight.placeholder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.partialRight.</span>placeholder (value)](#apidoc.element.json-rpc2._.partialRight.placeholder)
- description and source-code
```javascript
function lodash(value) {
  if (isObjectLike(value) && !isArray(value) && !(value instanceof LazyWrapper)) {
    if (value instanceof LodashWrapper) {
      return value;
    }
    if (hasOwnProperty.call(value, '__chain__') && hasOwnProperty.call(value, '__wrapped__')) {
      return wrapperClone(value);
    }
  }
  return new LodashWrapper(value);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-rpc2._.prototype"></a>[module json-rpc2._.prototype](#apidoc.module.json-rpc2._.prototype)

#### <a name="apidoc.element.json-rpc2._.prototype.add"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>add ()](#apidoc.element.json-rpc2._.prototype.add)
- description and source-code
```javascript
add = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.after"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>after ()](#apidoc.element.json-rpc2._.prototype.after)
- description and source-code
```javascript
after = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.all"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>all ()](#apidoc.element.json-rpc2._.prototype.all)
- description and source-code
```javascript
all = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.any"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>any ()](#apidoc.element.json-rpc2._.prototype.any)
- description and source-code
```javascript
any = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.ary"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>ary ()](#apidoc.element.json-rpc2._.prototype.ary)
- description and source-code
```javascript
ary = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.assign"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>assign ()](#apidoc.element.json-rpc2._.prototype.assign)
- description and source-code
```javascript
assign = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.at"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>at ()](#apidoc.element.json-rpc2._.prototype.at)
- description and source-code
```javascript
at = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.attempt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>attempt ()](#apidoc.element.json-rpc2._.prototype.attempt)
- description and source-code
```javascript
attempt = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.backflow"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>backflow ()](#apidoc.element.json-rpc2._.prototype.backflow)
- description and source-code
```javascript
backflow = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.before"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>before ()](#apidoc.element.json-rpc2._.prototype.before)
- description and source-code
```javascript
before = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.bind"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>bind ()](#apidoc.element.json-rpc2._.prototype.bind)
- description and source-code
```javascript
bind = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.bindAll"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>bindAll ()](#apidoc.element.json-rpc2._.prototype.bindAll)
- description and source-code
```javascript
bindAll = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.bindKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>bindKey ()](#apidoc.element.json-rpc2._.prototype.bindKey)
- description and source-code
```javascript
bindKey = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.callback"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>callback ()](#apidoc.element.json-rpc2._.prototype.callback)
- description and source-code
```javascript
callback = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.camelCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>camelCase ()](#apidoc.element.json-rpc2._.prototype.camelCase)
- description and source-code
```javascript
camelCase = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.capitalize"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>capitalize ()](#apidoc.element.json-rpc2._.prototype.capitalize)
- description and source-code
```javascript
capitalize = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.ceil"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>ceil ()](#apidoc.element.json-rpc2._.prototype.ceil)
- description and source-code
```javascript
ceil = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.chain"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>chain ()](#apidoc.element.json-rpc2._.prototype.chain)
- description and source-code
```javascript
function wrapperChain() {
  return chain(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.chunk"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>chunk ()](#apidoc.element.json-rpc2._.prototype.chunk)
- description and source-code
```javascript
chunk = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.clone"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>clone ()](#apidoc.element.json-rpc2._.prototype.clone)
- description and source-code
```javascript
clone = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.cloneDeep"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>cloneDeep ()](#apidoc.element.json-rpc2._.prototype.cloneDeep)
- description and source-code
```javascript
cloneDeep = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.collect"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>collect ()](#apidoc.element.json-rpc2._.prototype.collect)
- description and source-code
```javascript
collect = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.commit"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>commit ()](#apidoc.element.json-rpc2._.prototype.commit)
- description and source-code
```javascript
function wrapperCommit() {
  return new LodashWrapper(this.value(), this.__chain__);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.compact"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>compact ()](#apidoc.element.json-rpc2._.prototype.compact)
- description and source-code
```javascript
compact = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.compose"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>compose ()](#apidoc.element.json-rpc2._.prototype.compose)
- description and source-code
```javascript
compose = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.concat"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>concat ()](#apidoc.element.json-rpc2._.prototype.concat)
- description and source-code
```javascript
concat = function () {
  var args = arguments,
      index = -1,
      length = nativeMax(args.length - start, 0),
      rest = Array(length);

  while (++index < length) {
    rest[index] = args[start + index];
  }
  switch (start) {
    case 0: return func.call(this, rest);
    case 1: return func.call(this, args[0], rest);
    case 2: return func.call(this, args[0], args[1], rest);
  }
  var otherArgs = Array(start + 1);
  index = -1;
  while (++index < start) {
    otherArgs[index] = args[index];
  }
  otherArgs[start] = rest;
  return func.apply(this, otherArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.constant"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>constant ()](#apidoc.element.json-rpc2._.prototype.constant)
- description and source-code
```javascript
constant = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.contains"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>contains ()](#apidoc.element.json-rpc2._.prototype.contains)
- description and source-code
```javascript
contains = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.countBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>countBy ()](#apidoc.element.json-rpc2._.prototype.countBy)
- description and source-code
```javascript
countBy = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.create"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>create ()](#apidoc.element.json-rpc2._.prototype.create)
- description and source-code
```javascript
create = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.curry"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>curry ()](#apidoc.element.json-rpc2._.prototype.curry)
- description and source-code
```javascript
curry = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.curryRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>curryRight ()](#apidoc.element.json-rpc2._.prototype.curryRight)
- description and source-code
```javascript
curryRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.debounce"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>debounce ()](#apidoc.element.json-rpc2._.prototype.debounce)
- description and source-code
```javascript
debounce = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.deburr"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>deburr ()](#apidoc.element.json-rpc2._.prototype.deburr)
- description and source-code
```javascript
deburr = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.defaults"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>defaults ()](#apidoc.element.json-rpc2._.prototype.defaults)
- description and source-code
```javascript
defaults = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.defaultsDeep"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>defaultsDeep ()](#apidoc.element.json-rpc2._.prototype.defaultsDeep)
- description and source-code
```javascript
defaultsDeep = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.defer"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>defer ()](#apidoc.element.json-rpc2._.prototype.defer)
- description and source-code
```javascript
defer = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.delay"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>delay ()](#apidoc.element.json-rpc2._.prototype.delay)
- description and source-code
```javascript
delay = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.detect"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>detect ()](#apidoc.element.json-rpc2._.prototype.detect)
- description and source-code
```javascript
detect = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.difference"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>difference ()](#apidoc.element.json-rpc2._.prototype.difference)
- description and source-code
```javascript
difference = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.drop"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>drop ()](#apidoc.element.json-rpc2._.prototype.drop)
- description and source-code
```javascript
drop = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.dropRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>dropRight ()](#apidoc.element.json-rpc2._.prototype.dropRight)
- description and source-code
```javascript
dropRight = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.dropRightWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>dropRightWhile ()](#apidoc.element.json-rpc2._.prototype.dropRightWhile)
- description and source-code
```javascript
dropRightWhile = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.dropWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>dropWhile ()](#apidoc.element.json-rpc2._.prototype.dropWhile)
- description and source-code
```javascript
dropWhile = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.each"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>each ()](#apidoc.element.json-rpc2._.prototype.each)
- description and source-code
```javascript
each = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.eachRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>eachRight ()](#apidoc.element.json-rpc2._.prototype.eachRight)
- description and source-code
```javascript
eachRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.endsWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>endsWith ()](#apidoc.element.json-rpc2._.prototype.endsWith)
- description and source-code
```javascript
endsWith = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.eq"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>eq ()](#apidoc.element.json-rpc2._.prototype.eq)
- description and source-code
```javascript
eq = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.escape"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>escape ()](#apidoc.element.json-rpc2._.prototype.escape)
- description and source-code
```javascript
escape = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.escapeRegExp"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>escapeRegExp ()](#apidoc.element.json-rpc2._.prototype.escapeRegExp)
- description and source-code
```javascript
escapeRegExp = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.every"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>every ()](#apidoc.element.json-rpc2._.prototype.every)
- description and source-code
```javascript
every = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.extend"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>extend ()](#apidoc.element.json-rpc2._.prototype.extend)
- description and source-code
```javascript
extend = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.fill"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>fill ()](#apidoc.element.json-rpc2._.prototype.fill)
- description and source-code
```javascript
fill = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.filter"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>filter ()](#apidoc.element.json-rpc2._.prototype.filter)
- description and source-code
```javascript
filter = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.find"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>find ()](#apidoc.element.json-rpc2._.prototype.find)
- description and source-code
```javascript
find = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.findIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findIndex ()](#apidoc.element.json-rpc2._.prototype.findIndex)
- description and source-code
```javascript
findIndex = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.findKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findKey ()](#apidoc.element.json-rpc2._.prototype.findKey)
- description and source-code
```javascript
findKey = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.findLast"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findLast ()](#apidoc.element.json-rpc2._.prototype.findLast)
- description and source-code
```javascript
findLast = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.findLastIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findLastIndex ()](#apidoc.element.json-rpc2._.prototype.findLastIndex)
- description and source-code
```javascript
findLastIndex = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.findLastKey"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findLastKey ()](#apidoc.element.json-rpc2._.prototype.findLastKey)
- description and source-code
```javascript
findLastKey = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.findWhere"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>findWhere ()](#apidoc.element.json-rpc2._.prototype.findWhere)
- description and source-code
```javascript
findWhere = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.first"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>first ()](#apidoc.element.json-rpc2._.prototype.first)
- description and source-code
```javascript
first = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.flatten"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flatten ()](#apidoc.element.json-rpc2._.prototype.flatten)
- description and source-code
```javascript
flatten = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.flattenDeep"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flattenDeep ()](#apidoc.element.json-rpc2._.prototype.flattenDeep)
- description and source-code
```javascript
flattenDeep = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.floor"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>floor ()](#apidoc.element.json-rpc2._.prototype.floor)
- description and source-code
```javascript
floor = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.flow"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flow ()](#apidoc.element.json-rpc2._.prototype.flow)
- description and source-code
```javascript
flow = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.flowRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>flowRight ()](#apidoc.element.json-rpc2._.prototype.flowRight)
- description and source-code
```javascript
flowRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.foldl"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>foldl ()](#apidoc.element.json-rpc2._.prototype.foldl)
- description and source-code
```javascript
foldl = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.foldr"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>foldr ()](#apidoc.element.json-rpc2._.prototype.foldr)
- description and source-code
```javascript
foldr = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.forEach"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forEach ()](#apidoc.element.json-rpc2._.prototype.forEach)
- description and source-code
```javascript
forEach = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.forEachRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forEachRight ()](#apidoc.element.json-rpc2._.prototype.forEachRight)
- description and source-code
```javascript
forEachRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.forIn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forIn ()](#apidoc.element.json-rpc2._.prototype.forIn)
- description and source-code
```javascript
forIn = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.forInRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forInRight ()](#apidoc.element.json-rpc2._.prototype.forInRight)
- description and source-code
```javascript
forInRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.forOwn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forOwn ()](#apidoc.element.json-rpc2._.prototype.forOwn)
- description and source-code
```javascript
forOwn = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.forOwnRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>forOwnRight ()](#apidoc.element.json-rpc2._.prototype.forOwnRight)
- description and source-code
```javascript
forOwnRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.functions"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>functions ()](#apidoc.element.json-rpc2._.prototype.functions)
- description and source-code
```javascript
functions = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.get"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>get ()](#apidoc.element.json-rpc2._.prototype.get)
- description and source-code
```javascript
get = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.groupBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>groupBy ()](#apidoc.element.json-rpc2._.prototype.groupBy)
- description and source-code
```javascript
groupBy = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.gt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>gt ()](#apidoc.element.json-rpc2._.prototype.gt)
- description and source-code
```javascript
gt = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.gte"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>gte ()](#apidoc.element.json-rpc2._.prototype.gte)
- description and source-code
```javascript
gte = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.has"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>has ()](#apidoc.element.json-rpc2._.prototype.has)
- description and source-code
```javascript
has = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.head"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>head ()](#apidoc.element.json-rpc2._.prototype.head)
- description and source-code
```javascript
head = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.identity"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>identity ()](#apidoc.element.json-rpc2._.prototype.identity)
- description and source-code
```javascript
identity = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.inRange"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>inRange ()](#apidoc.element.json-rpc2._.prototype.inRange)
- description and source-code
```javascript
inRange = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.include"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>include ()](#apidoc.element.json-rpc2._.prototype.include)
- description and source-code
```javascript
include = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.includes"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>includes ()](#apidoc.element.json-rpc2._.prototype.includes)
- description and source-code
```javascript
includes = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.indexBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>indexBy ()](#apidoc.element.json-rpc2._.prototype.indexBy)
- description and source-code
```javascript
indexBy = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>indexOf ()](#apidoc.element.json-rpc2._.prototype.indexOf)
- description and source-code
```javascript
indexOf = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.initial"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>initial ()](#apidoc.element.json-rpc2._.prototype.initial)
- description and source-code
```javascript
initial = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.inject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>inject ()](#apidoc.element.json-rpc2._.prototype.inject)
- description and source-code
```javascript
inject = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.intersection"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>intersection ()](#apidoc.element.json-rpc2._.prototype.intersection)
- description and source-code
```javascript
intersection = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.invert"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>invert ()](#apidoc.element.json-rpc2._.prototype.invert)
- description and source-code
```javascript
invert = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.invoke"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>invoke ()](#apidoc.element.json-rpc2._.prototype.invoke)
- description and source-code
```javascript
invoke = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isArguments"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isArguments ()](#apidoc.element.json-rpc2._.prototype.isArguments)
- description and source-code
```javascript
isArguments = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isArray"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isArray ()](#apidoc.element.json-rpc2._.prototype.isArray)
- description and source-code
```javascript
isArray = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
...
      /**
       * Make a standard RPC call to the other endpoint.
       *
       * Note that some ways to make RPC calls bypass this method, for example HTTP
       * calls and responses are done in other places.
       */
      call     : function (method, params, callback){
if (!_.isArray(params)) {
  params = [params];
}

var id = null;
if (_.isFunction(callback)) {
  id = ++this.latestId;
  this.callbacks[id] = callback;
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.isBoolean"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isBoolean ()](#apidoc.element.json-rpc2._.prototype.isBoolean)
- description and source-code
```javascript
isBoolean = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isDate"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isDate ()](#apidoc.element.json-rpc2._.prototype.isDate)
- description and source-code
```javascript
isDate = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isElement"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isElement ()](#apidoc.element.json-rpc2._.prototype.isElement)
- description and source-code
```javascript
isElement = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isEmpty"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isEmpty ()](#apidoc.element.json-rpc2._.prototype.isEmpty)
- description and source-code
```javascript
isEmpty = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
...
       * receive as many messages as we like once the socket is established.
       */
      connectSocket: function (callback){
var self = this, socket, conn, parser;

socket = net.connect(this.port, this.host, function netConnect(){
  // Submit non-standard 'auth' message for raw sockets.
  if (!_.isEmpty(self.user) && !_.isEmpty(self.password)) {
    conn.call('auth', [self.user, self.password], function connectionAuth(err){
      if (err) {
        callback(err);
      } else {
        callback(null, conn);
      }
    });
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.isEqual"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isEqual ()](#apidoc.element.json-rpc2._.prototype.isEqual)
- description and source-code
```javascript
isEqual = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isError"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isError ()](#apidoc.element.json-rpc2._.prototype.isError)
- description and source-code
```javascript
isError = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isFinite"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isFinite ()](#apidoc.element.json-rpc2._.prototype.isFinite)
- description and source-code
```javascript
isFinite = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isFunction"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isFunction ()](#apidoc.element.json-rpc2._.prototype.isFunction)
- description and source-code
```javascript
isFunction = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
...
      /**
       * Make HTTP connection/request.
       *
       * In HTTP mode, we get to submit exactly one message and receive up to n
       * messages.
       */
      connectHttp  : function (method, params, opts, callback){
if (_.isFunction(opts)) {
  callback = opts;
  opts = {};
}
opts = opts || {};

var id = 1, self = this;
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.isMatch"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isMatch ()](#apidoc.element.json-rpc2._.prototype.isMatch)
- description and source-code
```javascript
isMatch = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isNaN"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNaN ()](#apidoc.element.json-rpc2._.prototype.isNaN)
- description and source-code
```javascript
isNaN = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isNative"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNative ()](#apidoc.element.json-rpc2._.prototype.isNative)
- description and source-code
```javascript
isNative = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isNull"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNull ()](#apidoc.element.json-rpc2._.prototype.isNull)
- description and source-code
```javascript
isNull = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isNumber"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isNumber ()](#apidoc.element.json-rpc2._.prototype.isNumber)
- description and source-code
```javascript
isNumber = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isObject ()](#apidoc.element.json-rpc2._.prototype.isObject)
- description and source-code
```javascript
isObject = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isPlainObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isPlainObject ()](#apidoc.element.json-rpc2._.prototype.isPlainObject)
- description and source-code
```javascript
isPlainObject = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isRegExp"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isRegExp ()](#apidoc.element.json-rpc2._.prototype.isRegExp)
- description and source-code
```javascript
isRegExp = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isString"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isString ()](#apidoc.element.json-rpc2._.prototype.isString)
- description and source-code
```javascript
isString = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isTypedArray"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isTypedArray ()](#apidoc.element.json-rpc2._.prototype.isTypedArray)
- description and source-code
```javascript
isTypedArray = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.isUndefined"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>isUndefined ()](#apidoc.element.json-rpc2._.prototype.isUndefined)
- description and source-code
```javascript
isUndefined = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.iteratee"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>iteratee ()](#apidoc.element.json-rpc2._.prototype.iteratee)
- description and source-code
```javascript
iteratee = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.join"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>join ()](#apidoc.element.json-rpc2._.prototype.join)
- description and source-code
```javascript
join = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
...
          if (scope) {
            this.scopes[name + '.' + funcName] = scope;
          }
        }
      }
    }

    EventEmitter.trace('***', 'exposing module: ' + name + ' [funs: ' + funcs.join(', ') + ']');
  }
  return func;
},
handleCall: function (decoded, conn, callback){
  EventEmitter.trace('<--', 'Request (id ' + decoded.id + '): ' +
    decoded.method + '(' + JSON.stringify(decoded.params) + ')');
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.kebabCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>kebabCase ()](#apidoc.element.json-rpc2._.prototype.kebabCase)
- description and source-code
```javascript
kebabCase = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.keys"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>keys ()](#apidoc.element.json-rpc2._.prototype.keys)
- description and source-code
```javascript
keys = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.keysIn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>keysIn ()](#apidoc.element.json-rpc2._.prototype.keysIn)
- description and source-code
```javascript
keysIn = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.last"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>last ()](#apidoc.element.json-rpc2._.prototype.last)
- description and source-code
```javascript
last = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.lastIndexOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>lastIndexOf ()](#apidoc.element.json-rpc2._.prototype.lastIndexOf)
- description and source-code
```javascript
lastIndexOf = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.lt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>lt ()](#apidoc.element.json-rpc2._.prototype.lt)
- description and source-code
```javascript
lt = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.lte"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>lte ()](#apidoc.element.json-rpc2._.prototype.lte)
- description and source-code
```javascript
lte = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.map"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>map ()](#apidoc.element.json-rpc2._.prototype.map)
- description and source-code
```javascript
map = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.mapKeys"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>mapKeys ()](#apidoc.element.json-rpc2._.prototype.mapKeys)
- description and source-code
```javascript
mapKeys = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.mapValues"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>mapValues ()](#apidoc.element.json-rpc2._.prototype.mapValues)
- description and source-code
```javascript
mapValues = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.matches"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>matches ()](#apidoc.element.json-rpc2._.prototype.matches)
- description and source-code
```javascript
matches = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.matchesProperty"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>matchesProperty ()](#apidoc.element.json-rpc2._.prototype.matchesProperty)
- description and source-code
```javascript
matchesProperty = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.max"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>max ()](#apidoc.element.json-rpc2._.prototype.max)
- description and source-code
```javascript
max = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.memoize"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>memoize ()](#apidoc.element.json-rpc2._.prototype.memoize)
- description and source-code
```javascript
memoize = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.merge"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>merge ()](#apidoc.element.json-rpc2._.prototype.merge)
- description and source-code
```javascript
merge = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.method"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>method ()](#apidoc.element.json-rpc2._.prototype.method)
- description and source-code
```javascript
method = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.methodOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>methodOf ()](#apidoc.element.json-rpc2._.prototype.methodOf)
- description and source-code
```javascript
methodOf = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.methods"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>methods ()](#apidoc.element.json-rpc2._.prototype.methods)
- description and source-code
```javascript
methods = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.min"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>min ()](#apidoc.element.json-rpc2._.prototype.min)
- description and source-code
```javascript
min = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.mixin"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>mixin ()](#apidoc.element.json-rpc2._.prototype.mixin)
- description and source-code
```javascript
mixin = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.modArgs"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>modArgs ()](#apidoc.element.json-rpc2._.prototype.modArgs)
- description and source-code
```javascript
modArgs = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.negate"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>negate ()](#apidoc.element.json-rpc2._.prototype.negate)
- description and source-code
```javascript
negate = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.noConflict"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>noConflict ()](#apidoc.element.json-rpc2._.prototype.noConflict)
- description and source-code
```javascript
noConflict = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.noop"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>noop ()](#apidoc.element.json-rpc2._.prototype.noop)
- description and source-code
```javascript
noop = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.now"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>now ()](#apidoc.element.json-rpc2._.prototype.now)
- description and source-code
```javascript
now = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.object"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>object ()](#apidoc.element.json-rpc2._.prototype.object)
- description and source-code
```javascript
object = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.omit"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>omit ()](#apidoc.element.json-rpc2._.prototype.omit)
- description and source-code
```javascript
omit = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.once"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>once ()](#apidoc.element.json-rpc2._.prototype.once)
- description and source-code
```javascript
once = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
...
  else if (decoded.hasOwnProperty('method')) {
    connection.emit('call:' + decoded.method, decoded);
  }
};

if (response) {
  // Handle headers
  connection.res.once('data', function connectionOnce(data){
    if (connection.res.statusCode === 200) {
      callback(null, connection);
    } else {
      callback(new Error('"' + connection.res.statusCode + '"' + data));
    }
  });
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.pad"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pad ()](#apidoc.element.json-rpc2._.prototype.pad)
- description and source-code
```javascript
pad = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.padLeft"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>padLeft ()](#apidoc.element.json-rpc2._.prototype.padLeft)
- description and source-code
```javascript
padLeft = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.padRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>padRight ()](#apidoc.element.json-rpc2._.prototype.padRight)
- description and source-code
```javascript
padRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.pairs"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pairs ()](#apidoc.element.json-rpc2._.prototype.pairs)
- description and source-code
```javascript
pairs = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.parseInt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>parseInt ()](#apidoc.element.json-rpc2._.prototype.parseInt)
- description and source-code
```javascript
parseInt = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.partial"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>partial ()](#apidoc.element.json-rpc2._.prototype.partial)
- description and source-code
```javascript
partial = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.partialRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>partialRight ()](#apidoc.element.json-rpc2._.prototype.partialRight)
- description and source-code
```javascript
partialRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.partition"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>partition ()](#apidoc.element.json-rpc2._.prototype.partition)
- description and source-code
```javascript
partition = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.pick"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pick ()](#apidoc.element.json-rpc2._.prototype.pick)
- description and source-code
```javascript
pick = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.plant"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>plant (value)](#apidoc.element.json-rpc2._.prototype.plant)
- description and source-code
```javascript
function wrapperPlant(value) {
  var result,
      parent = this;

  while (parent instanceof baseLodash) {
    var clone = wrapperClone(parent);
    if (result) {
      previous.__wrapped__ = clone;
    } else {
      result = clone;
    }
    var previous = clone;
    parent = parent.__wrapped__;
  }
  previous.__wrapped__ = value;
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.pluck"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pluck ()](#apidoc.element.json-rpc2._.prototype.pluck)
- description and source-code
```javascript
pluck = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.pop"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pop ()](#apidoc.element.json-rpc2._.prototype.pop)
- description and source-code
```javascript
pop = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
...
      },
      _checkAuth: function (req, res) {
        var self = this;

        if (self.authHandler) {
var
  authHeader = req.headers['authorization'] || '', // get the header
  authToken = authHeader.split(/\s+/).pop() || '', // get the token
  auth = new Buffer(authToken, 'base64').toString(), // base64 -> string
  parts = auth.split(/:/), // split on colon
  username = parts[0],
  password = parts[1];

if (!this.authHandler(username, password)) {
  if (res) {
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.property"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>property ()](#apidoc.element.json-rpc2._.prototype.property)
- description and source-code
```javascript
property = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.propertyOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>propertyOf ()](#apidoc.element.json-rpc2._.prototype.propertyOf)
- description and source-code
```javascript
propertyOf = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.pull"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pull ()](#apidoc.element.json-rpc2._.prototype.pull)
- description and source-code
```javascript
pull = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.pullAt"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>pullAt ()](#apidoc.element.json-rpc2._.prototype.pullAt)
- description and source-code
```javascript
pullAt = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.push"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>push ()](#apidoc.element.json-rpc2._.prototype.push)
- description and source-code
```javascript
push = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
...
var funcs = [];

for (var funcName in func) {
  if (Object.prototype.hasOwnProperty.call(func, funcName)) {
    var funcObj = func[funcName];
    if (_.isFunction(funcObj)) {
      this.functions[name + '.' + funcName] = funcObj;
      funcs.push(funcName);

      if (scope) {
        this.scopes[name + '.' + funcName] = scope;
      }
    }
  }
}
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.random"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>random ()](#apidoc.element.json-rpc2._.prototype.random)
- description and source-code
```javascript
random = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.range"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>range ()](#apidoc.element.json-rpc2._.prototype.range)
- description and source-code
```javascript
range = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.rearg"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>rearg ()](#apidoc.element.json-rpc2._.prototype.rearg)
- description and source-code
```javascript
rearg = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.reduce"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reduce ()](#apidoc.element.json-rpc2._.prototype.reduce)
- description and source-code
```javascript
reduce = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.reduceRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reduceRight ()](#apidoc.element.json-rpc2._.prototype.reduceRight)
- description and source-code
```javascript
reduceRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.reject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reject ()](#apidoc.element.json-rpc2._.prototype.reject)
- description and source-code
```javascript
reject = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.remove"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>remove ()](#apidoc.element.json-rpc2._.prototype.remove)
- description and source-code
```javascript
remove = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.repeat"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>repeat ()](#apidoc.element.json-rpc2._.prototype.repeat)
- description and source-code
```javascript
repeat = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.replace"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>replace ()](#apidoc.element.json-rpc2._.prototype.replace)
- description and source-code
```javascript
replace = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.rest"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>rest ()](#apidoc.element.json-rpc2._.prototype.rest)
- description and source-code
```javascript
rest = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.restParam"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>restParam ()](#apidoc.element.json-rpc2._.prototype.restParam)
- description and source-code
```javascript
restParam = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.result"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>result ()](#apidoc.element.json-rpc2._.prototype.result)
- description and source-code
```javascript
result = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.reverse"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>reverse ()](#apidoc.element.json-rpc2._.prototype.reverse)
- description and source-code
```javascript
function wrapperReverse() {
  var value = this.__wrapped__;

  var interceptor = function(value) {
    return (wrapped && wrapped.__dir__ < 0) ? value : value.reverse();
  };
  if (value instanceof LazyWrapper) {
    var wrapped = value;
    if (this.__actions__.length) {
      wrapped = new LazyWrapper(this);
    }
    wrapped = wrapped.reverse();
    wrapped.__actions__.push({ 'func': thru, 'args': [interceptor], 'thisArg': undefined });
    return new LodashWrapper(wrapped, this.__chain__);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.round"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>round ()](#apidoc.element.json-rpc2._.prototype.round)
- description and source-code
```javascript
round = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.run"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>run ()](#apidoc.element.json-rpc2._.prototype.run)
- description and source-code
```javascript
function wrapperValue() {
  return baseWrapperValue(this.__wrapped__, this.__actions__);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.runInContext"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>runInContext ()](#apidoc.element.json-rpc2._.prototype.runInContext)
- description and source-code
```javascript
runInContext = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sample"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sample (n)](#apidoc.element.json-rpc2._.prototype.sample)
- description and source-code
```javascript
sample = function (n) {
  if (!this.__chain__ && n == null) {
    return sample(this.value());
  }
  return this.thru(function(value) {
    return sample(value, n);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.select"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>select ()](#apidoc.element.json-rpc2._.prototype.select)
- description and source-code
```javascript
select = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.set"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>set ()](#apidoc.element.json-rpc2._.prototype.set)
- description and source-code
```javascript
set = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.shift"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>shift ()](#apidoc.element.json-rpc2._.prototype.shift)
- description and source-code
```javascript
shift = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.shuffle"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>shuffle ()](#apidoc.element.json-rpc2._.prototype.shuffle)
- description and source-code
```javascript
shuffle = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.size"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>size ()](#apidoc.element.json-rpc2._.prototype.size)
- description and source-code
```javascript
size = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.slice"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>slice ()](#apidoc.element.json-rpc2._.prototype.slice)
- description and source-code
```javascript
slice = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.snakeCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>snakeCase ()](#apidoc.element.json-rpc2._.prototype.snakeCase)
- description and source-code
```javascript
snakeCase = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.some"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>some ()](#apidoc.element.json-rpc2._.prototype.some)
- description and source-code
```javascript
some = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sort"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sort ()](#apidoc.element.json-rpc2._.prototype.sort)
- description and source-code
```javascript
sort = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sortBy"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortBy ()](#apidoc.element.json-rpc2._.prototype.sortBy)
- description and source-code
```javascript
sortBy = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sortByAll"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortByAll ()](#apidoc.element.json-rpc2._.prototype.sortByAll)
- description and source-code
```javascript
sortByAll = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sortByOrder"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortByOrder ()](#apidoc.element.json-rpc2._.prototype.sortByOrder)
- description and source-code
```javascript
sortByOrder = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sortedIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortedIndex ()](#apidoc.element.json-rpc2._.prototype.sortedIndex)
- description and source-code
```javascript
sortedIndex = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sortedLastIndex"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sortedLastIndex ()](#apidoc.element.json-rpc2._.prototype.sortedLastIndex)
- description and source-code
```javascript
sortedLastIndex = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.splice"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>splice ()](#apidoc.element.json-rpc2._.prototype.splice)
- description and source-code
```javascript
splice = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.split"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>split ()](#apidoc.element.json-rpc2._.prototype.split)
- description and source-code
```javascript
split = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
...
      },
      _checkAuth: function (req, res) {
        var self = this;

        if (self.authHandler) {
var
  authHeader = req.headers['authorization'] || '', // get the header
  authToken = authHeader.split(/\s+/).pop() || '', // get the token
  auth = new Buffer(authToken, 'base64').toString(), // base64 -> string
  parts = auth.split(/:/), // split on colon
  username = parts[0],
  password = parts[1];

if (!this.authHandler(username, password)) {
  if (res) {
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.spread"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>spread ()](#apidoc.element.json-rpc2._.prototype.spread)
- description and source-code
```javascript
spread = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.startCase"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>startCase ()](#apidoc.element.json-rpc2._.prototype.startCase)
- description and source-code
```javascript
startCase = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.startsWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>startsWith ()](#apidoc.element.json-rpc2._.prototype.startsWith)
- description and source-code
```javascript
startsWith = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.sum"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>sum ()](#apidoc.element.json-rpc2._.prototype.sum)
- description and source-code
```javascript
sum = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.tail"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>tail ()](#apidoc.element.json-rpc2._.prototype.tail)
- description and source-code
```javascript
tail = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.take"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>take ()](#apidoc.element.json-rpc2._.prototype.take)
- description and source-code
```javascript
take = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.takeRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>takeRight ()](#apidoc.element.json-rpc2._.prototype.takeRight)
- description and source-code
```javascript
takeRight = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.takeRightWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>takeRightWhile ()](#apidoc.element.json-rpc2._.prototype.takeRightWhile)
- description and source-code
```javascript
takeRightWhile = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.takeWhile"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>takeWhile ()](#apidoc.element.json-rpc2._.prototype.takeWhile)
- description and source-code
```javascript
takeWhile = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.tap"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>tap ()](#apidoc.element.json-rpc2._.prototype.tap)
- description and source-code
```javascript
tap = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.template"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>template ()](#apidoc.element.json-rpc2._.prototype.template)
- description and source-code
```javascript
template = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.throttle"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>throttle ()](#apidoc.element.json-rpc2._.prototype.throttle)
- description and source-code
```javascript
throttle = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.thru"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>thru ()](#apidoc.element.json-rpc2._.prototype.thru)
- description and source-code
```javascript
thru = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.times"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>times ()](#apidoc.element.json-rpc2._.prototype.times)
- description and source-code
```javascript
times = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.toArray"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toArray ()](#apidoc.element.json-rpc2._.prototype.toArray)
- description and source-code
```javascript
toArray = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toJSON ()](#apidoc.element.json-rpc2._.prototype.toJSON)
- description and source-code
```javascript
function wrapperValue() {
  return baseWrapperValue(this.__wrapped__, this.__actions__);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.toPlainObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toPlainObject ()](#apidoc.element.json-rpc2._.prototype.toPlainObject)
- description and source-code
```javascript
toPlainObject = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.toString"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>toString ()](#apidoc.element.json-rpc2._.prototype.toString)
- description and source-code
```javascript
function wrapperToString() {
  return (this.value() + '');
}
```
- example usage
```shell
...
  this.port = port;
  this.host = host;
  this.user = user;
  this.password = password;
},
_authHeader: function(headers){
  if (this.user && this.password) {
    var buff = new Buffer(this.user + ':' + this.password).toString('base64');
    headers['Authorization'] = 'Basic ' + buff;
  }
},
/**
 * Make HTTP connection/request.
 *
 * In HTTP mode, we get to submit exactly one message and receive up to n
...
```

#### <a name="apidoc.element.json-rpc2._.prototype.transform"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>transform ()](#apidoc.element.json-rpc2._.prototype.transform)
- description and source-code
```javascript
transform = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.trim"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trim ()](#apidoc.element.json-rpc2._.prototype.trim)
- description and source-code
```javascript
trim = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.trimLeft"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trimLeft ()](#apidoc.element.json-rpc2._.prototype.trimLeft)
- description and source-code
```javascript
trimLeft = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.trimRight"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trimRight ()](#apidoc.element.json-rpc2._.prototype.trimRight)
- description and source-code
```javascript
trimRight = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.trunc"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>trunc ()](#apidoc.element.json-rpc2._.prototype.trunc)
- description and source-code
```javascript
trunc = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.unescape"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unescape ()](#apidoc.element.json-rpc2._.prototype.unescape)
- description and source-code
```javascript
unescape = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.union"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>union ()](#apidoc.element.json-rpc2._.prototype.union)
- description and source-code
```javascript
union = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.uniq"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>uniq ()](#apidoc.element.json-rpc2._.prototype.uniq)
- description and source-code
```javascript
uniq = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.unique"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unique ()](#apidoc.element.json-rpc2._.prototype.unique)
- description and source-code
```javascript
unique = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.uniqueId"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>uniqueId ()](#apidoc.element.json-rpc2._.prototype.uniqueId)
- description and source-code
```javascript
uniqueId = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.unshift"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unshift ()](#apidoc.element.json-rpc2._.prototype.unshift)
- description and source-code
```javascript
unshift = function () {
  var args = arguments;
  if (retUnwrapped && !this.__chain__) {
    return func.apply(this.value(), args);
  }
  return this[chainName](function(value) {
    return func.apply(value, args);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.unzip"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unzip ()](#apidoc.element.json-rpc2._.prototype.unzip)
- description and source-code
```javascript
unzip = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.unzipWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>unzipWith ()](#apidoc.element.json-rpc2._.prototype.unzipWith)
- description and source-code
```javascript
unzipWith = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.value"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>value ()](#apidoc.element.json-rpc2._.prototype.value)
- description and source-code
```javascript
function wrapperValue() {
  return baseWrapperValue(this.__wrapped__, this.__actions__);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.valueOf"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>valueOf ()](#apidoc.element.json-rpc2._.prototype.valueOf)
- description and source-code
```javascript
function wrapperValue() {
  return baseWrapperValue(this.__wrapped__, this.__actions__);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.values"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>values ()](#apidoc.element.json-rpc2._.prototype.values)
- description and source-code
```javascript
values = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.valuesIn"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>valuesIn ()](#apidoc.element.json-rpc2._.prototype.valuesIn)
- description and source-code
```javascript
valuesIn = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.where"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>where ()](#apidoc.element.json-rpc2._.prototype.where)
- description and source-code
```javascript
where = function () {
  var args = retUnwrapped ? [1] : arguments,
      chainAll = this.__chain__,
      value = this.__wrapped__,
      isHybrid = !!this.__actions__.length,
      isLazy = value instanceof LazyWrapper,
      iteratee = args[0],
      useLazy = isLazy || isArray(value);

  if (useLazy && checkIteratee && typeof iteratee == 'function' && iteratee.length != 1) {
    // Avoid lazy use if the iteratee has a "length" value other than '1'.
    isLazy = useLazy = false;
  }
  var interceptor = function(value) {
    return (retUnwrapped && chainAll)
      ? lodashFunc(value, 1)[0]
      : lodashFunc.apply(undefined, arrayPush([value], args));
  };

  var action = { 'func': thru, 'args': [interceptor], 'thisArg': undefined },
      onlyLazy = isLazy && !isHybrid;

  if (retUnwrapped && !chainAll) {
    if (onlyLazy) {
      value = value.clone();
      value.__actions__.push(action);
      return func.call(value);
    }
    return lodashFunc.call(undefined, this.value())[0];
  }
  if (!retUnwrapped && useLazy) {
    value = onlyLazy ? value : new LazyWrapper(this);
    var result = func.apply(value, args);
    result.__actions__.push(action);
    return new LodashWrapper(result, chainAll);
  }
  return this.thru(interceptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.without"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>without ()](#apidoc.element.json-rpc2._.prototype.without)
- description and source-code
```javascript
without = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.words"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>words ()](#apidoc.element.json-rpc2._.prototype.words)
- description and source-code
```javascript
words = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.wrap"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>wrap ()](#apidoc.element.json-rpc2._.prototype.wrap)
- description and source-code
```javascript
wrap = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.xor"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>xor ()](#apidoc.element.json-rpc2._.prototype.xor)
- description and source-code
```javascript
xor = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.zip"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>zip ()](#apidoc.element.json-rpc2._.prototype.zip)
- description and source-code
```javascript
zip = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.zipObject"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>zipObject ()](#apidoc.element.json-rpc2._.prototype.zipObject)
- description and source-code
```javascript
zipObject = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-rpc2._.prototype.zipWith"></a>[function <span class="apidocSignatureSpan">json-rpc2._.prototype.</span>zipWith ()](#apidoc.element.json-rpc2._.prototype.zipWith)
- description and source-code
```javascript
zipWith = function () {
  var chainAll = this.__chain__;
  if (chain || chainAll) {
    var result = object(this.__wrapped__),
        actions = result.__actions__ = arrayCopy(this.__actions__);

    actions.push({ 'func': func, 'args': arguments, 'thisArg': object });
    result.__chain__ = chainAll;
    return result;
  }
  return func.apply(object, arrayPush([this.value()], arguments));
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
