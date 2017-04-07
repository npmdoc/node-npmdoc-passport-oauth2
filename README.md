# api documentation for  [passport-oauth2 (v1.4.0)](https://github.com/jaredhanson/passport-oauth2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-passport-oauth2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-passport-oauth2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-passport-oauth2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-passport-oauth2)
#### OAuth 2.0 authentication strategy for Passport.

[![NPM](https://nodei.co/npm/passport-oauth2.png?downloads=true)](https://www.npmjs.com/package/passport-oauth2)

[![apidoc](https://npmdoc.github.io/node-npmdoc-passport-oauth2/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-passport-oauth2_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-passport-oauth2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-passport-oauth2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-passport-oauth2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jared Hanson",
        "email": "jaredhanson@gmail.com",
        "url": "http://www.jaredhanson.net/"
    },
    "bugs": {
        "url": "http://github.com/jaredhanson/passport-oauth2/issues"
    },
    "dependencies": {
        "oauth": "0.9.x",
        "passport-strategy": "1.x.x",
        "uid2": "0.0.x",
        "utils-merge": "1.x.x"
    },
    "description": "OAuth 2.0 authentication strategy for Passport.",
    "devDependencies": {
        "chai": "2.x.x",
        "chai-passport-strategy": "1.x.x",
        "make-node": "0.3.x",
        "mocha": "2.x.x"
    },
    "directories": {},
    "dist": {
        "shasum": "f62f81583cbe12609be7ce6f160b9395a27b86ad",
        "tarball": "https://registry.npmjs.org/passport-oauth2/-/passport-oauth2-1.4.0.tgz"
    },
    "engines": {
        "node": ">= 0.4.0"
    },
    "gitHead": "a02839afb8d15f7d283ae09167973e4d22e8faf8",
    "homepage": "https://github.com/jaredhanson/passport-oauth2#readme",
    "keywords": [
        "passport",
        "auth",
        "authn",
        "authentication",
        "authz",
        "authorization",
        "oauth",
        "oauth2"
    ],
    "license": "MIT",
    "licenses": [
        {
            "type": "MIT",
            "url": "http://opensource.org/licenses/MIT"
        }
    ],
    "main": "./lib",
    "maintainers": [
        {
            "name": "jaredhanson",
            "email": "jaredhanson@gmail.com"
        }
    ],
    "name": "passport-oauth2",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/jaredhanson/passport-oauth2.git"
    },
    "scripts": {
        "test": "mocha --reporter spec --require test/bootstrap/node test/*.test.js test/**/*.test.js"
    },
    "version": "1.4.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module passport-oauth2](#apidoc.module.passport-oauth2)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>AuthorizationError (message, code, uri, status)](#apidoc.element.passport-oauth2.AuthorizationError)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>InternalOAuthError (message, err)](#apidoc.element.passport-oauth2.InternalOAuthError)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>Strategy (options, verify)](#apidoc.element.passport-oauth2.Strategy)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>TokenError (message, code, uri, status)](#apidoc.element.passport-oauth2.TokenError)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>super_ ()](#apidoc.element.passport-oauth2.super_)
1.  object <span class="apidocSignatureSpan">passport-oauth2.</span>InternalOAuthError.prototype
1.  object <span class="apidocSignatureSpan">passport-oauth2.</span>super_.prototype
1.  object <span class="apidocSignatureSpan">passport-oauth2.</span>utils

#### [module passport-oauth2.InternalOAuthError](#apidoc.module.passport-oauth2.InternalOAuthError)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>InternalOAuthError (message, err)](#apidoc.element.passport-oauth2.InternalOAuthError.InternalOAuthError)

#### [module passport-oauth2.InternalOAuthError.prototype](#apidoc.module.passport-oauth2.InternalOAuthError.prototype)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.InternalOAuthError.prototype.</span>toString ()](#apidoc.element.passport-oauth2.InternalOAuthError.prototype.toString)

#### [module passport-oauth2.super_](#apidoc.module.passport-oauth2.super_)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.</span>super_ ()](#apidoc.element.passport-oauth2.super_.super_)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.super_.</span>Strategy ()](#apidoc.element.passport-oauth2.super_.Strategy)

#### [module passport-oauth2.super_.prototype](#apidoc.module.passport-oauth2.super_.prototype)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.super_.prototype.</span>authenticate (req, options)](#apidoc.element.passport-oauth2.super_.prototype.authenticate)

#### [module passport-oauth2.utils](#apidoc.module.passport-oauth2.utils)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.utils.</span>merge (a, b)](#apidoc.element.passport-oauth2.utils.merge)
1.  [function <span class="apidocSignatureSpan">passport-oauth2.utils.</span>originalURL (req, options)](#apidoc.element.passport-oauth2.utils.originalURL)



# <a name="apidoc.module.passport-oauth2"></a>[module passport-oauth2](#apidoc.module.passport-oauth2)

#### <a name="apidoc.element.passport-oauth2.AuthorizationError"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>AuthorizationError (message, code, uri, status)](#apidoc.element.passport-oauth2.AuthorizationError)
- description and source-code
```javascript
function AuthorizationError(message, code, uri, status) {
  if (!status) {
    switch (code) {
      case 'access_denied': status = 403; break;
      case 'server_error': status = 502; break;
      case 'temporarily_unavailable': status = 503; break;
    }
  }

  Error.call(this);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
  this.message = message;
  this.code = code || 'server_error';
  this.uri = uri;
  this.status = status || 500;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-oauth2.InternalOAuthError"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>InternalOAuthError (message, err)](#apidoc.element.passport-oauth2.InternalOAuthError)
- description and source-code
```javascript
function InternalOAuthError(message, err) {
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
  this.message = message;
  this.oauthError = err;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-oauth2.Strategy"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>Strategy (options, verify)](#apidoc.element.passport-oauth2.Strategy)
- description and source-code
```javascript
function OAuth2Strategy(options, verify) {
  if (typeof options == 'function') {
    verify = options;
    options = undefined;
  }
  options = options || {};

  if (!verify) { throw new TypeError('OAuth2Strategy requires a verify callback'); }
  if (!options.authorizationURL) { throw new TypeError('OAuth2Strategy requires a authorizationURL option'); }
  if (!options.tokenURL) { throw new TypeError('OAuth2Strategy requires a tokenURL option'); }
  if (!options.clientID) { throw new TypeError('OAuth2Strategy requires a clientID option'); }

  passport.Strategy.call(this);
  this.name = 'oauth2';
  this._verify = verify;

  // NOTE: The _oauth2 property is considered "protected".  Subclasses are
  //       allowed to use it when making protected resource requests to retrieve
  //       the user profile.
  this._oauth2 = new OAuth2(options.clientID,  options.clientSecret,
      '', options.authorizationURL, options.tokenURL, options.customHeaders);

  this._callbackURL = options.callbackURL;
  this._scope = options.scope;
  this._scopeSeparator = options.scopeSeparator || ' ';
  this._key = options.sessionKey || ('oauth2:' + url.parse(options.authorizationURL).hostname);

  if (options.store) {
    this._stateStore = options.store;
  } else {
    if (options.state) {
      this._stateStore = new SessionStateStore({ key: this._key });
    } else {
      this._stateStore = new NullStateStore();
    }
  }
  this._trustProxy = options.proxy;
  this._passReqToCallback = options.passReqToCallback;
  this._skipUserProfile = (options.skipUserProfile === undefined) ? false : options.skipUserProfile;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-oauth2.TokenError"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>TokenError (message, code, uri, status)](#apidoc.element.passport-oauth2.TokenError)
- description and source-code
```javascript
function TokenError(message, code, uri, status) {
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
  this.message = message;
  this.code = code || 'invalid_request';
  this.uri = uri;
  this.status = status || 500;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-oauth2.super_"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>super_ ()](#apidoc.element.passport-oauth2.super_)
- description and source-code
```javascript
function Strategy() {
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.passport-oauth2.InternalOAuthError"></a>[module passport-oauth2.InternalOAuthError](#apidoc.module.passport-oauth2.InternalOAuthError)

#### <a name="apidoc.element.passport-oauth2.InternalOAuthError.InternalOAuthError"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>InternalOAuthError (message, err)](#apidoc.element.passport-oauth2.InternalOAuthError.InternalOAuthError)
- description and source-code
```javascript
function InternalOAuthError(message, err) {
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);
  this.name = this.constructor.name;
  this.message = message;
  this.oauthError = err;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.passport-oauth2.InternalOAuthError.prototype"></a>[module passport-oauth2.InternalOAuthError.prototype](#apidoc.module.passport-oauth2.InternalOAuthError.prototype)

#### <a name="apidoc.element.passport-oauth2.InternalOAuthError.prototype.toString"></a>[function <span class="apidocSignatureSpan">passport-oauth2.InternalOAuthError.prototype.</span>toString ()](#apidoc.element.passport-oauth2.InternalOAuthError.prototype.toString)
- description and source-code
```javascript
toString = function () {
  var m = this.name;
  if (this.message) { m += ': ' + this.message; }
  if (this.oauthError) {
    if (this.oauthError instanceof Error) {
      m = this.oauthError.toString();
    } else if (this.oauthError.statusCode && this.oauthError.data) {
      m += ' (status: ' + this.oauthError.statusCode + ' data: ' + this.oauthError.data + ')';
    }
  }
  return m;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.passport-oauth2.super_"></a>[module passport-oauth2.super_](#apidoc.module.passport-oauth2.super_)

#### <a name="apidoc.element.passport-oauth2.super_.super_"></a>[function <span class="apidocSignatureSpan">passport-oauth2.</span>super_ ()](#apidoc.element.passport-oauth2.super_.super_)
- description and source-code
```javascript
function Strategy() {
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-oauth2.super_.Strategy"></a>[function <span class="apidocSignatureSpan">passport-oauth2.super_.</span>Strategy ()](#apidoc.element.passport-oauth2.super_.Strategy)
- description and source-code
```javascript
function Strategy() {
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.passport-oauth2.super_.prototype"></a>[module passport-oauth2.super_.prototype](#apidoc.module.passport-oauth2.super_.prototype)

#### <a name="apidoc.element.passport-oauth2.super_.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">passport-oauth2.super_.prototype.</span>authenticate (req, options)](#apidoc.element.passport-oauth2.super_.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (req, options) {
  throw new Error('Strategy#authenticate must be overridden by subclass');
}
```
- example usage
```shell
...
    });
  }
));
'''

#### Authenticate Requests

Use 'passport.authenticate()', specifying the ''oauth2'' strategy, to
authenticate requests.

For example, as route middleware in an [Express](http://expressjs.com/)
application:

'''js
app.get('/auth/example',
...
```



# <a name="apidoc.module.passport-oauth2.utils"></a>[module passport-oauth2.utils](#apidoc.module.passport-oauth2.utils)

#### <a name="apidoc.element.passport-oauth2.utils.merge"></a>[function <span class="apidocSignatureSpan">passport-oauth2.utils.</span>merge (a, b)](#apidoc.element.passport-oauth2.utils.merge)
- description and source-code
```javascript
merge = function (a, b){
  if (a && b) {
    for (var key in b) {
      a[key] = b[key];
    }
  }
  return a;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-oauth2.utils.originalURL"></a>[function <span class="apidocSignatureSpan">passport-oauth2.utils.</span>originalURL (req, options)](#apidoc.element.passport-oauth2.utils.originalURL)
- description and source-code
```javascript
originalURL = function (req, options) {
  options = options || {};
  var app = req.app;
  if (app && app.get && app.get('trust proxy')) {
    options.proxy = true;
  }
  var trustProxy = options.proxy;

  var proto = (req.headers['x-forwarded-proto'] || '').toLowerCase()
    , tls = req.connection.encrypted || (trustProxy && 'https' == proto.split(/\s*,\s*/)[0])
    , host = (trustProxy && req.headers['x-forwarded-host']) || req.headers.host
    , protocol = tls ? 'https' : 'http'
    , path = req.url || '';
  return protocol + '://' + host + path;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
