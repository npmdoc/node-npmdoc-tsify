# api documentation for  [tsify (v3.0.1)](https://github.com/TypeStrong/tsify)  [![npm package](https://img.shields.io/npm/v/npmdoc-tsify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-tsify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-tsify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-tsify)
#### Browserify plugin for compiling Typescript

[![NPM](https://nodei.co/npm/tsify.png?downloads=true)](https://www.npmjs.com/package/tsify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-tsify/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-tsify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-tsify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-tsify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-tsify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Greg Smith"
    },
    "bugs": {
        "url": "https://github.com/TypeStrong/tsify/issues"
    },
    "dependencies": {
        "convert-source-map": "^1.1.0",
        "fs.realpath": "^1.0.0",
        "object-assign": "^4.1.0",
        "semver": "^5.1.0",
        "through2": "^2.0.0",
        "tsconfig": "^5.0.3"
    },
    "description": "Browserify plugin for compiling Typescript",
    "devDependencies": {
        "babel-preset-react": "^6.5.0",
        "babelify": "^7.2.0",
        "browserify": "^13.0.0",
        "eslint": "^3.3.1",
        "event-stream": "^3.3.1",
        "fs-extra": "^0.30.0",
        "node-foo": "^0.2.3",
        "source-map": "^0.5.3",
        "string-to-stream": "^1.1.0",
        "tape": "^4.0.0",
        "test-peer-range": "^1.0.1",
        "typescript": "~2.0.3",
        "watchify": "^3.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "23509ff3b4e7110ca9656f6c27ca13ec856056f6",
        "tarball": "https://registry.npmjs.org/tsify/-/tsify-3.0.1.tgz"
    },
    "engines": {
        "node": ">=0.12"
    },
    "gitHead": "74d77849f669f1db5012a423d9e5bf6407ea6a6d",
    "homepage": "https://github.com/TypeStrong/tsify",
    "keywords": [
        "browserify",
        "browserify-plugin",
        "typescript"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "basarat",
            "email": "basaratali@gmail.com"
        },
        {
            "name": "cartant",
            "email": "nicholas@cartant.com"
        },
        {
            "name": "smrq",
            "email": "smr.kyu@gmail.com"
        }
    ],
    "name": "tsify",
    "optionalDependencies": {},
    "peerDependencies": {
        "browserify": ">= 10.x",
        "typescript": ">= 2.x"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/TypeStrong/tsify.git"
    },
    "scripts": {
        "lint": "eslint .",
        "test": "test-peer-range browserify",
        "test-main": "node test/test.js"
    },
    "version": "3.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module tsify](#apidoc.module.tsify)
1.  object <span class="apidocSignatureSpan">tsify.</span>time

#### [module tsify.time](#apidoc.module.tsify.time)
1.  [function <span class="apidocSignatureSpan">tsify.time.</span>start ()](#apidoc.element.tsify.time.start)
1.  [function <span class="apidocSignatureSpan">tsify.time.</span>stop (t0, message)](#apidoc.element.tsify.time.stop)



# <a name="apidoc.module.tsify"></a>[module tsify](#apidoc.module.tsify)



# <a name="apidoc.module.tsify.time"></a>[module tsify.time](#apidoc.module.tsify.time)

#### <a name="apidoc.element.tsify.time.start"></a>[function <span class="apidocSignatureSpan">tsify.time.</span>start ()](#apidoc.element.tsify.time.start)
- description and source-code
```javascript
function start() {
	return process.hrtime();
}
```
- example usage
```shell
...
			self.host._addFile(file, true);
		});
	};

	Tsifier.prototype.compile = function () {
		var self = this;

		var createProgram_t0 = time.start();
		var program = self.host._compile(self.opts);
		time.stop(createProgram_t0, 'createProgram');

		var syntaxDiagnostics = self.checkSyntax(program);
		if (syntaxDiagnostics.length) {
			log('Compilation encountered fatal syntax errors');
			return;
...
```

#### <a name="apidoc.element.tsify.time.stop"></a>[function <span class="apidocSignatureSpan">tsify.time.</span>stop (t0, message)](#apidoc.element.tsify.time.stop)
- description and source-code
```javascript
function stop(t0, message) {
	var tDiff = process.hrtime(t0);
	log('%d sec -- %s', (tDiff[0] + (tDiff[1] / 1000000000)).toFixed(4), message);
}
```
- example usage
```shell
...
	};

	Tsifier.prototype.compile = function () {
		var self = this;

		var createProgram_t0 = time.start();
		var program = self.host._compile(self.opts);
		time.stop(createProgram_t0, 'createProgram');

		var syntaxDiagnostics = self.checkSyntax(program);
		if (syntaxDiagnostics.length) {
			log('Compilation encountered fatal syntax errors');
			return;
		}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
