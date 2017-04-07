# api documentation for  [parse-server (v2.3.7)](https://github.com/ParsePlatform/parse-server#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-parse-server.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-parse-server) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-parse-server.svg)](https://travis-ci.org/npmdoc/node-npmdoc-parse-server)
#### An express module providing a Parse-compatible API server

[![NPM](https://nodei.co/npm/parse-server.png?downloads=true)](https://www.npmjs.com/package/parse-server)

[![apidoc](https://npmdoc.github.io/node-npmdoc-parse-server/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-parse-server_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-parse-server/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-parse-server/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-parse-server/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "parse-server": "./bin/parse-server"
    },
    "bugs": {
        "url": "https://github.com/ParsePlatform/parse-server/issues"
    },
    "dependencies": {
        "bcrypt": "1.0.2",
        "bcryptjs": "2.4.3",
        "body-parser": "1.17.1",
        "commander": "2.9.0",
        "deepcopy": "0.6.3",
        "express": "4.15.2",
        "intersect": "1.0.1",
        "lodash": "4.17.4",
        "lru-cache": "4.0.2",
        "mime": "1.3.4",
        "mongodb": "2.2.24",
        "multer": "1.3.0",
        "parse": "1.9.2",
        "parse-server-fs-adapter": "1.0.1",
        "parse-server-push-adapter": "1.2.0",
        "parse-server-s3-adapter": "1.0.6",
        "parse-server-simple-mailgun-adapter": "1.0.0",
        "pg-promise": "5.6.2",
        "redis": "2.6.5",
        "request": "2.81.0",
        "semver": "5.2.0",
        "tv4": "1.2.7",
        "uws": "^0.13.0",
        "winston": "2.3.1",
        "winston-daily-rotate-file": "1.4.5",
        "ws": "2.2.0"
    },
    "description": "An express module providing a Parse-compatible API server",
    "devDependencies": {
        "babel-cli": "6.23.0",
        "babel-core": "6.23.1",
        "babel-eslint": "^7.1.1",
        "babel-plugin-syntax-flow": "6.13.0",
        "babel-plugin-transform-flow-strip-types": "6.22.0",
        "babel-preset-es2015": "6.22.0",
        "babel-preset-stage-0": "6.22.0",
        "babel-register": "6.23.0",
        "bcrypt-nodejs": "0.0.3",
        "cross-env": "3.1.4",
        "deep-diff": "0.3.4",
        "eslint": "^3.16.1",
        "eslint-plugin-flowtype": "^2.25.0",
        "gaze": "1.1.1",
        "istanbul": "1.0.0-alpha.1",
        "jasmine": "2.5.3",
        "jasmine-spec-reporter": "^3.1.0",
        "mongodb-runner": "3.4.0",
        "nodemon": "1.11.0",
        "request-promise": "4.1.1"
    },
    "directories": {},
    "dist": {
        "shasum": "f8305f3dba21596a663cc03ba6f87eaa2767f174",
        "tarball": "https://registry.npmjs.org/parse-server/-/parse-server-2.3.7.tgz"
    },
    "engines": {
        "node": ">=4.6"
    },
    "files": [
        "bin/",
        "lib/",
        "public_html/",
        "views/",
        "LICENSE",
        "PATENTS",
        "README.md"
    ],
    "gitHead": "593a7a62642008fffebd2ee9665a542bac57f718",
    "homepage": "https://github.com/ParsePlatform/parse-server#readme",
    "license": "BSD-3-Clause",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "drewgross",
            "email": "drewgross@fb.com"
        },
        {
            "name": "fosco",
            "email": "fosco@fosco.com"
        }
    ],
    "name": "parse-server",
    "optionalDependencies": {
        "bcrypt": "1.0.2",
        "uws": "^0.13.0"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/ParsePlatform/parse-server.git"
    },
    "scripts": {
        "build": "babel src/ -d lib/ --copy-files",
        "coverage": "cross-env COVERAGE_OPTION='./node_modules/.bin/istanbul cover' npm test",
        "coverage:win": "cross-env MONGODB_VERSION=${MONGODB_VERSION:=3.2.6} MONGODB_STORAGE_ENGINE=mmapv1 NODE_ENV=test TESTING=1 node ./node_modules/istanbul/lib/cli.js cover ./node_modules/jasmine/bin/jasmine.js",
        "dev": "npm run build && node bin/dev",
        "lint": "eslint --cache ./",
        "prepublish": "npm run build",
        "pretest": "npm run lint",
        "start": "node ./bin/parse-server",
        "test": "cross-env MONGODB_VERSION=${MONGODB_VERSION:=3.2.6} MONGODB_STORAGE_ENGINE=mmapv1 NODE_ENV=test TESTING=1 $COVERAGE_OPTION jasmine",
        "test:win": "cross-env MONGODB_VERSION=${MONGODB_VERSION:=3.2.6} MONGODB_STORAGE_ENGINE=mmapv1 NODE_ENV=test TESTING=1 jasmine"
    },
    "version": "2.3.7"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module parse-server](#apidoc.module.parse-server)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>FileSystemAdapter (options)](#apidoc.element.parse-server.FileSystemAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>GCSAdapter ()](#apidoc.element.parse-server.GCSAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>InMemoryCacheAdapter (ctx)](#apidoc.element.parse-server.InMemoryCacheAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>NullCacheAdapter ()](#apidoc.element.parse-server.NullCacheAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>ParseServer (options)](#apidoc.element.parse-server.ParseServer)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>PushWorker (pushAdapter)](#apidoc.element.parse-server.PushWorker)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>RedisCacheAdapter (redisCtx)](#apidoc.element.parse-server.RedisCacheAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>RestQuery (config, auth, className)](#apidoc.element.parse-server.RestQuery)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>RestWrite (config, auth, className, query, data, originalData, clientSDK)](#apidoc.element.parse-server.RestWrite)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>S3Adapter ()](#apidoc.element.parse-server.S3Adapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>default (_ref)](#apidoc.element.parse-server.default)
1.  object <span class="apidocSignatureSpan">parse-server.</span>AccountLockout
1.  object <span class="apidocSignatureSpan">parse-server.</span>Auth
1.  object <span class="apidocSignatureSpan">parse-server.</span>ClientSDK
1.  object <span class="apidocSignatureSpan">parse-server.</span>FileSystemAdapter.prototype
1.  object <span class="apidocSignatureSpan">parse-server.</span>ParseServerRESTController
1.  object <span class="apidocSignatureSpan">parse-server.</span>PromiseRouter
1.  object <span class="apidocSignatureSpan">parse-server.</span>RestQuery.prototype
1.  object <span class="apidocSignatureSpan">parse-server.</span>RestWrite.prototype
1.  object <span class="apidocSignatureSpan">parse-server.</span>S3Adapter.prototype
1.  object <span class="apidocSignatureSpan">parse-server.</span>StatusHandler
1.  object <span class="apidocSignatureSpan">parse-server.</span>TestUtils
1.  object <span class="apidocSignatureSpan">parse-server.</span>batch
1.  object <span class="apidocSignatureSpan">parse-server.</span>cryptoUtils
1.  object <span class="apidocSignatureSpan">parse-server.</span>deprecated
1.  object <span class="apidocSignatureSpan">parse-server.</span>logger
1.  object <span class="apidocSignatureSpan">parse-server.</span>middlewares
1.  object <span class="apidocSignatureSpan">parse-server.</span>password
1.  object <span class="apidocSignatureSpan">parse-server.</span>requiredParameter
1.  object <span class="apidocSignatureSpan">parse-server.</span>rest
1.  object <span class="apidocSignatureSpan">parse-server.</span>triggers

#### [module parse-server.AccountLockout](#apidoc.module.parse-server.AccountLockout)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>AccountLockout (user, config)](#apidoc.element.parse-server.AccountLockout.AccountLockout)
1.  [function <span class="apidocSignatureSpan">parse-server.AccountLockout.</span>default (user, config)](#apidoc.element.parse-server.AccountLockout.default)

#### [module parse-server.Auth](#apidoc.module.parse-server.Auth)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>Auth ()](#apidoc.element.parse-server.Auth.Auth)
1.  [function <span class="apidocSignatureSpan">parse-server.Auth.</span>getAuthForLegacySessionToken ()](#apidoc.element.parse-server.Auth.getAuthForLegacySessionToken)
1.  [function <span class="apidocSignatureSpan">parse-server.Auth.</span>getAuthForSessionToken ()](#apidoc.element.parse-server.Auth.getAuthForSessionToken)
1.  [function <span class="apidocSignatureSpan">parse-server.Auth.</span>master (config)](#apidoc.element.parse-server.Auth.master)
1.  [function <span class="apidocSignatureSpan">parse-server.Auth.</span>nobody (config)](#apidoc.element.parse-server.Auth.nobody)

#### [module parse-server.ClientSDK](#apidoc.module.parse-server.ClientSDK)
1.  [function <span class="apidocSignatureSpan">parse-server.ClientSDK.</span>compatible (compatibleSDK)](#apidoc.element.parse-server.ClientSDK.compatible)
1.  [function <span class="apidocSignatureSpan">parse-server.ClientSDK.</span>fromString (version)](#apidoc.element.parse-server.ClientSDK.fromString)
1.  [function <span class="apidocSignatureSpan">parse-server.ClientSDK.</span>supportsForwardDelete (clientSDK)](#apidoc.element.parse-server.ClientSDK.supportsForwardDelete)

#### [module parse-server.FileSystemAdapter](#apidoc.module.parse-server.FileSystemAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>FileSystemAdapter (options)](#apidoc.element.parse-server.FileSystemAdapter.FileSystemAdapter)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.</span>default (options)](#apidoc.element.parse-server.FileSystemAdapter.default)

#### [module parse-server.FileSystemAdapter.prototype](#apidoc.module.parse-server.FileSystemAdapter.prototype)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_applicationDirExist ()](#apidoc.element.parse-server.FileSystemAdapter.prototype._applicationDirExist)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_getApplicationDir ()](#apidoc.element.parse-server.FileSystemAdapter.prototype._getApplicationDir)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_getLocalFilePath (filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype._getLocalFilePath)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_mkdir (dirPath)](#apidoc.element.parse-server.FileSystemAdapter.prototype._mkdir)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>createFile (filename, data)](#apidoc.element.parse-server.FileSystemAdapter.prototype.createFile)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>deleteFile (filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype.deleteFile)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>getFileData (filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype.getFileData)
1.  [function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>getFileLocation (config, filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype.getFileLocation)

#### [module parse-server.ParseServer](#apidoc.module.parse-server.ParseServer)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>ParseServer (options)](#apidoc.element.parse-server.ParseServer.ParseServer)
1.  [function <span class="apidocSignatureSpan">parse-server.ParseServer.</span>createLiveQueryServer (httpServer, config)](#apidoc.element.parse-server.ParseServer.createLiveQueryServer)

#### [module parse-server.ParseServerRESTController](#apidoc.module.parse-server.ParseServerRESTController)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>ParseServerRESTController (applicationId, router)](#apidoc.element.parse-server.ParseServerRESTController.ParseServerRESTController)
1.  [function <span class="apidocSignatureSpan">parse-server.ParseServerRESTController.</span>default (applicationId, router)](#apidoc.element.parse-server.ParseServerRESTController.default)

#### [module parse-server.PromiseRouter](#apidoc.module.parse-server.PromiseRouter)
1.  [function <span class="apidocSignatureSpan">parse-server.PromiseRouter.</span>default ()](#apidoc.element.parse-server.PromiseRouter.default)

#### [module parse-server.RestQuery](#apidoc.module.parse-server.RestQuery)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>RestQuery (config, auth, className)](#apidoc.element.parse-server.RestQuery.RestQuery)

#### [module parse-server.RestQuery.prototype](#apidoc.module.parse-server.RestQuery.prototype)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>buildRestWhere ()](#apidoc.element.parse-server.RestQuery.prototype.buildRestWhere)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>execute (executeOptions)](#apidoc.element.parse-server.RestQuery.prototype.execute)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>getUserAndRoleACL ()](#apidoc.element.parse-server.RestQuery.prototype.getUserAndRoleACL)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>handleInclude ()](#apidoc.element.parse-server.RestQuery.prototype.handleInclude)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>redirectClassNameForKey ()](#apidoc.element.parse-server.RestQuery.prototype.redirectClassNameForKey)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceDontSelect ()](#apidoc.element.parse-server.RestQuery.prototype.replaceDontSelect)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceInQuery ()](#apidoc.element.parse-server.RestQuery.prototype.replaceInQuery)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceNotInQuery ()](#apidoc.element.parse-server.RestQuery.prototype.replaceNotInQuery)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceSelect ()](#apidoc.element.parse-server.RestQuery.prototype.replaceSelect)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>runAfterFindTrigger ()](#apidoc.element.parse-server.RestQuery.prototype.runAfterFindTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>runCount ()](#apidoc.element.parse-server.RestQuery.prototype.runCount)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>runFind ()](#apidoc.element.parse-server.RestQuery.prototype.runFind)
1.  [function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>validateClientClassCreation ()](#apidoc.element.parse-server.RestQuery.prototype.validateClientClassCreation)

#### [module parse-server.RestWrite](#apidoc.module.parse-server.RestWrite)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>RestWrite (config, auth, className, query, data, originalData, clientSDK)](#apidoc.element.parse-server.RestWrite.RestWrite)

#### [module parse-server.RestWrite.prototype](#apidoc.module.parse-server.RestWrite.prototype)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_updateResponseWithData (response, data)](#apidoc.element.parse-server.RestWrite.prototype._updateResponseWithData)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validateEmail ()](#apidoc.element.parse-server.RestWrite.prototype._validateEmail)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validatePasswordHistory ()](#apidoc.element.parse-server.RestWrite.prototype._validatePasswordHistory)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validatePasswordPolicy ()](#apidoc.element.parse-server.RestWrite.prototype._validatePasswordPolicy)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validatePasswordRequirements ()](#apidoc.element.parse-server.RestWrite.prototype._validatePasswordRequirements)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validateUserName ()](#apidoc.element.parse-server.RestWrite.prototype._validateUserName)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>cleanUserAuthData ()](#apidoc.element.parse-server.RestWrite.prototype.cleanUserAuthData)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>createSessionToken ()](#apidoc.element.parse-server.RestWrite.prototype.createSessionToken)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>createSessionTokenIfNeeded ()](#apidoc.element.parse-server.RestWrite.prototype.createSessionTokenIfNeeded)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>execute ()](#apidoc.element.parse-server.RestWrite.prototype.execute)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>expandFilesForExistingObjects ()](#apidoc.element.parse-server.RestWrite.prototype.expandFilesForExistingObjects)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>findUsersWithAuthData (authData)](#apidoc.element.parse-server.RestWrite.prototype.findUsersWithAuthData)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>getUserAndRoleACL ()](#apidoc.element.parse-server.RestWrite.prototype.getUserAndRoleACL)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleAuthData (authData)](#apidoc.element.parse-server.RestWrite.prototype.handleAuthData)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleAuthDataValidation (authData)](#apidoc.element.parse-server.RestWrite.prototype.handleAuthDataValidation)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleFollowup ()](#apidoc.element.parse-server.RestWrite.prototype.handleFollowup)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleInstallation ()](#apidoc.element.parse-server.RestWrite.prototype.handleInstallation)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleSession ()](#apidoc.element.parse-server.RestWrite.prototype.handleSession)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>location ()](#apidoc.element.parse-server.RestWrite.prototype.location)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>objectId ()](#apidoc.element.parse-server.RestWrite.prototype.objectId)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>runAfterTrigger ()](#apidoc.element.parse-server.RestWrite.prototype.runAfterTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>runBeforeTrigger ()](#apidoc.element.parse-server.RestWrite.prototype.runBeforeTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>runDatabaseOperation ()](#apidoc.element.parse-server.RestWrite.prototype.runDatabaseOperation)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>sanitizedData ()](#apidoc.element.parse-server.RestWrite.prototype.sanitizedData)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>setRequiredFieldsIfNeeded ()](#apidoc.element.parse-server.RestWrite.prototype.setRequiredFieldsIfNeeded)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>transformUser ()](#apidoc.element.parse-server.RestWrite.prototype.transformUser)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>validateAuthData ()](#apidoc.element.parse-server.RestWrite.prototype.validateAuthData)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>validateClientClassCreation ()](#apidoc.element.parse-server.RestWrite.prototype.validateClientClassCreation)
1.  [function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>validateSchema ()](#apidoc.element.parse-server.RestWrite.prototype.validateSchema)

#### [module parse-server.S3Adapter](#apidoc.module.parse-server.S3Adapter)
1.  [function <span class="apidocSignatureSpan">parse-server.</span>S3Adapter ()](#apidoc.element.parse-server.S3Adapter.S3Adapter)
1.  [function <span class="apidocSignatureSpan">parse-server.S3Adapter.</span>default ()](#apidoc.element.parse-server.S3Adapter.default)

#### [module parse-server.S3Adapter.prototype](#apidoc.module.parse-server.S3Adapter.prototype)
1.  [function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>createBucket ()](#apidoc.element.parse-server.S3Adapter.prototype.createBucket)
1.  [function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>createFile (filename, data, contentType)](#apidoc.element.parse-server.S3Adapter.prototype.createFile)
1.  [function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>deleteFile (filename)](#apidoc.element.parse-server.S3Adapter.prototype.deleteFile)
1.  [function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>getFileData (filename)](#apidoc.element.parse-server.S3Adapter.prototype.getFileData)
1.  [function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>getFileLocation (config, filename)](#apidoc.element.parse-server.S3Adapter.prototype.getFileLocation)

#### [module parse-server.StatusHandler](#apidoc.module.parse-server.StatusHandler)
1.  [function <span class="apidocSignatureSpan">parse-server.StatusHandler.</span>flatten (array)](#apidoc.element.parse-server.StatusHandler.flatten)
1.  [function <span class="apidocSignatureSpan">parse-server.StatusHandler.</span>jobStatusHandler (config)](#apidoc.element.parse-server.StatusHandler.jobStatusHandler)
1.  [function <span class="apidocSignatureSpan">parse-server.StatusHandler.</span>pushStatusHandler (config)](#apidoc.element.parse-server.StatusHandler.pushStatusHandler)

#### [module parse-server.TestUtils](#apidoc.module.parse-server.TestUtils)
1.  [function <span class="apidocSignatureSpan">parse-server.TestUtils.</span>destroyAllDataPermanently ()](#apidoc.element.parse-server.TestUtils.destroyAllDataPermanently)

#### [module parse-server.batch](#apidoc.module.parse-server.batch)
1.  [function <span class="apidocSignatureSpan">parse-server.batch.</span>makeBatchRoutingPathFunction (originalUrl, serverURL, publicServerURL)](#apidoc.element.parse-server.batch.makeBatchRoutingPathFunction)
1.  [function <span class="apidocSignatureSpan">parse-server.batch.</span>mountOnto (router)](#apidoc.element.parse-server.batch.mountOnto)

#### [module parse-server.cryptoUtils](#apidoc.module.parse-server.cryptoUtils)
1.  [function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>md5Hash (string)](#apidoc.element.parse-server.cryptoUtils.md5Hash)
1.  [function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>newObjectId ()](#apidoc.element.parse-server.cryptoUtils.newObjectId)
1.  [function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>newToken ()](#apidoc.element.parse-server.cryptoUtils.newToken)
1.  [function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>randomHexString (size)](#apidoc.element.parse-server.cryptoUtils.randomHexString)
1.  [function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>randomString (size)](#apidoc.element.parse-server.cryptoUtils.randomString)

#### [module parse-server.deprecated](#apidoc.module.parse-server.deprecated)
1.  [function <span class="apidocSignatureSpan">parse-server.deprecated.</span>useExternal (name, moduleName)](#apidoc.element.parse-server.deprecated.useExternal)

#### [module parse-server.logger](#apidoc.module.parse-server.logger)
1.  [function <span class="apidocSignatureSpan">parse-server.logger.</span>getLogger ()](#apidoc.element.parse-server.logger.getLogger)
1.  [function <span class="apidocSignatureSpan">parse-server.logger.</span>setLogger (aLogger)](#apidoc.element.parse-server.logger.setLogger)

#### [module parse-server.middlewares](#apidoc.module.parse-server.middlewares)
1.  [function <span class="apidocSignatureSpan">parse-server.middlewares.</span>allowCrossDomain (req, res, next)](#apidoc.element.parse-server.middlewares.allowCrossDomain)
1.  [function <span class="apidocSignatureSpan">parse-server.middlewares.</span>allowMethodOverride (req, res, next)](#apidoc.element.parse-server.middlewares.allowMethodOverride)
1.  [function <span class="apidocSignatureSpan">parse-server.middlewares.</span>enforceMasterKeyAccess (req, res, next)](#apidoc.element.parse-server.middlewares.enforceMasterKeyAccess)
1.  [function <span class="apidocSignatureSpan">parse-server.middlewares.</span>handleParseErrors (err, req, res, next)](#apidoc.element.parse-server.middlewares.handleParseErrors)
1.  [function <span class="apidocSignatureSpan">parse-server.middlewares.</span>handleParseHeaders (req, res, next)](#apidoc.element.parse-server.middlewares.handleParseHeaders)
1.  [function <span class="apidocSignatureSpan">parse-server.middlewares.</span>promiseEnforceMasterKeyAccess (request)](#apidoc.element.parse-server.middlewares.promiseEnforceMasterKeyAccess)

#### [module parse-server.password](#apidoc.module.parse-server.password)
1.  [function <span class="apidocSignatureSpan">parse-server.password.</span>compare (password, hashedPassword)](#apidoc.element.parse-server.password.compare)
1.  [function <span class="apidocSignatureSpan">parse-server.password.</span>hash (password)](#apidoc.element.parse-server.password.hash)

#### [module parse-server.requiredParameter](#apidoc.module.parse-server.requiredParameter)
1.  [function <span class="apidocSignatureSpan">parse-server.requiredParameter.</span>default (errorMessage)](#apidoc.element.parse-server.requiredParameter.default)

#### [module parse-server.rest](#apidoc.module.parse-server.rest)
1.  [function <span class="apidocSignatureSpan">parse-server.rest.</span>create (config, auth, className, restObject, clientSDK)](#apidoc.element.parse-server.rest.create)
1.  [function <span class="apidocSignatureSpan">parse-server.rest.</span>del (config, auth, className, objectId)](#apidoc.element.parse-server.rest.del)
1.  [function <span class="apidocSignatureSpan">parse-server.rest.</span>find (config, auth, className, restWhere, restOptions, clientSDK)](#apidoc.element.parse-server.rest.find)
1.  [function <span class="apidocSignatureSpan">parse-server.rest.</span>get (config, auth, className, objectId, restOptions, clientSDK)](#apidoc.element.parse-server.rest.get)
1.  [function <span class="apidocSignatureSpan">parse-server.rest.</span>update (config, auth, className, objectId, restObject, clientSDK)](#apidoc.element.parse-server.rest.update)

#### [module parse-server.triggers](#apidoc.module.parse-server.triggers)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>_unregister (appId, category, className, type)](#apidoc.element.parse-server.triggers._unregister)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>_unregisterAll ()](#apidoc.element.parse-server.triggers._unregisterAll)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>addFunction (functionName, handler, validationHandler, applicationId)](#apidoc.element.parse-server.triggers.addFunction)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>addJob (jobName, handler, applicationId)](#apidoc.element.parse-server.triggers.addJob)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>addTrigger (type, className, handler, applicationId)](#apidoc.element.parse-server.triggers.addTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getFunction (functionName, applicationId)](#apidoc.element.parse-server.triggers.getFunction)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getJob (jobName, applicationId)](#apidoc.element.parse-server.triggers.getJob)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getJobs (applicationId)](#apidoc.element.parse-server.triggers.getJobs)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getRequestObject (triggerType, auth, parseObject, originalParseObject, config)](#apidoc.element.parse-server.triggers.getRequestObject)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getRequestQueryObject (triggerType, auth, query, config)](#apidoc.element.parse-server.triggers.getRequestQueryObject)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getResponseObject (request, resolve, reject)](#apidoc.element.parse-server.triggers.getResponseObject)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getTrigger (className, triggerType, applicationId)](#apidoc.element.parse-server.triggers.getTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>getValidator (functionName, applicationId)](#apidoc.element.parse-server.triggers.getValidator)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>inflate (data, restObject)](#apidoc.element.parse-server.triggers.inflate)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>maybeRunAfterFindTrigger (triggerType, auth, className, objects, config)](#apidoc.element.parse-server.triggers.maybeRunAfterFindTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>maybeRunQueryTrigger (triggerType, className, restWhere, restOptions, config, auth)](#apidoc.element.parse-server.triggers.maybeRunQueryTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>maybeRunTrigger (triggerType, auth, parseObject, originalParseObject, config)](#apidoc.element.parse-server.triggers.maybeRunTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>removeFunction (functionName, applicationId)](#apidoc.element.parse-server.triggers.removeFunction)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>removeJob (jobName, applicationId)](#apidoc.element.parse-server.triggers.removeJob)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>removeTrigger (type, className, applicationId)](#apidoc.element.parse-server.triggers.removeTrigger)
1.  [function <span class="apidocSignatureSpan">parse-server.triggers.</span>triggerExists (className, type, applicationId)](#apidoc.element.parse-server.triggers.triggerExists)
1.  object <span class="apidocSignatureSpan">parse-server.triggers.</span>Types



# <a name="apidoc.module.parse-server"></a>[module parse-server](#apidoc.module.parse-server)

#### <a name="apidoc.element.parse-server.FileSystemAdapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>FileSystemAdapter (options)](#apidoc.element.parse-server.FileSystemAdapter)
- description and source-code
```javascript
function FileSystemAdapter(options) {
  options = options || {};
  let filesSubDirectory = options.filesSubDirectory || '';
  this._filesDir = filesSubDirectory;
  this._mkdir(this._getApplicationDir());
  if (!this._applicationDirExist()) {
    throw "Files directory doesn't exist.";
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.GCSAdapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>GCSAdapter ()](#apidoc.element.parse-server.GCSAdapter)
- description and source-code
```javascript
GCSAdapter = function () {
  throw name + " is not provided by parse-server anymore; please install " + moduleName;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.InMemoryCacheAdapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>InMemoryCacheAdapter (ctx)](#apidoc.element.parse-server.InMemoryCacheAdapter)
- description and source-code
```javascript
function InMemoryCacheAdapter(ctx) {
  _classCallCheck(this, InMemoryCacheAdapter);

  this.cache = new _InMemoryCache.InMemoryCache(ctx);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.NullCacheAdapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>NullCacheAdapter ()](#apidoc.element.parse-server.NullCacheAdapter)
- description and source-code
```javascript
function NullCacheAdapter() {
  _classCallCheck(this, NullCacheAdapter);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.ParseServer"></a>[function <span class="apidocSignatureSpan">parse-server.</span>ParseServer (options)](#apidoc.element.parse-server.ParseServer)
- description and source-code
```javascript
function _ParseServer(options) {
  var server = new _ParseServer3.default(options);
  return server.app;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.PushWorker"></a>[function <span class="apidocSignatureSpan">parse-server.</span>PushWorker (pushAdapter)](#apidoc.element.parse-server.PushWorker)
- description and source-code
```javascript
function PushWorker(pushAdapter) {
  var _this = this;

  var subscriberConfig = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : {};

  _classCallCheck(this, PushWorker);

  _AdaptableController2.default.validateAdapter(pushAdapter, this, _PushAdapter.PushAdapter);
  this.adapter = pushAdapter;

  this.channel = subscriberConfig.channel || _PushQueue.PushQueue.defaultPushChannel();
  this.subscriber = _ParseMessageQueue.ParseMessageQueue.createSubscriber(subscriberConfig);
  if (this.subscriber) {
    var subscriber = this.subscriber;
    subscriber.subscribe(this.channel);
    subscriber.on('message', function (channel, messageStr) {
      var workItem = JSON.parse(messageStr);
      _this.run(workItem);
    });
  }
}
```
- example usage
```shell
...

var disablePushWorker = pushQueueOptions.disablePushWorker;


var pushControllerQueue = new _PushQueue.PushQueue(pushQueueOptions);
var pushWorker = void 0;
if (!disablePushWorker) {
  pushWorker = new _PushWorker.PushWorker(pushAdapter, pushQueueOptions);
}

var emailControllerAdapter = (0, _AdapterLoader.loadAdapter)(emailAdapter);
var userController = new _UserController.UserController(emailControllerAdapter, appId, { verifyUserEmails: verifyUserEmails });

var cacheControllerAdapter = (0, _AdapterLoader.loadAdapter)(cacheAdapter, _InMemoryCacheAdapter.InMemoryCacheAdapter, { appId:
appId });
var cacheController = new _CacheController.CacheController(cacheControllerAdapter, appId);
...
```

#### <a name="apidoc.element.parse-server.RedisCacheAdapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>RedisCacheAdapter (redisCtx)](#apidoc.element.parse-server.RedisCacheAdapter)
- description and source-code
```javascript
function RedisCacheAdapter(redisCtx) {
  var ttl = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : DEFAULT_REDIS_TTL;

  _classCallCheck(this, RedisCacheAdapter);

  this.client = _redis2.default.createClient(redisCtx);
  this.p = Promise.resolve();
  this.ttl = ttl;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.RestQuery"></a>[function <span class="apidocSignatureSpan">parse-server.</span>RestQuery (config, auth, className)](#apidoc.element.parse-server.RestQuery)
- description and source-code
```javascript
function RestQuery(config, auth, className) {
  var restWhere = arguments.length > 3 && arguments[3] !== undefined ? arguments[3] : {};
  var restOptions = arguments.length > 4 && arguments[4] !== undefined ? arguments[4] : {};
  var clientSDK = arguments[5];


  this.config = config;
  this.auth = auth;
  this.className = className;
  this.restWhere = restWhere;
  this.restOptions = restOptions;
  this.clientSDK = clientSDK;
  this.response = null;
  this.findOptions = {};
  if (!this.auth.isMaster) {
    this.findOptions.acl = this.auth.user ? [this.auth.user.id] : null;
    if (this.className == '_Session') {
      if (!this.findOptions.acl) {
        throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'This session token is invalid.');
      }
      this.restWhere = {
        '$and': [this.restWhere, {
          'user': {
            __type: 'Pointer',
            className: '_User',
            objectId: this.auth.user.id
          }
        }]
      };
    }
  }

  this.doCount = false;

  // The format for this.include is not the same as the format for the
  // include option - it's the paths we should include, in order,
  // stored as arrays, taking into account that we need to include foo
  // before including foo.bar. Also it should dedupe.
  // For example, passing an arg of include=foo.bar,foo.baz could lead to
  // this.include = [['foo'], ['foo', 'baz'], ['foo', 'bar']]
  this.include = [];

  // If we have keys, we probably want to force some includes (n-1 level)
  // See issue: https://github.com/ParsePlatform/parse-server/issues/3185
  if (restOptions.hasOwnProperty('keys')) {
    var keysForInclude = restOptions.keys.split(',').filter(function (key) {
      // At least 2 components
      return key.split(".").length > 1;
    }).map(function (key) {
      // Slice the last component (a.b.c -> a.b)
      // Otherwise we'll include one level too much.
      return key.slice(0, key.lastIndexOf("."));
    }).join(',');

    // Concat the possibly present include string with the one from the keys
    // Dedup / sorting is handle in 'include' case.
    if (keysForInclude.length > 0) {
      if (!restOptions.include || restOptions.include.length == 0) {
        restOptions.include = keysForInclude;
      } else {
        restOptions.include += "," + keysForInclude;
      }
    }
  }

  for (var option in restOptions) {
    switch (option) {
      case 'keys':
        {
          var keys = restOptions.keys.split(',').concat(AlwaysSelectedKeys);
          this.keys = Array.from(new Set(keys));
          break;
        }
      case 'count':
        this.doCount = true;
        break;
      case 'skip':
      case 'limit':
        this.findOptions[option] = restOptions[option];
        break;
      case 'order':
        var fields = restOptions.order.split(',');
        this.findOptions.sort = fields.reduce(function (sortMap, field) {
          field = field.trim();
          if (field[0] == '-') {
            sortMap[field.slice(1)] = -1;
          } else {
            sortMap[field] = 1;
          }
          return sortMap;
        }, {});
        break;
      case 'include':
        {
          var paths = restOptions.include.split(',');
          // Load the existing includes (from keys)
          var pathSet = paths.reduce(function (memo, path) {
            // Split each paths on . (a.b.c -> [a,b,c])
            // reduce to create all paths
            // ([a,b,c] -> {a: true, 'a.b': true, 'a.b.c': true})
            return path.split('.').reduce(function (memo, path, index, parts) {
              memo[parts.slice(0, index + 1).join('.')] = true;
              return memo;
            }, memo);
          }, {});

          this.include = Object.keys(pathSet).map(function (s) {
            return s.split('.');
          }).sort(function (a, b) {
            return a.length - b.length; // Sort by number of components
          });
          break;
        }
      case 'redirectClassNameForKey':
        this.redirectKey = restOptions.redirectClassNameForKey;
        this.redirectClassName = null; ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.RestWrite"></a>[function <span class="apidocSignatureSpan">parse-server.</span>RestWrite (config, auth, className, query, data, originalData, clientSDK)](#apidoc.element.parse-server.RestWrite)
- description and source-code
```javascript
function RestWrite(config, auth, className, query, data, originalData, clientSDK) {
  this.config = config;
  this.auth = auth;
  this.className = className;
  this.clientSDK = clientSDK;
  this.storage = {};
  this.runOptions = {};
  if (!query && data.objectId) {
    throw new Parse.Error(Parse.Error.INVALID_KEY_NAME, 'objectId is an invalid field name.');
  }

  // When the operation is complete, this.response may have several
  // fields.
  // response: the actual data to be returned
  // status: the http status code. if not present, treated like a 200
  // location: the location header. if not present, no location header
  this.response = null;

  // Processing this operation may mutate our data, so we operate on a
  // copy
  this.query = deepcopy(query);
  this.data = deepcopy(data);
  // We never change originalData, so we do not need a deep copy
  this.originalData = originalData;

  // The timestamp we'll use for this whole operation
  this.updatedAt = Parse._encode(new Date()).iso;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.S3Adapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>S3Adapter ()](#apidoc.element.parse-server.S3Adapter)
- description and source-code
```javascript
function S3Adapter() {
  var options = optionsFromArguments(arguments);
  this._region = options.region;
  this._bucket = options.bucket;
  this._bucketPrefix = options.bucketPrefix;
  this._directAccess = options.directAccess;
  this._baseUrl = options.baseUrl;
  this._baseUrlDirect = options.baseUrlDirect;
  this._signatureVersion = options.signatureVersion;
  this._globalCacheControl = options.globalCacheControl;

  let s3Options = {
    params: { Bucket: this._bucket },
    region: this._region,
    signatureVersion: this._signatureVersion,
    globalCacheControl: this._globalCacheControl
  };

  if (options.accessKey && options.secretKey) {
    s3Options.accessKeyId = options.accessKey;
    s3Options.secretAccessKey = options.secretKey;
  }

  Object.assign(s3Options, options.s3overrides);

  this._s3Client = new AWS.S3(s3Options);
  this._hasBucket = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.default"></a>[function <span class="apidocSignatureSpan">parse-server.</span>default (_ref)](#apidoc.element.parse-server.default)
- description and source-code
```javascript
function ParseServer(_ref) {
  var _ref$appId = _ref.appId,
      appId = _ref$appId === undefined ? (0, _requiredParameter2.default)('You must provide an appId!') : _ref$appId,
      _ref$masterKey = _ref.masterKey,
      masterKey = _ref$masterKey === undefined ? (0, _requiredParameter2.default)('You must provide a masterKey!') : _ref$masterKey
,
      appName = _ref.appName,
      analyticsAdapter = _ref.analyticsAdapter,
      filesAdapter = _ref.filesAdapter,
      push = _ref.push,
      loggerAdapter = _ref.loggerAdapter,
      _ref$jsonLogs = _ref.jsonLogs,
      jsonLogs = _ref$jsonLogs === undefined ? _defaults2.default.jsonLogs : _ref$jsonLogs,
      _ref$logsFolder = _ref.logsFolder,
      logsFolder = _ref$logsFolder === undefined ? _defaults2.default.logsFolder : _ref$logsFolder,
      _ref$verbose = _ref.verbose,
      verbose = _ref$verbose === undefined ? _defaults2.default.verbose : _ref$verbose,
      _ref$logLevel = _ref.logLevel,
      logLevel = _ref$logLevel === undefined ? _defaults2.default.level : _ref$logLevel,
      _ref$silent = _ref.silent,
      silent = _ref$silent === undefined ? _defaults2.default.silent : _ref$silent,
      _ref$databaseURI = _ref.databaseURI,
      databaseURI = _ref$databaseURI === undefined ? _defaults2.default.DefaultMongoURI : _ref$databaseURI,
      databaseOptions = _ref.databaseOptions,
      databaseAdapter = _ref.databaseAdapter,
      cloud = _ref.cloud,
      _ref$collectionPrefix = _ref.collectionPrefix,
      collectionPrefix = _ref$collectionPrefix === undefined ? '' : _ref$collectionPrefix,
      clientKey = _ref.clientKey,
      javascriptKey = _ref.javascriptKey,
      dotNetKey = _ref.dotNetKey,
      restAPIKey = _ref.restAPIKey,
      webhookKey = _ref.webhookKey,
      fileKey = _ref.fileKey,
      _ref$userSensitiveFie = _ref.userSensitiveFields,
      userSensitiveFields = _ref$userSensitiveFie === undefined ? [] : _ref$userSensitiveFie,
      _ref$enableAnonymousU = _ref.enableAnonymousUsers,
      enableAnonymousUsers = _ref$enableAnonymousU === undefined ? _defaults2.default.enableAnonymousUsers : _ref$enableAnonymousU
,
      _ref$allowClientClass = _ref.allowClientClassCreation,
      allowClientClassCreation = _ref$allowClientClass === undefined ? _defaults2.default.allowClientClassCreation : _ref$allowClientClass
,
      _ref$oauth = _ref.oauth,
      oauth = _ref$oauth === undefined ? {} : _ref$oauth,
      _ref$auth = _ref.auth,
      auth = _ref$auth === undefined ? {} : _ref$auth,
      _ref$serverURL = _ref.serverURL,
      serverURL = _ref$serverURL === undefined ? (0, _requiredParameter2.default)('You must provide a serverURL!') : _ref$serverURL
,
      _ref$maxUploadSize = _ref.maxUploadSize,
      maxUploadSize = _ref$maxUploadSize === undefined ? _defaults2.default.maxUploadSize : _ref$maxUploadSize,
      _ref$verifyUserEmails = _ref.verifyUserEmails,
      verifyUserEmails = _ref$verifyUserEmails === undefined ? _defaults2.default.verifyUserEmails : _ref$verifyUserEmails,
      _ref$preventLoginWith = _ref.preventLoginWithUnverifiedEmail,
      preventLoginWithUnverifiedEmail = _ref$preventLoginWith === undefined ? _defaults2.default.preventLoginWithUnverifiedEmail
 : _ref$preventLoginWith,
      emailVerifyTokenValidityDuration = _ref.emailVerifyTokenValidityDuration,
      accountLockout = _ref.accountLockout,
      passwordPolicy = _ref.passwordPolicy,
      cacheAdapter = _ref.cacheAdapter,
      emailAdapter = _ref.emailAdapter,
      publicServerURL = _ref.publicServerURL,
      _ref$customPages = _ref.customPages,
      customPages = _ref$customPages === undefined ? {
    invalidLink: undefined,
    verifyEmailSuccess: undefined,
    choosePassword: undefined,
    passwordResetSuccess: undefined
  } : _ref$customPages,
      _ref$liveQuery = _ref.liveQuery,
      liveQuery = _ref$liveQuery === undefined ? {} : _ref$liveQuery,
      _ref$sessionLength = _ref.sessionLength,
      sessionLength = _ref$sessionLength === undefined ? _defaults2.default.sessionLength : _ref$sessionLength,
      _ref$expireInactiveSe = _ref.expi ...
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.AccountLockout"></a>[module parse-server.AccountLockout](#apidoc.module.parse-server.AccountLockout)

#### <a name="apidoc.element.parse-server.AccountLockout.AccountLockout"></a>[function <span class="apidocSignatureSpan">parse-server.</span>AccountLockout (user, config)](#apidoc.element.parse-server.AccountLockout.AccountLockout)
- description and source-code
```javascript
function AccountLockout(user, config) {
  _classCallCheck(this, AccountLockout);

  this._user = user;
  this._config = config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.AccountLockout.default"></a>[function <span class="apidocSignatureSpan">parse-server.AccountLockout.</span>default (user, config)](#apidoc.element.parse-server.AccountLockout.default)
- description and source-code
```javascript
function AccountLockout(user, config) {
  _classCallCheck(this, AccountLockout);

  this._user = user;
  this._config = config;
}
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.Auth"></a>[module parse-server.Auth](#apidoc.module.parse-server.Auth)

#### <a name="apidoc.element.parse-server.Auth.Auth"></a>[function <span class="apidocSignatureSpan">parse-server.</span>Auth ()](#apidoc.element.parse-server.Auth.Auth)
- description and source-code
```javascript
function Auth() {
  var _ref = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {},
      config = _ref.config,
      _ref$isMaster = _ref.isMaster,
      isMaster = _ref$isMaster === undefined ? false : _ref$isMaster,
      user = _ref.user,
      installationId = _ref.installationId;

  this.config = config;
  this.installationId = installationId;
  this.isMaster = isMaster;
  this.user = user;

  // Assuming a users roles won't change during a single request, we'll
  // only load them once.
  this.userRoles = [];
  this.fetchedRoles = false;
  this.rolePromise = null;
}
```
- example usage
```shell
...

function getAuth() {
var options = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {};
var config = arguments[1];

var installationId = options.installationId || 'cloud';
if (options.useMasterKey) {
  return Parse.Promise.as(new Auth.Auth({ config: config, isMaster: true, installationId: installationId }));
}
return getSessionToken(options).then(function (sessionToken) {
  if (sessionToken) {
    options.sessionToken = sessionToken;
    return Auth.getAuthForSessionToken({
      config: config,
      sessionToken: sessionToken,
...
```

#### <a name="apidoc.element.parse-server.Auth.getAuthForLegacySessionToken"></a>[function <span class="apidocSignatureSpan">parse-server.Auth.</span>getAuthForLegacySessionToken ()](#apidoc.element.parse-server.Auth.getAuthForLegacySessionToken)
- description and source-code
```javascript
function getAuthForLegacySessionToken() {
  var _ref3 = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {},
      config = _ref3.config,
      sessionToken = _ref3.sessionToken,
      installationId = _ref3.installationId;

  var restOptions = {
    limit: 1
  };
  var query = new RestQuery(config, master(config), '_User', { sessionToken: sessionToken }, restOptions);
  return query.execute().then(function (response) {
    var results = response.results;
    if (results.length !== 1) {
      throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'invalid legacy session token');
    }
    var obj = results[0];
    obj.className = '_User';
    var userObject = Parse.Object.fromJSON(obj);
    return new Auth({ config: config, isMaster: false, installationId: installationId, user: userObject });
  });
}
```
- example usage
```shell
...
  next();
  return;
}

return Promise.resolve().then(function () {
  // handle the upgradeToRevocableSession path on it's own
  if (info.sessionToken && req.url === '/upgradeToRevocableSession' && info.sessionToken.indexOf('r:') != 0) {
    return _Auth2.default.getAuthForLegacySessionToken({ config: req.config, installationId: info.installationId, sessionToken:
info.sessionToken });
  } else {
    return _Auth2.default.getAuthForSessionToken({ config: req.config, installationId: info.installationId, sessionToken: info.sessionToken
 });
  }
}).then(function (auth) {
  if (auth) {
    req.auth = auth;
    next();
...
```

#### <a name="apidoc.element.parse-server.Auth.getAuthForSessionToken"></a>[function <span class="apidocSignatureSpan">parse-server.Auth.</span>getAuthForSessionToken ()](#apidoc.element.parse-server.Auth.getAuthForSessionToken)
- description and source-code
```javascript
function getAuthForSessionToken() {
  var _ref2 = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {},
      config = _ref2.config,
      sessionToken = _ref2.sessionToken,
      installationId = _ref2.installationId;

  return config.cacheController.user.get(sessionToken).then(function (userJSON) {
    if (userJSON) {
      var cachedUser = Parse.Object.fromJSON(userJSON);
      return Promise.resolve(new Auth({ config: config, isMaster: false, installationId: installationId, user: cachedUser }));
    }

    var restOptions = {
      limit: 1,
      include: 'user'
    };

    var query = new RestQuery(config, master(config), '_Session', { sessionToken: sessionToken }, restOptions);
    return query.execute().then(function (response) {
      var results = response.results;
      if (results.length !== 1 || !results[0]['user']) {
        throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'invalid session token');
      }

      var now = new Date(),
          expiresAt = results[0].expiresAt ? new Date(results[0].expiresAt.iso) : undefined;
      if (expiresAt < now) {
        throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'Session token is expired.');
      }
      var obj = results[0]['user'];
      delete obj.password;
      obj['className'] = '_User';
      obj['sessionToken'] = sessionToken;
      config.cacheController.user.put(sessionToken, obj);
      var userObject = Parse.Object.fromJSON(obj);
      return new Auth({ config: config, isMaster: false, installationId: installationId, user: userObject });
    });
  });
}
```
- example usage
```shell
...
var installationId = options.installationId || 'cloud';
if (options.useMasterKey) {
  return Parse.Promise.as(new Auth.Auth({ config: config, isMaster: true, installationId: installationId }));
}
return getSessionToken(options).then(function (sessionToken) {
  if (sessionToken) {
    options.sessionToken = sessionToken;
    return Auth.getAuthForSessionToken({
      config: config,
      sessionToken: sessionToken,
      installationId: installationId
    });
  } else {
    return Parse.Promise.as(new Auth.Auth({ config: config, installationId: installationId }));
  }
...
```

#### <a name="apidoc.element.parse-server.Auth.master"></a>[function <span class="apidocSignatureSpan">parse-server.Auth.</span>master (config)](#apidoc.element.parse-server.Auth.master)
- description and source-code
```javascript
function master(config) {
  return new Auth({ config: config, isMaster: true });
}
```
- example usage
```shell
...
if (this.className !== '_User') {
  return promise;
}

if (this.query) {
  // If we're updating a _User object, we need to clear out the cache for that user. Find all their
  // session tokens, and remove them from the cache.
  promise = new _RestQuery2.default(this.config, Auth.master(this.config), '_Session', {
    user: {
      __type: "Pointer",
      className: "_User",
      objectId: this.objectId()
    }
  }).execute().then(function (results) {
    results.results.forEach(function (session) {
...
```

#### <a name="apidoc.element.parse-server.Auth.nobody"></a>[function <span class="apidocSignatureSpan">parse-server.Auth.</span>nobody (config)](#apidoc.element.parse-server.Auth.nobody)
- description and source-code
```javascript
function nobody(config) {
  return new Auth({ config: config, isMaster: false });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.ClientSDK"></a>[module parse-server.ClientSDK](#apidoc.module.parse-server.ClientSDK)

#### <a name="apidoc.element.parse-server.ClientSDK.compatible"></a>[function <span class="apidocSignatureSpan">parse-server.ClientSDK.</span>compatible (compatibleSDK)](#apidoc.element.parse-server.ClientSDK.compatible)
- description and source-code
```javascript
function compatible(compatibleSDK) {
  return function (clientSDK) {
    if (typeof clientSDK === 'string') {
      clientSDK = fromString(clientSDK);
    }
    // REST API, or custom SDK
    if (!clientSDK) {
      return true;
    }
    var clientVersion = clientSDK.version;
    var compatiblityVersion = compatibleSDK[clientSDK.sdk];
    return semver.satisfies(clientVersion, compatiblityVersion);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.ClientSDK.fromString"></a>[function <span class="apidocSignatureSpan">parse-server.ClientSDK.</span>fromString (version)](#apidoc.element.parse-server.ClientSDK.fromString)
- description and source-code
```javascript
function fromString(version) {
  var versionRE = /([-a-zA-Z]+)([0-9\.]+)/;
  var match = version.toLowerCase().match(versionRE);
  if (match && match.length === 3) {
    return {
      sdk: match[1],
      version: match[2]
    };
  }
  return undefined;
}
```
- example usage
```shell
...
    }
  } else {
    return invalidRequest(req, res);
  }
}

if (info.clientVersion) {
  info.clientSDK = _ClientSDK2.default.fromString(info.clientVersion);
}

if (fileViaJSON) {
  // We need to repopulate req.body with a buffer
  var base64 = req.body.base64;
  req.body = new Buffer(base64, 'base64');
}
...
```

#### <a name="apidoc.element.parse-server.ClientSDK.supportsForwardDelete"></a>[function <span class="apidocSignatureSpan">parse-server.ClientSDK.</span>supportsForwardDelete (clientSDK)](#apidoc.element.parse-server.ClientSDK.supportsForwardDelete)
- description and source-code
```javascript
function supportsForwardDelete(clientSDK) {
  return compatible({
    js: '>=1.9.0'
  })(clientSDK);
}
```
- example usage
```shell
...
  }
};

RestWrite.prototype._updateResponseWithData = function (response, data) {
  if (_lodash2.default.isEmpty(this.storage.fieldsChangedByTrigger)) {
return response;
  }
  var clientSupportsDelete = ClientSDK.supportsForwardDelete(this.clientSDK);
  this.storage.fieldsChangedByTrigger.forEach(function (fieldName) {
var dataValue = data[fieldName];
var responseValue = response[fieldName];

response[fieldName] = responseValue || dataValue;

// Strips operations from responses
...
```



# <a name="apidoc.module.parse-server.FileSystemAdapter"></a>[module parse-server.FileSystemAdapter](#apidoc.module.parse-server.FileSystemAdapter)

#### <a name="apidoc.element.parse-server.FileSystemAdapter.FileSystemAdapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>FileSystemAdapter (options)](#apidoc.element.parse-server.FileSystemAdapter.FileSystemAdapter)
- description and source-code
```javascript
function FileSystemAdapter(options) {
  options = options || {};
  let filesSubDirectory = options.filesSubDirectory || '';
  this._filesDir = filesSubDirectory;
  this._mkdir(this._getApplicationDir());
  if (!this._applicationDirExist()) {
    throw "Files directory doesn't exist.";
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.default"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.</span>default (options)](#apidoc.element.parse-server.FileSystemAdapter.default)
- description and source-code
```javascript
function FileSystemAdapter(options) {
  options = options || {};
  let filesSubDirectory = options.filesSubDirectory || '';
  this._filesDir = filesSubDirectory;
  this._mkdir(this._getApplicationDir());
  if (!this._applicationDirExist()) {
    throw "Files directory doesn't exist.";
  }
}
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.FileSystemAdapter.prototype"></a>[module parse-server.FileSystemAdapter.prototype](#apidoc.module.parse-server.FileSystemAdapter.prototype)

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype._applicationDirExist"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_applicationDirExist ()](#apidoc.element.parse-server.FileSystemAdapter.prototype._applicationDirExist)
- description and source-code
```javascript
_applicationDirExist = function () {
  return fs.existsSync(this._getApplicationDir());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype._getApplicationDir"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_getApplicationDir ()](#apidoc.element.parse-server.FileSystemAdapter.prototype._getApplicationDir)
- description and source-code
```javascript
_getApplicationDir = function () {
 if (this._filesDir) {
   return path.join('files', this._filesDir);
 } else {
   return 'files';
 }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype._getLocalFilePath"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_getLocalFilePath (filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype._getLocalFilePath)
- description and source-code
```javascript
_getLocalFilePath = function (filename) {
  let applicationDir = this._getApplicationDir();
  if (!fs.existsSync(applicationDir)) {
    this._mkdir(applicationDir);
  }
  return path.join(applicationDir, encodeURIComponent(filename));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype._mkdir"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>_mkdir (dirPath)](#apidoc.element.parse-server.FileSystemAdapter.prototype._mkdir)
- description and source-code
```javascript
_mkdir = function (dirPath) {
  // snippet found on -> https://gist.github.com/danherbert-epam/3960169
  let dirs = dirPath.split(pathSep);
  var root = "";

  while (dirs.length > 0) {
    var dir = dirs.shift();
    if (dir === "") { // If directory starts with a /, the first path will be an empty string.
      root = pathSep;
    }
    if (!fs.existsSync(path.join(root, dir))) {
      try {
        fs.mkdirSync(path.join(root, dir));
      }
      catch (e) {
        if ( e.code == 'EACCES' ) {
          throw new Error("PERMISSION ERROR: In order to use the FileSystemAdapter, write access to the server's file system is
required.");
        }
      }
    }
    root = path.join(root, dir, pathSep);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype.createFile"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>createFile (filename, data)](#apidoc.element.parse-server.FileSystemAdapter.prototype.createFile)
- description and source-code
```javascript
createFile = function (filename, data) {
  return new Promise((resolve, reject) => {
    let filepath = this._getLocalFilePath(filename);
    fs.writeFile(filepath, data, (err) => {
      if(err !== null) {
        return reject(err);
      }
      resolve(data);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype.deleteFile"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>deleteFile (filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype.deleteFile)
- description and source-code
```javascript
deleteFile = function (filename) {
  return new Promise((resolve, reject) => {
    let filepath = this._getLocalFilePath(filename);
    fs.readFile( filepath , function (err, data) {
      if(err !== null) {
        return reject(err);
      }
      fs.unlink(filepath, (unlinkErr) => {
      if(err !== null) {
          return reject(unlinkErr);
        }
        resolve(data);
      });
    });

  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype.getFileData"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>getFileData (filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype.getFileData)
- description and source-code
```javascript
getFileData = function (filename) {
  return new Promise((resolve, reject) => {
    let filepath = this._getLocalFilePath(filename);
    fs.readFile( filepath , function (err, data) {
      if(err !== null) {
        return reject(err);
      }
      resolve(data);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.FileSystemAdapter.prototype.getFileLocation"></a>[function <span class="apidocSignatureSpan">parse-server.FileSystemAdapter.prototype.</span>getFileLocation (config, filename)](#apidoc.element.parse-server.FileSystemAdapter.prototype.getFileLocation)
- description and source-code
```javascript
getFileLocation = function (config, filename) {
  return config.mount + '/files/' + config.applicationId + '/' + encodeURIComponent(filename);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.ParseServer"></a>[module parse-server.ParseServer](#apidoc.module.parse-server.ParseServer)

#### <a name="apidoc.element.parse-server.ParseServer.ParseServer"></a>[function <span class="apidocSignatureSpan">parse-server.</span>ParseServer (options)](#apidoc.element.parse-server.ParseServer.ParseServer)
- description and source-code
```javascript
function _ParseServer(options) {
  var server = new _ParseServer3.default(options);
  return server.app;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.ParseServer.createLiveQueryServer"></a>[function <span class="apidocSignatureSpan">parse-server.ParseServer.</span>createLiveQueryServer (httpServer, config)](#apidoc.element.parse-server.ParseServer.createLiveQueryServer)
- description and source-code
```javascript
function createLiveQueryServer(httpServer, config) {
  return new _ParseLiveQueryServer.ParseLiveQueryServer(httpServer, config);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.ParseServerRESTController"></a>[module parse-server.ParseServerRESTController](#apidoc.module.parse-server.ParseServerRESTController)

#### <a name="apidoc.element.parse-server.ParseServerRESTController.ParseServerRESTController"></a>[function <span class="apidocSignatureSpan">parse-server.</span>ParseServerRESTController (applicationId, router)](#apidoc.element.parse-server.ParseServerRESTController.ParseServerRESTController)
- description and source-code
```javascript
function ParseServerRESTController(applicationId, router) {
  function handleRequest(method, path) {
    var data = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : {};
    var options = arguments.length > 3 && arguments[3] !== undefined ? arguments[3] : {};

    // Store the arguments, for later use if internal fails
    var args = arguments;

    var config = new Config(applicationId);
    var serverURL = URL.parse(config.serverURL);
    if (path.indexOf(serverURL.path) === 0) {
      path = path.slice(serverURL.path.length, path.length);
    }

    if (path[0] !== "/") {
      path = "/" + path;
    }

    if (path === '/batch') {
      var promises = data.requests.map(function (request) {
        return handleRequest(request.method, request.path, request.body, options).then(function (response) {
          return Parse.Promise.as({ success: response });
        }, function (error) {
          return Parse.Promise.as({ error: { code: error.code, error: error.message } });
        });
      });
      return Parse.Promise.all(promises);
    }

    var query = void 0;
    if (method === 'GET') {
      query = data;
    }

    return new Parse.Promise(function (resolve, reject) {
      getAuth(options, config).then(function (auth) {
        var request = {
          body: data,
          config: config,
          auth: auth,
          info: {
            applicationId: applicationId,
            sessionToken: options.sessionToken
          },
          query: query
        };
        return Promise.resolve().then(function () {
          return router.tryRouteRequest(method, path, request);
        }).then(function (response) {
          resolve(response.response, response.status, response);
        }, function (err) {
          if (err instanceof Parse.Error && err.code == Parse.Error.INVALID_JSON && err.message == 'cannot route ' + method + ' ' +
path) {
            RESTController.request.apply(null, args).then(resolve, reject);
          } else {
            reject(err);
          }
        });
      }, reject);
    });
  }

  return {
    request: handleRequest,
    ajax: RESTController.ajax
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.ParseServerRESTController.default"></a>[function <span class="apidocSignatureSpan">parse-server.ParseServerRESTController.</span>default (applicationId, router)](#apidoc.element.parse-server.ParseServerRESTController.default)
- description and source-code
```javascript
function ParseServerRESTController(applicationId, router) {
  function handleRequest(method, path) {
    var data = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : {};
    var options = arguments.length > 3 && arguments[3] !== undefined ? arguments[3] : {};

    // Store the arguments, for later use if internal fails
    var args = arguments;

    var config = new Config(applicationId);
    var serverURL = URL.parse(config.serverURL);
    if (path.indexOf(serverURL.path) === 0) {
      path = path.slice(serverURL.path.length, path.length);
    }

    if (path[0] !== "/") {
      path = "/" + path;
    }

    if (path === '/batch') {
      var promises = data.requests.map(function (request) {
        return handleRequest(request.method, request.path, request.body, options).then(function (response) {
          return Parse.Promise.as({ success: response });
        }, function (error) {
          return Parse.Promise.as({ error: { code: error.code, error: error.message } });
        });
      });
      return Parse.Promise.all(promises);
    }

    var query = void 0;
    if (method === 'GET') {
      query = data;
    }

    return new Parse.Promise(function (resolve, reject) {
      getAuth(options, config).then(function (auth) {
        var request = {
          body: data,
          config: config,
          auth: auth,
          info: {
            applicationId: applicationId,
            sessionToken: options.sessionToken
          },
          query: query
        };
        return Promise.resolve().then(function () {
          return router.tryRouteRequest(method, path, request);
        }).then(function (response) {
          resolve(response.response, response.status, response);
        }, function (err) {
          if (err instanceof Parse.Error && err.code == Parse.Error.INVALID_JSON && err.message == 'cannot route ' + method + ' ' +
path) {
            RESTController.request.apply(null, args).then(resolve, reject);
          } else {
            reject(err);
          }
        });
      }, reject);
    });
  }

  return {
    request: handleRequest,
    ajax: RESTController.ajax
  };
}
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.PromiseRouter"></a>[module parse-server.PromiseRouter](#apidoc.module.parse-server.PromiseRouter)

#### <a name="apidoc.element.parse-server.PromiseRouter.default"></a>[function <span class="apidocSignatureSpan">parse-server.PromiseRouter.</span>default ()](#apidoc.element.parse-server.PromiseRouter.default)
- description and source-code
```javascript
function PromiseRouter() {
  var routes = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : [];
  var appId = arguments[1];

  _classCallCheck(this, PromiseRouter);

  this.routes = routes;
  this.appId = appId;
  this.mountRoutes();
}
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.RestQuery"></a>[module parse-server.RestQuery](#apidoc.module.parse-server.RestQuery)

#### <a name="apidoc.element.parse-server.RestQuery.RestQuery"></a>[function <span class="apidocSignatureSpan">parse-server.</span>RestQuery (config, auth, className)](#apidoc.element.parse-server.RestQuery.RestQuery)
- description and source-code
```javascript
function RestQuery(config, auth, className) {
  var restWhere = arguments.length > 3 && arguments[3] !== undefined ? arguments[3] : {};
  var restOptions = arguments.length > 4 && arguments[4] !== undefined ? arguments[4] : {};
  var clientSDK = arguments[5];


  this.config = config;
  this.auth = auth;
  this.className = className;
  this.restWhere = restWhere;
  this.restOptions = restOptions;
  this.clientSDK = clientSDK;
  this.response = null;
  this.findOptions = {};
  if (!this.auth.isMaster) {
    this.findOptions.acl = this.auth.user ? [this.auth.user.id] : null;
    if (this.className == '_Session') {
      if (!this.findOptions.acl) {
        throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'This session token is invalid.');
      }
      this.restWhere = {
        '$and': [this.restWhere, {
          'user': {
            __type: 'Pointer',
            className: '_User',
            objectId: this.auth.user.id
          }
        }]
      };
    }
  }

  this.doCount = false;

  // The format for this.include is not the same as the format for the
  // include option - it's the paths we should include, in order,
  // stored as arrays, taking into account that we need to include foo
  // before including foo.bar. Also it should dedupe.
  // For example, passing an arg of include=foo.bar,foo.baz could lead to
  // this.include = [['foo'], ['foo', 'baz'], ['foo', 'bar']]
  this.include = [];

  // If we have keys, we probably want to force some includes (n-1 level)
  // See issue: https://github.com/ParsePlatform/parse-server/issues/3185
  if (restOptions.hasOwnProperty('keys')) {
    var keysForInclude = restOptions.keys.split(',').filter(function (key) {
      // At least 2 components
      return key.split(".").length > 1;
    }).map(function (key) {
      // Slice the last component (a.b.c -> a.b)
      // Otherwise we'll include one level too much.
      return key.slice(0, key.lastIndexOf("."));
    }).join(',');

    // Concat the possibly present include string with the one from the keys
    // Dedup / sorting is handle in 'include' case.
    if (keysForInclude.length > 0) {
      if (!restOptions.include || restOptions.include.length == 0) {
        restOptions.include = keysForInclude;
      } else {
        restOptions.include += "," + keysForInclude;
      }
    }
  }

  for (var option in restOptions) {
    switch (option) {
      case 'keys':
        {
          var keys = restOptions.keys.split(',').concat(AlwaysSelectedKeys);
          this.keys = Array.from(new Set(keys));
          break;
        }
      case 'count':
        this.doCount = true;
        break;
      case 'skip':
      case 'limit':
        this.findOptions[option] = restOptions[option];
        break;
      case 'order':
        var fields = restOptions.order.split(',');
        this.findOptions.sort = fields.reduce(function (sortMap, field) {
          field = field.trim();
          if (field[0] == '-') {
            sortMap[field.slice(1)] = -1;
          } else {
            sortMap[field] = 1;
          }
          return sortMap;
        }, {});
        break;
      case 'include':
        {
          var paths = restOptions.include.split(',');
          // Load the existing includes (from keys)
          var pathSet = paths.reduce(function (memo, path) {
            // Split each paths on . (a.b.c -> [a,b,c])
            // reduce to create all paths
            // ([a,b,c] -> {a: true, 'a.b': true, 'a.b.c': true})
            return path.split('.').reduce(function (memo, path, index, parts) {
              memo[parts.slice(0, index + 1).join('.')] = true;
              return memo;
            }, memo);
          }, {});

          this.include = Object.keys(pathSet).map(function (s) {
            return s.split('.');
          }).sort(function (a, b) {
            return a.length - b.length; // Sort by number of components
          });
          break;
        }
      case 'redirectClassNameForKey':
        this.redirectKey = restOptions.redirectClassNameForKey;
        this.redirectClassName = null; ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.RestQuery.prototype"></a>[module parse-server.RestQuery.prototype](#apidoc.module.parse-server.RestQuery.prototype)

#### <a name="apidoc.element.parse-server.RestQuery.prototype.buildRestWhere"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>buildRestWhere ()](#apidoc.element.parse-server.RestQuery.prototype.buildRestWhere)
- description and source-code
```javascript
buildRestWhere = function () {
  var _this2 = this;

  return Promise.resolve().then(function () {
    return _this2.getUserAndRoleACL();
  }).then(function () {
    return _this2.redirectClassNameForKey();
  }).then(function () {
    return _this2.validateClientClassCreation();
  }).then(function () {
    return _this2.replaceSelect();
  }).then(function () {
    return _this2.replaceDontSelect();
  }).then(function () {
    return _this2.replaceInQuery();
  }).then(function () {
    return _this2.replaceNotInQuery();
  });
}
```
- example usage
```shell
...
// Returns a promise for the response - an object with optional keys
// 'results' and 'count'.
// TODO: consolidate the replaceX functions
RestQuery.prototype.execute = function (executeOptions) {
var _this = this;

return Promise.resolve().then(function () {
  return _this.buildRestWhere();
}).then(function () {
  return _this.runFind(executeOptions);
}).then(function () {
  return _this.runCount();
}).then(function () {
  return _this.handleInclude();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.execute"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>execute (executeOptions)](#apidoc.element.parse-server.RestQuery.prototype.execute)
- description and source-code
```javascript
execute = function (executeOptions) {
  var _this = this;

  return Promise.resolve().then(function () {
    return _this.buildRestWhere();
  }).then(function () {
    return _this.runFind(executeOptions);
  }).then(function () {
    return _this.runCount();
  }).then(function () {
    return _this.handleInclude();
  }).then(function () {
    return _this.runAfterFindTrigger();
  }).then(function () {
    return _this.response;
  });
}
```
- example usage
```shell
...

    var restOptions = {
limit: 1,
include: 'user'
    };

    var query = new RestQuery(config, master(config), '_Session', { sessionToken: sessionToken }, restOptions);
    return query.execute().then(function (response) {
var results = response.results;
if (results.length !== 1 || !results[0]['user']) {
  throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'invalid session token');
}

var now = new Date(),
    expiresAt = results[0].expiresAt ? new Date(results[0].expiresAt.iso) : undefined;
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.getUserAndRoleACL"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>getUserAndRoleACL ()](#apidoc.element.parse-server.RestQuery.prototype.getUserAndRoleACL)
- description and source-code
```javascript
getUserAndRoleACL = function () {
  var _this3 = this;

  if (this.auth.isMaster || !this.auth.user) {
    return Promise.resolve();
  }
  return this.auth.getUserRoles().then(function (roles) {
    // Concat with the roles to prevent duplications on multiple calls
    var aclSet = new Set([].concat(_this3.findOptions.acl, roles));
    _this3.findOptions.acl = Array.from(aclSet);
    return Promise.resolve();
  });
}
```
- example usage
```shell
...
});
};

RestQuery.prototype.buildRestWhere = function () {
var _this2 = this;

return Promise.resolve().then(function () {
  return _this2.getUserAndRoleACL();
}).then(function () {
  return _this2.redirectClassNameForKey();
}).then(function () {
  return _this2.validateClientClassCreation();
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.handleInclude"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>handleInclude ()](#apidoc.element.parse-server.RestQuery.prototype.handleInclude)
- description and source-code
```javascript
handleInclude = function () {
  var _this12 = this;

  if (this.include.length == 0) {
    return;
  }

  var pathResponse = includePath(this.config, this.auth, this.response, this.include[0], this.restOptions);
  if (pathResponse.then) {
    return pathResponse.then(function (newResponse) {
      _this12.response = newResponse;
      _this12.include = _this12.include.slice(1);
      return _this12.handleInclude();
    });
  } else if (this.include.length > 0) {
    this.include = this.include.slice(1);
    return this.handleInclude();
  }

  return pathResponse;
}
```
- example usage
```shell
...
  return Promise.resolve().then(function () {
    return _this.buildRestWhere();
  }).then(function () {
    return _this.runFind(executeOptions);
  }).then(function () {
    return _this.runCount();
  }).then(function () {
    return _this.handleInclude();
  }).then(function () {
    return _this.runAfterFindTrigger();
  }).then(function () {
    return _this.response;
  });
};
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.redirectClassNameForKey"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>redirectClassNameForKey ()](#apidoc.element.parse-server.RestQuery.prototype.redirectClassNameForKey)
- description and source-code
```javascript
redirectClassNameForKey = function () {
  var _this4 = this;

  if (!this.redirectKey) {
    return Promise.resolve();
  }

  // We need to change the class name based on the schema
  return this.config.database.redirectClassNameForKey(this.className, this.redirectKey).then(function (newClassName) {
    _this4.className = newClassName;
    _this4.redirectClassName = newClassName;
  });
}
```
- example usage
```shell
...

RestQuery.prototype.buildRestWhere = function () {
var _this2 = this;

return Promise.resolve().then(function () {
  return _this2.getUserAndRoleACL();
}).then(function () {
  return _this2.redirectClassNameForKey();
}).then(function () {
  return _this2.validateClientClassCreation();
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
  return _this2.replaceDontSelect();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.replaceDontSelect"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceDontSelect ()](#apidoc.element.parse-server.RestQuery.prototype.replaceDontSelect)
- description and source-code
```javascript
replaceDontSelect = function () {
  var _this9 = this;

  var dontSelectObject = findObjectWithKey(this.restWhere, '$dontSelect');
  if (!dontSelectObject) {
    return;
  }

  // The dontSelect value must have precisely two keys - query and key
  var dontSelectValue = dontSelectObject['$dontSelect'];
  if (!dontSelectValue.query || !dontSelectValue.key || _typeof(dontSelectValue.query) !== 'object' || !dontSelectValue.query.className
 || Object.keys(dontSelectValue).length !== 2) {
    throw new Parse.Error(Parse.Error.INVALID_QUERY, 'improper usage of $dontSelect');
  }
  var additionalOptions = {
    redirectClassNameForKey: dontSelectValue.query.redirectClassNameForKey
  };

  var subquery = new RestQuery(this.config, this.auth, dontSelectValue.query.className, dontSelectValue.query.where, additionalOptions
);
  return subquery.execute().then(function (response) {
    transformDontSelect(dontSelectObject, dontSelectValue.key, response.results);
    // Keep replacing $dontSelect clauses
    return _this9.replaceDontSelect();
  });
}
```
- example usage
```shell
...
  }).then(function () {
    return _this2.redirectClassNameForKey();
  }).then(function () {
    return _this2.validateClientClassCreation();
  }).then(function () {
    return _this2.replaceSelect();
  }).then(function () {
    return _this2.replaceDontSelect();
  }).then(function () {
    return _this2.replaceInQuery();
  }).then(function () {
    return _this2.replaceNotInQuery();
  });
};
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.replaceInQuery"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceInQuery ()](#apidoc.element.parse-server.RestQuery.prototype.replaceInQuery)
- description and source-code
```javascript
replaceInQuery = function () {
  var _this6 = this;

  var inQueryObject = findObjectWithKey(this.restWhere, '$inQuery');
  if (!inQueryObject) {
    return;
  }

  // The inQuery value must have precisely two keys - where and className
  var inQueryValue = inQueryObject['$inQuery'];
  if (!inQueryValue.where || !inQueryValue.className) {
    throw new Parse.Error(Parse.Error.INVALID_QUERY, 'improper usage of $inQuery');
  }

  var additionalOptions = {
    redirectClassNameForKey: inQueryValue.redirectClassNameForKey
  };

  var subquery = new RestQuery(this.config, this.auth, inQueryValue.className, inQueryValue.where, additionalOptions);
  return subquery.execute().then(function (response) {
    transformInQuery(inQueryObject, subquery.className, response.results);
    // Recurse to repeat
    return _this6.replaceInQuery();
  });
}
```
- example usage
```shell
...
  }).then(function () {
    return _this2.validateClientClassCreation();
  }).then(function () {
    return _this2.replaceSelect();
  }).then(function () {
    return _this2.replaceDontSelect();
  }).then(function () {
    return _this2.replaceInQuery();
  }).then(function () {
    return _this2.replaceNotInQuery();
  });
};

// Uses the Auth object to get the list of roles, adds the user id
RestQuery.prototype.getUserAndRoleACL = function () {
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.replaceNotInQuery"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceNotInQuery ()](#apidoc.element.parse-server.RestQuery.prototype.replaceNotInQuery)
- description and source-code
```javascript
replaceNotInQuery = function () {
  var _this7 = this;

  var notInQueryObject = findObjectWithKey(this.restWhere, '$notInQuery');
  if (!notInQueryObject) {
    return;
  }

  // The notInQuery value must have precisely two keys - where and className
  var notInQueryValue = notInQueryObject['$notInQuery'];
  if (!notInQueryValue.where || !notInQueryValue.className) {
    throw new Parse.Error(Parse.Error.INVALID_QUERY, 'improper usage of $notInQuery');
  }

  var additionalOptions = {
    redirectClassNameForKey: notInQueryValue.redirectClassNameForKey
  };

  var subquery = new RestQuery(this.config, this.auth, notInQueryValue.className, notInQueryValue.where, additionalOptions);
  return subquery.execute().then(function (response) {
    transformNotInQuery(notInQueryObject, subquery.className, response.results);
    // Recurse to repeat
    return _this7.replaceNotInQuery();
  });
}
```
- example usage
```shell
...
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
  return _this2.replaceDontSelect();
}).then(function () {
  return _this2.replaceInQuery();
}).then(function () {
  return _this2.replaceNotInQuery();
});
};

// Uses the Auth object to get the list of roles, adds the user id
RestQuery.prototype.getUserAndRoleACL = function () {
var _this3 = this;
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.replaceSelect"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>replaceSelect ()](#apidoc.element.parse-server.RestQuery.prototype.replaceSelect)
- description and source-code
```javascript
replaceSelect = function () {
  var _this8 = this;

  var selectObject = findObjectWithKey(this.restWhere, '$select');
  if (!selectObject) {
    return;
  }

  // The select value must have precisely two keys - query and key
  var selectValue = selectObject['$select'];
  // iOS SDK don't send where if not set, let it pass
  if (!selectValue.query || !selectValue.key || _typeof(selectValue.query) !== 'object' || !selectValue.query.className || Object
.keys(selectValue).length !== 2) {
    throw new Parse.Error(Parse.Error.INVALID_QUERY, 'improper usage of $select');
  }

  var additionalOptions = {
    redirectClassNameForKey: selectValue.query.redirectClassNameForKey
  };

  var subquery = new RestQuery(this.config, this.auth, selectValue.query.className, selectValue.query.where, additionalOptions);
  return subquery.execute().then(function (response) {
    transformSelect(selectObject, selectValue.key, response.results);
    // Keep replacing $select clauses
    return _this8.replaceSelect();
  });
}
```
- example usage
```shell
...
return Promise.resolve().then(function () {
  return _this2.getUserAndRoleACL();
}).then(function () {
  return _this2.redirectClassNameForKey();
}).then(function () {
  return _this2.validateClientClassCreation();
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
  return _this2.replaceDontSelect();
}).then(function () {
  return _this2.replaceInQuery();
}).then(function () {
  return _this2.replaceNotInQuery();
});
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.runAfterFindTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>runAfterFindTrigger ()](#apidoc.element.parse-server.RestQuery.prototype.runAfterFindTrigger)
- description and source-code
```javascript
runAfterFindTrigger = function () {
  var _this13 = this;

  if (!this.response) {
    return;
  }
  // Avoid doing any setup for triggers if there is no 'afterFind' trigger for this class.
  var hasAfterFindHook = triggers.triggerExists(this.className, triggers.Types.afterFind, this.config.applicationId);
  if (!hasAfterFindHook) {
    return Promise.resolve();
  }
  // Run afterFind trigger and set the new results
  return triggers.maybeRunAfterFindTrigger(triggers.Types.afterFind, this.auth, this.className, this.response.results, this.config
).then(function (results) {
    _this13.response.results = results;
  });
}
```
- example usage
```shell
...
}).then(function () {
  return _this.runFind(executeOptions);
}).then(function () {
  return _this.runCount();
}).then(function () {
  return _this.handleInclude();
}).then(function () {
  return _this.runAfterFindTrigger();
}).then(function () {
  return _this.response;
});
};

RestQuery.prototype.buildRestWhere = function () {
var _this2 = this;
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.runCount"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>runCount ()](#apidoc.element.parse-server.RestQuery.prototype.runCount)
- description and source-code
```javascript
runCount = function () {
  var _this11 = this;

  if (!this.doCount) {
    return;
  }
  this.findOptions.count = true;
  delete this.findOptions.skip;
  delete this.findOptions.limit;
  return this.config.database.find(this.className, this.restWhere, this.findOptions).then(function (c) {
    _this11.response.count = c;
  });
}
```
- example usage
```shell
...
var _this = this;

return Promise.resolve().then(function () {
  return _this.buildRestWhere();
}).then(function () {
  return _this.runFind(executeOptions);
}).then(function () {
  return _this.runCount();
}).then(function () {
  return _this.handleInclude();
}).then(function () {
  return _this.runAfterFindTrigger();
}).then(function () {
  return _this.response;
});
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.runFind"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>runFind ()](#apidoc.element.parse-server.RestQuery.prototype.runFind)
- description and source-code
```javascript
runFind = function () {
  var _this10 = this;

  var options = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {};

  if (this.findOptions.limit === 0) {
    this.response = { results: [] };
    return Promise.resolve();
  }
  var findOptions = Object.assign({}, this.findOptions);
  if (this.keys) {
    findOptions.keys = this.keys.map(function (key) {
      return key.split('.')[0];
    });
  }
  if (options.op) {
    findOptions.op = options.op;
  }
  return this.config.database.find(this.className, this.restWhere, findOptions).then(function (results) {
    if (_this10.className === '_User') {
      var _iteratorNormalCompletion6 = true;
      var _didIteratorError6 = false;
      var _iteratorError6 = undefined;

      try {
        for (var _iterator6 = results[Symbol.iterator](), _step6; !(_iteratorNormalCompletion6 = (_step6 = _iterator6.next()).done
); _iteratorNormalCompletion6 = true) {
          var result = _step6.value;

          cleanResultOfSensitiveUserInfo(result, _this10.auth, _this10.config);
          cleanResultAuthData(result);
        }
      } catch (err) {
        _didIteratorError6 = true;
        _iteratorError6 = err;
      } finally {
        try {
          if (!_iteratorNormalCompletion6 && _iterator6.return) {
            _iterator6.return();
          }
        } finally {
          if (_didIteratorError6) {
            throw _iteratorError6;
          }
        }
      }
    }

    _this10.config.filesController.expandFilesInObject(_this10.config, results);

    if (_this10.redirectClassName) {
      var _iteratorNormalCompletion7 = true;
      var _didIteratorError7 = false;
      var _iteratorError7 = undefined;

      try {
        for (var _iterator7 = results[Symbol.iterator](), _step7; !(_iteratorNormalCompletion7 = (_step7 = _iterator7.next()).done
); _iteratorNormalCompletion7 = true) {
          var r = _step7.value;

          r.className = _this10.redirectClassName;
        }
      } catch (err) {
        _didIteratorError7 = true;
        _iteratorError7 = err;
      } finally {
        try {
          if (!_iteratorNormalCompletion7 && _iterator7.return) {
            _iterator7.return();
          }
        } finally {
          if (_didIteratorError7) {
            throw _iteratorError7;
          }
        }
      }
    }
    _this10.response = { results: results };
  });
}
```
- example usage
```shell
...
// TODO: consolidate the replaceX functions
RestQuery.prototype.execute = function (executeOptions) {
var _this = this;

return Promise.resolve().then(function () {
  return _this.buildRestWhere();
}).then(function () {
  return _this.runFind(executeOptions);
}).then(function () {
  return _this.runCount();
}).then(function () {
  return _this.handleInclude();
}).then(function () {
  return _this.runAfterFindTrigger();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestQuery.prototype.validateClientClassCreation"></a>[function <span class="apidocSignatureSpan">parse-server.RestQuery.prototype.</span>validateClientClassCreation ()](#apidoc.element.parse-server.RestQuery.prototype.validateClientClassCreation)
- description and source-code
```javascript
validateClientClassCreation = function () {
  var _this5 = this;

  if (this.config.allowClientClassCreation === false && !this.auth.isMaster && SchemaController.systemClasses.indexOf(this.className
) === -1) {
    return this.config.database.loadSchema().then(function (schemaController) {
      return schemaController.hasClass(_this5.className);
    }).then(function (hasClass) {
      if (hasClass !== true) {
        throw new Parse.Error(Parse.Error.OPERATION_FORBIDDEN, 'This user is not allowed to access ' + 'non-existent class: ' +
_this5.className);
      }
    });
  } else {
    return Promise.resolve();
  }
}
```
- example usage
```shell
...
var _this2 = this;

return Promise.resolve().then(function () {
  return _this2.getUserAndRoleACL();
}).then(function () {
  return _this2.redirectClassNameForKey();
}).then(function () {
  return _this2.validateClientClassCreation();
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
  return _this2.replaceDontSelect();
}).then(function () {
  return _this2.replaceInQuery();
}).then(function () {
...
```



# <a name="apidoc.module.parse-server.RestWrite"></a>[module parse-server.RestWrite](#apidoc.module.parse-server.RestWrite)

#### <a name="apidoc.element.parse-server.RestWrite.RestWrite"></a>[function <span class="apidocSignatureSpan">parse-server.</span>RestWrite (config, auth, className, query, data, originalData, clientSDK)](#apidoc.element.parse-server.RestWrite.RestWrite)
- description and source-code
```javascript
function RestWrite(config, auth, className, query, data, originalData, clientSDK) {
  this.config = config;
  this.auth = auth;
  this.className = className;
  this.clientSDK = clientSDK;
  this.storage = {};
  this.runOptions = {};
  if (!query && data.objectId) {
    throw new Parse.Error(Parse.Error.INVALID_KEY_NAME, 'objectId is an invalid field name.');
  }

  // When the operation is complete, this.response may have several
  // fields.
  // response: the actual data to be returned
  // status: the http status code. if not present, treated like a 200
  // location: the location header. if not present, no location header
  this.response = null;

  // Processing this operation may mutate our data, so we operate on a
  // copy
  this.query = deepcopy(query);
  this.data = deepcopy(data);
  // We never change originalData, so we do not need a deep copy
  this.originalData = originalData;

  // The timestamp we'll use for this whole operation
  this.updatedAt = Parse._encode(new Date()).iso;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.RestWrite.prototype"></a>[module parse-server.RestWrite.prototype](#apidoc.module.parse-server.RestWrite.prototype)

#### <a name="apidoc.element.parse-server.RestWrite.prototype._updateResponseWithData"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_updateResponseWithData (response, data)](#apidoc.element.parse-server.RestWrite.prototype._updateResponseWithData)
- description and source-code
```javascript
_updateResponseWithData = function (response, data) {
  if (_lodash2.default.isEmpty(this.storage.fieldsChangedByTrigger)) {
    return response;
  }
  var clientSupportsDelete = ClientSDK.supportsForwardDelete(this.clientSDK);
  this.storage.fieldsChangedByTrigger.forEach(function (fieldName) {
    var dataValue = data[fieldName];
    var responseValue = response[fieldName];

    response[fieldName] = responseValue || dataValue;

    // Strips operations from responses
    if (response[fieldName] && response[fieldName].__op) {
      delete response[fieldName];
      if (clientSupportsDelete && dataValue.__op == 'Delete') {
        response[fieldName] = dataValue;
      }
    }
  });
  return response;
}
```
- example usage
```shell
...
    });
  }

  return defer.then(function () {
    // Run an update
    return _this14.config.database.update(_this14.className, _this14.query, _this14.data, _this14.runOptions).then(function (response
) {
      response.updatedAt = _this14.updatedAt;
      _this14._updateResponseWithData(response, _this14.data);
      _this14.response = { response: response };
    });
  });
} else {
  // Set the default ACL and password timestamp for the new _User
  if (this.className === '_User') {
    var ACL = this.data.ACL;
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype._validateEmail"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validateEmail ()](#apidoc.element.parse-server.RestWrite.prototype._validateEmail)
- description and source-code
```javascript
_validateEmail = function () {
  var _this8 = this;

  if (!this.data.email || this.data.email.__op === 'Delete') {
    return Promise.resolve();
  }
  // Validate basic email address format
  if (!this.data.email.match(/^.+@.+$/)) {
    return Promise.reject(new Parse.Error(Parse.Error.INVALID_EMAIL_ADDRESS, 'Email address format is invalid.'));
  }
  // Same problem for email as above for username
  return this.config.database.find(this.className, { email: this.data.email, objectId: { '$ne': this.objectId() } }, { limit: 1 }).
then(function (results) {
    if (results.length > 0) {
      throw new Parse.Error(Parse.Error.EMAIL_TAKEN, 'Account already exists for this email address.');
    }
    // We updated the email, send a new validation
    _this8.storage['sendVerificationEmail'] = true;
    _this8.config.userController.setEmailVerifyToken(_this8.data);
  });
}
```
- example usage
```shell
...
      _this7.data._hashed_password = hashedPassword;
      delete _this7.data.password;
    });
  });
}).then(function () {
  return _this7._validateUserName();
}).then(function () {
  return _this7._validateEmail();
});
};

RestWrite.prototype._validateUserName = function () {
// Check for username uniqueness
if (!this.data.username) {
  if (!this.query) {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype._validatePasswordHistory"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validatePasswordHistory ()](#apidoc.element.parse-server.RestWrite.prototype._validatePasswordHistory)
- description and source-code
```javascript
_validatePasswordHistory = function () {
  var _this11 = this;

  // check whether password is repeating from specified history
  if (this.query && this.config.passwordPolicy.maxPasswordHistory) {
    return this.config.database.find('_User', { objectId: this.objectId() }, { keys: ["_password_history", "_hashed_password"] }).
then(function (results) {
      if (results.length != 1) {
        throw undefined;
      }
      var user = results[0];
      var oldPasswords = [];
      if (user._password_history) oldPasswords = _lodash2.default.take(user._password_history, _this11.config.passwordPolicy.maxPasswordHistory
 - 1);
      oldPasswords.push(user.password);
      var newPassword = _this11.data.password;
      // compare the new password hash with all old password hashes
      var promises = oldPasswords.map(function (hash) {
        return passwordCrypto.compare(newPassword, hash).then(function (result) {
          if (result) // reject if there is a match
            return Promise.reject("REPEAT_PASSWORD");
          return Promise.resolve();
        });
      });
      // wait for all comparisons to complete
      return Promise.all(promises).then(function () {
        return Promise.resolve();
      }).catch(function (err) {
        if (err === "REPEAT_PASSWORD") // a match was found
          return Promise.reject(new Parse.Error(Parse.Error.VALIDATION_ERROR, 'New password should not be the same as last ' + _this11
.config.passwordPolicy.maxPasswordHistory + ' passwords.'));
        throw err;
      });
    });
  }
  return Promise.resolve();
}
```
- example usage
```shell
...
};

RestWrite.prototype._validatePasswordPolicy = function () {
var _this9 = this;

if (!this.config.passwordPolicy) return Promise.resolve();
return this._validatePasswordRequirements().then(function () {
  return _this9._validatePasswordHistory();
});
};

RestWrite.prototype._validatePasswordRequirements = function () {
var _this10 = this;

// check if the password conforms to the defined password policy if configured
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype._validatePasswordPolicy"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validatePasswordPolicy ()](#apidoc.element.parse-server.RestWrite.prototype._validatePasswordPolicy)
- description and source-code
```javascript
_validatePasswordPolicy = function () {
  var _this9 = this;

  if (!this.config.passwordPolicy) return Promise.resolve();
  return this._validatePasswordRequirements().then(function () {
    return _this9._validatePasswordHistory();
  });
}
```
- example usage
```shell
...
  }

  if (_this7.query && !_this7.auth.isMaster) {
    _this7.storage['clearSessions'] = true;
    _this7.storage['generateNewSession'] = true;
  }

  return _this7._validatePasswordPolicy().then(function () {
    return passwordCrypto.hash(_this7.data.password).then(function (hashedPassword) {
      _this7.data._hashed_password = hashedPassword;
      delete _this7.data.password;
    });
  });
}).then(function () {
  return _this7._validateUserName();
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype._validatePasswordRequirements"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validatePasswordRequirements ()](#apidoc.element.parse-server.RestWrite.prototype._validatePasswordRequirements)
- description and source-code
```javascript
_validatePasswordRequirements = function () {
  var _this10 = this;

  // check if the password conforms to the defined password policy if configured
  var policyError = 'Password does not meet the Password Policy requirements.';

  // check whether the password meets the password strength requirements
  if (this.config.passwordPolicy.patternValidator && !this.config.passwordPolicy.patternValidator(this.data.password) || this.config
.passwordPolicy.validatorCallback && !this.config.passwordPolicy.validatorCallback(this.data.password)) {
    return Promise.reject(new Parse.Error(Parse.Error.VALIDATION_ERROR, policyError));
  }

  // check whether password contain username
  if (this.config.passwordPolicy.doNotAllowUsername === true) {
    if (this.data.username) {
      // username is not passed during password reset
      if (this.data.password.indexOf(this.data.username) >= 0) return Promise.reject(new Parse.Error(Parse.Error.VALIDATION_ERROR
, policyError));
    } else {
      // retrieve the User object using objectId during password reset
      return this.config.database.find('_User', { objectId: this.objectId() }).then(function (results) {
        if (results.length != 1) {
          throw undefined;
        }
        if (_this10.data.password.indexOf(results[0].username) >= 0) return Promise.reject(new Parse.Error(Parse.Error.VALIDATION_ERROR
, policyError));
        return Promise.resolve();
      });
    }
  }
  return Promise.resolve();
}
```
- example usage
```shell
...
});
};

RestWrite.prototype._validatePasswordPolicy = function () {
var _this9 = this;

if (!this.config.passwordPolicy) return Promise.resolve();
return this._validatePasswordRequirements().then(function () {
  return _this9._validatePasswordHistory();
});
};

RestWrite.prototype._validatePasswordRequirements = function () {
var _this10 = this;
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype._validateUserName"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>_validateUserName ()](#apidoc.element.parse-server.RestWrite.prototype._validateUserName)
- description and source-code
```javascript
_validateUserName = function () {
  // Check for username uniqueness
  if (!this.data.username) {
    if (!this.query) {
      this.data.username = cryptoUtils.randomString(25);
      this.responseShouldHaveUsername = true;
    }
    return Promise.resolve();
  }
  // We need to a find to check for duplicate username in case they are missing the unique index on usernames
  // TODO: Check if there is a unique index, and if so, skip this query.
  return this.config.database.find(this.className, { username: this.data.username, objectId: { '$ne': this.objectId() } }, { limit
: 1 }).then(function (results) {
    if (results.length > 0) {
      throw new Parse.Error(Parse.Error.USERNAME_TAKEN, 'Account already exists for this username.');
    }
    return;
  });
}
```
- example usage
```shell
...
  return _this7._validatePasswordPolicy().then(function () {
    return passwordCrypto.hash(_this7.data.password).then(function (hashedPassword) {
      _this7.data._hashed_password = hashedPassword;
      delete _this7.data.password;
    });
  });
}).then(function () {
  return _this7._validateUserName();
}).then(function () {
  return _this7._validateEmail();
});
};

RestWrite.prototype._validateUserName = function () {
// Check for username uniqueness
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.cleanUserAuthData"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>cleanUserAuthData ()](#apidoc.element.parse-server.RestWrite.prototype.cleanUserAuthData)
- description and source-code
```javascript
cleanUserAuthData = function () {
  if (this.response && this.response.response && this.className === '_User') {
    var user = this.response.response;
    if (user.authData) {
      Object.keys(user.authData).forEach(function (provider) {
        if (user.authData[provider] === null) {
          delete user.authData[provider];
        }
      });
      if (Object.keys(user.authData).length == 0) {
        delete user.authData;
      }
    }
  }
}
```
- example usage
```shell
...
  }).then(function () {
    return _this.createSessionTokenIfNeeded();
  }).then(function () {
    return _this.handleFollowup();
  }).then(function () {
    return _this.runAfterTrigger();
  }).then(function () {
    return _this.cleanUserAuthData();
  }).then(function () {
    return _this.response;
  });
};

// Uses the Auth object to get the list of roles, adds the user id
RestWrite.prototype.getUserAndRoleACL = function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.createSessionToken"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>createSessionToken ()](#apidoc.element.parse-server.RestWrite.prototype.createSessionToken)
- description and source-code
```javascript
createSessionToken = function () {
  // cloud installationId from Cloud Code,
  // never create session tokens from there.
  if (this.auth.installationId && this.auth.installationId === 'cloud') {
    return;
  }
  var token = 'r:' + cryptoUtils.newToken();

  var expiresAt = this.config.generateSessionExpiresAt();
  var sessionData = {
    sessionToken: token,
    user: {
      __type: 'Pointer',
      className: '_User',
      objectId: this.objectId()
    },
    createdWith: {
      'action': 'signup',
      'authProvider': this.storage['authProvider'] || 'password'
    },
    restricted: false,
    installationId: this.auth.installationId,
    expiresAt: Parse._encode(expiresAt)
  };
  if (this.response && this.response.response) {
    this.response.response.sessionToken = token;
  }
  var create = new RestWrite(this.config, Auth.master(this.config), '_Session', null, sessionData);
  return create.execute();
}
```
- example usage
```shell
...
RestWrite.prototype.createSessionTokenIfNeeded = function () {
if (this.className !== '_User') {
  return;
}
if (this.query) {
  return;
}
return this.createSessionToken();
};

RestWrite.prototype.createSessionToken = function () {
// cloud installationId from Cloud Code,
// never create session tokens from there.
if (this.auth.installationId && this.auth.installationId === 'cloud') {
  return;
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.createSessionTokenIfNeeded"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>createSessionTokenIfNeeded ()](#apidoc.element.parse-server.RestWrite.prototype.createSessionTokenIfNeeded)
- description and source-code
```javascript
createSessionTokenIfNeeded = function () {
  if (this.className !== '_User') {
    return;
  }
  if (this.query) {
    return;
  }
  return this.createSessionToken();
}
```
- example usage
```shell
...
}).then(function () {
  return _this.transformUser();
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
  return _this.runDatabaseOperation();
}).then(function () {
  return _this.createSessionTokenIfNeeded();
}).then(function () {
  return _this.handleFollowup();
}).then(function () {
  return _this.runAfterTrigger();
}).then(function () {
  return _this.cleanUserAuthData();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.execute"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>execute ()](#apidoc.element.parse-server.RestWrite.prototype.execute)
- description and source-code
```javascript
execute = function () {
  var _this = this;

  return Promise.resolve().then(function () {
    return _this.getUserAndRoleACL();
  }).then(function () {
    return _this.validateClientClassCreation();
  }).then(function () {
    return _this.handleInstallation();
  }).then(function () {
    return _this.handleSession();
  }).then(function () {
    return _this.validateAuthData();
  }).then(function () {
    return _this.runBeforeTrigger();
  }).then(function () {
    return _this.validateSchema();
  }).then(function () {
    return _this.setRequiredFieldsIfNeeded();
  }).then(function () {
    return _this.transformUser();
  }).then(function () {
    return _this.expandFilesForExistingObjects();
  }).then(function () {
    return _this.runDatabaseOperation();
  }).then(function () {
    return _this.createSessionTokenIfNeeded();
  }).then(function () {
    return _this.handleFollowup();
  }).then(function () {
    return _this.runAfterTrigger();
  }).then(function () {
    return _this.cleanUserAuthData();
  }).then(function () {
    return _this.response;
  });
}
```
- example usage
```shell
...

    var restOptions = {
limit: 1,
include: 'user'
    };

    var query = new RestQuery(config, master(config), '_Session', { sessionToken: sessionToken }, restOptions);
    return query.execute().then(function (response) {
var results = response.results;
if (results.length !== 1 || !results[0]['user']) {
  throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'invalid session token');
}

var now = new Date(),
    expiresAt = results[0].expiresAt ? new Date(results[0].expiresAt.iso) : undefined;
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.expandFilesForExistingObjects"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>expandFilesForExistingObjects ()](#apidoc.element.parse-server.RestWrite.prototype.expandFilesForExistingObjects)
- description and source-code
```javascript
expandFilesForExistingObjects = function () {
  // Check whether we have a short-circuited response - only then run expansion.
  if (this.response && this.response.response) {
    this.config.filesController.expandFilesInObject(this.config, this.response.response);
  }
}
```
- example usage
```shell
...
}).then(function () {
  return _this.validateSchema();
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
  return _this.transformUser();
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
  return _this.runDatabaseOperation();
}).then(function () {
  return _this.createSessionTokenIfNeeded();
}).then(function () {
  return _this.handleFollowup();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.findUsersWithAuthData"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>findUsersWithAuthData (authData)](#apidoc.element.parse-server.RestWrite.prototype.findUsersWithAuthData)
- description and source-code
```javascript
findUsersWithAuthData = function (authData) {
  var providers = Object.keys(authData);
  var query = providers.reduce(function (memo, provider) {
    if (!authData[provider]) {
      return memo;
    }
    var queryKey = 'authData.' + provider + '.id';
    var query = {};
    query[queryKey] = authData[provider].id;
    memo.push(query);
    return memo;
  }, []).filter(function (q) {
    return typeof q !== 'undefined';
  });

  var findPromise = Promise.resolve([]);
  if (query.length > 0) {
    findPromise = this.config.database.find(this.className, { '$or': query }, {});
  }

  return findPromise;
}
```
- example usage
```shell
...
};

RestWrite.prototype.handleAuthData = function (authData) {
var _this6 = this;

var results = void 0;
return this.handleAuthDataValidation(authData).then(function () {
  return _this6.findUsersWithAuthData(authData);
}).then(function (r) {
  results = r;
  if (results.length > 1) {
    // More than 1 user with the passed id's
    throw new Parse.Error(Parse.Error.ACCOUNT_ALREADY_LINKED, 'this auth is already used');
  }
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.getUserAndRoleACL"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>getUserAndRoleACL ()](#apidoc.element.parse-server.RestWrite.prototype.getUserAndRoleACL)
- description and source-code
```javascript
getUserAndRoleACL = function () {
  var _this2 = this;

  if (this.auth.isMaster) {
    return Promise.resolve();
  }

  this.runOptions.acl = ['*'];

  if (this.auth.user) {
    return this.auth.getUserRoles().then(function (roles) {
      roles.push(_this2.auth.user.id);
      _this2.runOptions.acl = _this2.runOptions.acl.concat(roles);
      return;
    });
  } else {
    return Promise.resolve();
  }
}
```
- example usage
```shell
...
});
};

RestQuery.prototype.buildRestWhere = function () {
var _this2 = this;

return Promise.resolve().then(function () {
  return _this2.getUserAndRoleACL();
}).then(function () {
  return _this2.redirectClassNameForKey();
}).then(function () {
  return _this2.validateClientClassCreation();
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.handleAuthData"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleAuthData (authData)](#apidoc.element.parse-server.RestWrite.prototype.handleAuthData)
- description and source-code
```javascript
handleAuthData = function (authData) {
  var _this6 = this;

  var results = void 0;
  return this.handleAuthDataValidation(authData).then(function () {
    return _this6.findUsersWithAuthData(authData);
  }).then(function (r) {
    results = r;
    if (results.length > 1) {
      // More than 1 user with the passed id's
      throw new Parse.Error(Parse.Error.ACCOUNT_ALREADY_LINKED, 'this auth is already used');
    }

    _this6.storage['authProvider'] = Object.keys(authData).join(',');

    if (results.length > 0) {
      if (!_this6.query) {
        // Login with auth data
        delete results[0].password;
        var userResult = results[0];

        // need to set the objectId first otherwise location has trailing undefined
        _this6.data.objectId = userResult.objectId;

        // Determine if authData was updated
        var mutatedAuthData = {};
        Object.keys(authData).forEach(function (provider) {
          var providerData = authData[provider];
          var userAuthData = userResult.authData[provider];
          if (!_lodash2.default.isEqual(providerData, userAuthData)) {
            mutatedAuthData[provider] = providerData;
          }
        });

        _this6.response = {
          response: userResult,
          location: _this6.location()
        };

        // We have authData that is updated on login
        // that can happen when token are refreshed,
        // We should update the token and let the user in
        if (Object.keys(mutatedAuthData).length > 0) {
          // Assign the new authData in the response
          Object.keys(mutatedAuthData).forEach(function (provider) {
            _this6.response.response.authData[provider] = mutatedAuthData[provider];
          });
          // Run the DB update directly, as 'master'
          // Just update the authData part
          return _this6.config.database.update(_this6.className, { objectId: _this6.data.objectId }, { authData: mutatedAuthData
 }, {});
        }
        return;
      } else if (_this6.query && _this6.query.objectId) {
        // Trying to update auth data but users
        // are different
        if (results[0].objectId !== _this6.query.objectId) {
          throw new Parse.Error(Parse.Error.ACCOUNT_ALREADY_LINKED, 'this auth is already used');
        }
      }
    }
    return;
  });
}
```
- example usage
```shell
...
if (providers.length > 0) {
  var canHandleAuthData = providers.reduce(function (canHandle, provider) {
    var providerAuthData = authData[provider];
    var hasToken = providerAuthData && providerAuthData.id;
    return canHandle && (hasToken || providerAuthData == null);
  }, true);
  if (canHandleAuthData) {
    return this.handleAuthData(authData);
  }
}
throw new Parse.Error(Parse.Error.UNSUPPORTED_SERVICE, 'This authentication method is unsupported.');
};

RestWrite.prototype.handleAuthDataValidation = function (authData) {
var _this5 = this;
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.handleAuthDataValidation"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleAuthDataValidation (authData)](#apidoc.element.parse-server.RestWrite.prototype.handleAuthDataValidation)
- description and source-code
```javascript
handleAuthDataValidation = function (authData) {
  var _this5 = this;

  var validations = Object.keys(authData).map(function (provider) {
    if (authData[provider] === null) {
      return Promise.resolve();
    }
    var validateAuthData = _this5.config.authDataManager.getValidatorForProvider(provider);
    if (!validateAuthData) {
      throw new Parse.Error(Parse.Error.UNSUPPORTED_SERVICE, 'This authentication method is unsupported.');
    }
    return validateAuthData(authData[provider]);
  });
  return Promise.all(validations);
}
```
- example usage
```shell
...
return findPromise;
};

RestWrite.prototype.handleAuthData = function (authData) {
var _this6 = this;

var results = void 0;
return this.handleAuthDataValidation(authData).then(function () {
  return _this6.findUsersWithAuthData(authData);
}).then(function (r) {
  results = r;
  if (results.length > 1) {
    // More than 1 user with the passed id's
    throw new Parse.Error(Parse.Error.ACCOUNT_ALREADY_LINKED, 'this auth is already used');
  }
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.handleFollowup"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleFollowup ()](#apidoc.element.parse-server.RestWrite.prototype.handleFollowup)
- description and source-code
```javascript
handleFollowup = function () {
  if (this.storage && this.storage['clearSessions'] && this.config.revokeSessionOnPasswordReset) {
    var sessionQuery = {
      user: {
        __type: 'Pointer',
        className: '_User',
        objectId: this.objectId()
      }
    };
    delete this.storage['clearSessions'];
    return this.config.database.destroy('_Session', sessionQuery).then(this.handleFollowup.bind(this));
  }

  if (this.storage && this.storage['generateNewSession']) {
    delete this.storage['generateNewSession'];
    return this.createSessionToken().then(this.handleFollowup.bind(this));
  }

  if (this.storage && this.storage['sendVerificationEmail']) {
    delete this.storage['sendVerificationEmail'];
    // Fire and forget!
    this.config.userController.sendVerificationEmail(this.data);
    return this.handleFollowup.bind(this);
  }
}
```
- example usage
```shell
...
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
  return _this.runDatabaseOperation();
}).then(function () {
  return _this.createSessionTokenIfNeeded();
}).then(function () {
  return _this.handleFollowup();
}).then(function () {
  return _this.runAfterTrigger();
}).then(function () {
  return _this.cleanUserAuthData();
}).then(function () {
  return _this.response;
});
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.handleInstallation"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleInstallation ()](#apidoc.element.parse-server.RestWrite.prototype.handleInstallation)
- description and source-code
```javascript
handleInstallation = function () {
  var _this13 = this;

  if (this.response || this.className !== '_Installation') {
    return;
  }

  if (!this.query && !this.data.deviceToken && !this.data.installationId && !this.auth.installationId) {
    throw new Parse.Error(135, 'at least one ID field (deviceToken, installationId) ' + 'must be specified in this operation');
  }

  // If the device token is 64 characters long, we assume it is for iOS
  // and lowercase it.
  if (this.data.deviceToken && this.data.deviceToken.length == 64) {
    this.data.deviceToken = this.data.deviceToken.toLowerCase();
  }

  // We lowercase the installationId if present
  if (this.data.installationId) {
    this.data.installationId = this.data.installationId.toLowerCase();
  }

  var installationId = this.data.installationId;

  // If data.installationId is not set and we're not master, we can lookup in auth
  if (!installationId && !this.auth.isMaster) {
    installationId = this.auth.installationId;
  }

  if (installationId) {
    installationId = installationId.toLowerCase();
  }

  // Updating _Installation but not updating anything critical
  if (this.query && !this.data.deviceToken && !installationId && !this.data.deviceType) {
    return;
  }

  var promise = Promise.resolve();

  var idMatch; // Will be a match on either objectId or installationId
  var objectIdMatch;
  var installationIdMatch;
  var deviceTokenMatches = [];

  // Instead of issuing 3 reads, let's do it with one OR.
  var orQueries = [];
  if (this.query && this.query.objectId) {
    orQueries.push({
      objectId: this.query.objectId
    });
  }
  if (installationId) {
    orQueries.push({
      'installationId': installationId
    });
  }
  if (this.data.deviceToken) {
    orQueries.push({ 'deviceToken': this.data.deviceToken });
  }

  if (orQueries.length == 0) {
    return;
  }

  promise = promise.then(function () {
    return _this13.config.database.find('_Installation', {
      '$or': orQueries
    }, {});
  }).then(function (results) {
    results.forEach(function (result) {
      if (_this13.query && _this13.query.objectId && result.objectId == _this13.query.objectId) {
        objectIdMatch = result;
      }
      if (result.installationId == installationId) {
        installationIdMatch = result;
      }
      if (result.deviceToken == _this13.data.deviceToken) {
        deviceTokenMatches.push(result);
      }
    });

    // Sanity checks when running a query
    if (_this13.query && _this13.query.objectId) {
      if (!objectIdMatch) {
        throw new Parse.Error(Parse.Error.OBJECT_NOT_FOUND, 'Object not found for update.');
      }
      if (_this13.data.installationId && objectIdMatch.installationId && _this13.data.installationId !== objectIdMatch.installationId
) {
        throw new Parse.Error(136, 'installationId may not be changed in this ' + 'operation');
      }
      if (_this13.data.deviceToken && objectIdMatch.deviceToken && _this13.data.deviceToken !== objectIdMatch.deviceToken && !_this13
.data.installationId && !objectIdMatch.installationId) {
        throw new Parse.Error(136, 'deviceToken may not be changed in this ' + 'operation');
      }
      if (_this13.data.deviceType && _this13.data.deviceType && _this13.data.deviceType !== objectIdMatch.deviceType) {
        throw new Parse.Error(136, 'deviceType may not be changed in this ' + 'operation');
      }
    }

    if (_this13.query && _this13.query.objectId && objectIdMatch) {
      idMatch = objectIdMatch;
    }

    if (installationId && installationIdMatch) {
      idMatch = installationIdMatch;
    }
    // need to specify deviceType only if it's new
    if (!_this13.query && !_this13.data.deviceType && !idMatch) {
      throw new Parse.Error(135, 'deviceType must be specified in this operation');
    }
  }).then(function () {
    if (!idMatch) {
      if (!deviceTokenMatches.length) {
        return;
      } else if (deviceTokenMatches.length == 1 && (!deviceTokenMatches[0]['installationId'] || !installationId)) {
        // Single match on device token but none on installationId, and either ...
```
- example usage
```shell
...
var _this = this;

return Promise.resolve().then(function () {
  return _this.getUserAndRoleACL();
}).then(function () {
  return _this.validateClientClassCreation();
}).then(function () {
  return _this.handleInstallation();
}).then(function () {
  return _this.handleSession();
}).then(function () {
  return _this.validateAuthData();
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.handleSession"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>handleSession ()](#apidoc.element.parse-server.RestWrite.prototype.handleSession)
- description and source-code
```javascript
handleSession = function () {
  var _this12 = this;

  if (this.response || this.className !== '_Session') {
    return;
  }

  if (!this.auth.user && !this.auth.isMaster) {
    throw new Parse.Error(Parse.Error.INVALID_SESSION_TOKEN, 'Session token required.');
  }

  // TODO: Verify proper error to throw
  if (this.data.ACL) {
    throw new Parse.Error(Parse.Error.INVALID_KEY_NAME, 'Cannot set ' + 'ACL on a Session.');
  }

  if (!this.query && !this.auth.isMaster) {
    var token = 'r:' + cryptoUtils.newToken();
    var expiresAt = this.config.generateSessionExpiresAt();
    var sessionData = {
      sessionToken: token,
      user: {
        __type: 'Pointer',
        className: '_User',
        objectId: this.auth.user.id
      },
      createdWith: {
        'action': 'create'
      },
      restricted: true,
      expiresAt: Parse._encode(expiresAt)
    };
    for (var key in this.data) {
      if (key == 'objectId') {
        continue;
      }
      sessionData[key] = this.data[key];
    }
    var create = new RestWrite(this.config, Auth.master(this.config), '_Session', null, sessionData);
    return create.execute().then(function (results) {
      if (!results.response) {
        throw new Parse.Error(Parse.Error.INTERNAL_SERVER_ERROR, 'Error creating session.');
      }
      sessionData['objectId'] = results.response['objectId'];
      _this12.response = {
        status: 201,
        location: results.location,
        response: sessionData
      };
    });
  }
}
```
- example usage
```shell
...
return Promise.resolve().then(function () {
  return _this.getUserAndRoleACL();
}).then(function () {
  return _this.validateClientClassCreation();
}).then(function () {
  return _this.handleInstallation();
}).then(function () {
  return _this.handleSession();
}).then(function () {
  return _this.validateAuthData();
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
  return _this.validateSchema();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.location"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>location ()](#apidoc.element.parse-server.RestWrite.prototype.location)
- description and source-code
```javascript
location = function () {
  var middle = this.className === '_User' ? '/users/' : '/classes/' + this.className + '/';
  return this.config.mount + middle + this.data.objectId;
}
```
- example usage
```shell
...
  if (!_lodash2.default.isEqual(providerData, userAuthData)) {
    mutatedAuthData[provider] = providerData;
  }
});

_this6.response = {
  response: userResult,
  location: _this6.location()
};

// We have authData that is updated on login
// that can happen when token are refreshed,
// We should update the token and let the user in
if (Object.keys(mutatedAuthData).length > 0) {
  // Assign the new authData in the response
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.objectId"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>objectId ()](#apidoc.element.parse-server.RestWrite.prototype.objectId)
- description and source-code
```javascript
objectId = function () {
  return this.data.objectId || this.query.objectId;
}
```
- example usage
```shell
...
if (this.query) {
  // If we're updating a _User object, we need to clear out the cache for that user. Find all their
  // session tokens, and remove them from the cache.
  promise = new _RestQuery2.default(this.config, Auth.master(this.config), '_Session', {
    user: {
      __type: "Pointer",
      className: "_User",
      objectId: this.objectId()
    }
  }).execute().then(function (results) {
    results.results.forEach(function (session) {
      return _this7.config.cacheController.user.del(session.sessionToken);
    });
  });
}
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.runAfterTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>runAfterTrigger ()](#apidoc.element.parse-server.RestWrite.prototype.runAfterTrigger)
- description and source-code
```javascript
runAfterTrigger = function () {
  if (!this.response || !this.response.response) {
    return;
  }

  // Avoid doing any setup for triggers if there is no 'afterSave' trigger for this class.
  var hasAfterSaveHook = triggers.triggerExists(this.className, triggers.Types.afterSave, this.config.applicationId);
  var hasLiveQuery = this.config.liveQueryController.hasLiveQuery(this.className);
  if (!hasAfterSaveHook && !hasLiveQuery) {
    return Promise.resolve();
  }

  var extraData = { className: this.className };
  if (this.query && this.query.objectId) {
    extraData.objectId = this.query.objectId;
  }

  // Build the original object, we only do this for a update write.
  var originalObject = void 0;
  if (this.query && this.query.objectId) {
    originalObject = triggers.inflate(extraData, this.originalData);
  }

  // Build the inflated object, different from beforeSave, originalData is not empty
  // since developers can change data in the beforeSave.
  var updatedObject = triggers.inflate(extraData, this.originalData);
  updatedObject.set(this.sanitizedData());
  updatedObject._handleSaveResponse(this.response.response, this.response.status || 200);

  // Notifiy LiveQueryServer if possible
  this.config.liveQueryController.onAfterSave(updatedObject.className, updatedObject, originalObject);

  // Run afterSave trigger
  return triggers.maybeRunTrigger(triggers.Types.afterSave, this.auth, updatedObject, originalObject, this.config);
}
```
- example usage
```shell
...
  }).then(function () {
    return _this.runDatabaseOperation();
  }).then(function () {
    return _this.createSessionTokenIfNeeded();
  }).then(function () {
    return _this.handleFollowup();
  }).then(function () {
    return _this.runAfterTrigger();
  }).then(function () {
    return _this.cleanUserAuthData();
  }).then(function () {
    return _this.response;
  });
};
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.runBeforeTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>runBeforeTrigger ()](#apidoc.element.parse-server.RestWrite.prototype.runBeforeTrigger)
- description and source-code
```javascript
runBeforeTrigger = function () {
  var _this4 = this;

  if (this.response) {
    return;
  }

  // Avoid doing any setup for triggers if there is no 'beforeSave' trigger for this class.
  if (!triggers.triggerExists(this.className, triggers.Types.beforeSave, this.config.applicationId)) {
    return Promise.resolve();
  }

  // Cloud code gets a bit of extra data for its objects
  var extraData = { className: this.className };
  if (this.query && this.query.objectId) {
    extraData.objectId = this.query.objectId;
  }

  var originalObject = null;
  var updatedObject = triggers.inflate(extraData, this.originalData);
  if (this.query && this.query.objectId) {
    // This is an update for existing object.
    originalObject = triggers.inflate(extraData, this.originalData);
  }
  updatedObject.set(this.sanitizedData());

  return Promise.resolve().then(function () {
    return triggers.maybeRunTrigger(triggers.Types.beforeSave, _this4.auth, updatedObject, originalObject, _this4.config);
  }).then(function (response) {
    if (response && response.object) {
      _this4.storage.fieldsChangedByTrigger = _lodash2.default.reduce(response.object, function (result, value, key) {
        if (!_lodash2.default.isEqual(_this4.data[key], value)) {
          result.push(key);
        }
        return result;
      }, []);
      _this4.data = response.object;
      // We should delete the objectId for an update write
      if (_this4.query && _this4.query.objectId) {
        delete _this4.data.objectId;
      }
    }
  });
}
```
- example usage
```shell
...
}).then(function () {
  return _this.handleInstallation();
}).then(function () {
  return _this.handleSession();
}).then(function () {
  return _this.validateAuthData();
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
  return _this.validateSchema();
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
  return _this.transformUser();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.runDatabaseOperation"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>runDatabaseOperation ()](#apidoc.element.parse-server.RestWrite.prototype.runDatabaseOperation)
- description and source-code
```javascript
runDatabaseOperation = function () {
  var _this14 = this;

  if (this.response) {
    return;
  }

  if (this.className === '_Role') {
    this.config.cacheController.role.clear();
  }

  if (this.className === '_User' && this.query && !this.auth.couldUpdateUserId(this.query.objectId)) {
    throw new Parse.Error(Parse.Error.SESSION_MISSING, 'Cannot modify user ' + this.query.objectId + '.');
  }

  if (this.className === '_Product' && this.data.download) {
    this.data.downloadName = this.data.download.name;
  }

  // TODO: Add better detection for ACL, ensuring a user can't be locked from
  //       their own user record.
  if (this.data.ACL && this.data.ACL['*unresolved']) {
    throw new Parse.Error(Parse.Error.INVALID_ACL, 'Invalid ACL.');
  }

  if (this.query) {
    // Force the user to not lockout
    // Matched with parse.com
    if (this.className === '_User' && this.data.ACL) {
      this.data.ACL[this.query.objectId] = { read: true, write: true };
    }
    // update password timestamp if user password is being changed
    if (this.className === '_User' && this.data._hashed_password && this.config.passwordPolicy && this.config.passwordPolicy.maxPasswordAge
) {
      this.data._password_changed_at = Parse._encode(new Date());
    }
    // Ignore createdAt when update
    delete this.data.createdAt;

    var defer = Promise.resolve();
    // if password history is enabled then save the current password to history
    if (this.className === '_User' && this.data._hashed_password && this.config.passwordPolicy && this.config.passwordPolicy.maxPasswordHistory
) {
      defer = this.config.database.find('_User', { objectId: this.objectId() }, { keys: ["_password_history", "_hashed_password"] }).
then(function (results) {
        if (results.length != 1) {
          throw undefined;
        }
        var user = results[0];
        var oldPasswords = [];
        if (user._password_history) {
          oldPasswords = _lodash2.default.take(user._password_history, _this14.config.passwordPolicy.maxPasswordHistory);
        }
        //n-1 passwords go into history including last password
        while (oldPasswords.length > _this14.config.passwordPolicy.maxPasswordHistory - 2) {
          oldPasswords.shift();
        }
        oldPasswords.push(user.password);
        _this14.data._password_history = oldPasswords;
      });
    }

    return defer.then(function () {
      // Run an update
      return _this14.config.database.update(_this14.className, _this14.query, _this14.data, _this14.runOptions).then(function (response
) {
        response.updatedAt = _this14.updatedAt;
        _this14._updateResponseWithData(response, _this14.data);
        _this14.response = { response: response };
      });
    });
  } else {
    // Set the default ACL and password timestamp for the new _User
    if (this.className === '_User') {
      var ACL = this.data.ACL;
      // default public r/w ACL
      if (!ACL) {
        ACL = {};
        ACL['*'] = { read: true, write: false };
      }
      // make sure the user is not locked down
      ACL[this.data.objectId] = { read: true, write: true };
      this.data.ACL = ACL;
      // password timestamp to be used when password expiry policy is enforced
      if (this.config.passwordPolicy && this.config.passwordPolicy.maxPasswordAge) {
        this.data._password_changed_at = Parse._encode(new Date());
      }
    }

    // Run a create
    return this.config.database.create(this.className, this.data, this.runOptions).catch(function (error) {
      if (_this14.className !== '_User' || error.code !== Parse.Error.DUPLICATE_VALUE) {
        throw error;
      }
      // If this was a failed user creation due to username or email already taken, we need to
      // check whether it was username or email and return the appropriate error.

      // TODO: See if we can later do this without additional queries by using named indexes.
      return _this14.config.database.find(_this14.className, { username: _this14.data.username, objectId: { '$ne': _this14.objectId
() } }, { limit: 1 }).then(function (results) {
        if ...
```
- example usage
```shell
...
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
  return _this.transformUser();
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
  return _this.runDatabaseOperation();
}).then(function () {
  return _this.createSessionTokenIfNeeded();
}).then(function () {
  return _this.handleFollowup();
}).then(function () {
  return _this.runAfterTrigger();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.sanitizedData"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>sanitizedData ()](#apidoc.element.parse-server.RestWrite.prototype.sanitizedData)
- description and source-code
```javascript
sanitizedData = function () {
  var data = Object.keys(this.data).reduce(function (data, key) {
    // Regexp comes from Parse.Object.prototype.validate
    if (!/^[A-Za-z][0-9A-Za-z_]*$/.test(key)) {
      delete data[key];
    }
    return data;
  }, deepcopy(this.data));
  return Parse._decode(undefined, data);
}
```
- example usage
```shell
...

var originalObject = null;
var updatedObject = triggers.inflate(extraData, this.originalData);
if (this.query && this.query.objectId) {
  // This is an update for existing object.
  originalObject = triggers.inflate(extraData, this.originalData);
}
updatedObject.set(this.sanitizedData());

return Promise.resolve().then(function () {
  return triggers.maybeRunTrigger(triggers.Types.beforeSave, _this4.auth, updatedObject, originalObject, _this4.config);
}).then(function (response) {
  if (response && response.object) {
    _this4.storage.fieldsChangedByTrigger = _lodash2.default.reduce(response.object, function (result, value, key) {
      if (!_lodash2.default.isEqual(_this4.data[key], value)) {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.setRequiredFieldsIfNeeded"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>setRequiredFieldsIfNeeded ()](#apidoc.element.parse-server.RestWrite.prototype.setRequiredFieldsIfNeeded)
- description and source-code
```javascript
setRequiredFieldsIfNeeded = function () {
  if (this.data) {
    // Add default fields
    this.data.updatedAt = this.updatedAt;
    if (!this.query) {
      this.data.createdAt = this.updatedAt;

      // Only assign new objectId if we are creating new object
      if (!this.data.objectId) {
        this.data.objectId = cryptoUtils.newObjectId();
      }
    }
  }
  return Promise.resolve();
}
```
- example usage
```shell
...
}).then(function () {
  return _this.validateAuthData();
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
  return _this.validateSchema();
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
  return _this.transformUser();
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
  return _this.runDatabaseOperation();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.transformUser"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>transformUser ()](#apidoc.element.parse-server.RestWrite.prototype.transformUser)
- description and source-code
```javascript
transformUser = function () {
  var _this7 = this;

  var promise = Promise.resolve();

  if (this.className !== '_User') {
    return promise;
  }

  if (this.query) {
    // If we're updating a _User object, we need to clear out the cache for that user. Find all their
    // session tokens, and remove them from the cache.
    promise = new _RestQuery2.default(this.config, Auth.master(this.config), '_Session', {
      user: {
        __type: "Pointer",
        className: "_User",
        objectId: this.objectId()
      }
    }).execute().then(function (results) {
      results.results.forEach(function (session) {
        return _this7.config.cacheController.user.del(session.sessionToken);
      });
    });
  }

  return promise.then(function () {
    // Transform the password
    if (_this7.data.password === undefined) {
      // ignore only if undefined. should proceed if empty ('')
      return Promise.resolve();
    }

    if (_this7.query && !_this7.auth.isMaster) {
      _this7.storage['clearSessions'] = true;
      _this7.storage['generateNewSession'] = true;
    }

    return _this7._validatePasswordPolicy().then(function () {
      return passwordCrypto.hash(_this7.data.password).then(function (hashedPassword) {
        _this7.data._hashed_password = hashedPassword;
        delete _this7.data.password;
      });
    });
  }).then(function () {
    return _this7._validateUserName();
  }).then(function () {
    return _this7._validateEmail();
  });
}
```
- example usage
```shell
...
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
  return _this.validateSchema();
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
  return _this.transformUser();
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
  return _this.runDatabaseOperation();
}).then(function () {
  return _this.createSessionTokenIfNeeded();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.validateAuthData"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>validateAuthData ()](#apidoc.element.parse-server.RestWrite.prototype.validateAuthData)
- description and source-code
```javascript
validateAuthData = function () {
  if (this.className !== '_User') {
    return;
  }

  if (!this.query && !this.data.authData) {
    if (typeof this.data.username !== 'string') {
      throw new Parse.Error(Parse.Error.USERNAME_MISSING, 'bad or missing username');
    }
    if (typeof this.data.password !== 'string') {
      throw new Parse.Error(Parse.Error.PASSWORD_MISSING, 'password is required');
    }
  }

  if (!this.data.authData || !Object.keys(this.data.authData).length) {
    return;
  }

  var authData = this.data.authData;
  var providers = Object.keys(authData);
  if (providers.length > 0) {
    var canHandleAuthData = providers.reduce(function (canHandle, provider) {
      var providerAuthData = authData[provider];
      var hasToken = providerAuthData && providerAuthData.id;
      return canHandle && (hasToken || providerAuthData == null);
    }, true);
    if (canHandleAuthData) {
      return this.handleAuthData(authData);
    }
  }
  throw new Parse.Error(Parse.Error.UNSUPPORTED_SERVICE, 'This authentication method is unsupported.');
}
```
- example usage
```shell
...
}).then(function () {
  return _this.validateClientClassCreation();
}).then(function () {
  return _this.handleInstallation();
}).then(function () {
  return _this.handleSession();
}).then(function () {
  return _this.validateAuthData();
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
  return _this.validateSchema();
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.validateClientClassCreation"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>validateClientClassCreation ()](#apidoc.element.parse-server.RestWrite.prototype.validateClientClassCreation)
- description and source-code
```javascript
validateClientClassCreation = function () {
  var _this3 = this;

  if (this.config.allowClientClassCreation === false && !this.auth.isMaster && SchemaController.systemClasses.indexOf(this.className
) === -1) {
    return this.config.database.loadSchema().then(function (schemaController) {
      return schemaController.hasClass(_this3.className);
    }).then(function (hasClass) {
      if (hasClass !== true) {
        throw new Parse.Error(Parse.Error.OPERATION_FORBIDDEN, 'This user is not allowed to access ' + 'non-existent class: ' +
_this3.className);
      }
    });
  } else {
    return Promise.resolve();
  }
}
```
- example usage
```shell
...
var _this2 = this;

return Promise.resolve().then(function () {
  return _this2.getUserAndRoleACL();
}).then(function () {
  return _this2.redirectClassNameForKey();
}).then(function () {
  return _this2.validateClientClassCreation();
}).then(function () {
  return _this2.replaceSelect();
}).then(function () {
  return _this2.replaceDontSelect();
}).then(function () {
  return _this2.replaceInQuery();
}).then(function () {
...
```

#### <a name="apidoc.element.parse-server.RestWrite.prototype.validateSchema"></a>[function <span class="apidocSignatureSpan">parse-server.RestWrite.prototype.</span>validateSchema ()](#apidoc.element.parse-server.RestWrite.prototype.validateSchema)
- description and source-code
```javascript
validateSchema = function () {
  return this.config.database.validateObject(this.className, this.data, this.query, this.runOptions);
}
```
- example usage
```shell
...
}).then(function () {
  return _this.handleSession();
}).then(function () {
  return _this.validateAuthData();
}).then(function () {
  return _this.runBeforeTrigger();
}).then(function () {
  return _this.validateSchema();
}).then(function () {
  return _this.setRequiredFieldsIfNeeded();
}).then(function () {
  return _this.transformUser();
}).then(function () {
  return _this.expandFilesForExistingObjects();
}).then(function () {
...
```



# <a name="apidoc.module.parse-server.S3Adapter"></a>[module parse-server.S3Adapter](#apidoc.module.parse-server.S3Adapter)

#### <a name="apidoc.element.parse-server.S3Adapter.S3Adapter"></a>[function <span class="apidocSignatureSpan">parse-server.</span>S3Adapter ()](#apidoc.element.parse-server.S3Adapter.S3Adapter)
- description and source-code
```javascript
function S3Adapter() {
  var options = optionsFromArguments(arguments);
  this._region = options.region;
  this._bucket = options.bucket;
  this._bucketPrefix = options.bucketPrefix;
  this._directAccess = options.directAccess;
  this._baseUrl = options.baseUrl;
  this._baseUrlDirect = options.baseUrlDirect;
  this._signatureVersion = options.signatureVersion;
  this._globalCacheControl = options.globalCacheControl;

  let s3Options = {
    params: { Bucket: this._bucket },
    region: this._region,
    signatureVersion: this._signatureVersion,
    globalCacheControl: this._globalCacheControl
  };

  if (options.accessKey && options.secretKey) {
    s3Options.accessKeyId = options.accessKey;
    s3Options.secretAccessKey = options.secretKey;
  }

  Object.assign(s3Options, options.s3overrides);

  this._s3Client = new AWS.S3(s3Options);
  this._hasBucket = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.S3Adapter.default"></a>[function <span class="apidocSignatureSpan">parse-server.S3Adapter.</span>default ()](#apidoc.element.parse-server.S3Adapter.default)
- description and source-code
```javascript
function S3Adapter() {
  var options = optionsFromArguments(arguments);
  this._region = options.region;
  this._bucket = options.bucket;
  this._bucketPrefix = options.bucketPrefix;
  this._directAccess = options.directAccess;
  this._baseUrl = options.baseUrl;
  this._baseUrlDirect = options.baseUrlDirect;
  this._signatureVersion = options.signatureVersion;
  this._globalCacheControl = options.globalCacheControl;

  let s3Options = {
    params: { Bucket: this._bucket },
    region: this._region,
    signatureVersion: this._signatureVersion,
    globalCacheControl: this._globalCacheControl
  };

  if (options.accessKey && options.secretKey) {
    s3Options.accessKeyId = options.accessKey;
    s3Options.secretAccessKey = options.secretKey;
  }

  Object.assign(s3Options, options.s3overrides);

  this._s3Client = new AWS.S3(s3Options);
  this._hasBucket = false;
}
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.S3Adapter.prototype"></a>[module parse-server.S3Adapter.prototype](#apidoc.module.parse-server.S3Adapter.prototype)

#### <a name="apidoc.element.parse-server.S3Adapter.prototype.createBucket"></a>[function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>createBucket ()](#apidoc.element.parse-server.S3Adapter.prototype.createBucket)
- description and source-code
```javascript
createBucket = function () {
  var promise;
  if (this._hasBucket) {
    promise = Promise.resolve();
  } else {
    promise = new Promise((resolve) => {
      this._s3Client.createBucket(() => {
        this._hasBucket = true;
        resolve();
      });
    });
  }
  return promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.S3Adapter.prototype.createFile"></a>[function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>createFile (filename, data, contentType)](#apidoc.element.parse-server.S3Adapter.prototype.createFile)
- description and source-code
```javascript
createFile = function (filename, data, contentType) {
  let params = {
    Key: this._bucketPrefix + filename,
    Body: data
  };
  if (this._directAccess) {
    params.ACL = "public-read"
  }
  if (contentType) {
    params.ContentType = contentType;
  }
  if(this._globalCacheControl) {
    params.CacheControl = this._globalCacheControl;
  }
  return this.createBucket().then(() => {
    return new Promise((resolve, reject) => {
      this._s3Client.upload(params, (err, data) => {
        if (err !== null) {
          return reject(err);
        }
        resolve(data);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.S3Adapter.prototype.deleteFile"></a>[function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>deleteFile (filename)](#apidoc.element.parse-server.S3Adapter.prototype.deleteFile)
- description and source-code
```javascript
deleteFile = function (filename) {
  return this.createBucket().then(() => {
    return new Promise((resolve, reject) => {
      let params = {
        Key: this._bucketPrefix + filename
      };
      this._s3Client.deleteObject(params, (err, data) =>{
        if(err !== null) {
          return reject(err);
        }
        resolve(data);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.S3Adapter.prototype.getFileData"></a>[function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>getFileData (filename)](#apidoc.element.parse-server.S3Adapter.prototype.getFileData)
- description and source-code
```javascript
getFileData = function (filename) {
  let params = {Key: this._bucketPrefix + filename};
  return this.createBucket().then(() => {
    return new Promise((resolve, reject) => {
      this._s3Client.getObject(params, (err, data) => {
        if (err !== null) {
          return reject(err);
        }
        // Something happened here...
        if (data && !data.Body) {
          return reject(data);
        }
        resolve(data.Body);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.S3Adapter.prototype.getFileLocation"></a>[function <span class="apidocSignatureSpan">parse-server.S3Adapter.prototype.</span>getFileLocation (config, filename)](#apidoc.element.parse-server.S3Adapter.prototype.getFileLocation)
- description and source-code
```javascript
getFileLocation = function (config, filename) {
  filename = encodeURIComponent(filename);
  if (this._directAccess) {
    if (this._baseUrl && this._baseUrlDirect) {
      return '${this._baseUrl}/${filename}';
    } else if (this._baseUrl) {
      return '${this._baseUrl}/${this._bucketPrefix + filename}';
    } else {
      return 'https://${this._bucket}.s3.amazonaws.com/${this._bucketPrefix + filename}';
    }
  }
  return (config.mount + '/files/' + config.applicationId + '/' + filename);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.StatusHandler"></a>[module parse-server.StatusHandler](#apidoc.module.parse-server.StatusHandler)

#### <a name="apidoc.element.parse-server.StatusHandler.flatten"></a>[function <span class="apidocSignatureSpan">parse-server.StatusHandler.</span>flatten (array)](#apidoc.element.parse-server.StatusHandler.flatten)
- description and source-code
```javascript
function flatten(array) {
  var flattened = [];
  for (var i = 0; i < array.length; i++) {
    if (Array.isArray(array[i])) {
      flattened = flattened.concat(flatten(array[i]));
    } else {
      flattened.push(array[i]);
    }
  }
  return flattened;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.StatusHandler.jobStatusHandler"></a>[function <span class="apidocSignatureSpan">parse-server.StatusHandler.</span>jobStatusHandler (config)](#apidoc.element.parse-server.StatusHandler.jobStatusHandler)
- description and source-code
```javascript
function jobStatusHandler(config) {
  var jobStatus = void 0;
  var objectId = (0, _cryptoUtils.newObjectId)();
  var database = config.database;
  var handler = statusHandler(JOB_STATUS_COLLECTION, database);
  var setRunning = function setRunning(jobName, params) {
    var now = new Date();
    jobStatus = {
      objectId: objectId,
      jobName: jobName,
      params: params,
      status: 'running',
      source: 'api',
      createdAt: now,
      // lockdown!
      ACL: {}
    };

    return handler.create(jobStatus);
  };

  var setMessage = function setMessage(message) {
    if (!message || typeof message !== 'string') {
      return Promise.resolve();
    }
    return handler.update({ objectId: objectId }, { message: message });
  };

  var setSucceeded = function setSucceeded(message) {
    return setFinalStatus('succeeded', message);
  };

  var setFailed = function setFailed(message) {
    return setFinalStatus('failed', message);
  };

  var setFinalStatus = function setFinalStatus(status) {
    var message = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : undefined;

    var finishedAt = new Date();
    var update = { status: status, finishedAt: finishedAt };
    if (message && typeof message === 'string') {
      update.message = message;
    }
    return handler.update({ objectId: objectId }, update);
  };

  return Object.freeze({
    setRunning: setRunning,
    setSucceeded: setSucceeded,
    setMessage: setMessage,
    setFailed: setFailed
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.StatusHandler.pushStatusHandler"></a>[function <span class="apidocSignatureSpan">parse-server.StatusHandler.</span>pushStatusHandler (config)](#apidoc.element.parse-server.StatusHandler.pushStatusHandler)
- description and source-code
```javascript
function pushStatusHandler(config) {
  var objectId = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : (0, _cryptoUtils.newObjectId)();


  var pushStatus = void 0;
  var database = config.database;
  var handler = statusHandler(PUSH_STATUS_COLLECTION, database);
  var setInitial = function setInitial() {
    var body = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {};
    var where = arguments[1];
    var options = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : { source: 'rest' };

    var now = new Date();
    var data = body.data || {};
    var payloadString = JSON.stringify(data);
    var pushHash = void 0;
    if (typeof data.alert === 'string') {
      pushHash = (0, _cryptoUtils.md5Hash)(data.alert);
    } else if (_typeof(data.alert) === 'object') {
      pushHash = (0, _cryptoUtils.md5Hash)(JSON.stringify(data.alert));
    } else {
      pushHash = 'd41d8cd98f00b204e9800998ecf8427e';
    }
    var object = {
      objectId: objectId,
      createdAt: now,
      pushTime: now.toISOString(),
      query: JSON.stringify(where),
      payload: payloadString,
      source: options.source,
      title: options.title,
      expiry: body.expiration_time,
      status: "pending",
      numSent: 0,
      pushHash: pushHash,
      // lockdown!
      ACL: {}
    };

    return handler.create(object).then(function () {
      pushStatus = {
        objectId: objectId
      };
      return Promise.resolve(pushStatus);
    });
  };

  var setRunning = function setRunning(count) {
    _logger.logger.verbose('_PushStatus ' + objectId + ': sending push to %d installations', count);
    return handler.update({ status: "pending", objectId: objectId }, { status: "running", updatedAt: new Date(), count: count });
  };

  var trackSent = function trackSent(results) {
    var _this = this;

    var update = {
      updatedAt: new Date(),
      numSent: 0,
      numFailed: 0
    };
    if (Array.isArray(results)) {
      results = flatten(results);
      results.reduce(function (memo, result) {
        // Cannot handle that
        if (!result || !result.device || !result.device.deviceType) {
          return memo;
        }
        var deviceType = result.device.deviceType;
        var key = result.transmitted ? 'sentPerType.' + deviceType : 'failedPerType.' + deviceType;
        memo[key] = incrementOp(memo, key);
        if (result.transmitted) {
          memo.numSent++;
        } else {
          memo.numFailed++;
        }
        return memo;
      }, update);
      incrementOp(update, 'count', -results.length);
    }

    _logger.logger.verbose('_PushStatus ' + objectId + ': sent push! %d success, %d failures', update.numSent, update.numFailed);

    ['numSent', 'numFailed'].forEach(function (key) {
      if (update[key] > 0) {
        update[key] = {
          __op: 'Increment',
          amount: update[key]
        };
      } else {
        delete update[key];
      }
    });

    return handler.update({ objectId: objectId }, update).then(function (res) {
      if (res && res.count === 0) {
        return _this.complete();
      }
    });
  };

  var complete = function complete() {
    return handler.update({ objectId: objectId }, {
      status: 'succeeded',
      count: { __op: 'Delete' },
      updatedAt: new Date()
    });
  };

  var fail = function fail(err) {
    var update = {
      errorMessage: JSON.stringify(err),
      status: 'failed',
      updatedAt: new Date()
    };
    _logger.logger.warn('_PushStatus ' + objectId + ': error while sending push', err);
    return handler.update({ objectId: objectId }, update);
  };

  return Object.freeze({
    objectId: objectId,
    setInitial: setInitial,
    setRunning: setRunning,
    trackSent: trackSent,
    complete: complete,
    fail: fail
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.TestUtils"></a>[module parse-server.TestUtils](#apidoc.module.parse-server.TestUtils)

#### <a name="apidoc.element.parse-server.TestUtils.destroyAllDataPermanently"></a>[function <span class="apidocSignatureSpan">parse-server.TestUtils.</span>destroyAllDataPermanently ()](#apidoc.element.parse-server.TestUtils.destroyAllDataPermanently)
- description and source-code
```javascript
function destroyAllDataPermanently() {
  if (!process.env.TESTING) {
    throw 'Only supported in test environment';
  }
  return Promise.all(Object.keys(_cache2.default.cache).map(function (appId) {
    var app = _cache2.default.get(appId);
    if (app.databaseController) {
      return app.databaseController.deleteEverything();
    } else {
      return Promise.resolve();
    }
  }));
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.batch"></a>[module parse-server.batch](#apidoc.module.parse-server.batch)

#### <a name="apidoc.element.parse-server.batch.makeBatchRoutingPathFunction"></a>[function <span class="apidocSignatureSpan">parse-server.batch.</span>makeBatchRoutingPathFunction (originalUrl, serverURL, publicServerURL)](#apidoc.element.parse-server.batch.makeBatchRoutingPathFunction)
- description and source-code
```javascript
function makeBatchRoutingPathFunction(originalUrl, serverURL, publicServerURL) {
  serverURL = serverURL ? parseURL(serverURL) : undefined;
  publicServerURL = publicServerURL ? parseURL(publicServerURL) : undefined;

  var apiPrefixLength = originalUrl.length - batchPath.length;
  var apiPrefix = originalUrl.slice(0, apiPrefixLength);

  var makeRoutablePath = function makeRoutablePath(requestPath) {
    // The routablePath is the path minus the api prefix
    if (requestPath.slice(0, apiPrefix.length) != apiPrefix) {
      throw new Parse.Error(Parse.Error.INVALID_JSON, 'cannot route batch path ' + requestPath);
    }
    return path.posix.join('/', requestPath.slice(apiPrefix.length));
  };

  if (serverURL && publicServerURL && serverURL.path != publicServerURL.path) {
    var localPath = serverURL.path;
    var publicPath = publicServerURL.path;
    // Override the api prefix
    apiPrefix = localPath;
    return function (requestPath) {
      // Build the new path by removing the public path
      // and joining with the local path
      var newPath = path.posix.join('/', localPath, '/', requestPath.slice(publicPath.length));
      // Use the method for local routing
      return makeRoutablePath(newPath);
    };
  }

  return makeRoutablePath;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.batch.mountOnto"></a>[function <span class="apidocSignatureSpan">parse-server.batch.</span>mountOnto (router)](#apidoc.element.parse-server.batch.mountOnto)
- description and source-code
```javascript
function mountOnto(router) {
  router.route('POST', batchPath, function (req) {
    return handleBatch(router, req);
  });
}
```
- example usage
```shell
...

    var routes = routers.reduce(function (memo, router) {
      return memo.concat(router.routes);
    }, []);

    var appRouter = new _PromiseRouter2.default(routes, appId);

    batch.mountOnto(appRouter);
    return appRouter;
  }
}, {
  key: 'createLiveQueryServer',
  value: function createLiveQueryServer(httpServer, config) {
    return new _ParseLiveQueryServer.ParseLiveQueryServer(httpServer, config);
  }
...
```



# <a name="apidoc.module.parse-server.cryptoUtils"></a>[module parse-server.cryptoUtils](#apidoc.module.parse-server.cryptoUtils)

#### <a name="apidoc.element.parse-server.cryptoUtils.md5Hash"></a>[function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>md5Hash (string)](#apidoc.element.parse-server.cryptoUtils.md5Hash)
- description and source-code
```javascript
function md5Hash(string) {
  return (0, _crypto.createHash)('md5').update(string).digest('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.cryptoUtils.newObjectId"></a>[function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>newObjectId ()](#apidoc.element.parse-server.cryptoUtils.newObjectId)
- description and source-code
```javascript
function newObjectId() {
  //TODO: increase length to better protect against collisions.
  return randomString(10);
}
```
- example usage
```shell
...
    // Add default fields
    this.data.updatedAt = this.updatedAt;
    if (!this.query) {
      this.data.createdAt = this.updatedAt;

      // Only assign new objectId if we are creating new object
      if (!this.data.objectId) {
        this.data.objectId = cryptoUtils.newObjectId();
      }
    }
  }
  return Promise.resolve();
};

// Transforms auth data for a user object.
...
```

#### <a name="apidoc.element.parse-server.cryptoUtils.newToken"></a>[function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>newToken ()](#apidoc.element.parse-server.cryptoUtils.newToken)
- description and source-code
```javascript
function newToken() {
  return randomHexString(32);
}
```
- example usage
```shell
...

RestWrite.prototype.createSessionToken = function () {
// cloud installationId from Cloud Code,
// never create session tokens from there.
if (this.auth.installationId && this.auth.installationId === 'cloud') {
  return;
}
var token = 'r:' + cryptoUtils.newToken();

var expiresAt = this.config.generateSessionExpiresAt();
var sessionData = {
  sessionToken: token,
  user: {
    __type: 'Pointer',
    className: '_User',
...
```

#### <a name="apidoc.element.parse-server.cryptoUtils.randomHexString"></a>[function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>randomHexString (size)](#apidoc.element.parse-server.cryptoUtils.randomHexString)
- description and source-code
```javascript
function randomHexString(size) {
  if (size === 0) {
    throw new Error('Zero-length randomHexString is useless.');
  }
  if (size % 2 !== 0) {
    throw new Error('randomHexString size must be divisible by 2.');
  }
  return (0, _crypto.randomBytes)(size / 2).toString('hex');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.cryptoUtils.randomString"></a>[function <span class="apidocSignatureSpan">parse-server.cryptoUtils.</span>randomString (size)](#apidoc.element.parse-server.cryptoUtils.randomString)
- description and source-code
```javascript
function randomString(size) {
  if (size === 0) {
    throw new Error('Zero-length randomString is useless.');
  }
  var chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ' + 'abcdefghijklmnopqrstuvwxyz' + '0123456789';
  var objectId = '';
  var bytes = (0, _crypto.randomBytes)(size);
  for (var i = 0; i < bytes.length; ++i) {
    objectId += chars[bytes.readUInt8(i) % chars.length];
  }
  return objectId;
}
```
- example usage
```shell
...
});
};

RestWrite.prototype._validateUserName = function () {
// Check for username uniqueness
if (!this.data.username) {
  if (!this.query) {
    this.data.username = cryptoUtils.randomString(25);
    this.responseShouldHaveUsername = true;
  }
  return Promise.resolve();
}
// We need to a find to check for duplicate username in case they are missing the unique index on usernames
// TODO: Check if there is a unique index, and if so, skip this query.
return this.config.database.find(this.className, { username: this.data.username, objectId: { '$ne': this.objectId() } }, { limit
: 1 }).then(function (results) {
...
```



# <a name="apidoc.module.parse-server.deprecated"></a>[module parse-server.deprecated](#apidoc.module.parse-server.deprecated)

#### <a name="apidoc.element.parse-server.deprecated.useExternal"></a>[function <span class="apidocSignatureSpan">parse-server.deprecated.</span>useExternal (name, moduleName)](#apidoc.element.parse-server.deprecated.useExternal)
- description and source-code
```javascript
function useExternal(name, moduleName) {
  return function () {
    throw name + " is not provided by parse-server anymore; please install " + moduleName;
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.logger"></a>[module parse-server.logger](#apidoc.module.parse-server.logger)

#### <a name="apidoc.element.parse-server.logger.getLogger"></a>[function <span class="apidocSignatureSpan">parse-server.logger.</span>getLogger ()](#apidoc.element.parse-server.logger.getLogger)
- description and source-code
```javascript
function getLogger() {
  return logger;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.logger.setLogger"></a>[function <span class="apidocSignatureSpan">parse-server.logger.</span>setLogger (aLogger)](#apidoc.element.parse-server.logger.setLogger)
- description and source-code
```javascript
function setLogger(aLogger) {
  logger = aLogger;
}
```
- example usage
```shell
...
  throw 'When using an explicit database adapter, you must also use an explicit filesAdapter.';
}

userSensitiveFields = Array.from(new Set(userSensitiveFields.concat(_defaults2.default.userSensitiveFields, userSensitiveFields)));

var loggerControllerAdapter = (0, _AdapterLoader.loadAdapter)(loggerAdapter, _WinstonLoggerAdapter.WinstonLoggerAdapter, { jsonLogs
: jsonLogs, logsFolder: logsFolder, verbose: verbose, logLevel: logLevel, silent: silent });
var loggerController = new _LoggerController.LoggerController(loggerControllerAdapter, appId);
logging.setLogger(loggerController);

var filesControllerAdapter = (0, _AdapterLoader.loadAdapter)(filesAdapter, function () {
  return new _GridStoreAdapter.GridStoreAdapter(databaseURI);
});
var filesController = new _FilesController.FilesController(filesControllerAdapter, appId);

var pushOptions = Object.assign({}, push);
...
```



# <a name="apidoc.module.parse-server.middlewares"></a>[module parse-server.middlewares](#apidoc.module.parse-server.middlewares)

#### <a name="apidoc.element.parse-server.middlewares.allowCrossDomain"></a>[function <span class="apidocSignatureSpan">parse-server.middlewares.</span>allowCrossDomain (req, res, next)](#apidoc.element.parse-server.middlewares.allowCrossDomain)
- description and source-code
```javascript
function allowCrossDomain(req, res, next) {
  res.header('Access-Control-Allow-Origin', '*');
  res.header('Access-Control-Allow-Methods', 'GET,PUT,POST,DELETE,OPTIONS');
  res.header('Access-Control-Allow-Headers', 'X-Parse-Master-Key, X-Parse-REST-API-Key, X-Parse-Javascript-Key, X-Parse-Application
-Id, X-Parse-Client-Version, X-Parse-Session-Token, X-Requested-With, X-Parse-Revocable-Session, Content-Type');

  // intercept OPTIONS method
  if ('OPTIONS' == req.method) {
    res.sendStatus(200);
  } else {
    next();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.middlewares.allowMethodOverride"></a>[function <span class="apidocSignatureSpan">parse-server.middlewares.</span>allowMethodOverride (req, res, next)](#apidoc.element.parse-server.middlewares.allowMethodOverride)
- description and source-code
```javascript
function allowMethodOverride(req, res, next) {
  if (req.method === 'POST' && req.body._method) {
    req.originalMethod = req.method;
    req.method = req.body._method;
    delete req.body._method;
  }
  next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.middlewares.enforceMasterKeyAccess"></a>[function <span class="apidocSignatureSpan">parse-server.middlewares.</span>enforceMasterKeyAccess (req, res, next)](#apidoc.element.parse-server.middlewares.enforceMasterKeyAccess)
- description and source-code
```javascript
function enforceMasterKeyAccess(req, res, next) {
  if (!req.auth.isMaster) {
    res.status(403);
    res.end('{"error":"unauthorized: master key is required"}');
    return;
  }
  next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.middlewares.handleParseErrors"></a>[function <span class="apidocSignatureSpan">parse-server.middlewares.</span>handleParseErrors (err, req, res, next)](#apidoc.element.parse-server.middlewares.handleParseErrors)
- description and source-code
```javascript
function handleParseErrors(err, req, res, next) {
  if (err instanceof _node2.default.Error) {
    var httpStatus = void 0;
    // TODO: fill out this mapping
    switch (err.code) {
      case _node2.default.Error.INTERNAL_SERVER_ERROR:
        httpStatus = 500;
        break;
      case _node2.default.Error.OBJECT_NOT_FOUND:
        httpStatus = 404;
        break;
      default:
        httpStatus = 400;
    }

    res.status(httpStatus);
    res.json({ code: err.code, error: err.message });
    _logger2.default.error(err.message, err);
  } else if (err.status && err.message) {
    res.status(err.status);
    res.json({ error: err.message });
    next(err);
  } else {
    _logger2.default.error('Uncaught internal server error.', err, err.stack);
    res.status(500);
    res.json({
      code: _node2.default.Error.INTERNAL_SERVER_ERROR,
      message: 'Internal server error.'
    });
    next(err);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.middlewares.handleParseHeaders"></a>[function <span class="apidocSignatureSpan">parse-server.middlewares.</span>handleParseHeaders (req, res, next)](#apidoc.element.parse-server.middlewares.handleParseHeaders)
- description and source-code
```javascript
function handleParseHeaders(req, res, next) {
  var mountPathLength = req.originalUrl.length - req.url.length;
  var mountPath = req.originalUrl.slice(0, mountPathLength);
  var mount = req.protocol + '://' + req.get('host') + mountPath;

  var info = {
    appId: req.get('X-Parse-Application-Id'),
    sessionToken: req.get('X-Parse-Session-Token'),
    masterKey: req.get('X-Parse-Master-Key'),
    installationId: req.get('X-Parse-Installation-Id'),
    clientKey: req.get('X-Parse-Client-Key'),
    javascriptKey: req.get('X-Parse-Javascript-Key'),
    dotNetKey: req.get('X-Parse-Windows-Key'),
    restAPIKey: req.get('X-Parse-REST-API-Key'),
    clientVersion: req.get('X-Parse-Client-Version')
  };

  var basicAuth = httpAuth(req);

  if (basicAuth) {
    var basicAuthAppId = basicAuth.appId;
    if (_cache2.default.get(basicAuthAppId)) {
      info.appId = basicAuthAppId;
      info.masterKey = basicAuth.masterKey || info.masterKey;
      info.javascriptKey = basicAuth.javascriptKey || info.javascriptKey;
    }
  }

  if (req.body) {
    // Unity SDK sends a _noBody key which needs to be removed.
    // Unclear at this point if action needs to be taken.
    delete req.body._noBody;
  }

  var fileViaJSON = false;

  if (!info.appId || !_cache2.default.get(info.appId)) {
    // See if we can find the app id on the body.
    if (req.body instanceof Buffer) {
      // The only chance to find the app id is if this is a file
      // upload that actually is a JSON body. So try to parse it.
      req.body = JSON.parse(req.body);
      fileViaJSON = true;
    }

    if (req.body) {
      delete req.body._RevocableSession;
    }

    if (req.body && req.body._ApplicationId && _cache2.default.get(req.body._ApplicationId) && (!info.masterKey || _cache2.default
.get(req.body._ApplicationId).masterKey === info.masterKey)) {
      info.appId = req.body._ApplicationId;
      info.javascriptKey = req.body._JavaScriptKey || '';
      delete req.body._ApplicationId;
      delete req.body._JavaScriptKey;
      // TODO: test that the REST API formats generated by the other
      // SDKs are handled ok
      if (req.body._ClientVersion) {
        info.clientVersion = req.body._ClientVersion;
        delete req.body._ClientVersion;
      }
      if (req.body._InstallationId) {
        info.installationId = req.body._InstallationId;
        delete req.body._InstallationId;
      }
      if (req.body._SessionToken) {
        info.sessionToken = req.body._SessionToken;
        delete req.body._SessionToken;
      }
      if (req.body._MasterKey) {
        info.masterKey = req.body._MasterKey;
        delete req.body._MasterKey;
      }
      if (req.body._ContentType) {
        req.headers['content-type'] = req.body._ContentType;
        delete req.body._ContentType;
      }
    } else {
      return invalidRequest(req, res);
    }
  }

  if (info.clientVersion) {
    info.clientSDK = _ClientSDK2.default.fromString(info.clientVersion);
  }

  if (fileViaJSON) {
    // We need to repopulate req.body with a buffer
    var base64 = req.body.base64;
    req.body = new Buffer(base64, 'base64');
  }

  info.app = _cache2.default.get(info.appId);
  req.config = new _Config2.default(info.appId, mount);
  req.info = info;

  var isMaster = info.masterKey === req.config.masterKey;

  if (isMaster) {
    req.auth = new _Auth2.default.Auth({ config: req.config, installationId: info.installationId, isMaster: true });
    next();
    return;
  }

  // Client keys are not required in parse-server, but if any have been configured in the server, validate them
  //  to preserve original behavior.
  var keys = ["clientKey", "javascriptKey", "dotNetKey", "restAPIKey"];
  var oneKeyConfigured = keys.some(function (key) {
    return req.config[key] !== undefined;
  });
  var oneKeyMatches = keys.some(function (key) {
    return req.config[key] !== undefined && info[key] === req.config[key];
  });

  if (oneKeyConfigured && !oneKeyMatches) {
    return invalidRequest(req, res);
  }

  if (req.url == "/login") {
    delete info.sessionToken;
  }

  if (!info.sessionT ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.middlewares.promiseEnforceMasterKeyAccess"></a>[function <span class="apidocSignatureSpan">parse-server.middlewares.</span>promiseEnforceMasterKeyAccess (request)](#apidoc.element.parse-server.middlewares.promiseEnforceMasterKeyAccess)
- description and source-code
```javascript
function promiseEnforceMasterKeyAccess(request) {
  if (!request.auth.isMaster) {
    var error = new Error();
    error.status = 403;
    error.message = "unauthorized: master key is required";
    throw error;
  }
  return Promise.resolve();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parse-server.password"></a>[module parse-server.password](#apidoc.module.parse-server.password)

#### <a name="apidoc.element.parse-server.password.compare"></a>[function <span class="apidocSignatureSpan">parse-server.password.</span>compare (password, hashedPassword)](#apidoc.element.parse-server.password.compare)
- description and source-code
```javascript
function compare(password, hashedPassword) {
  return new Promise(function (fulfill, reject) {
    // Cannot bcrypt compare when one is undefined
    if (!password || !hashedPassword) {
      return fulfill(false);
    }
    bcrypt.compare(password, hashedPassword, function (err, success) {
      if (err) {
        reject(err);
      } else {
        fulfill(success);
      }
    });
  });
}
```
- example usage
```shell
...
var user = results[0];
var oldPasswords = [];
if (user._password_history) oldPasswords = _lodash2.default.take(user._password_history, _this11.config.passwordPolicy.maxPasswordHistory
 - 1);
oldPasswords.push(user.password);
var newPassword = _this11.data.password;
// compare the new password hash with all old password hashes
var promises = oldPasswords.map(function (hash) {
  return passwordCrypto.compare(newPassword, hash).then(function (result) {
    if (result) // reject if there is a match
      return Promise.reject("REPEAT_PASSWORD");
    return Promise.resolve();
  });
});
// wait for all comparisons to complete
return Promise.all(promises).then(function () {
...
```

#### <a name="apidoc.element.parse-server.password.hash"></a>[function <span class="apidocSignatureSpan">parse-server.password.</span>hash (password)](#apidoc.element.parse-server.password.hash)
- description and source-code
```javascript
function hash(password) {
  return new Promise(function (fulfill, reject) {
    bcrypt.hash(password, 10, function (err, hashedPassword) {
      if (err) {
        reject(err);
      } else {
        fulfill(hashedPassword);
      }
    });
  });
}
```
- example usage
```shell
...

  if (_this7.query && !_this7.auth.isMaster) {
    _this7.storage['clearSessions'] = true;
    _this7.storage['generateNewSession'] = true;
  }

  return _this7._validatePasswordPolicy().then(function () {
    return passwordCrypto.hash(_this7.data.password).then(function (hashedPassword) {
      _this7.data._hashed_password = hashedPassword;
      delete _this7.data.password;
    });
  });
}).then(function () {
  return _this7._validateUserName();
}).then(function () {
...
```



# <a name="apidoc.module.parse-server.requiredParameter"></a>[module parse-server.requiredParameter](#apidoc.module.parse-server.requiredParameter)

#### <a name="apidoc.element.parse-server.requiredParameter.default"></a>[function <span class="apidocSignatureSpan">parse-server.requiredParameter.</span>default (errorMessage)](#apidoc.element.parse-server.requiredParameter.default)
- description and source-code
```javascript
default = function (errorMessage) {
  throw errorMessage;
}
```
- example usage
```shell
...
this.webhookKey = cacheInfo.webhookKey;
this.fileKey = cacheInfo.fileKey;
this.allowClientClassCreation = cacheInfo.allowClientClassCreation;
this.userSensitiveFields = cacheInfo.userSensitiveFields;

// Create a new DatabaseController per request
if (cacheInfo.databaseController) {
  var schemaCache = new _SchemaCache2.default(cacheInfo.cacheController, cacheInfo.schemaCacheTTL, cacheInfo.enableSingleSchemaCache
);
  this.database = new _DatabaseController2.default(cacheInfo.databaseController.adapter, schemaCache);
}

this.schemaCacheTTL = cacheInfo.schemaCacheTTL;
this.enableSingleSchemaCache = cacheInfo.enableSingleSchemaCache;

this.serverURL = cacheInfo.serverURL;
...
```



# <a name="apidoc.module.parse-server.rest"></a>[module parse-server.rest](#apidoc.module.parse-server.rest)

#### <a name="apidoc.element.parse-server.rest.create"></a>[function <span class="apidocSignatureSpan">parse-server.rest.</span>create (config, auth, className, restObject, clientSDK)](#apidoc.element.parse-server.rest.create)
- description and source-code
```javascript
function create(config, auth, className, restObject, clientSDK) {
  enforceRoleSecurity('create', className, auth);
  var write = new RestWrite(config, auth, className, null, restObject, null, clientSDK);
  return write.execute();
}
```
- example usage
```shell
...
// password timestamp to be used when password expiry policy is enforced
if (this.config.passwordPolicy && this.config.passwordPolicy.maxPasswordAge) {
  this.data._password_changed_at = Parse._encode(new Date());
}
    }

    // Run a create
    return this.config.database.create(this.className, this.data, this.runOptions).catch(function (error) {
if (_this14.className !== '_User' || error.code !== Parse.Error.DUPLICATE_VALUE) {
  throw error;
}
// If this was a failed user creation due to username or email already taken, we need to
// check whether it was username or email and return the appropriate error.

// TODO: See if we can later do this without additional queries by using named indexes.
...
```

#### <a name="apidoc.element.parse-server.rest.del"></a>[function <span class="apidocSignatureSpan">parse-server.rest.</span>del (config, auth, className, objectId)](#apidoc.element.parse-server.rest.del)
- description and source-code
```javascript
function del(config, auth, className, objectId) {
  if (typeof objectId !== 'string') {
    throw new Parse.Error(Parse.Error.INVALID_JSON, 'bad objectId');
  }

  if (className === '_User' && !auth.couldUpdateUserId(objectId)) {
    throw new Parse.Error(Parse.Error.SESSION_MISSING, 'insufficient auth to delete user');
  }

  enforceRoleSecurity('delete', className, auth);

  var inflatedObject;

  return Promise.resolve().then(function () {
    var hasTriggers = checkTriggers(className, config, ['beforeDelete', 'afterDelete']);
    var hasLiveQuery = checkLiveQuery(className, config);
    if (hasTriggers || hasLiveQuery || className == '_Session') {
      return find(config, _Auth2.default.master(config), className, { objectId: objectId }).then(function (response) {
        if (response && response.results && response.results.length) {
          response.results[0].className = className;

          var cacheAdapter = config.cacheController;
          cacheAdapter.user.del(response.results[0].sessionToken);
          inflatedObject = Parse.Object.fromJSON(response.results[0]);
          // Notify LiveQuery server if possible
          config.liveQueryController.onAfterDelete(inflatedObject.className, inflatedObject);
          return triggers.maybeRunTrigger(triggers.Types.beforeDelete, auth, inflatedObject, null, config);
        }
        throw new Parse.Error(Parse.Error.OBJECT_NOT_FOUND, 'Object not found for delete.');
      });
    }
    return Promise.resolve({});
  }).then(function () {
    if (!auth.isMaster) {
      return auth.getUserRoles();
    } else {
      return;
    }
  }).then(function () {
    var options = {};
    if (!auth.isMaster) {
      options.acl = ['*'];
      if (auth.user) {
        options.acl.push(auth.user.id);
        options.acl = options.acl.concat(auth.userRoles);
      }
    }

    return config.database.destroy(className, {
      objectId: objectId
    }, options);
  }).then(function () {
    return triggers.maybeRunTrigger(triggers.Types.afterDelete, auth, inflatedObject, null, config);
  });
}
```
- example usage
```shell
...
    user: {
      __type: "Pointer",
      className: "_User",
      objectId: this.objectId()
    }
  }).execute().then(function (results) {
    results.results.forEach(function (session) {
      return _this7.config.cacheController.user.del(session.sessionToken);
    });
  });
}

return promise.then(function () {
  // Transform the password
  if (_this7.data.password === undefined) {
...
```

#### <a name="apidoc.element.parse-server.rest.find"></a>[function <span class="apidocSignatureSpan">parse-server.rest.</span>find (config, auth, className, restWhere, restOptions, clientSDK)](#apidoc.element.parse-server.rest.find)
- description and source-code
```javascript
function find(config, auth, className, restWhere, restOptions, clientSDK) {
  enforceRoleSecurity('find', className, auth);
  return triggers.maybeRunQueryTrigger(triggers.Types.beforeFind, className, restWhere, restOptions, config, auth).then(function
 (result) {
    restWhere = result.restWhere || restWhere;
    restOptions = result.restOptions || restOptions;
    var query = new RestQuery(config, auth, className, restWhere, restOptions, clientSDK);
    return query.execute();
  });
}
```
- example usage
```shell
...

      return new Promise(function (resolve, reject) {
var query = {
  username: _this._user.username,
  _failed_login_count: { $exists: true }
};

_this._config.database.find('_User', query).then(function (users) {
  if (Array.isArray(users) && users.length > 0) {
    resolve(true);
  } else {
    resolve(false);
  }
}).catch(function (err) {
  reject(err);
...
```

#### <a name="apidoc.element.parse-server.rest.get"></a>[function <span class="apidocSignatureSpan">parse-server.rest.</span>get (config, auth, className, objectId, restOptions, clientSDK)](#apidoc.element.parse-server.rest.get)
- description and source-code
```javascript
function get(config, auth, className, objectId, restOptions, clientSDK) {
  enforceRoleSecurity('get', className, auth);
  var query = new RestQuery(config, auth, className, { objectId: objectId }, restOptions, clientSDK);
  return query.execute();
}
```
- example usage
```shell
...
// Returns a promise that resolves to an Auth object
var getAuthForSessionToken = function getAuthForSessionToken() {
  var _ref2 = arguments.length > 0 && arguments[0] !== undefined ? arguments[0] : {},
  config = _ref2.config,
  sessionToken = _ref2.sessionToken,
  installationId = _ref2.installationId;

  return config.cacheController.user.get(sessionToken).then(function (userJSON) {
if (userJSON) {
  var cachedUser = Parse.Object.fromJSON(userJSON);
  return Promise.resolve(new Auth({ config: config, isMaster: false, installationId: installationId, user: cachedUser }));
}

var restOptions = {
  limit: 1,
...
```

#### <a name="apidoc.element.parse-server.rest.update"></a>[function <span class="apidocSignatureSpan">parse-server.rest.</span>update (config, auth, className, objectId, restObject, clientSDK)](#apidoc.element.parse-server.rest.update)
- description and source-code
```javascript
function update(config, auth, className, objectId, restObject, clientSDK) {
  enforceRoleSecurity('update', className, auth);

  return Promise.resolve().then(function () {
    var hasTriggers = checkTriggers(className, config, ['beforeSave', 'afterSave']);
    var hasLiveQuery = checkLiveQuery(className, config);
    if (hasTriggers || hasLiveQuery) {
      return find(config, _Auth2.default.master(config), className, { objectId: objectId });
    }
    return Promise.resolve({});
  }).then(function (response) {
    var originalRestObject;
    if (response && response.results && response.results.length) {
      originalRestObject = response.results[0];
    }

    var write = new RestWrite(config, auth, className, { objectId: objectId }, restObject, originalRestObject, clientSDK);
    return write.execute();
  });
}
```
- example usage
```shell
...
      username: this._user.username
    };

    var updateFields = {
      _failed_login_count: value
    };

    return this._config.database.update('_User', query, updateFields);
  }

  /**
   * check if the _failed_login_count field has been set
   */

}, {
...
```



# <a name="apidoc.module.parse-server.triggers"></a>[module parse-server.triggers](#apidoc.module.parse-server.triggers)

#### <a name="apidoc.element.parse-server.triggers._unregister"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>_unregister (appId, category, className, type)](#apidoc.element.parse-server.triggers._unregister)
- description and source-code
```javascript
function _unregister(appId, category, className, type) {
  if (type) {
    removeTrigger(className, type, appId);
    delete _triggerStore[appId][category][className][type];
  } else {
    delete _triggerStore[appId][category][className];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers._unregisterAll"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>_unregisterAll ()](#apidoc.element.parse-server.triggers._unregisterAll)
- description and source-code
```javascript
function _unregisterAll() {
  Object.keys(_triggerStore).forEach(function (appId) {
    return delete _triggerStore[appId];
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.addFunction"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>addFunction (functionName, handler, validationHandler, applicationId)](#apidoc.element.parse-server.triggers.addFunction)
- description and source-code
```javascript
function addFunction(functionName, handler, validationHandler, applicationId) {
  applicationId = applicationId || _node2.default.applicationId;
  _triggerStore[applicationId] = _triggerStore[applicationId] || baseStore();
  _triggerStore[applicationId].Functions[functionName] = handler;
  _triggerStore[applicationId].Validators[functionName] = validationHandler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.addJob"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>addJob (jobName, handler, applicationId)](#apidoc.element.parse-server.triggers.addJob)
- description and source-code
```javascript
function addJob(jobName, handler, applicationId) {
  applicationId = applicationId || _node2.default.applicationId;
  _triggerStore[applicationId] = _triggerStore[applicationId] || baseStore();
  _triggerStore[applicationId].Jobs[jobName] = handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.addTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>addTrigger (type, className, handler, applicationId)](#apidoc.element.parse-server.triggers.addTrigger)
- description and source-code
```javascript
function addTrigger(type, className, handler, applicationId) {
  applicationId = applicationId || _node2.default.applicationId;
  _triggerStore[applicationId] = _triggerStore[applicationId] || baseStore();
  _triggerStore[applicationId].Triggers[type][className] = handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getFunction"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getFunction (functionName, applicationId)](#apidoc.element.parse-server.triggers.getFunction)
- description and source-code
```javascript
function getFunction(functionName, applicationId) {
  var manager = _triggerStore[applicationId];
  if (manager && manager.Functions) {
    return manager.Functions[functionName];
  }
  return undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getJob"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getJob (jobName, applicationId)](#apidoc.element.parse-server.triggers.getJob)
- description and source-code
```javascript
function getJob(jobName, applicationId) {
  var manager = _triggerStore[applicationId];
  if (manager && manager.Jobs) {
    return manager.Jobs[jobName];
  }
  return undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getJobs"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getJobs (applicationId)](#apidoc.element.parse-server.triggers.getJobs)
- description and source-code
```javascript
function getJobs(applicationId) {
  var manager = _triggerStore[applicationId];
  if (manager && manager.Jobs) {
    return manager.Jobs;
  }
  return undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getRequestObject"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getRequestObject (triggerType, auth, parseObject, originalParseObject, config)](#apidoc.element.parse-server.triggers.getRequestObject)
- description and source-code
```javascript
function getRequestObject(triggerType, auth, parseObject, originalParseObject, config) {
  var request = {
    triggerName: triggerType,
    object: parseObject,
    master: false,
    log: config.loggerController
  };

  if (originalParseObject) {
    request.original = originalParseObject;
  }

  if (!auth) {
    return request;
  }
  if (auth.isMaster) {
    request['master'] = true;
  }
  if (auth.user) {
    request['user'] = auth.user;
  }
  if (auth.installationId) {
    request['installationId'] = auth.installationId;
  }
  return request;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getRequestQueryObject"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getRequestQueryObject (triggerType, auth, query, config)](#apidoc.element.parse-server.triggers.getRequestQueryObject)
- description and source-code
```javascript
function getRequestQueryObject(triggerType, auth, query, config) {
  var request = {
    triggerName: triggerType,
    query: query,
    master: false,
    log: config.loggerController
  };

  if (!auth) {
    return request;
  }
  if (auth.isMaster) {
    request['master'] = true;
  }
  if (auth.user) {
    request['user'] = auth.user;
  }
  if (auth.installationId) {
    request['installationId'] = auth.installationId;
  }
  return request;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getResponseObject"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getResponseObject (request, resolve, reject)](#apidoc.element.parse-server.triggers.getResponseObject)
- description and source-code
```javascript
function getResponseObject(request, resolve, reject) {
  return {
    success: function success(response) {
      if (request.triggerName === Types.afterFind) {
        if (!response) {
          response = request.objects;
        }
        response = response.map(function (object) {
          return object.toJSON();
        });
        return resolve(response);
      }
      // Use the JSON response
      if (response && !request.object.equals(response) && request.triggerName === Types.beforeSave) {
        return resolve(response);
      }
      response = {};
      if (request.triggerName === Types.beforeSave) {
        response['object'] = request.object._getSaveJSON();
      }
      return resolve(response);
    },
    error: function error(code, message) {
      if (!message) {
        message = code;
        code = _node2.default.Error.SCRIPT_FAILED;
      }
      var scriptError = new _node2.default.Error(code, message);
      return reject(scriptError);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.getTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getTrigger (className, triggerType, applicationId)](#apidoc.element.parse-server.triggers.getTrigger)
- description and source-code
```javascript
function getTrigger(className, triggerType, applicationId) {
  if (!applicationId) {
    throw "Missing ApplicationID";
  }
  var manager = _triggerStore[applicationId];
  if (manager && manager.Triggers && manager.Triggers[triggerType] && manager.Triggers[triggerType][className]) {
    return manager.Triggers[triggerType][className];
  }
  return undefined;
}
```
- example usage
```shell
...

var RestQuery = require('./RestQuery');
var RestWrite = require('./RestWrite');
var triggers = require('./triggers');

function checkTriggers(className, config, types) {
  return types.some(function (triggerType) {
    return triggers.getTrigger(className, triggers.Types[triggerType], config.applicationId);
  });
}

function checkLiveQuery(className, config) {
  return config.liveQueryController && config.liveQueryController.hasLiveQuery(className);
}
...
```

#### <a name="apidoc.element.parse-server.triggers.getValidator"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>getValidator (functionName, applicationId)](#apidoc.element.parse-server.triggers.getValidator)
- description and source-code
```javascript
function getValidator(functionName, applicationId) {
  var manager = _triggerStore[applicationId];
  if (manager && manager.Validators) {
    return manager.Validators[functionName];
  }
  return undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.inflate"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>inflate (data, restObject)](#apidoc.element.parse-server.triggers.inflate)
- description and source-code
```javascript
function inflate(data, restObject) {
  var copy = (typeof data === 'undefined' ? 'undefined' : _typeof(data)) == 'object' ? data : { className: data };
  for (var key in restObject) {
    copy[key] = restObject[key];
  }
  return _node2.default.Object.fromJSON(copy);
}
```
- example usage
```shell
...
// Cloud code gets a bit of extra data for its objects
var extraData = { className: this.className };
if (this.query && this.query.objectId) {
  extraData.objectId = this.query.objectId;
}

var originalObject = null;
var updatedObject = triggers.inflate(extraData, this.originalData);
if (this.query && this.query.objectId) {
  // This is an update for existing object.
  originalObject = triggers.inflate(extraData, this.originalData);
}
updatedObject.set(this.sanitizedData());

return Promise.resolve().then(function () {
...
```

#### <a name="apidoc.element.parse-server.triggers.maybeRunAfterFindTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>maybeRunAfterFindTrigger (triggerType, auth, className, objects, config)](#apidoc.element.parse-server.triggers.maybeRunAfterFindTrigger)
- description and source-code
```javascript
function maybeRunAfterFindTrigger(triggerType, auth, className, objects, config) {
  return new Promise(function (resolve, reject) {
    var trigger = getTrigger(className, triggerType, config.applicationId);
    if (!trigger) {
      return resolve();
    }
    var request = getRequestObject(triggerType, auth, null, null, config);
    var response = getResponseObject(request, function (object) {
      resolve(object);
    }, function (error) {
      reject(error);
    });
    logTriggerSuccessBeforeHook(triggerType, className, 'AfterFind', JSON.stringify(objects), auth);
    request.objects = objects.map(function (object) {
      //setting the class name to transform into parse object
      object.className = className;
      return _node2.default.Object.fromJSON(object);
    });
    var triggerPromise = trigger(request, response);
    if (triggerPromise && typeof triggerPromise.then === "function") {
      return triggerPromise.then(function (promiseResults) {
        if (promiseResults) {
          resolve(promiseResults);
        } else {
          return reject(new _node2.default.Error(_node2.default.Error.SCRIPT_FAILED, "AfterFind expect results to be returned in
 the promise"));
        }
      });
    }
  }).then(function (results) {
    logTriggerAfterHook(triggerType, className, JSON.stringify(results), auth);
    return results;
  });
}
```
- example usage
```shell
...
  }
  // Avoid doing any setup for triggers if there is no 'afterFind' trigger for this class.
  var hasAfterFindHook = triggers.triggerExists(this.className, triggers.Types.afterFind, this.config.applicationId);
  if (!hasAfterFindHook) {
    return Promise.resolve();
  }
  // Run afterFind trigger and set the new results
  return triggers.maybeRunAfterFindTrigger(triggers.Types.afterFind, this.auth, this.className, this.response.results, this.config
).then(function (results) {
    _this13.response.results = results;
  });
};

// Adds included values to the response.
// Path is a list of field names.
// Returns a promise for an augmented response.
...
```

#### <a name="apidoc.element.parse-server.triggers.maybeRunQueryTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>maybeRunQueryTrigger (triggerType, className, restWhere, restOptions, config, auth)](#apidoc.element.parse-server.triggers.maybeRunQueryTrigger)
- description and source-code
```javascript
function maybeRunQueryTrigger(triggerType, className, restWhere, restOptions, config, auth) {
  var trigger = getTrigger(className, triggerType, config.applicationId);
  if (!trigger) {
    return Promise.resolve({
      restWhere: restWhere,
      restOptions: restOptions
    });
  }

  var parseQuery = new _node2.default.Query(className);
  if (restWhere) {
    parseQuery._where = restWhere;
  }
  if (restOptions) {
    if (restOptions.include && restOptions.include.length > 0) {
      parseQuery._include = restOptions.include.split(',');
    }
    if (restOptions.skip) {
      parseQuery._skip = restOptions.skip;
    }
    if (restOptions.limit) {
      parseQuery._limit = restOptions.limit;
    }
  }
  var requestObject = getRequestQueryObject(triggerType, auth, parseQuery, config);
  return Promise.resolve().then(function () {
    return trigger(requestObject);
  }).then(function (result) {
    var queryResult = parseQuery;
    if (result && result instanceof _node2.default.Query) {
      queryResult = result;
    }
    var jsonQuery = queryResult.toJSON();
    if (jsonQuery.where) {
      restWhere = jsonQuery.where;
    }
    if (jsonQuery.limit) {
      restOptions = restOptions || {};
      restOptions.limit = jsonQuery.limit;
    }
    if (jsonQuery.skip) {
      restOptions = restOptions || {};
      restOptions.skip = jsonQuery.skip;
    }
    if (jsonQuery.include) {
      restOptions = restOptions || {};
      restOptions.include = jsonQuery.include;
    }
    if (jsonQuery.keys) {
      restOptions = restOptions || {};
      restOptions.keys = jsonQuery.keys;
    }
    return {
      restWhere: restWhere,
      restOptions: restOptions
    };
  }, function (err) {
    if (typeof err === 'string') {
      throw new _node2.default.Error(1, err);
    } else {
      throw err;
    }
  });
}
```
- example usage
```shell
...
function checkLiveQuery(className, config) {
  return config.liveQueryController && config.liveQueryController.hasLiveQuery(className);
}

// Returns a promise for an object with optional keys 'results' and 'count'.
function find(config, auth, className, restWhere, restOptions, clientSDK) {
  enforceRoleSecurity('find', className, auth);
  return triggers.maybeRunQueryTrigger(triggers.Types.beforeFind, className, restWhere, restOptions, config, auth).then(function
 (result) {
    restWhere = result.restWhere || restWhere;
    restOptions = result.restOptions || restOptions;
    var query = new RestQuery(config, auth, className, restWhere, restOptions, clientSDK);
    return query.execute();
  });
}
...
```

#### <a name="apidoc.element.parse-server.triggers.maybeRunTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>maybeRunTrigger (triggerType, auth, parseObject, originalParseObject, config)](#apidoc.element.parse-server.triggers.maybeRunTrigger)
- description and source-code
```javascript
function maybeRunTrigger(triggerType, auth, parseObject, originalParseObject, config) {
  if (!parseObject) {
    return Promise.resolve({});
  }
  return new Promise(function (resolve, reject) {
    var trigger = getTrigger(parseObject.className, triggerType, config.applicationId);
    if (!trigger) return resolve();
    var request = getRequestObject(triggerType, auth, parseObject, originalParseObject, config);
    var response = getResponseObject(request, function (object) {
      logTriggerSuccessBeforeHook(triggerType, parseObject.className, parseObject.toJSON(), object, auth);
      resolve(object);
    }, function (error) {
      logTriggerErrorBeforeHook(triggerType, parseObject.className, parseObject.toJSON(), auth, error);
      reject(error);
    });
    // Force the current Parse app before the trigger
    _node2.default.applicationId = config.applicationId;
    _node2.default.javascriptKey = config.javascriptKey || '';
    _node2.default.masterKey = config.masterKey;

    // AfterSave and afterDelete triggers can return a promise, which if they
    // do, needs to be resolved before this promise is resolved,
    // so trigger execution is synced with RestWrite.execute() call.
    // If triggers do not return a promise, they can run async code parallel
    // to the RestWrite.execute() call.
    var triggerPromise = trigger(request, response);
    if (triggerType === Types.afterSave || triggerType === Types.afterDelete) {
      logTriggerAfterHook(triggerType, parseObject.className, parseObject.toJSON(), auth);
      if (triggerPromise && typeof triggerPromise.then === "function") {
        return triggerPromise.then(resolve, resolve);
      } else {
        return resolve();
      }
    }
  });
}
```
- example usage
```shell
...
if (this.query && this.query.objectId) {
  // This is an update for existing object.
  originalObject = triggers.inflate(extraData, this.originalData);
}
updatedObject.set(this.sanitizedData());

return Promise.resolve().then(function () {
  return triggers.maybeRunTrigger(triggers.Types.beforeSave, _this4.auth, updatedObject, originalObject, _this4.config);
}).then(function (response) {
  if (response && response.object) {
    _this4.storage.fieldsChangedByTrigger = _lodash2.default.reduce(response.object, function (result, value, key) {
      if (!_lodash2.default.isEqual(_this4.data[key], value)) {
        result.push(key);
      }
      return result;
...
```

#### <a name="apidoc.element.parse-server.triggers.removeFunction"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>removeFunction (functionName, applicationId)](#apidoc.element.parse-server.triggers.removeFunction)
- description and source-code
```javascript
function removeFunction(functionName, applicationId) {
  applicationId = applicationId || _node2.default.applicationId;
  delete _triggerStore[applicationId].Functions[functionName];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.removeJob"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>removeJob (jobName, applicationId)](#apidoc.element.parse-server.triggers.removeJob)
- description and source-code
```javascript
function removeJob(jobName, applicationId) {
  applicationId = applicationId || _node2.default.applicationId;
  delete _triggerStore[applicationId].Jobs[jobName];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.removeTrigger"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>removeTrigger (type, className, applicationId)](#apidoc.element.parse-server.triggers.removeTrigger)
- description and source-code
```javascript
function removeTrigger(type, className, applicationId) {
  applicationId = applicationId || _node2.default.applicationId;
  delete _triggerStore[applicationId].Triggers[type][className];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parse-server.triggers.triggerExists"></a>[function <span class="apidocSignatureSpan">parse-server.triggers.</span>triggerExists (className, type, applicationId)](#apidoc.element.parse-server.triggers.triggerExists)
- description and source-code
```javascript
function triggerExists(className, type, applicationId) {
  return getTrigger(className, type, applicationId) != undefined;
}
```
- example usage
```shell
...
RestQuery.prototype.runAfterFindTrigger = function () {
var _this13 = this;

if (!this.response) {
  return;
}
// Avoid doing any setup for triggers if there is no 'afterFind' trigger for this class.
var hasAfterFindHook = triggers.triggerExists(this.className, triggers.Types.afterFind, this.config.applicationId);
if (!hasAfterFindHook) {
  return Promise.resolve();
}
// Run afterFind trigger and set the new results
return triggers.maybeRunAfterFindTrigger(triggers.Types.afterFind, this.auth, this.className, this.response.results, this.config
).then(function (results) {
  _this13.response.results = results;
});
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
