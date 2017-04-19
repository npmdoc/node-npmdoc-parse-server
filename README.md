# npmdoc-parse-server

#### api documentation for  [parse-server (v2.3.8)](https://github.com/ParsePlatform/parse-server#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-parse-server.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-parse-server) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-parse-server.svg)](https://travis-ci.org/npmdoc/node-npmdoc-parse-server)

#### An express module providing a Parse-compatible API server

[![NPM](https://nodei.co/npm/parse-server.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/parse-server)

- [https://npmdoc.github.io/node-npmdoc-parse-server/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-parse-server/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-parse-server/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-parse-server/build/apidoc.html)

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
        "mongodb": "2.2.25",
        "multer": "1.3.0",
        "parse": "1.9.2",
        "parse-server-fs-adapter": "1.0.1",
        "parse-server-push-adapter": "1.3.0",
        "parse-server-s3-adapter": "1.0.6",
        "parse-server-simple-mailgun-adapter": "1.0.0",
        "pg-promise": "5.6.4",
        "redis": "2.7.1",
        "request": "2.81.0",
        "semver": "5.2.0",
        "tv4": "1.3.0",
        "uws": "^0.14.0",
        "winston": "2.3.1",
        "winston-daily-rotate-file": "1.4.6",
        "ws": "2.2.3"
    },
    "description": "An express module providing a Parse-compatible API server",
    "devDependencies": {
        "babel-cli": "6.24.0",
        "babel-core": "6.24.0",
        "babel-eslint": "^7.1.1",
        "babel-plugin-syntax-flow": "6.18.0",
        "babel-plugin-transform-flow-strip-types": "6.22.0",
        "babel-preset-es2015": "6.24.0",
        "babel-preset-stage-0": "6.22.0",
        "babel-register": "6.24.0",
        "bcrypt-nodejs": "0.0.3",
        "cross-env": "4.0.0",
        "deep-diff": "0.3.4",
        "eslint": "^3.16.1",
        "eslint-plugin-flowtype": "^2.25.0",
        "gaze": "1.1.1",
        "jasmine": "2.5.3",
        "jasmine-spec-reporter": "^3.1.0",
        "mongodb-runner": "3.4.0",
        "nodemon": "1.11.0",
        "nyc": "^10.1.2",
        "request-promise": "4.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "85696071e485bca3107518007409eaa70a0a964c",
        "tarball": "https://registry.npmjs.org/parse-server/-/parse-server-2.3.8.tgz"
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
    "gitHead": "302a0dda7355babff5979b30104859a4e6a246f5",
    "homepage": "https://github.com/ParsePlatform/parse-server#readme",
    "license": "BSD-3-Clause",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "drewgross"
        },
        {
            "name": "flovilmart"
        },
        {
            "name": "fosco"
        }
    ],
    "name": "parse-server",
    "optionalDependencies": {
        "bcrypt": "1.0.2",
        "uws": "^0.14.0"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/ParsePlatform/parse-server.git"
    },
    "scripts": {
        "build": "babel src/ -d lib/ --copy-files",
        "coverage": "cross-env COVERAGE_OPTION='./node_modules/.bin/nyc' npm test",
        "coverage:win": "cross-env MONGODB_VERSION=${MONGODB_VERSION:=3.2.6} MONGODB_STORAGE_ENGINE=mmapv1 NODE_ENV=test TESTING=1 node ./node_modules/.bin/nyc ./node_modules/jasmine/bin/jasmine.js",
        "dev": "npm run build && node bin/dev",
        "lint": "eslint --cache ./",
        "prepublish": "npm run build",
        "pretest": "npm run lint",
        "start": "node ./bin/parse-server",
        "test": "cross-env MONGODB_VERSION=${MONGODB_VERSION:=3.2.6} MONGODB_STORAGE_ENGINE=mmapv1 NODE_ENV=test TESTING=1 $COVERAGE_OPTION jasmine",
        "test:win": "cross-env MONGODB_VERSION=${MONGODB_VERSION:=3.2.6} MONGODB_STORAGE_ENGINE=mmapv1 NODE_ENV=test TESTING=1 jasmine"
    },
    "version": "2.3.8"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
