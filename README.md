# api documentation for  [dispatchr (v1.1.1)](https://github.com/yahoo/fluxible#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-dispatchr.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-dispatchr) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-dispatchr.svg)](https://travis-ci.org/npmdoc/node-npmdoc-dispatchr)
#### A Flux dispatcher for applications that run on the server and the client.

[![NPM](https://nodei.co/npm/dispatchr.png?downloads=true)](https://www.npmjs.com/package/dispatchr)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dispatchr/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-dispatchr_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dispatchr/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-dispatchr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-dispatchr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Michael Ridgway",
        "email": "mridgway@yahoo-inc.com"
    },
    "bugs": {
        "url": "https://github.com/yahoo/fluxible/issues"
    },
    "dependencies": {
        "debug": "^2.0.0",
        "eventemitter3": "^2.0.0",
        "inherits": "^2.0.1"
    },
    "description": "A Flux dispatcher for applications that run on the server and the client.",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "b48373a7d1b0e86d82c8f8b572e3bf8b66a96158",
        "tarball": "https://registry.npmjs.org/dispatchr/-/dispatchr-1.1.1.tgz"
    },
    "homepage": "https://github.com/yahoo/fluxible#readme",
    "keywords": [
        "yahoo",
        "flux",
        "react",
        "dispatcher"
    ],
    "licenses": [
        {
            "type": "BSD-3-Clause",
            "url": "https://github.com/yahoo/fluxible/blob/master/LICENSE.md"
        }
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "mridgway",
            "email": "mcridgway@gmail.com"
        },
        {
            "name": "vijar",
            "email": "r@jiv.me"
        },
        {
            "name": "redonkulus",
            "email": "seth@bertalotto.net"
        },
        {
            "name": "lingyan",
            "email": "lingyan.zhu@gmail.com"
        }
    ],
    "name": "dispatchr",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/yahoo/fluxible.git"
    },
    "scripts": {
        "cover": "../../node_modules/.bin/istanbul cover --dir artifacts -- ../../node_modules/.bin/_mocha tests/unit/ --recursive --compilers js:babel-register --reporter spec",
        "lint": "../../node_modules/.bin/eslint lib/ addons/ utils/ index.js",
        "test": "../../node_modules/.bin/mocha tests/unit/ --recursive --compilers js:babel-register --reporter spec"
    },
    "version": "1.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module dispatchr](#apidoc.module.dispatchr)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>Action (name, payload)](#apidoc.element.dispatchr.Action)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>BaseStore (dispatcher)](#apidoc.element.dispatchr.BaseStore)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>DispatcherContext (dispatcher, context)](#apidoc.element.dispatchr.DispatcherContext)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>createDispatcher (options)](#apidoc.element.dispatchr.createDispatcher)
1.  object <span class="apidocSignatureSpan">dispatchr.</span>Action.prototype
1.  object <span class="apidocSignatureSpan">dispatchr.</span>BaseStore.prototype
1.  object <span class="apidocSignatureSpan">dispatchr.</span>DispatcherContext.prototype

#### [module dispatchr.Action](#apidoc.module.dispatchr.Action)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>Action (name, payload)](#apidoc.element.dispatchr.Action.Action)

#### [module dispatchr.Action.prototype](#apidoc.module.dispatchr.Action.prototype)
1.  [function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>_callHandler (storeName)](#apidoc.element.dispatchr.Action.prototype._callHandler)
1.  [function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>execute (handlers)](#apidoc.element.dispatchr.Action.prototype.execute)
1.  [function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>getStoreName (store)](#apidoc.element.dispatchr.Action.prototype.getStoreName)
1.  [function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>waitFor (stores, callback)](#apidoc.element.dispatchr.Action.prototype.waitFor)

#### [module dispatchr.BaseStore](#apidoc.module.dispatchr.BaseStore)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>BaseStore (dispatcher)](#apidoc.element.dispatchr.BaseStore.BaseStore)
1.  [function <span class="apidocSignatureSpan">dispatchr.BaseStore.</span>super_ ()](#apidoc.element.dispatchr.BaseStore.super_)

#### [module dispatchr.BaseStore.prototype](#apidoc.module.dispatchr.BaseStore.prototype)
1.  [function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>addChangeListener (callback)](#apidoc.element.dispatchr.BaseStore.prototype.addChangeListener)
1.  [function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>emitChange (param)](#apidoc.element.dispatchr.BaseStore.prototype.emitChange)
1.  [function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>getContext ()](#apidoc.element.dispatchr.BaseStore.prototype.getContext)
1.  [function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>removeChangeListener (callback)](#apidoc.element.dispatchr.BaseStore.prototype.removeChangeListener)
1.  [function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>shouldDehydrate ()](#apidoc.element.dispatchr.BaseStore.prototype.shouldDehydrate)

#### [module dispatchr.DispatcherContext](#apidoc.module.dispatchr.DispatcherContext)
1.  [function <span class="apidocSignatureSpan">dispatchr.</span>DispatcherContext (dispatcher, context)](#apidoc.element.dispatchr.DispatcherContext.DispatcherContext)

#### [module dispatchr.DispatcherContext.prototype](#apidoc.module.dispatchr.DispatcherContext.prototype)
1.  [function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>dehydrate ()](#apidoc.element.dispatchr.DispatcherContext.prototype.dehydrate)
1.  [function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>dispatch (actionName, payload)](#apidoc.element.dispatchr.DispatcherContext.prototype.dispatch)
1.  [function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>getStore (name)](#apidoc.element.dispatchr.DispatcherContext.prototype.getStore)
1.  [function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>rehydrate (dispatcherState)](#apidoc.element.dispatchr.DispatcherContext.prototype.rehydrate)
1.  [function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>waitFor (stores, callback)](#apidoc.element.dispatchr.DispatcherContext.prototype.waitFor)



# <a name="apidoc.module.dispatchr"></a>[module dispatchr](#apidoc.module.dispatchr)

#### <a name="apidoc.element.dispatchr.Action"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>Action (name, payload)](#apidoc.element.dispatchr.Action)
- description and source-code
```javascript
function Action(name, payload) {
    this.name = name;
    this.payload = payload;
    this._handlers = null;
    this._isExecuting = false;
    this._isCompleted = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dispatchr.BaseStore"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>BaseStore (dispatcher)](#apidoc.element.dispatchr.BaseStore)
- description and source-code
```javascript
function BaseStore(dispatcher) {
    this.dispatcher = dispatcher;
    this._hasChanged = false;
    EventEmitter.call(this);
    if (this.initialize) {
        this.initialize();
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dispatchr.DispatcherContext"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>DispatcherContext (dispatcher, context)](#apidoc.element.dispatchr.DispatcherContext)
- description and source-code
```javascript
function DispatcherContext(dispatcher, context) {
    this.context = context;
    this.dispatcher = dispatcher;
    this.storeInstances = {};
    this.currentAction = null;
    this.dispatcherInterface = {
        getContext: function getContext() { return context; },
        getStore: this.getStore.bind(this),
        waitFor: this.waitFor.bind(this)
    };
    this.rehydratedStoreState = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dispatchr.createDispatcher"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>createDispatcher (options)](#apidoc.element.dispatchr.createDispatcher)
- description and source-code
```javascript
createDispatcher = function (options) {
    return new Dispatcher(options);
}
```
- example usage
```shell
...

## Usage

For a more detailed example, see our [example applications](../../examples).

'''js
var ExampleStore = require('./stores/ExampleStore.js');
var dispatcher = require('dispatchr').createDispatcher({
    stores: [ExampleStore]
});

var contextOptions = {};
var dispatcherContext = dispatcher.createContext(contextOptions);

dispatcherContext.dispatch('NAVIGATE', {});
...
```



# <a name="apidoc.module.dispatchr.Action"></a>[module dispatchr.Action](#apidoc.module.dispatchr.Action)

#### <a name="apidoc.element.dispatchr.Action.Action"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>Action (name, payload)](#apidoc.element.dispatchr.Action.Action)
- description and source-code
```javascript
function Action(name, payload) {
    this.name = name;
    this.payload = payload;
    this._handlers = null;
    this._isExecuting = false;
    this._isCompleted = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dispatchr.Action.prototype"></a>[module dispatchr.Action.prototype](#apidoc.module.dispatchr.Action.prototype)

#### <a name="apidoc.element.dispatchr.Action.prototype._callHandler"></a>[function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>_callHandler (storeName)](#apidoc.element.dispatchr.Action.prototype._callHandler)
- description and source-code
```javascript
function callHandler(storeName) {
    var self = this,
        handlerFn = self._handlers[storeName];
    if (!handlerFn) {
        throw new Error(storeName + ' does not have a handler for action ' + self.name);
    }
    if (self._isCompleted[storeName]) {
        return;
    }
    self._isCompleted[storeName] = false;
    debug('executing handler for ' + storeName);
    handlerFn(self.payload, self.name);
    self._isCompleted[storeName] = true;
}
```
- example usage
```shell
...
       throw new Error('Action is already dispatched');
   }
   var self = this;
   this._handlers = handlers;
   this._isExecuting = true;
   this._isCompleted = {};
   Object.keys(handlers).forEach(function handlersEach(storeName) {
       self._callHandler(storeName);
   });
};

/**
* Calls an individual store's handler function
* @method _callHandler
* @param {String} storeName
...
```

#### <a name="apidoc.element.dispatchr.Action.prototype.execute"></a>[function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>execute (handlers)](#apidoc.element.dispatchr.Action.prototype.execute)
- description and source-code
```javascript
function execute(handlers) {
    if (this._isExecuting) {
        throw new Error('Action is already dispatched');
    }
    var self = this;
    this._handlers = handlers;
    this._isExecuting = true;
    this._isCompleted = {};
    Object.keys(handlers).forEach(function handlersEach(storeName) {
        self._callHandler(storeName);
    });
}
```
- example usage
```shell
...
                        store: store
                    };
                    return self.dispatcher._throwOrCallErrorHandler(message, 'DISPATCH_INVALID_STORE_METHOD', self.context, meta
);
                }
                handlerFns[store.name] = storeInstance[store.handler].bind(storeInstance);
            }
        });
        this.currentAction.execute(handlerFns);
    } catch (e) {
        throw e;
    } finally {
        debug('finished ' + actionName);
        this.currentAction = null;
    }
};
...
```

#### <a name="apidoc.element.dispatchr.Action.prototype.getStoreName"></a>[function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>getStoreName (store)](#apidoc.element.dispatchr.Action.prototype.getStoreName)
- description and source-code
```javascript
function getStoreName(store) {
    if ('string' === typeof store) {
        return store;
    }
    return store.storeName;
}
```
- example usage
```shell
...
    }
    if (!Array.isArray(stores)) {
        stores = [stores];
    }

    debug('waiting on ' + stores.join(', '));
    stores.forEach(function storesEach(storeName) {
        storeName = self.getStoreName(storeName);
        if (self._handlers[storeName]) {
            self._callHandler(storeName);
        }
    });

    callback();
};
...
```

#### <a name="apidoc.element.dispatchr.Action.prototype.waitFor"></a>[function <span class="apidocSignatureSpan">dispatchr.Action.prototype.</span>waitFor (stores, callback)](#apidoc.element.dispatchr.Action.prototype.waitFor)
- description and source-code
```javascript
function waitFor(stores, callback) {
    var self = this;
    if (!self._isExecuting) {
        throw new Error('waitFor called even though there is no action being executed!');
    }
    if (!Array.isArray(stores)) {
        stores = [stores];
    }

    debug('waiting on ' + stores.join(', '));
    stores.forEach(function storesEach(storeName) {
        storeName = self.getStoreName(storeName);
        if (self._handlers[storeName]) {
            self._callHandler(storeName);
        }
    });

    callback();
}
```
- example usage
```shell
...
    if (!this.currentAction) {
        var message = 'waitFor called even though there is no action dispatching';
        var meta = {
            stores: stores
        };
        return this.dispatcher._throwOrCallErrorHandler(message, 'WAITFOR_NO_ACTION', this.context, meta);
    }
    this.currentAction.waitFor(stores, callback);
};

module.exports = DispatcherContext;
...
```



# <a name="apidoc.module.dispatchr.BaseStore"></a>[module dispatchr.BaseStore](#apidoc.module.dispatchr.BaseStore)

#### <a name="apidoc.element.dispatchr.BaseStore.BaseStore"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>BaseStore (dispatcher)](#apidoc.element.dispatchr.BaseStore.BaseStore)
- description and source-code
```javascript
function BaseStore(dispatcher) {
    this.dispatcher = dispatcher;
    this._hasChanged = false;
    EventEmitter.call(this);
    if (this.initialize) {
        this.initialize();
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dispatchr.BaseStore.super_"></a>[function <span class="apidocSignatureSpan">dispatchr.BaseStore.</span>super_ ()](#apidoc.element.dispatchr.BaseStore.super_)
- description and source-code
```javascript
function EventEmitter() {
  this._events = new Events();
  this._eventsCount = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dispatchr.BaseStore.prototype"></a>[module dispatchr.BaseStore.prototype](#apidoc.module.dispatchr.BaseStore.prototype)

#### <a name="apidoc.element.dispatchr.BaseStore.prototype.addChangeListener"></a>[function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>addChangeListener (callback)](#apidoc.element.dispatchr.BaseStore.prototype.addChangeListener)
- description and source-code
```javascript
function addChangeListener(callback) {
    this.on(CHANGE_EVENT, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dispatchr.BaseStore.prototype.emitChange"></a>[function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>emitChange (param)](#apidoc.element.dispatchr.BaseStore.prototype.emitChange)
- description and source-code
```javascript
function emitChange(param) {
    this._hasChanged = true;
    this.emit(CHANGE_EVENT, param || this);
}
```
- example usage
```shell
...
var BaseStore = require('dispatchr/addons/BaseStore');
var MyStore = function (dispatcherInterface) {
    BaseStore.apply(this, arguments);
};
inherits(MyStore, BaseStore);
MyStore.storeName = 'MyStore';
MyStore.handlers = {
    'NAVIGATE': function (payload) { ... this.emitChange() ... }
};
MyStore.prototype.getFoo = function () { var context = this.getContext(), ... }
module.exports = MyStore;
'''


### createStore
...
```

#### <a name="apidoc.element.dispatchr.BaseStore.prototype.getContext"></a>[function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>getContext ()](#apidoc.element.dispatchr.BaseStore.prototype.getContext)
- description and source-code
```javascript
function getContext() {
    return this.dispatcher.getContext();
}
```
- example usage
```shell
...
    BaseStore.apply(this, arguments);
};
inherits(MyStore, BaseStore);
MyStore.storeName = 'MyStore';
MyStore.handlers = {
    'NAVIGATE': function (payload) { ... this.emitChange() ... }
};
MyStore.prototype.getFoo = function () { var context = this.getContext(), ... }
module.exports = MyStore;
'''


### createStore

'require('dispatchr/addons/createStore')' provides a helper function for
...
```

#### <a name="apidoc.element.dispatchr.BaseStore.prototype.removeChangeListener"></a>[function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>removeChangeListener (callback)](#apidoc.element.dispatchr.BaseStore.prototype.removeChangeListener)
- description and source-code
```javascript
function removeChangeListener(callback) {
    this.removeListener(CHANGE_EVENT, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dispatchr.BaseStore.prototype.shouldDehydrate"></a>[function <span class="apidocSignatureSpan">dispatchr.BaseStore.prototype.</span>shouldDehydrate ()](#apidoc.element.dispatchr.BaseStore.prototype.shouldDehydrate)
- description and source-code
```javascript
function shouldDehydrate() {
    return this._hasChanged;
}
```
- example usage
```shell
...
 * @returns {Object} dehydrated dispatcher data
 */
DispatcherContext.prototype.dehydrate = function dehydrate() {
var self = this,
    stores = {};
Object.keys(self.storeInstances).forEach(function storeInstancesEach(storeName) {
    var store = self.storeInstances[storeName];
    if (!store.dehydrate || (store.shouldDehydrate && !store.shouldDehydrate())) {
        return;
    }
    stores[storeName] = store.dehydrate();
});
return {
    stores: stores
};
...
```



# <a name="apidoc.module.dispatchr.DispatcherContext"></a>[module dispatchr.DispatcherContext](#apidoc.module.dispatchr.DispatcherContext)

#### <a name="apidoc.element.dispatchr.DispatcherContext.DispatcherContext"></a>[function <span class="apidocSignatureSpan">dispatchr.</span>DispatcherContext (dispatcher, context)](#apidoc.element.dispatchr.DispatcherContext.DispatcherContext)
- description and source-code
```javascript
function DispatcherContext(dispatcher, context) {
    this.context = context;
    this.dispatcher = dispatcher;
    this.storeInstances = {};
    this.currentAction = null;
    this.dispatcherInterface = {
        getContext: function getContext() { return context; },
        getStore: this.getStore.bind(this),
        waitFor: this.waitFor.bind(this)
    };
    this.rehydratedStoreState = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.dispatchr.DispatcherContext.prototype"></a>[module dispatchr.DispatcherContext.prototype](#apidoc.module.dispatchr.DispatcherContext.prototype)

#### <a name="apidoc.element.dispatchr.DispatcherContext.prototype.dehydrate"></a>[function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>dehydrate ()](#apidoc.element.dispatchr.DispatcherContext.prototype.dehydrate)
- description and source-code
```javascript
function dehydrate() {
    var self = this,
        stores = {};
    Object.keys(self.storeInstances).forEach(function storeInstancesEach(storeName) {
        var store = self.storeInstances[storeName];
        if (!store.dehydrate || (store.shouldDehydrate && !store.shouldDehydrate())) {
            return;
        }
        stores[storeName] = store.dehydrate();
    });
    return {
        stores: stores
    };
}
```
- example usage
```shell
...
    var self = this,
        stores = {};
    Object.keys(self.storeInstances).forEach(function storeInstancesEach(storeName) {
        var store = self.storeInstances[storeName];
        if (!store.dehydrate || (store.shouldDehydrate && !store.shouldDehydrate())) {
            return;
        }
        stores[storeName] = store.dehydrate();
    });
    return {
        stores: stores
    };
};

/**
...
```

#### <a name="apidoc.element.dispatchr.DispatcherContext.prototype.dispatch"></a>[function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>dispatch (actionName, payload)](#apidoc.element.dispatchr.DispatcherContext.prototype.dispatch)
- description and source-code
```javascript
function dispatch(actionName, payload) {
    if (!actionName) {
        var message = 'actionName parameter '' + actionName + '' is invalid.';
        return this.dispatcher._throwOrCallErrorHandler(message, 'DISPATCH_INVALID_ACTIONNAME', this.context);
    }
    if (this.currentAction) {
        var message = 'Cannot call dispatch while another dispatch is executing. Attempted to execute \'' + actionName + '\' but\'' + this.currentAction.name + '\' is already executing.';
        var meta = {
            actionName: actionName,
            payload: payload
        };
        return this.dispatcher._throwOrCallErrorHandler(message, 'DISPATCH_EXECUTING', this.context, meta);
    }
    var actionHandlers = this.dispatcher.handlers[actionName] || [],
        defaultHandlers = this.dispatcher.handlers[DEFAULT] || [];
    if (!actionHandlers.length && !defaultHandlers.length) {
        debug(actionName + ' does not have any registered handlers');
        return;
    }
    debug('dispatching ' + actionName, payload);
    this.currentAction = new Action(actionName, payload);
    var self = this,
        allHandlers = actionHandlers.concat(defaultHandlers),
        handlerFns = {};

    try {
        allHandlers.forEach(function actionHandlersEach(store) {
            if (handlerFns[store.name]) {
                // Don't call the default if the store has an explicit action handler
                return;
            }
            var storeInstance = self.getStore(store.name);
            if ('function' === typeof store.handler) {
                handlerFns[store.name] = store.handler.bind(storeInstance);
            } else {
                if (!storeInstance[store.handler]) {
                    var message = store.name + ' does not have a method called ' + store.handler;
                    var meta = {
                        store: store
                    };
                    return self.dispatcher._throwOrCallErrorHandler(message, 'DISPATCH_INVALID_STORE_METHOD', self.context, meta
);
                }
                handlerFns[store.name] = storeInstance[store.handler].bind(storeInstance);
            }
        });
        this.currentAction.execute(handlerFns);
    } catch (e) {
        throw e;
    } finally {
        debug('finished ' + actionName);
        this.currentAction = null;
    }
}
```
- example usage
```shell
...
var dispatcher = require('dispatchr').createDispatcher({
    stores: [ExampleStore]
});

var contextOptions = {};
var dispatcherContext = dispatcher.createContext(contextOptions);

dispatcherContext.dispatch('NAVIGATE', {});
// Action has been handled fully
'''

## Differences from [Facebook's Flux Dispatcher](https://github.com/facebook/flux/blob/master/src/Dispatcher.js)

Dispatchr's main goal is to facilitate server-side rendering of Flux
applications while also working on the client-side to encourage code reuse. In
...
```

#### <a name="apidoc.element.dispatchr.DispatcherContext.prototype.getStore"></a>[function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>getStore (name)](#apidoc.element.dispatchr.DispatcherContext.prototype.getStore)
- description and source-code
```javascript
function getStore(name) {
    var storeName = this.dispatcher.getStoreName(name);
    if (!this.storeInstances[storeName]) {
        var Store = this.dispatcher.stores[storeName];
        if (!Store) {
            var message = 'Store ' + storeName + ' was not registered.';
            var meta = {
                storeName: storeName
            };
            return this.dispatcher._throwOrCallErrorHandler(message, 'STORE_UNREGISTERED', this.context, meta);
        }
        this.storeInstances[storeName] = new (this.dispatcher.stores[storeName])(this.dispatcherInterface);
        if (this.rehydratedStoreState && this.rehydratedStoreState[storeName]) {
            var state = this.rehydratedStoreState[storeName];
            if (this.storeInstances[storeName].rehydrate) {
                this.storeInstances[storeName].rehydrate(state);
            }
            this.rehydratedStoreState[storeName] = null;
        }
    }
    return this.storeInstances[storeName];
}
```
- example usage
```shell
...

    try {
allHandlers.forEach(function actionHandlersEach(store) {
    if (handlerFns[store.name]) {
        // Don't call the default if the store has an explicit action handler
        return;
    }
    var storeInstance = self.getStore(store.name);
    if ('function' === typeof store.handler) {
        handlerFns[store.name] = store.handler.bind(storeInstance);
    } else {
        if (!storeInstance[store.handler]) {
            var message = store.name + ' does not have a method called ' + store.handler;
            var meta = {
                store: store
...
```

#### <a name="apidoc.element.dispatchr.DispatcherContext.prototype.rehydrate"></a>[function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>rehydrate (dispatcherState)](#apidoc.element.dispatchr.DispatcherContext.prototype.rehydrate)
- description and source-code
```javascript
function rehydrate(dispatcherState) {
    var self = this;
    if (dispatcherState.stores) {
        Object.keys(dispatcherState.stores).forEach(function storeStateEach(storeName) {
            self.rehydratedStoreState[storeName] = dispatcherState.stores[storeName];
        });
    }
}
```
- example usage
```shell
...
            };
            return this.dispatcher._throwOrCallErrorHandler(message, 'STORE_UNREGISTERED', this.context, meta);
        }
        this.storeInstances[storeName] = new (this.dispatcher.stores[storeName])(this.dispatcherInterface);
        if (this.rehydratedStoreState && this.rehydratedStoreState[storeName]) {
            var state = this.rehydratedStoreState[storeName];
            if (this.storeInstances[storeName].rehydrate) {
                this.storeInstances[storeName].rehydrate(state);
            }
            this.rehydratedStoreState[storeName] = null;
        }
    }
    return this.storeInstances[storeName];
};
...
```

#### <a name="apidoc.element.dispatchr.DispatcherContext.prototype.waitFor"></a>[function <span class="apidocSignatureSpan">dispatchr.DispatcherContext.prototype.</span>waitFor (stores, callback)](#apidoc.element.dispatchr.DispatcherContext.prototype.waitFor)
- description and source-code
```javascript
function waitFor(stores, callback) {
    if (!this.currentAction) {
        var message = 'waitFor called even though there is no action dispatching';
        var meta = {
            stores: stores
        };
        return this.dispatcher._throwOrCallErrorHandler(message, 'WAITFOR_NO_ACTION', this.context, meta);
    }
    this.currentAction.waitFor(stores, callback);
}
```
- example usage
```shell
...
    if (!this.currentAction) {
        var message = 'waitFor called even though there is no action dispatching';
        var meta = {
            stores: stores
        };
        return this.dispatcher._throwOrCallErrorHandler(message, 'WAITFOR_NO_ACTION', this.context, meta);
    }
    this.currentAction.waitFor(stores, callback);
};

module.exports = DispatcherContext;
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
