# api documentation for  [backoff (v2.5.0)](https://github.com/MathieuTurcotte/node-backoff#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-backoff.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-backoff) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-backoff.svg)](https://travis-ci.org/npmdoc/node-npmdoc-backoff)
#### Fibonacci and exponential backoffs.

[![NPM](https://nodei.co/npm/backoff.png?downloads=true)](https://www.npmjs.com/package/backoff)

[![apidoc](https://npmdoc.github.io/node-npmdoc-backoff/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-backoff_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-backoff/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-backoff/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-backoff/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mathieu Turcotte",
        "email": "turcotte.mat@gmail.com"
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
            "name": "mathieu",
            "email": "turcotte.mat@gmail.com"
        }
    ],
    "name": "backoff",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/MathieuTurcotte/node-backoff.git"
    },
    "scripts": {
        "docco": "docco lib/*.js lib/strategy/* index.js",
        "pretest": "jshint lib/ tests/ examples/ index.js",
        "test": "node_modules/nodeunit/bin/nodeunit tests/"
    },
    "version": "2.5.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module backoff](#apidoc.module.backoff)
1.  [function <span class="apidocSignatureSpan">backoff.</span>Backoff (backoffStrategy)](#apidoc.element.backoff.Backoff)
1.  [function <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy (options)](#apidoc.element.backoff.ExponentialStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy.super_ (options)](#apidoc.element.backoff.ExponentialStrategy.super_)
1.  [function <span class="apidocSignatureSpan">backoff.</span>FibonacciStrategy (options)](#apidoc.element.backoff.FibonacciStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.</span>FunctionCall (fn, args, callback)](#apidoc.element.backoff.FunctionCall)
1.  [function <span class="apidocSignatureSpan">backoff.</span>call (fn, vargs, callback)](#apidoc.element.backoff.call)
1.  [function <span class="apidocSignatureSpan">backoff.</span>exponential (options)](#apidoc.element.backoff.exponential)
1.  [function <span class="apidocSignatureSpan">backoff.</span>fibonacci (options)](#apidoc.element.backoff.fibonacci)
1.  object <span class="apidocSignatureSpan">backoff.</span>Backoff.prototype
1.  object <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy.prototype
1.  object <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy.super_.prototype
1.  object <span class="apidocSignatureSpan">backoff.</span>FibonacciStrategy.prototype
1.  object <span class="apidocSignatureSpan">backoff.</span>FunctionCall.prototype

#### [module backoff.Backoff](#apidoc.module.backoff.Backoff)
1.  [function <span class="apidocSignatureSpan">backoff.</span>Backoff (backoffStrategy)](#apidoc.element.backoff.Backoff.Backoff)
1.  [function <span class="apidocSignatureSpan">backoff.Backoff.</span>super_ ()](#apidoc.element.backoff.Backoff.super_)

#### [module backoff.Backoff.prototype](#apidoc.module.backoff.Backoff.prototype)
1.  [function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>backoff (err)](#apidoc.element.backoff.Backoff.prototype.backoff)
1.  [function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>failAfter (maxNumberOfRetry)](#apidoc.element.backoff.Backoff.prototype.failAfter)
1.  [function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>onBackoff_ ()](#apidoc.element.backoff.Backoff.prototype.onBackoff_)
1.  [function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>reset ()](#apidoc.element.backoff.Backoff.prototype.reset)

#### [module backoff.ExponentialStrategy](#apidoc.module.backoff.ExponentialStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy (options)](#apidoc.element.backoff.ExponentialStrategy.ExponentialStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.</span>super_ (options)](#apidoc.element.backoff.ExponentialStrategy.super_)
1.  number <span class="apidocSignatureSpan">backoff.ExponentialStrategy.</span>DEFAULT_FACTOR

#### [module backoff.ExponentialStrategy.prototype](#apidoc.module.backoff.ExponentialStrategy.prototype)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.prototype.</span>next_ ()](#apidoc.element.backoff.ExponentialStrategy.prototype.next_)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.prototype.</span>reset_ ()](#apidoc.element.backoff.ExponentialStrategy.prototype.reset_)

#### [module backoff.ExponentialStrategy.super_](#apidoc.module.backoff.ExponentialStrategy.super_)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.</span>super_ (options)](#apidoc.element.backoff.ExponentialStrategy.super_.super_)

#### [module backoff.ExponentialStrategy.super_.prototype](#apidoc.module.backoff.ExponentialStrategy.super_.prototype)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>getInitialDelay ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.getInitialDelay)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>getMaxDelay ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.getMaxDelay)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>next ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.next)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>next_ ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.next_)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>reset ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.reset)
1.  [function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>reset_ ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.reset_)

#### [module backoff.FibonacciStrategy](#apidoc.module.backoff.FibonacciStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.</span>FibonacciStrategy (options)](#apidoc.element.backoff.FibonacciStrategy.FibonacciStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.FibonacciStrategy.</span>super_ (options)](#apidoc.element.backoff.FibonacciStrategy.super_)

#### [module backoff.FibonacciStrategy.prototype](#apidoc.module.backoff.FibonacciStrategy.prototype)
1.  [function <span class="apidocSignatureSpan">backoff.FibonacciStrategy.prototype.</span>next_ ()](#apidoc.element.backoff.FibonacciStrategy.prototype.next_)
1.  [function <span class="apidocSignatureSpan">backoff.FibonacciStrategy.prototype.</span>reset_ ()](#apidoc.element.backoff.FibonacciStrategy.prototype.reset_)

#### [module backoff.FunctionCall](#apidoc.module.backoff.FunctionCall)
1.  [function <span class="apidocSignatureSpan">backoff.</span>FunctionCall (fn, args, callback)](#apidoc.element.backoff.FunctionCall.FunctionCall)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.</span>DEFAULT_RETRY_PREDICATE_ (err)](#apidoc.element.backoff.FunctionCall.DEFAULT_RETRY_PREDICATE_)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.</span>super_ ()](#apidoc.element.backoff.FunctionCall.super_)
1.  object <span class="apidocSignatureSpan">backoff.FunctionCall.</span>State_

#### [module backoff.FunctionCall.prototype](#apidoc.module.backoff.FunctionCall.prototype)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>abort ()](#apidoc.element.backoff.FunctionCall.prototype.abort)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>doCall_ (isRetry)](#apidoc.element.backoff.FunctionCall.prototype.doCall_)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>doCallback_ ()](#apidoc.element.backoff.FunctionCall.prototype.doCallback_)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>failAfter (maxNumberOfRetry)](#apidoc.element.backoff.FunctionCall.prototype.failAfter)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>getLastResult ()](#apidoc.element.backoff.FunctionCall.prototype.getLastResult)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>getNumRetries ()](#apidoc.element.backoff.FunctionCall.prototype.getNumRetries)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>handleBackoff_ (number, delay, err)](#apidoc.element.backoff.FunctionCall.prototype.handleBackoff_)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>handleFunctionCallback_ ()](#apidoc.element.backoff.FunctionCall.prototype.handleFunctionCallback_)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isAborted ()](#apidoc.element.backoff.FunctionCall.prototype.isAborted)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isCompleted ()](#apidoc.element.backoff.FunctionCall.prototype.isCompleted)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isPending ()](#apidoc.element.backoff.FunctionCall.prototype.isPending)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isRunning ()](#apidoc.element.backoff.FunctionCall.prototype.isRunning)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>retryIf (retryPredicate)](#apidoc.element.backoff.FunctionCall.prototype.retryIf)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>setStrategy (strategy)](#apidoc.element.backoff.FunctionCall.prototype.setStrategy)
1.  [function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>start (backoffFactory)](#apidoc.element.backoff.FunctionCall.prototype.start)



# <a name="apidoc.module.backoff"></a>[module backoff](#apidoc.module.backoff)

#### <a name="apidoc.element.backoff.Backoff"></a>[function <span class="apidocSignatureSpan">backoff.</span>Backoff (backoffStrategy)](#apidoc.element.backoff.Backoff)
- description and source-code
```javascript
function Backoff(backoffStrategy) {
    events.EventEmitter.call(this);

    this.backoffStrategy_ = backoffStrategy;
    this.maxNumberOfRetry_ = -1;
    this.backoffNumber_ = 0;
    this.backoffDelay_ = 0;
    this.timeoutID_ = -1;

    this.handlers = {
        backoff: this.onBackoff_.bind(this)
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.ExponentialStrategy"></a>[function <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy (options)](#apidoc.element.backoff.ExponentialStrategy)
- description and source-code
```javascript
function ExponentialBackoffStrategy(options) {
    BackoffStrategy.call(this, options);
    this.backoffDelay_ = 0;
    this.nextBackoffDelay_ = this.getInitialDelay();
    this.factor_ = ExponentialBackoffStrategy.DEFAULT_FACTOR;

    if (options && options.factor !== undefined) {
        precond.checkArgument(options.factor > 1,
            'Exponential factor should be greater than 1 but got %s.',
            options.factor);
        this.factor_ = options.factor;
    }
}
```
- example usage
```shell
...
        console.log('Error: ' + err.message);
    } else {
        console.log('Status: ' + res.statusCode);
    }
});

call.retryIf(function(err) { return err.status == 503; });
call.setStrategy(new backoff.ExponentialStrategy());
call.failAfter(10);
call.start();
'''

## API

### backoff.fibonacci([options])
...
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_"></a>[function <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy.super_ (options)](#apidoc.element.backoff.ExponentialStrategy.super_)
- description and source-code
```javascript
function BackoffStrategy(options) {
    options = options || {};

    if (isDef(options.initialDelay) && options.initialDelay < 1) {
        throw new Error('The initial timeout must be greater than 0.');
    } else if (isDef(options.maxDelay) && options.maxDelay < 1) {
        throw new Error('The maximal timeout must be greater than 0.');
    }

    this.initialDelay_ = options.initialDelay || 100;
    this.maxDelay_ = options.maxDelay || 10000;

    if (this.maxDelay_ <= this.initialDelay_) {
        throw new Error('The maximal backoff delay must be ' +
                        'greater than the initial backoff delay.');
    }

    if (isDef(options.randomisationFactor) &&
        (options.randomisationFactor < 0 || options.randomisationFactor > 1)) {
        throw new Error('The randomisation factor must be between 0 and 1.');
    }

    this.randomisationFactor_ = options.randomisationFactor || 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FibonacciStrategy"></a>[function <span class="apidocSignatureSpan">backoff.</span>FibonacciStrategy (options)](#apidoc.element.backoff.FibonacciStrategy)
- description and source-code
```javascript
function FibonacciBackoffStrategy(options) {
    BackoffStrategy.call(this, options);
    this.backoffDelay_ = 0;
    this.nextBackoffDelay_ = this.getInitialDelay();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall"></a>[function <span class="apidocSignatureSpan">backoff.</span>FunctionCall (fn, args, callback)](#apidoc.element.backoff.FunctionCall)
- description and source-code
```javascript
function FunctionCall(fn, args, callback) {
    events.EventEmitter.call(this);

    precond.checkIsFunction(fn, 'Expected fn to be a function.');
    precond.checkIsArray(args, 'Expected args to be an array.');
    precond.checkIsFunction(callback, 'Expected callback to be a function.');

    this.function_ = fn;
    this.arguments_ = args;
    this.callback_ = callback;
    this.lastResult_ = [];
    this.numRetries_ = 0;

    this.backoff_ = null;
    this.strategy_ = null;
    this.failAfter_ = -1;
    this.retryPredicate_ = FunctionCall.DEFAULT_RETRY_PREDICATE_;

    this.state_ = FunctionCall.State_.PENDING;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.call"></a>[function <span class="apidocSignatureSpan">backoff.</span>call (fn, vargs, callback)](#apidoc.element.backoff.call)
- description and source-code
```javascript
call = function (fn, vargs, callback) {
    var args = Array.prototype.slice.call(arguments);
    fn = args[0];
    vargs = args.slice(1, args.length - 1);
    callback = args[args.length - 1];
    return new FunctionCall(fn, vargs, callback);
}
```
- example usage
```shell
...

Note that 'Backoff' objects are meant to be instantiated once and reused
several times by calling 'reset' after a successful "retry".

### Functional

It's also possible to avoid some boilerplate code when invoking an asynchronous
function in a backoff loop by using 'backoff.call(fn, [args, ...], callback)'.

Typical usage looks like the following.

''' js
var call = backoff.call(get, 'https://duplika.ca/', function(err, res) {
console.log('Num retries: ' + call.getNumRetries());
...
```

#### <a name="apidoc.element.backoff.exponential"></a>[function <span class="apidocSignatureSpan">backoff.</span>exponential (options)](#apidoc.element.backoff.exponential)
- description and source-code
```javascript
exponential = function (options) {
    return new Backoff(new ExponentialBackoffStrategy(options));
}
```
- example usage
```shell
...
'''

## Usage

### Object Oriented

The usual way to instantiate a new 'Backoff' object is to use one predefined
factory method: 'backoff.fibonacci([options])', 'backoff.exponential([options])'.

'Backoff' inherits from 'EventEmitter'. When a backoff starts, a 'backoff'
event is emitted and, when a backoff ends, a 'ready' event is emitted.
Handlers for these two events are called with the current backoff number and
delay.

''' js
...
```

#### <a name="apidoc.element.backoff.fibonacci"></a>[function <span class="apidocSignatureSpan">backoff.</span>fibonacci (options)](#apidoc.element.backoff.fibonacci)
- description and source-code
```javascript
fibonacci = function (options) {
    return new Backoff(new FibonacciBackoffStrategy(options));
}
```
- example usage
```shell
...
'''

## Usage

### Object Oriented

The usual way to instantiate a new 'Backoff' object is to use one predefined
factory method: 'backoff.fibonacci([options])', 'backoff.exponential([options])'.

'Backoff' inherits from 'EventEmitter'. When a backoff starts, a 'backoff'
event is emitted and, when a backoff ends, a 'ready' event is emitted.
Handlers for these two events are called with the current backoff number and
delay.

''' js
...
```



# <a name="apidoc.module.backoff.Backoff"></a>[module backoff.Backoff](#apidoc.module.backoff.Backoff)

#### <a name="apidoc.element.backoff.Backoff.Backoff"></a>[function <span class="apidocSignatureSpan">backoff.</span>Backoff (backoffStrategy)](#apidoc.element.backoff.Backoff.Backoff)
- description and source-code
```javascript
function Backoff(backoffStrategy) {
    events.EventEmitter.call(this);

    this.backoffStrategy_ = backoffStrategy;
    this.maxNumberOfRetry_ = -1;
    this.backoffNumber_ = 0;
    this.backoffDelay_ = 0;
    this.timeoutID_ = -1;

    this.handlers = {
        backoff: this.onBackoff_.bind(this)
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.Backoff.super_"></a>[function <span class="apidocSignatureSpan">backoff.Backoff.</span>super_ ()](#apidoc.element.backoff.Backoff.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.Backoff.prototype"></a>[module backoff.Backoff.prototype](#apidoc.module.backoff.Backoff.prototype)

#### <a name="apidoc.element.backoff.Backoff.prototype.backoff"></a>[function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>backoff (err)](#apidoc.element.backoff.Backoff.prototype.backoff)
- description and source-code
```javascript
backoff = function (err) {
    precond.checkState(this.timeoutID_ === -1, 'Backoff in progress.');

    if (this.backoffNumber_ === this.maxNumberOfRetry_) {
        this.emit('fail', err);
        this.reset();
    } else {
        this.backoffDelay_ = this.backoffStrategy_.next();
        this.timeoutID_ = setTimeout(this.handlers.backoff, this.backoffDelay_);
        this.emit('backoff', this.backoffNumber_, this.backoffDelay_, err);
    }
}
```
- example usage
```shell
...
});

fibonacciBackoff.on('ready', function(number, delay) {
    // Do something when backoff ends, e.g. retry a failed
    // operation (DNS lookup, API call, etc.). If it fails
    // again then backoff, otherwise reset the backoff
    // instance.
    fibonacciBackoff.backoff();
});

fibonacciBackoff.on('fail', function() {
    // Do something when the maximum number of backoffs is
    // reached, e.g. ask the user to check its connection.
    console.log('fail');
});
...
```

#### <a name="apidoc.element.backoff.Backoff.prototype.failAfter"></a>[function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>failAfter (maxNumberOfRetry)](#apidoc.element.backoff.Backoff.prototype.failAfter)
- description and source-code
```javascript
failAfter = function (maxNumberOfRetry) {
    precond.checkArgument(maxNumberOfRetry > 0,
        'Expected a maximum number of retry greater than 0 but got %s.',
        maxNumberOfRetry);

    this.maxNumberOfRetry_ = maxNumberOfRetry;
}
```
- example usage
```shell
...

var fibonacciBackoff = backoff.fibonacci({
    randomisationFactor: 0,
    initialDelay: 10,
    maxDelay: 300
});

fibonacciBackoff.failAfter(10);

fibonacciBackoff.on('backoff', function(number, delay) {
    // Do something when backoff starts, e.g. show to the
    // user the delay before next reconnection attempt.
    console.log(number + ' ' + delay + 'ms');
});
...
```

#### <a name="apidoc.element.backoff.Backoff.prototype.onBackoff_"></a>[function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>onBackoff_ ()](#apidoc.element.backoff.Backoff.prototype.onBackoff_)
- description and source-code
```javascript
onBackoff_ = function () {
    this.timeoutID_ = -1;
    this.emit('ready', this.backoffNumber_, this.backoffDelay_);
    this.backoffNumber_++;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.Backoff.prototype.reset"></a>[function <span class="apidocSignatureSpan">backoff.Backoff.prototype.</span>reset ()](#apidoc.element.backoff.Backoff.prototype.reset)
- description and source-code
```javascript
reset = function () {
    this.backoffNumber_ = 0;
    this.backoffStrategy_.reset();
    clearTimeout(this.timeoutID_);
    this.timeoutID_ = -1;
}
```
- example usage
```shell
...

An error will be thrown if a backoff operation is already in progress.

In practice, this method should be called after a failed attempt to perform a
sensitive operation (connecting to a database, downloading a resource over the
network, etc.).

#### backoff.reset()

Resets the backoff delay to the initial backoff delay and stop any backoff
operation in progress. After reset, a backoff instance can and should be
reused.

In practice, this method should be called after having successfully completed
the sensitive operation guarded by the backoff instance or if the client code
...
```



# <a name="apidoc.module.backoff.ExponentialStrategy"></a>[module backoff.ExponentialStrategy](#apidoc.module.backoff.ExponentialStrategy)

#### <a name="apidoc.element.backoff.ExponentialStrategy.ExponentialStrategy"></a>[function <span class="apidocSignatureSpan">backoff.</span>ExponentialStrategy (options)](#apidoc.element.backoff.ExponentialStrategy.ExponentialStrategy)
- description and source-code
```javascript
function ExponentialBackoffStrategy(options) {
    BackoffStrategy.call(this, options);
    this.backoffDelay_ = 0;
    this.nextBackoffDelay_ = this.getInitialDelay();
    this.factor_ = ExponentialBackoffStrategy.DEFAULT_FACTOR;

    if (options && options.factor !== undefined) {
        precond.checkArgument(options.factor > 1,
            'Exponential factor should be greater than 1 but got %s.',
            options.factor);
        this.factor_ = options.factor;
    }
}
```
- example usage
```shell
...
        console.log('Error: ' + err.message);
    } else {
        console.log('Status: ' + res.statusCode);
    }
});

call.retryIf(function(err) { return err.status == 503; });
call.setStrategy(new backoff.ExponentialStrategy());
call.failAfter(10);
call.start();
'''

## API

### backoff.fibonacci([options])
...
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.</span>super_ (options)](#apidoc.element.backoff.ExponentialStrategy.super_)
- description and source-code
```javascript
function BackoffStrategy(options) {
    options = options || {};

    if (isDef(options.initialDelay) && options.initialDelay < 1) {
        throw new Error('The initial timeout must be greater than 0.');
    } else if (isDef(options.maxDelay) && options.maxDelay < 1) {
        throw new Error('The maximal timeout must be greater than 0.');
    }

    this.initialDelay_ = options.initialDelay || 100;
    this.maxDelay_ = options.maxDelay || 10000;

    if (this.maxDelay_ <= this.initialDelay_) {
        throw new Error('The maximal backoff delay must be ' +
                        'greater than the initial backoff delay.');
    }

    if (isDef(options.randomisationFactor) &&
        (options.randomisationFactor < 0 || options.randomisationFactor > 1)) {
        throw new Error('The randomisation factor must be between 0 and 1.');
    }

    this.randomisationFactor_ = options.randomisationFactor || 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.ExponentialStrategy.prototype"></a>[module backoff.ExponentialStrategy.prototype](#apidoc.module.backoff.ExponentialStrategy.prototype)

#### <a name="apidoc.element.backoff.ExponentialStrategy.prototype.next_"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.prototype.</span>next_ ()](#apidoc.element.backoff.ExponentialStrategy.prototype.next_)
- description and source-code
```javascript
next_ = function () {
    this.backoffDelay_ = Math.min(this.nextBackoffDelay_, this.getMaxDelay());
    this.nextBackoffDelay_ = this.backoffDelay_ * this.factor_;
    return this.backoffDelay_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.prototype.reset_"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.prototype.</span>reset_ ()](#apidoc.element.backoff.ExponentialStrategy.prototype.reset_)
- description and source-code
```javascript
reset_ = function () {
    this.backoffDelay_ = 0;
    this.nextBackoffDelay_ = this.getInitialDelay();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.ExponentialStrategy.super_"></a>[module backoff.ExponentialStrategy.super_](#apidoc.module.backoff.ExponentialStrategy.super_)

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.super_"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.</span>super_ (options)](#apidoc.element.backoff.ExponentialStrategy.super_.super_)
- description and source-code
```javascript
function BackoffStrategy(options) {
    options = options || {};

    if (isDef(options.initialDelay) && options.initialDelay < 1) {
        throw new Error('The initial timeout must be greater than 0.');
    } else if (isDef(options.maxDelay) && options.maxDelay < 1) {
        throw new Error('The maximal timeout must be greater than 0.');
    }

    this.initialDelay_ = options.initialDelay || 100;
    this.maxDelay_ = options.maxDelay || 10000;

    if (this.maxDelay_ <= this.initialDelay_) {
        throw new Error('The maximal backoff delay must be ' +
                        'greater than the initial backoff delay.');
    }

    if (isDef(options.randomisationFactor) &&
        (options.randomisationFactor < 0 || options.randomisationFactor > 1)) {
        throw new Error('The randomisation factor must be between 0 and 1.');
    }

    this.randomisationFactor_ = options.randomisationFactor || 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.ExponentialStrategy.super_.prototype"></a>[module backoff.ExponentialStrategy.super_.prototype](#apidoc.module.backoff.ExponentialStrategy.super_.prototype)

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.prototype.getInitialDelay"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>getInitialDelay ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.getInitialDelay)
- description and source-code
```javascript
getInitialDelay = function () {
    return this.initialDelay_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.prototype.getMaxDelay"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>getMaxDelay ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.getMaxDelay)
- description and source-code
```javascript
getMaxDelay = function () {
    return this.maxDelay_;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.prototype.next"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>next ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.next)
- description and source-code
```javascript
next = function () {
    var backoffDelay = this.next_();
    var randomisationMultiple = 1 + Math.random() * this.randomisationFactor_;
    var randomizedDelay = Math.round(backoffDelay * randomisationMultiple);
    return randomizedDelay;
}
```
- example usage
```shell
...
'backoff.failAfter(numberOfBackoffs)'. The backoff instance is automatically
reset after this event is emitted.

### Interface BackoffStrategy

A backoff strategy must provide the following methods.

#### strategy.next()

Computes and returns the next backoff delay.

#### strategy.reset()

Resets the backoff delay to its initial value.
...
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.prototype.next_"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>next_ ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.next_)
- description and source-code
```javascript
next_ = function () {
    throw new Error('BackoffStrategy.next_() unimplemented.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.prototype.reset"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>reset ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.reset)
- description and source-code
```javascript
reset = function () {
    this.reset_();
}
```
- example usage
```shell
...

An error will be thrown if a backoff operation is already in progress.

In practice, this method should be called after a failed attempt to perform a
sensitive operation (connecting to a database, downloading a resource over the
network, etc.).

#### backoff.reset()

Resets the backoff delay to the initial backoff delay and stop any backoff
operation in progress. After reset, a backoff instance can and should be
reused.

In practice, this method should be called after having successfully completed
the sensitive operation guarded by the backoff instance or if the client code
...
```

#### <a name="apidoc.element.backoff.ExponentialStrategy.super_.prototype.reset_"></a>[function <span class="apidocSignatureSpan">backoff.ExponentialStrategy.super_.prototype.</span>reset_ ()](#apidoc.element.backoff.ExponentialStrategy.super_.prototype.reset_)
- description and source-code
```javascript
reset_ = function () {
    throw new Error('BackoffStrategy.reset_() unimplemented.');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.FibonacciStrategy"></a>[module backoff.FibonacciStrategy](#apidoc.module.backoff.FibonacciStrategy)

#### <a name="apidoc.element.backoff.FibonacciStrategy.FibonacciStrategy"></a>[function <span class="apidocSignatureSpan">backoff.</span>FibonacciStrategy (options)](#apidoc.element.backoff.FibonacciStrategy.FibonacciStrategy)
- description and source-code
```javascript
function FibonacciBackoffStrategy(options) {
    BackoffStrategy.call(this, options);
    this.backoffDelay_ = 0;
    this.nextBackoffDelay_ = this.getInitialDelay();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FibonacciStrategy.super_"></a>[function <span class="apidocSignatureSpan">backoff.FibonacciStrategy.</span>super_ (options)](#apidoc.element.backoff.FibonacciStrategy.super_)
- description and source-code
```javascript
function BackoffStrategy(options) {
    options = options || {};

    if (isDef(options.initialDelay) && options.initialDelay < 1) {
        throw new Error('The initial timeout must be greater than 0.');
    } else if (isDef(options.maxDelay) && options.maxDelay < 1) {
        throw new Error('The maximal timeout must be greater than 0.');
    }

    this.initialDelay_ = options.initialDelay || 100;
    this.maxDelay_ = options.maxDelay || 10000;

    if (this.maxDelay_ <= this.initialDelay_) {
        throw new Error('The maximal backoff delay must be ' +
                        'greater than the initial backoff delay.');
    }

    if (isDef(options.randomisationFactor) &&
        (options.randomisationFactor < 0 || options.randomisationFactor > 1)) {
        throw new Error('The randomisation factor must be between 0 and 1.');
    }

    this.randomisationFactor_ = options.randomisationFactor || 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.FibonacciStrategy.prototype"></a>[module backoff.FibonacciStrategy.prototype](#apidoc.module.backoff.FibonacciStrategy.prototype)

#### <a name="apidoc.element.backoff.FibonacciStrategy.prototype.next_"></a>[function <span class="apidocSignatureSpan">backoff.FibonacciStrategy.prototype.</span>next_ ()](#apidoc.element.backoff.FibonacciStrategy.prototype.next_)
- description and source-code
```javascript
next_ = function () {
    var backoffDelay = Math.min(this.nextBackoffDelay_, this.getMaxDelay());
    this.nextBackoffDelay_ += this.backoffDelay_;
    this.backoffDelay_ = backoffDelay;
    return backoffDelay;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FibonacciStrategy.prototype.reset_"></a>[function <span class="apidocSignatureSpan">backoff.FibonacciStrategy.prototype.</span>reset_ ()](#apidoc.element.backoff.FibonacciStrategy.prototype.reset_)
- description and source-code
```javascript
reset_ = function () {
    this.nextBackoffDelay_ = this.getInitialDelay();
    this.backoffDelay_ = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.FunctionCall"></a>[module backoff.FunctionCall](#apidoc.module.backoff.FunctionCall)

#### <a name="apidoc.element.backoff.FunctionCall.FunctionCall"></a>[function <span class="apidocSignatureSpan">backoff.</span>FunctionCall (fn, args, callback)](#apidoc.element.backoff.FunctionCall.FunctionCall)
- description and source-code
```javascript
function FunctionCall(fn, args, callback) {
    events.EventEmitter.call(this);

    precond.checkIsFunction(fn, 'Expected fn to be a function.');
    precond.checkIsArray(args, 'Expected args to be an array.');
    precond.checkIsFunction(callback, 'Expected callback to be a function.');

    this.function_ = fn;
    this.arguments_ = args;
    this.callback_ = callback;
    this.lastResult_ = [];
    this.numRetries_ = 0;

    this.backoff_ = null;
    this.strategy_ = null;
    this.failAfter_ = -1;
    this.retryPredicate_ = FunctionCall.DEFAULT_RETRY_PREDICATE_;

    this.state_ = FunctionCall.State_.PENDING;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall.DEFAULT_RETRY_PREDICATE_"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.</span>DEFAULT_RETRY_PREDICATE_ (err)](#apidoc.element.backoff.FunctionCall.DEFAULT_RETRY_PREDICATE_)
- description and source-code
```javascript
DEFAULT_RETRY_PREDICATE_ = function (err) {
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall.super_"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.</span>super_ ()](#apidoc.element.backoff.FunctionCall.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.backoff.FunctionCall.prototype"></a>[module backoff.FunctionCall.prototype](#apidoc.module.backoff.FunctionCall.prototype)

#### <a name="apidoc.element.backoff.FunctionCall.prototype.abort"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>abort ()](#apidoc.element.backoff.FunctionCall.prototype.abort)
- description and source-code
```javascript
abort = function () {
    if (this.isCompleted() || this.isAborted()) {
      return;
    }

    if (this.isRunning()) {
        this.backoff_.reset();
    }

    this.state_ = FunctionCall.State_.ABORTED;
    this.lastResult_ = [new Error('Backoff aborted.')];
    this.emit('abort');
    this.doCallback_();
}
```
- example usage
```shell
...
before, during and after the wrapped function invocation.

#### call.start()

Initiates the call the wrapped function. This method should only be called
once otherwise an exception will be thrown.

#### call.abort()

Aborts the call and causes the completion callback to be invoked with an abort
error if the call was pending or running; does nothing otherwise. This method
can safely be called mutliple times.

#### Event: 'call'
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.doCall_"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>doCall_ (isRetry)](#apidoc.element.backoff.FunctionCall.prototype.doCall_)
- description and source-code
```javascript
doCall_ = function (isRetry) {
    if (isRetry) {
        this.numRetries_++;
    }
    var eventArgs = ['call'].concat(this.arguments_);
    events.EventEmitter.prototype.emit.apply(this, eventArgs);
    var callback = this.handleFunctionCallback_.bind(this);
    this.function_.apply(null, this.arguments_.concat(callback));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.doCallback_"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>doCallback_ ()](#apidoc.element.backoff.FunctionCall.prototype.doCallback_)
- description and source-code
```javascript
doCallback_ = function () {
    this.callback_.apply(null, this.lastResult_);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.failAfter"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>failAfter (maxNumberOfRetry)](#apidoc.element.backoff.FunctionCall.prototype.failAfter)
- description and source-code
```javascript
failAfter = function (maxNumberOfRetry) {
    precond.checkState(this.isPending(), 'FunctionCall in progress.');
    this.failAfter_ = maxNumberOfRetry;
    return this; // Return this for chaining.
}
```
- example usage
```shell
...

var fibonacciBackoff = backoff.fibonacci({
    randomisationFactor: 0,
    initialDelay: 10,
    maxDelay: 300
});

fibonacciBackoff.failAfter(10);

fibonacciBackoff.on('backoff', function(number, delay) {
    // Do something when backoff starts, e.g. show to the
    // user the delay before next reconnection attempt.
    console.log(number + ' ' + delay + 'ms');
});
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.getLastResult"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>getLastResult ()](#apidoc.element.backoff.FunctionCall.prototype.getLastResult)
- description and source-code
```javascript
getLastResult = function () {
    return this.lastResult_.concat();
}
```
- example usage
```shell
...
should be retried or not, e.g. a network error would be retriable while a type
error would stop the function call. By default, all errors are considered to be
retriable.

This method should be called before 'call.start()' otherwise an exception will
be thrown.

#### call.getLastResult()

Returns an array containing the last arguments passed to the completion callback
of the wrapped function. For example, to get the error code returned by the last
call, one would do the following.

''' js
var results = call.getLastResult();
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.getNumRetries"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>getNumRetries ()](#apidoc.element.backoff.FunctionCall.prototype.getNumRetries)
- description and source-code
```javascript
getNumRetries = function () {
    return this.numRetries_;
}
```
- example usage
```shell
...
It's also possible to avoid some boilerplate code when invoking an asynchronous
function in a backoff loop by using 'backoff.call(fn, [args, ...], callback)'.

Typical usage looks like the following.

''' js
var call = backoff.call(get, 'https://duplika.ca/', function(err, res) {
    console.log('Num retries: ' + call.getNumRetries());

    if (err) {
        console.log('Error: ' + err.message);
    } else {
        console.log('Status: ' + res.statusCode);
    }
});
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.handleBackoff_"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>handleBackoff_ (number, delay, err)](#apidoc.element.backoff.FunctionCall.prototype.handleBackoff_)
- description and source-code
```javascript
handleBackoff_ = function (number, delay, err) {
    this.emit('backoff', number, delay, err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.handleFunctionCallback_"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>handleFunctionCallback_ ()](#apidoc.element.backoff.FunctionCall.prototype.handleFunctionCallback_)
- description and source-code
```javascript
handleFunctionCallback_ = function () {
    if (this.isAborted()) {
        return;
    }

    var args = Array.prototype.slice.call(arguments);
    this.lastResult_ = args; // Save last callback arguments.
    events.EventEmitter.prototype.emit.apply(this, ['callback'].concat(args));

    var err = args[0];
    if (err && this.retryPredicate_(err)) {
        this.backoff_.backoff(err);
    } else {
        this.state_ = FunctionCall.State_.COMPLETED;
        this.doCallback_();
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.isAborted"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isAborted ()](#apidoc.element.backoff.FunctionCall.prototype.isAborted)
- description and source-code
```javascript
isAborted = function () {
    return this.state_ == FunctionCall.State_.ABORTED;
}
```
- example usage
```shell
...

Returns whether the call is in progress.

#### call.isCompleted()

Returns whether the call is completed.

#### call.isAborted()

Returns whether the call is aborted.

#### call.setStrategy(strategy)

- strategy: strategy instance to use, defaults to 'FibonacciStrategy'.
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.isCompleted"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isCompleted ()](#apidoc.element.backoff.FunctionCall.prototype.isCompleted)
- description and source-code
```javascript
isCompleted = function () {
    return this.state_ == FunctionCall.State_.COMPLETED;
}
```
- example usage
```shell
...

Returns whether the call is pending, i.e. hasn't been started.

#### call.isRunning()

Returns whether the call is in progress.

#### call.isCompleted()

Returns whether the call is completed.

#### call.isAborted()

Returns whether the call is aborted.
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.isPending"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isPending ()](#apidoc.element.backoff.FunctionCall.prototype.isPending)
- description and source-code
```javascript
isPending = function () {
    return this.state_ == FunctionCall.State_.PENDING;
}
```
- example usage
```shell
...

- fn: asynchronous function to call
- args: an array containing fn's args
- callback: fn's callback

Constructs a function handler for the given asynchronous function.

#### call.isPending()

Returns whether the call is pending, i.e. hasn't been started.

#### call.isRunning()

Returns whether the call is in progress.
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.isRunning"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>isRunning ()](#apidoc.element.backoff.FunctionCall.prototype.isRunning)
- description and source-code
```javascript
isRunning = function () {
    return this.state_ == FunctionCall.State_.RUNNING;
}
```
- example usage
```shell
...

Constructs a function handler for the given asynchronous function.

#### call.isPending()

Returns whether the call is pending, i.e. hasn't been started.

#### call.isRunning()

Returns whether the call is in progress.

#### call.isCompleted()

Returns whether the call is completed.
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.retryIf"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>retryIf (retryPredicate)](#apidoc.element.backoff.FunctionCall.prototype.retryIf)
- description and source-code
```javascript
retryIf = function (retryPredicate) {
    precond.checkState(this.isPending(), 'FunctionCall in progress.');
    this.retryPredicate_ = retryPredicate;
    return this;
}
```
- example usage
```shell
...
    if (err) {
        console.log('Error: ' + err.message);
    } else {
        console.log('Status: ' + res.statusCode);
    }
});

call.retryIf(function(err) { return err.status == 503; });
call.setStrategy(new backoff.ExponentialStrategy());
call.failAfter(10);
call.start();
'''

## API
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.setStrategy"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>setStrategy (strategy)](#apidoc.element.backoff.FunctionCall.prototype.setStrategy)
- description and source-code
```javascript
setStrategy = function (strategy) {
    precond.checkState(this.isPending(), 'FunctionCall in progress.');
    this.strategy_ = strategy;
    return this; // Return this for chaining.
}
```
- example usage
```shell
...
        console.log('Error: ' + err.message);
    } else {
        console.log('Status: ' + res.statusCode);
    }
});

call.retryIf(function(err) { return err.status == 503; });
call.setStrategy(new backoff.ExponentialStrategy());
call.failAfter(10);
call.start();
'''

## API

### backoff.fibonacci([options])
...
```

#### <a name="apidoc.element.backoff.FunctionCall.prototype.start"></a>[function <span class="apidocSignatureSpan">backoff.FunctionCall.prototype.</span>start (backoffFactory)](#apidoc.element.backoff.FunctionCall.prototype.start)
- description and source-code
```javascript
start = function (backoffFactory) {
    precond.checkState(!this.isAborted(), 'FunctionCall is aborted.');
    precond.checkState(this.isPending(), 'FunctionCall already started.');

    var strategy = this.strategy_ || new FibonacciBackoffStrategy();

    this.backoff_ = backoffFactory ?
        backoffFactory(strategy) :
        new Backoff(strategy);

    this.backoff_.on('ready', this.doCall_.bind(this, true /* isRetry */));
    this.backoff_.on('fail', this.doCallback_.bind(this));
    this.backoff_.on('backoff', this.handleBackoff_.bind(this));

    if (this.failAfter_ > 0) {
        this.backoff_.failAfter(this.failAfter_);
    }

    this.state_ = FunctionCall.State_.RUNNING;
    this.doCall_(false /* isRetry */);
}
```
- example usage
```shell
...
        console.log('Status: ' + res.statusCode);
    }
});

call.retryIf(function(err) { return err.status == 503; });
call.setStrategy(new backoff.ExponentialStrategy());
call.failAfter(10);
call.start();
'''

## API

### backoff.fibonacci([options])

Constructs a Fibonacci backoff (10, 10, 20, 30, 50, etc.).
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
