# api documentation for  [jscs (v3.0.7)](http://jscs.info)  [![npm package](https://img.shields.io/npm/v/npmdoc-jscs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-jscs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-jscs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-jscs)
#### JavaScript Code Style

[![NPM](https://nodei.co/npm/jscs.png?downloads=true)](https://www.npmjs.com/package/jscs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-jscs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-jscs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-jscs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-jscs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-jscs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marat Dulin",
        "email": "mdevils@yandex.ru",
        "url": "https://github.com/jscs-dev/node-jscs/graphs/contributors"
    },
    "bin": {
        "jscs": "./bin/jscs"
    },
    "bugs": {
        "url": "https://github.com/jscs-dev/node-jscs/issues"
    },
    "dependencies": {
        "chalk": "~1.1.0",
        "cli-table": "~0.3.1",
        "commander": "~2.9.0",
        "cst": "^0.4.3",
        "estraverse": "^4.1.0",
        "exit": "~0.1.2",
        "glob": "^5.0.1",
        "htmlparser2": "3.8.3",
        "js-yaml": "~3.4.0",
        "jscs-jsdoc": "^2.0.0",
        "jscs-preset-wikimedia": "~1.0.0",
        "jsonlint": "~1.6.2",
        "lodash": "~3.10.0",
        "minimatch": "~3.0.0",
        "natural-compare": "~1.2.2",
        "pathval": "~0.1.1",
        "prompt": "~0.2.14",
        "reserved-words": "^0.1.1",
        "resolve": "^1.1.6",
        "strip-bom": "^2.0.0",
        "strip-json-comments": "~1.0.2",
        "to-double-quotes": "^2.0.0",
        "to-single-quotes": "^2.0.0",
        "vow": "~0.4.8",
        "vow-fs": "~0.3.4",
        "xmlbuilder": "^3.1.0"
    },
    "description": "JavaScript Code Style",
    "devDependencies": {
        "chai": "^3.3.0",
        "coveralls": "~2.11.2",
        "has-ansi": "~2.0.0",
        "jshint": "~2.8.0",
        "mocha": "^2.2.0",
        "regenerate": "~1.2.1",
        "rewire": "^2.3.1",
        "sinon": "^1.13.0",
        "sinon-chai": "^2.8.0",
        "unicode-7.0.0": "~0.1.5",
        "unit-coverage": "^4.0.1",
        "xml2js": "~0.4.4"
    },
    "directories": {},
    "dist": {
        "shasum": "7141b4dff5b86e32d0e99d764b836767c30d201a",
        "tarball": "https://registry.npmjs.org/jscs/-/jscs-3.0.7.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "files": [
        "bin",
        "lib",
        "patterns",
        "presets",
        "LICENSE"
    ],
    "gitHead": "e177990d913aafd3e96870a9202194cbbda05167",
    "homepage": "http://jscs.info",
    "keywords": [
        "code style",
        "formatter",
        "lint",
        "linter",
        "style guide",
        "validate"
    ],
    "license": "MIT",
    "main": "lib/checker",
    "maintainers": [
        {
            "name": "hzoo",
            "email": "hi@henryzoo.com"
        },
        {
            "name": "markelog",
            "email": "markelog@gmail.com"
        },
        {
            "name": "mdevils",
            "email": "mdevils@yandex.ru"
        },
        {
            "name": "mikesherov",
            "email": "mike.sherov@gmail.com"
        },
        {
            "name": "mrjoelkemp",
            "email": "joel@mrjoelkemp.com"
        },
        {
            "name": "qfox",
            "email": "zxqfox@gmail.com"
        }
    ],
    "name": "jscs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jscs-dev/node-jscs.git"
    },
    "scripts": {
        "changelog": "git log 'git describe --tags --abbrev=0'..HEAD --pretty=format:' * %s (%an)' | grep -v 'Merge pull request'",
        "coverage": "unit-coverage run -p common",
        "coverage-html": "unit-coverage run -p common -r html -o coverage.html",
        "coveralls": "unit-coverage run -p common -r lcov -o out.lcov && cat out.lcov | coveralls",
        "integration": "#node test/scripts/integration.js",
        "jscs": "node bin/jscs lib test bin publish",
        "jshint": "jshint .",
        "lint": "npm run jshint && npm run jscs",
        "pretest": "npm run lint",
        "release": "node publish/prepublish && npm test && npm publish",
        "test": "mocha --color",
        "watch": "mocha --color --watch"
    },
    "unit-coverage": {
        "common": [
            "-a",
            "lib",
            "-a",
            "test",
            "-s",
            "lib/**/*.js",
            "-t",
            "test/specs/**/*.js",
            "-e",
            "lib/cli-config.js",
            "-S",
            "relative",
            "-O",
            "sources=lib",
            "-O",
            "tests=test/specs"
        ]
    },
    "version": "3.0.7"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module jscs](#apidoc.module.jscs)
1.  [function <span class="apidocSignatureSpan">jscs.</span>errors (file)](#apidoc.element.jscs.errors)
1.  [function <span class="apidocSignatureSpan">jscs.</span>js_file (params)](#apidoc.element.jscs.js_file)
1.  [function <span class="apidocSignatureSpan">jscs.</span>super_ ()](#apidoc.element.jscs.super_)
1.  [function <span class="apidocSignatureSpan">jscs.</span>token_assert (file)](#apidoc.element.jscs.token_assert)
1.  object <span class="apidocSignatureSpan">jscs.</span>errors.prototype
1.  object <span class="apidocSignatureSpan">jscs.</span>js_file.prototype
1.  object <span class="apidocSignatureSpan">jscs.</span>super_.prototype
1.  object <span class="apidocSignatureSpan">jscs.</span>token_assert.prototype
1.  object <span class="apidocSignatureSpan">jscs.</span>token_categorizer
1.  object <span class="apidocSignatureSpan">jscs.</span>tree_iterator
1.  object <span class="apidocSignatureSpan">jscs.</span>utils

#### [module jscs.errors](#apidoc.module.jscs.errors)
1.  [function <span class="apidocSignatureSpan">jscs.</span>errors (file)](#apidoc.element.jscs.errors.errors)
1.  [function <span class="apidocSignatureSpan">jscs.errors.</span>getPosition (error, tokenIndex)](#apidoc.element.jscs.errors.getPosition)

#### [module jscs.errors.prototype](#apidoc.module.jscs.errors.prototype)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>_addError (errorInfo)](#apidoc.element.jscs.errors.prototype._addError)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>_addParseError (errorInfo)](#apidoc.element.jscs.errors.prototype._addParseError)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>_prepareMessage (errorInfo)](#apidoc.element.jscs.errors.prototype._prepareMessage)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>add (message, element, offset)](#apidoc.element.jscs.errors.prototype.add)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>calculateErrorLocations (tokenIndex)](#apidoc.element.jscs.errors.prototype.calculateErrorLocations)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>cast (errorInfo)](#apidoc.element.jscs.errors.prototype.cast)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>explainError (error, colorize)](#apidoc.element.jscs.errors.prototype.explainError)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>filter (filter)](#apidoc.element.jscs.errors.prototype.filter)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getErrorCount ()](#apidoc.element.jscs.errors.prototype.getErrorCount)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getErrorList ()](#apidoc.element.jscs.errors.prototype.getErrorList)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getFilename ()](#apidoc.element.jscs.errors.prototype.getFilename)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getValidationErrorCount ()](#apidoc.element.jscs.errors.prototype.getValidationErrorCount)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>isEmpty ()](#apidoc.element.jscs.errors.prototype.isEmpty)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>setCurrentRule (rule)](#apidoc.element.jscs.errors.prototype.setCurrentRule)
1.  [function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>stripErrorList (length)](#apidoc.element.jscs.errors.prototype.stripErrorList)

#### [module jscs.js_file](#apidoc.module.jscs.js_file)
1.  [function <span class="apidocSignatureSpan">jscs.</span>js_file (params)](#apidoc.element.jscs.js_file.js_file)

#### [module jscs.js_file.prototype](#apidoc.module.jscs.js_file.prototype)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>_setTokenBefore (token, fragment)](#apidoc.element.jscs.js_file.prototype._setTokenBefore)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findNextOperatorToken (token, value)](#apidoc.element.jscs.js_file.prototype.findNextOperatorToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findNextToken (token, type, value)](#apidoc.element.jscs.js_file.prototype.findNextToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findPrevOperatorToken (token, value)](#apidoc.element.jscs.js_file.prototype.findPrevOperatorToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findPrevToken (token, type, value)](#apidoc.element.jscs.js_file.prototype.findPrevToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getComments ()](#apidoc.element.jscs.js_file.prototype.getComments)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getDialect ()](#apidoc.element.jscs.js_file.prototype.getDialect)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getDistanceBetween (tokenBefore, tokenAfter)](#apidoc.element.jscs.js_file.prototype.getDistanceBetween)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFilename ()](#apidoc.element.jscs.js_file.prototype.getFilename)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFirstNodeToken (node)](#apidoc.element.jscs.js_file.prototype.getFirstNodeToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFirstToken ()](#apidoc.element.jscs.js_file.prototype.getFirstToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFirstTokenOnLineWith (element, options)](#apidoc.element.jscs.js_file.prototype.getFirstTokenOnLineWith)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLastNodeToken (node)](#apidoc.element.jscs.js_file.prototype.getLastNodeToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLastToken ()](#apidoc.element.jscs.js_file.prototype.getLastToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLastTokenOnLine (lineNumber, options)](#apidoc.element.jscs.js_file.prototype.getLastTokenOnLine)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLineBreakStyle ()](#apidoc.element.jscs.js_file.prototype.getLineBreakStyle)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLineBreaks ()](#apidoc.element.jscs.js_file.prototype.getLineBreaks)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLineCountBetween (tokenBefore, tokenAfter)](#apidoc.element.jscs.js_file.prototype.getLineCountBetween)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLines ()](#apidoc.element.jscs.js_file.prototype.getLines)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLinesWithCommentsRemoved ()](#apidoc.element.jscs.js_file.prototype.getLinesWithCommentsRemoved)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getNextToken (token, options)](#apidoc.element.jscs.js_file.prototype.getNextToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getNodesByType (type)](#apidoc.element.jscs.js_file.prototype.getNodesByType)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getParseErrors ()](#apidoc.element.jscs.js_file.prototype.getParseErrors)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getPrevToken (token, options)](#apidoc.element.jscs.js_file.prototype.getPrevToken)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getProgram ()](#apidoc.element.jscs.js_file.prototype.getProgram)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getScopes ()](#apidoc.element.jscs.js_file.prototype.getScopes)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getSource ()](#apidoc.element.jscs.js_file.prototype.getSource)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getTree ()](#apidoc.element.jscs.js_file.prototype.getTree)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getWhitespaceBefore (token)](#apidoc.element.jscs.js_file.prototype.getWhitespaceBefore)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>isOnTheSameLine (tokenBefore, tokenAfter)](#apidoc.element.jscs.js_file.prototype.isOnTheSameLine)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterate (cb, tree)](#apidoc.element.jscs.js_file.prototype.iterate)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterateNodesByType (type, cb, context)](#apidoc.element.jscs.js_file.prototype.iterateNodesByType)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterateTokensByType (type, cb)](#apidoc.element.jscs.js_file.prototype.iterateTokensByType)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterateTokensByTypeAndValue (type, value, cb)](#apidoc.element.jscs.js_file.prototype.iterateTokensByTypeAndValue)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>render ()](#apidoc.element.jscs.js_file.prototype.render)
1.  [function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>setWhitespaceBefore (token, whitespace)](#apidoc.element.jscs.js_file.prototype.setWhitespaceBefore)

#### [module jscs.super_](#apidoc.module.jscs.super_)
1.  [function <span class="apidocSignatureSpan">jscs.</span>super_ ()](#apidoc.element.jscs.super_.super_)

#### [module jscs.super_.prototype](#apidoc.module.jscs.super_.prototype)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_addParseError (errors, parseError, file)](#apidoc.element.jscs.super_.prototype._addParseError)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_checkJsFile (file, errors)](#apidoc.element.jscs.super_.prototype._checkJsFile)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_createConfiguration ()](#apidoc.element.jscs.super_.prototype._createConfiguration)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_createJsFileInstance (filename, source)](#apidoc.element.jscs.super_.prototype._createJsFileInstance)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_fixCommonError (error)](#apidoc.element.jscs.super_.prototype._fixCommonError)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_fixJsFile (file, errors)](#apidoc.element.jscs.super_.prototype._fixJsFile)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_fixSpecificError (file, error)](#apidoc.element.jscs.super_.prototype._fixSpecificError)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>checkString (source, filename)](#apidoc.element.jscs.super_.prototype.checkString)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>configure (config)](#apidoc.element.jscs.super_.prototype.configure)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>fixString (source, filename)](#apidoc.element.jscs.super_.prototype.fixString)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>getConfiguration ()](#apidoc.element.jscs.super_.prototype.getConfiguration)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>getProcessedConfig ()](#apidoc.element.jscs.super_.prototype.getProcessedConfig)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>maxErrorsEnabled ()](#apidoc.element.jscs.super_.prototype.maxErrorsEnabled)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>maxErrorsExceeded ()](#apidoc.element.jscs.super_.prototype.maxErrorsExceeded)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>registerDefaultRules ()](#apidoc.element.jscs.super_.prototype.registerDefaultRules)
1.  [function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>registerRule (rule)](#apidoc.element.jscs.super_.prototype.registerRule)

#### [module jscs.token_assert](#apidoc.module.jscs.token_assert)
1.  [function <span class="apidocSignatureSpan">jscs.</span>token_assert (file)](#apidoc.element.jscs.token_assert.token_assert)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.</span>super_ ()](#apidoc.element.jscs.token_assert.super_)

#### [module jscs.token_assert.prototype](#apidoc.module.jscs.token_assert.prototype)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_augmentLineCount (options, lineCount)](#apidoc.element.jscs.token_assert.prototype._augmentLineCount)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_updateCommentWhitespace (token, indentChar, actual, expected)](#apidoc.element.jscs.token_assert.prototype._updateCommentWhitespace)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_updateWhitespaceByLine (token, callback)](#apidoc.element.jscs.token_assert.prototype._updateWhitespaceByLine)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_validateOptions (options)](#apidoc.element.jscs.token_assert.prototype._validateOptions)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>differentLine (options)](#apidoc.element.jscs.token_assert.prototype.differentLine)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>indentation (options)](#apidoc.element.jscs.token_assert.prototype.indentation)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>linesBetween (options)](#apidoc.element.jscs.token_assert.prototype.linesBetween)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>noWhitespaceBetween (options)](#apidoc.element.jscs.token_assert.prototype.noWhitespaceBetween)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>sameLine (options)](#apidoc.element.jscs.token_assert.prototype.sameLine)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>spacesBetween (options)](#apidoc.element.jscs.token_assert.prototype.spacesBetween)
1.  [function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>whitespaceBetween (options)](#apidoc.element.jscs.token_assert.prototype.whitespaceBetween)

#### [module jscs.token_categorizer](#apidoc.module.jscs.token_categorizer)
1.  [function <span class="apidocSignatureSpan">jscs.token_categorizer.</span>categorizeCloseParen (token)](#apidoc.element.jscs.token_categorizer.categorizeCloseParen)
1.  [function <span class="apidocSignatureSpan">jscs.token_categorizer.</span>categorizeOpenParen (token)](#apidoc.element.jscs.token_categorizer.categorizeOpenParen)

#### [module jscs.tree_iterator](#apidoc.module.jscs.tree_iterator)
1.  [function <span class="apidocSignatureSpan">jscs.tree_iterator.</span>iterate (node, cb)](#apidoc.element.jscs.tree_iterator.iterate)

#### [module jscs.utils](#apidoc.module.jscs.utils)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>getFunctionNodeFromIIFE (node)](#apidoc.element.jscs.utils.getFunctionNodeFromIIFE)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>isPragma (additionalExceptions)](#apidoc.element.jscs.utils.isPragma)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>isRelativePath (path)](#apidoc.element.jscs.utils.isRelativePath)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>isSnakeCased (name)](#apidoc.element.jscs.utils.isSnakeCased)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>isValidIdentifierName (name, dialect)](#apidoc.element.jscs.utils.isValidIdentifierName)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>normalizePath (filepath, basePath)](#apidoc.element.jscs.utils.normalizePath)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>promisify (fn)](#apidoc.element.jscs.utils.promisify)
1.  [function <span class="apidocSignatureSpan">jscs.utils.</span>trimUnderscores (name)](#apidoc.element.jscs.utils.trimUnderscores)
1.  object <span class="apidocSignatureSpan">jscs.utils.</span>binaryOperators
1.  object <span class="apidocSignatureSpan">jscs.utils.</span>curlyBracedKeywords
1.  object <span class="apidocSignatureSpan">jscs.utils.</span>incrementAndDecrementOperators
1.  object <span class="apidocSignatureSpan">jscs.utils.</span>operators
1.  object <span class="apidocSignatureSpan">jscs.utils.</span>spacedKeywords
1.  object <span class="apidocSignatureSpan">jscs.utils.</span>unaryOperators



# <a name="apidoc.module.jscs"></a>[module jscs](#apidoc.module.jscs)

#### <a name="apidoc.element.jscs.errors"></a>[function <span class="apidocSignatureSpan">jscs.</span>errors (file)](#apidoc.element.jscs.errors)
- description and source-code
```javascript
errors = function (file) {
    this._errorList = [];
    this._file = file;
    this._currentRule = '';

<span class="apidocCodeCommentSpan">    /**
     * @type {TokenAssert}
     * @public
     */
</span>    this.assert = new TokenAssert(file);
    this.assert.on('error', this._addError.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file"></a>[function <span class="apidocSignatureSpan">jscs.</span>js_file (params)](#apidoc.element.jscs.js_file)
- description and source-code
```javascript
js_file = function (params) {
    params = params || {};
    this._parseErrors = [];
    this._filename = params.filename;
    this._source = params.source;

    this._es3 = params.es3 || false;

    this._lineBreaks = null;
    this._lines = this._source.split(/\r\n|\r|\n/);

    var parser = new Parser({
        strictMode: false,
        languageExtensions: {
            gritDirectives: true,
            appleInstrumentationDirectives: true
        }
    });

    try {
        this._program = parser.parse(this._source);
    } catch (e) {
        this._parseErrors.push(e);
        this._program = new Program([
            new Token('EOF', '')
        ]);
    }

    // Lazy initialization
    this._scopes = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_"></a>[function <span class="apidocSignatureSpan">jscs.</span>super_ ()](#apidoc.element.jscs.super_)
- description and source-code
```javascript
super_ = function () {
    this._configuredRules = [];

    this._errorsFound = 0;
    this._maxErrorsExceeded = false;

    this._configuration = this._createConfiguration();
    this._configuration.registerDefaultPresets();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_assert"></a>[function <span class="apidocSignatureSpan">jscs.</span>token_assert (file)](#apidoc.element.jscs.token_assert)
- description and source-code
```javascript
function TokenAssert(file) {
    EventEmitter.call(this);

    this._file = file;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.errors"></a>[module jscs.errors](#apidoc.module.jscs.errors)

#### <a name="apidoc.element.jscs.errors.errors"></a>[function <span class="apidocSignatureSpan">jscs.</span>errors (file)](#apidoc.element.jscs.errors.errors)
- description and source-code
```javascript
errors = function (file) {
    this._errorList = [];
    this._file = file;
    this._currentRule = '';

<span class="apidocCodeCommentSpan">    /**
     * @type {TokenAssert}
     * @public
     */
</span>    this.assert = new TokenAssert(file);
    this.assert.on('error', this._addError.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.getPosition"></a>[function <span class="apidocSignatureSpan">jscs.errors.</span>getPosition (error, tokenIndex)](#apidoc.element.jscs.errors.getPosition)
- description and source-code
```javascript
getPosition = function (error, tokenIndex) {
    var element = error.element;
    var offset = error.offset;
    var rule = error.rule;

    if (!element) {
        return EMPTY_POS;
    }

    if (offset === undefined) {
        // TODO: probably should be generalized
        if (rule === 'validateQuoteMarks') {
            offset = 0;
        } else if (element.getSourceCodeLength() === 1) {
            offset = 0;
        } else {
            offset = (element.getNewlineCount() === 0 && Math.ceil(element.getSourceCodeLength() / 2)) || 0;
        }
    }

    var pos = tokenIndex ? tokenIndex.getElementLoc(element) : element.getLoc().start;
    if (!pos) {
        return EMPTY_POS;
    }

    if (offset === 0) {
        return pos;
    }

    var newlineCount = element.getNewlineCount();
    if (newlineCount > 0) {
        var code = element.getSourceCode();
        LINE_SEPARATOR.lastIndex = 0;
        var lineOffset = 0;
        var match;
        var previousOffset = 0;
        var firstLineColumnOffset = pos.column;
        while ((match = LINE_SEPARATOR.exec(code)) !== null) {
            var currentOffset = match.index;
            if (offset <= currentOffset) {
                return {
                    line: pos.line + lineOffset,
                    column: firstLineColumnOffset + offset - previousOffset
                };
            }
            previousOffset = currentOffset + match[0].length;
            firstLineColumnOffset = 0;
            lineOffset++;
        }
        return {
            line: pos.line + newlineCount,
            column: offset - previousOffset
        };
    } else {
        return {
            line: pos.line,
            column: pos.column + offset
        };
    }
}
```
- example usage
```shell
...
},

/**
 * @param {TokenIndex} tokenIndex
 */
calculateErrorLocations: function(tokenIndex) {
    this._errorList.forEach(function(error) {
        var pos = Errors.getPosition(error, tokenIndex);
        error.line = pos.line;
        error.column = pos.column;
    });
},

/**
 * Formats error for further output.
...
```



# <a name="apidoc.module.jscs.errors.prototype"></a>[module jscs.errors.prototype](#apidoc.module.jscs.errors.prototype)

#### <a name="apidoc.element.jscs.errors.prototype._addError"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>_addError (errorInfo)](#apidoc.element.jscs.errors.prototype._addError)
- description and source-code
```javascript
_addError = function (errorInfo) {
    this._errorList.push({
        filename: this._file.getFilename(),
        rule: this._currentRule,
        message: this._prepareMessage(errorInfo),
        element: errorInfo.element,
        offset: errorInfo.offset,
        additional: errorInfo.additional,
        fixed: false,
        fix: errorInfo.fix
    });
}
```
- example usage
```shell
...
 */
add: function(message, element, offset) {
    if (message instanceof Error) {
        this._addParseError(message);
        return;
    }

    this._addError({
        message: message,
        element: element,
        offset: offset
    });
},

/**
...
```

#### <a name="apidoc.element.jscs.errors.prototype._addParseError"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>_addParseError (errorInfo)](#apidoc.element.jscs.errors.prototype._addParseError)
- description and source-code
```javascript
_addParseError = function (errorInfo) {
    this._errorList.push({
        filename: this._file.getFilename(),
        rule: 'parseError',
        message: errorInfo.message,
        line: errorInfo.loc ? errorInfo.loc.line : 1,
        column: errorInfo.loc ? errorInfo.loc.column : 0
    });
}
```
- example usage
```shell
...
     *
     * @param {String | Error} message
     * @param {cst.types.Element} element
     * @param {Number} [offset] relative offset
     */
    add: function(message, element, offset) {
if (message instanceof Error) {
    this._addParseError(message);
    return;
}

this._addError({
    message: message,
    element: element,
    offset: offset
...
```

#### <a name="apidoc.element.jscs.errors.prototype._prepareMessage"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>_prepareMessage (errorInfo)](#apidoc.element.jscs.errors.prototype._prepareMessage)
- description and source-code
```javascript
_prepareMessage = function (errorInfo) {
    var rule = errorInfo instanceof Error ? 'parseError' : this._currentRule;

    if (rule) {
        return rule + ': ' + errorInfo.message;
    }

    return errorInfo.message;
}
```
- example usage
```shell
...
 * @param {Object} errorInfo
 * @private
 */
_addError: function(errorInfo) {
    this._errorList.push({
        filename: this._file.getFilename(),
        rule: this._currentRule,
        message: this._prepareMessage(errorInfo),
        element: errorInfo.element,
        offset: errorInfo.offset,
        additional: errorInfo.additional,
        fixed: false,
        fix: errorInfo.fix
    });
},
...
```

#### <a name="apidoc.element.jscs.errors.prototype.add"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>add (message, element, offset)](#apidoc.element.jscs.errors.prototype.add)
- description and source-code
```javascript
add = function (message, element, offset) {
    if (message instanceof Error) {
        this._addParseError(message);
        return;
    }

    this._addError({
        message: message,
        element: element,
        offset: offset
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.calculateErrorLocations"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>calculateErrorLocations (tokenIndex)](#apidoc.element.jscs.errors.prototype.calculateErrorLocations)
- description and source-code
```javascript
calculateErrorLocations = function (tokenIndex) {
    this._errorList.forEach(function(error) {
        var pos = Errors.getPosition(error, tokenIndex);
        error.line = pos.line;
        error.column = pos.column;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.cast"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>cast (errorInfo)](#apidoc.element.jscs.errors.prototype.cast)
- description and source-code
```javascript
cast = function (errorInfo) {
    this._addError(errorInfo);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.explainError"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>explainError (error, colorize)](#apidoc.element.jscs.errors.prototype.explainError)
- description and source-code
```javascript
explainError = function (error, colorize) {
    var lineNumber = error.line - 1;
    var lines = this._file.getLines();
    var result = [
        renderLine(lineNumber, lines[lineNumber], colorize),
        renderPointer(error.column, colorize)
    ];
    var i = lineNumber - 1;
    var linesAround = 2;
    while (i >= 0 && i >= (lineNumber - linesAround)) {
        result.unshift(renderLine(i, lines[i], colorize));
        i--;
    }
    i = lineNumber + 1;
    while (i < lines.length && i <= (lineNumber + linesAround)) {
        result.push(renderLine(i, lines[i], colorize));
        i++;
    }
    result.unshift(formatErrorMessage(error.message, this.getFilename(), colorize));
    return result.join('\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.filter"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>filter (filter)](#apidoc.element.jscs.errors.prototype.filter)
- description and source-code
```javascript
filter = function (filter) {
    this._errorList = this._errorList.filter(filter);
}
```
- example usage
```shell
...

/**
 * Returns amount of errors added by the rules.
 *
 * @returns {Number}
 */
getValidationErrorCount: function() {
    return this._errorList.filter(function(error) {
        return error.rule !== 'parseError' && error.rule !== 'internalError';
    });
},

/**
 * Returns amount of errors added by the rules.
 *
...
```

#### <a name="apidoc.element.jscs.errors.prototype.getErrorCount"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getErrorCount ()](#apidoc.element.jscs.errors.prototype.getErrorCount)
- description and source-code
```javascript
getErrorCount = function () {
    return this._errorList.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.getErrorList"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getErrorList ()](#apidoc.element.jscs.errors.prototype.getErrorList)
- description and source-code
```javascript
getErrorList = function () {
    return this._errorList;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.getFilename"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getFilename ()](#apidoc.element.jscs.errors.prototype.getFilename)
- description and source-code
```javascript
getFilename = function () {
    return this._file.getFilename();
}
```
- example usage
```shell
...
 * Adds parser error to error list.
 *
 * @param {Object} errorInfo
 * @private
 */
_addParseError: function(errorInfo) {
    this._errorList.push({
        filename: this._file.getFilename(),
        rule: 'parseError',
        message: errorInfo.message,
        line: errorInfo.loc ? errorInfo.loc.line : 1,
        column: errorInfo.loc ? errorInfo.loc.column : 0
    });
},
...
```

#### <a name="apidoc.element.jscs.errors.prototype.getValidationErrorCount"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>getValidationErrorCount ()](#apidoc.element.jscs.errors.prototype.getValidationErrorCount)
- description and source-code
```javascript
getValidationErrorCount = function () {
    return this._errorList.filter(function(error) {
        return error.rule !== 'parseError' && error.rule !== 'internalError';
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.isEmpty"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>isEmpty ()](#apidoc.element.jscs.errors.prototype.isEmpty)
- description and source-code
```javascript
isEmpty = function () {
    return this._errorList.length === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.setCurrentRule"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>setCurrentRule (rule)](#apidoc.element.jscs.errors.prototype.setCurrentRule)
- description and source-code
```javascript
setCurrentRule = function (rule) {
    this._currentRule = rule;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.errors.prototype.stripErrorList"></a>[function <span class="apidocSignatureSpan">jscs.errors.prototype.</span>stripErrorList (length)](#apidoc.element.jscs.errors.prototype.stripErrorList)
- description and source-code
```javascript
stripErrorList = function (length) {
    this._errorList.splice(length);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.js_file"></a>[module jscs.js_file](#apidoc.module.jscs.js_file)

#### <a name="apidoc.element.jscs.js_file.js_file"></a>[function <span class="apidocSignatureSpan">jscs.</span>js_file (params)](#apidoc.element.jscs.js_file.js_file)
- description and source-code
```javascript
js_file = function (params) {
    params = params || {};
    this._parseErrors = [];
    this._filename = params.filename;
    this._source = params.source;

    this._es3 = params.es3 || false;

    this._lineBreaks = null;
    this._lines = this._source.split(/\r\n|\r|\n/);

    var parser = new Parser({
        strictMode: false,
        languageExtensions: {
            gritDirectives: true,
            appleInstrumentationDirectives: true
        }
    });

    try {
        this._program = parser.parse(this._source);
    } catch (e) {
        this._parseErrors.push(e);
        this._program = new Program([
            new Token('EOF', '')
        ]);
    }

    // Lazy initialization
    this._scopes = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.js_file.prototype"></a>[module jscs.js_file.prototype](#apidoc.module.jscs.js_file.prototype)

#### <a name="apidoc.element.jscs.js_file.prototype._setTokenBefore"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>_setTokenBefore (token, fragment)](#apidoc.element.jscs.js_file.prototype._setTokenBefore)
- description and source-code
```javascript
_setTokenBefore = function (token, fragment) {
    var parent = token;
    var grandpa = parent.parentElement;

    while (grandpa) {
        try {
            grandpa.insertChildBefore(fragment, parent);
            break;
        } catch (e) {}

        parent = grandpa;
        grandpa = parent.parentElement;
    }
}
```
- example usage
```shell
...
        return;
    }

    prevToken.parentElement.replaceChild(fragment, prevToken);
    return;
}

this._setTokenBefore(token, fragment);
    },

    _setTokenBefore: function(token, fragment) {
var parent = token;
var grandpa = parent.parentElement;

while (grandpa) {
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.findNextOperatorToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findNextOperatorToken (token, value)](#apidoc.element.jscs.js_file.prototype.findNextOperatorToken)
- description and source-code
```javascript
findNextOperatorToken = function (token, value) {
    return this.findNextToken(token, value in KEYWORD_OPERATORS ? 'Keyword' : 'Punctuator', value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.findNextToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findNextToken (token, type, value)](#apidoc.element.jscs.js_file.prototype.findNextToken)
- description and source-code
```javascript
findNextToken = function (token, type, value) {
    var nextToken = token.getNextToken();

    while (nextToken) {
        if (nextToken.type === type && (value === undefined || nextToken.value === value)) {
            return nextToken;
        }

        nextToken = nextToken.getNextToken();
    }
    return nextToken;
}
```
- example usage
```shell
...
 * Returns the first token after the given which matches type (and value).
 *
 * @param {Object} token
 * @param {String} value
 * @returns {Object|null}
 */
findNextOperatorToken: function(token, value) {
    return this.findNextToken(token, value in KEYWORD_OPERATORS ? 'Keyword' : 'Punctuator', value);
},

/**
 * Iterates through the token tree using tree iterator.
 * Calls passed function for every token.
 *
 * @param {Function} cb
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.findPrevOperatorToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findPrevOperatorToken (token, value)](#apidoc.element.jscs.js_file.prototype.findPrevOperatorToken)
- description and source-code
```javascript
findPrevOperatorToken = function (token, value) {
    return this.findPrevToken(token, value in KEYWORD_OPERATORS ? 'Keyword' : 'Punctuator', value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.findPrevToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>findPrevToken (token, type, value)](#apidoc.element.jscs.js_file.prototype.findPrevToken)
- description and source-code
```javascript
findPrevToken = function (token, type, value) {
    var prevToken = this.getPrevToken(token);
    while (prevToken) {
        if (prevToken.type === type && (value === undefined || prevToken.value === value)) {
            return prevToken;
        }

        prevToken = this.getPrevToken(prevToken);
    }
    return prevToken;
}
```
- example usage
```shell
...
 * Returns the first token before the given which matches type (and value).
 *
 * @param {Object} token
 * @param {String} value
 * @returns {Object|null}
 */
findPrevOperatorToken: function(token, value) {
    return this.findPrevToken(token, value in KEYWORD_OPERATORS ? 'Keyword' : 'Punctuator', value);
},

/**
 * Returns the first token after the given which matches type (and value).
 *
 * @param {Object} token
 * @param {String} value
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getComments"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getComments ()](#apidoc.element.jscs.js_file.prototype.getComments)
- description and source-code
```javascript
getComments = function () {
    var comments = [];
    var token = this._program.getFirstToken();
    while (token) {
        if (token.isComment) {
            comments[comments.length] = token;
        }
        token = token.getNextToken();
    }
    return comments;
}
```
- example usage
```shell
...
     * Returns array of source lines for the file with comments removed.
     *
     * @returns {Array}
     */
    getLinesWithCommentsRemoved: function() {
var lines = this.getLines().concat();

this.getComments().concat().reverse().forEach(function(comment) {
    var loc = comment.getLoc();
    var startLine = loc.start.line;
    var startCol = loc.start.column;
    var endLine = loc.end.line;
    var endCol = loc.end.column;
    var i = startLine - 1;
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getDialect"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getDialect ()](#apidoc.element.jscs.js_file.prototype.getDialect)
- description and source-code
```javascript
getDialect = function () {
    if (this._es3) {
        return 'es3';
    }

    return 'es6';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getDistanceBetween"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getDistanceBetween (tokenBefore, tokenAfter)](#apidoc.element.jscs.js_file.prototype.getDistanceBetween)
- description and source-code
```javascript
getDistanceBetween = function (tokenBefore, tokenAfter) {
    if (tokenBefore === tokenAfter) {
        return 0;
    }
    tokenBefore = tokenBefore instanceof Token ? tokenBefore : tokenBefore.getLastToken();
    tokenAfter = tokenAfter instanceof Token ? tokenAfter : tokenAfter.getFirstToken();
    var currentToken = tokenBefore.getNextToken();
    var distance = 0;
    while (currentToken) {
        if (currentToken === tokenAfter) {
            break;
        }

        distance += currentToken.getSourceCodeLength();
        currentToken = currentToken.getNextToken();
    }
    return distance;
}
```
- example usage
```shell
...
        message: options.message,
        element: token,
        offset: token.getSourceCodeLength(),
        fix: fixed ? fix : undefined
    });
}.bind(this);

var spacesBetween = this._file.getDistanceBetween(token, nextToken);

if (atLeast !== undefined && spacesBetween < atLeast) {
    emitError('at least', atLeast);
    return true;
}

if (atMost !== undefined && spacesBetween > atMost) {
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getFilename"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFilename ()](#apidoc.element.jscs.js_file.prototype.getFilename)
- description and source-code
```javascript
getFilename = function () {
    return this._filename;
}
```
- example usage
```shell
...
 * Adds parser error to error list.
 *
 * @param {Object} errorInfo
 * @private
 */
_addParseError: function(errorInfo) {
    this._errorList.push({
        filename: this._file.getFilename(),
        rule: 'parseError',
        message: errorInfo.message,
        line: errorInfo.loc ? errorInfo.loc.line : 1,
        column: errorInfo.loc ? errorInfo.loc.column : 0
    });
},
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getFirstNodeToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFirstNodeToken (node)](#apidoc.element.jscs.js_file.prototype.getFirstNodeToken)
- description and source-code
```javascript
getFirstNodeToken = function (node) {
    return node.getFirstToken();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getFirstToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFirstToken ()](#apidoc.element.jscs.js_file.prototype.getFirstToken)
- description and source-code
```javascript
getFirstToken = function () {
    return this._program.getFirstToken();
}
```
- example usage
```shell
...
/**
 * Returns the first token for the node from the AST.
 *
 * @param {Object} node
 * @returns {Object}
 */
getFirstNodeToken: function(node) {
    return node.getFirstToken();
},

/**
 * Returns the last token for the node from the AST.
 *
 * @param {Object} node
 * @returns {Object}
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getFirstTokenOnLineWith"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getFirstTokenOnLineWith (element, options)](#apidoc.element.jscs.js_file.prototype.getFirstTokenOnLineWith)
- description and source-code
```javascript
getFirstTokenOnLineWith = function (element, options) {
    options = options || {};
    var firstToken = element;

    if (element.isComment && !options.includeComments) {
        firstToken = null;
    }

    if (element.isWhitespace && !options.includeWhitespace) {
        firstToken = null;
    }

    var currentToken = element.getPreviousToken();
    while (currentToken) {
        if (currentToken.isWhitespace) {
            if (currentToken.getNewlineCount() > 0 || !currentToken.getPreviousToken()) {
                if (options.includeWhitespace) {
                    firstToken = currentToken;
                }
                break;
            }
        } else if (currentToken.isComment) {
            if (options.includeComments) {
                firstToken = currentToken;
                break;
            }
            if (currentToken.getNewlineCount() > 0) {
                break;
            }
        } else {
            firstToken = currentToken;
        }

        currentToken = currentToken.getPreviousToken();
    }

    if (firstToken) {
        return firstToken;
    }

    currentToken = element.getNextToken();
    while (currentToken) {
        if (currentToken.isWhitespace) {
            if (currentToken.getNewlineCount() > 0 || !currentToken.getNextToken()) {
                if (options.includeWhitespace) {
                    firstToken = currentToken;
                }
                break;
            }
        } else if (currentToken.isComment) {
            if (options.includeComments) {
                firstToken = currentToken;
                break;
            }
            if (currentToken.getNewlineCount() > 0) {
                break;
            }
        } else {
            firstToken = currentToken;
        }

        currentToken = currentToken.getNextToken();
    }

    return firstToken;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLastNodeToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLastNodeToken (node)](#apidoc.element.jscs.js_file.prototype.getLastNodeToken)
- description and source-code
```javascript
getLastNodeToken = function (node) {
    return node.getLastToken();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLastToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLastToken ()](#apidoc.element.jscs.js_file.prototype.getLastToken)
- description and source-code
```javascript
getLastToken = function () {
    return this._program.getLastToken();
}
```
- example usage
```shell
...
/**
 * Returns the last token for the node from the AST.
 *
 * @param {Object} node
 * @returns {Object}
 */
getLastNodeToken: function(node) {
    return node.getLastToken();
},

/**
 * Returns the first token for the file.
 *
 * @param {Option} [options]
 * @param {Boolean} [options.includeComments=false]
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLastTokenOnLine"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLastTokenOnLine (lineNumber, options)](#apidoc.element.jscs.js_file.prototype.getLastTokenOnLine)
- description and source-code
```javascript
getLastTokenOnLine = function (lineNumber, options) {
    options = options || {};

    var loc;
    var token = this._program.getLastToken();
    var currentToken;

    while (token) {
        loc = token.getLoc();
        currentToken = token;
        token = token.getPreviousToken();

        if (loc.start.line <= lineNumber && loc.end.line >= lineNumber) {

            // Since whitespace tokens can contain newlines we need to check
            // if position is in the range, not exact match
            if (currentToken.isWhitespace && !options.includeWhitespace) {
                continue;
            }
        }

        if (loc.start.line === lineNumber || loc.end.line === lineNumber) {
            if (currentToken.isComment && !options.includeComments) {
                continue;
            }

            return currentToken;
        }
    }

    return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLineBreakStyle"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLineBreakStyle ()](#apidoc.element.jscs.js_file.prototype.getLineBreakStyle)
- description and source-code
```javascript
getLineBreakStyle = function () {
    var lineBreaks = this.getLineBreaks();
    return lineBreaks.length ? lineBreaks[0] : '\n';
}
```
- example usage
```shell
...
 * Updates the whitespace of a line by passing split lines to a callback function
 * for editing.
 *
 * @param {Object} token
 * @param {Function} callback
 */
TokenAssert.prototype._updateWhitespaceByLine = function(token, callback) {
    var lineBreak = this._file.getLineBreakStyle();
    var lines = this._file.getWhitespaceBefore(token).split(/\r\n|\r|\n/);

    lines = callback(lines);
    this._file.setWhitespaceBefore(token, lines.join(lineBreak));
};

/**
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLineBreaks"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLineBreaks ()](#apidoc.element.jscs.js_file.prototype.getLineBreaks)
- description and source-code
```javascript
getLineBreaks = function () {
    if (this._lineBreaks === null) {
        this._lineBreaks = this._source.match(/\r\n|\r|\n/g) || [];
    }
    return this._lineBreaks;
}
```
- example usage
```shell
...
/**
 * Returns the first line break character encountered in the file.
 * Assumes LF if the file is only one line.
 *
 * @returns {String}
 */
getLineBreakStyle: function() {
    var lineBreaks = this.getLineBreaks();
    return lineBreaks.length ? lineBreaks[0] : '\n';
},

/**
 * Returns all line break characters from the file.
 *
 * @returns {String[]}
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLineCountBetween"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLineCountBetween (tokenBefore, tokenAfter)](#apidoc.element.jscs.js_file.prototype.getLineCountBetween)
- description and source-code
```javascript
getLineCountBetween = function (tokenBefore, tokenAfter) {
    if (tokenBefore === tokenAfter) {
        return 0;
    }
    tokenBefore = tokenBefore instanceof Token ? tokenBefore : tokenBefore.getLastToken();
    tokenAfter = tokenAfter instanceof Token ? tokenAfter : tokenAfter.getFirstToken();

    var currentToken = tokenBefore.getNextToken();
    var lineCount = 0;
    while (currentToken) {
        if (currentToken === tokenAfter) {
            break;
        }

        lineCount += currentToken.getNewlineCount();
        currentToken = currentToken.getNextToken();
    }
    return lineCount;
}
```
- example usage
```shell
...

    this._validateOptions(options);

    // Only attempt to remove or add lines if there are no comments between the two nodes
    // as this prevents accidentally moving a valid token onto a line comment ed line
    var fixed = !options.token.getNextNonWhitespaceToken().isComment;

    var linesBetween = this._file.getLineCountBetween(token, nextToken);

    var emitError = function(countPrefix, lineCount) {
var msgPrefix = token.value + ' and ' + nextToken.value;

var fix = function() {
    this._augmentLineCount(options, lineCount);
}.bind(this);
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLines"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLines ()](#apidoc.element.jscs.js_file.prototype.getLines)
- description and source-code
```javascript
getLines = function () {
    return this._lines;
}
```
- example usage
```shell
...
 *
 * @param {Object} error
 * @param {Boolean} [colorize = false]
 * @returns {String}
 */
explainError: function(error, colorize) {
    var lineNumber = error.line - 1;
    var lines = this._file.getLines();
    var result = [
        renderLine(lineNumber, lines[lineNumber], colorize),
        renderPointer(error.column, colorize)
    ];
    var i = lineNumber - 1;
    var linesAround = 2;
    while (i >= 0 && i >= (lineNumber - linesAround)) {
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getLinesWithCommentsRemoved"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getLinesWithCommentsRemoved ()](#apidoc.element.jscs.js_file.prototype.getLinesWithCommentsRemoved)
- description and source-code
```javascript
getLinesWithCommentsRemoved = function () {
    var lines = this.getLines().concat();

    this.getComments().concat().reverse().forEach(function(comment) {
        var loc = comment.getLoc();
        var startLine = loc.start.line;
        var startCol = loc.start.column;
        var endLine = loc.end.line;
        var endCol = loc.end.column;
        var i = startLine - 1;

        if (startLine === endLine) {
            // Remove tralling spaces (see gh-1968)
            lines[i] = lines[i].replace(/\*\/\s+/, '\*\/');
            lines[i] = lines[i].substring(0, startCol) + lines[i].substring(endCol);
        } else {
            lines[i] = lines[i].substring(0, startCol);
            for (var x = i + 1; x < endLine - 1; x++) {
                lines[x] = '';
            }

            lines[x] = lines[x].substring(endCol);
        }
    });

    return lines;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getNextToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getNextToken (token, options)](#apidoc.element.jscs.js_file.prototype.getNextToken)
- description and source-code
```javascript
getNextToken = function (token, options) {
    if (options && options.includeComments) {
        return token.getNextNonWhitespaceToken();
    } else {
        return token.getNextCodeToken();
    }
}
```
- example usage
```shell
...
     *
     * @param {Object} token
     * @param {String} type
     * @param {String} [value]
     * @returns {Object|null}
     */
    findNextToken: function(token, type, value) {
        var nextToken = token.getNextToken();

        while (nextToken) {
if (nextToken.type === type && (value === undefined || nextToken.value === value)) {
    return nextToken;
}

nextToken = nextToken.getNextToken();
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getNodesByType"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getNodesByType (type)](#apidoc.element.jscs.js_file.prototype.getNodesByType)
- description and source-code
```javascript
getNodesByType = function (type) {
    type = Array.isArray(type) ? type : [type];
    var result = [];

    for (var i = 0, l = type.length; i < l; i++) {
        var nodes = this._program.selectNodesByType(type[i]);

        if (nodes) {
            result = result.concat(nodes);
        }
    }

    return result;
}
```
- example usage
```shell
...
 * Calls passed function for every matched node.
 *
 * @param {String|String[]} type
 * @param {Function} cb
 * @param {Object} context
 */
iterateNodesByType: function(type, cb, context) {
    return this.getNodesByType(type).forEach(cb, context || this);
},

/**
 * Iterates tokens by type(s) from the token array.
 * Calls passed function for every matched token.
 *
 * @param {String|String[]} type
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getParseErrors"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getParseErrors ()](#apidoc.element.jscs.js_file.prototype.getParseErrors)
- description and source-code
```javascript
getParseErrors = function () {
    return this._parseErrors;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getPrevToken"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getPrevToken (token, options)](#apidoc.element.jscs.js_file.prototype.getPrevToken)
- description and source-code
```javascript
getPrevToken = function (token, options) {
    if (options && options.includeComments) {
        return token.getPreviousNonWhitespaceToken();
    }

    return token.getPreviousCodeToken();
}
```
- example usage
```shell
...
     *
     * @param {Object} token
     * @param {String} type
     * @param {String} [value]
     * @returns {Object|null}
     */
    findPrevToken: function(token, type, value) {
var prevToken = this.getPrevToken(token);
while (prevToken) {
    if (prevToken.type === type && (value === undefined || prevToken.value === value)) {
        return prevToken;
    }

    prevToken = this.getPrevToken(prevToken);
}
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.getProgram"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getProgram ()](#apidoc.element.jscs.js_file.prototype.getProgram)
- description and source-code
```javascript
getProgram = function () {
    return this._program;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getScopes"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getScopes ()](#apidoc.element.jscs.js_file.prototype.getScopes)
- description and source-code
```javascript
getScopes = function () {
    if (!this._scopes) {
        this._scopes = new ScopesApi(this._program);
    }

    return this._scopes;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getSource"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getSource ()](#apidoc.element.jscs.js_file.prototype.getSource)
- description and source-code
```javascript
getSource = function () {
    return this._source;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getTree"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getTree ()](#apidoc.element.jscs.js_file.prototype.getTree)
- description and source-code
```javascript
getTree = function () {
    return this._program || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.getWhitespaceBefore"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>getWhitespaceBefore (token)](#apidoc.element.jscs.js_file.prototype.getWhitespaceBefore)
- description and source-code
```javascript
getWhitespaceBefore = function (token) {
    if (!token.getPreviousToken) {
        console.log(token);
    }
    var prev = token.getPreviousToken();

    if (prev && prev.isWhitespace) {
        return prev.getSourceCode();
    }

    return '';
}
```
- example usage
```shell
...
* for editing.
*
* @param {Object} token
* @param {Function} callback
*/
TokenAssert.prototype._updateWhitespaceByLine = function(token, callback) {
   var lineBreak = this._file.getLineBreakStyle();
   var lines = this._file.getWhitespaceBefore(token).split(/\r\n|\r|\n/);

   lines = callback(lines);
   this._file.setWhitespaceBefore(token, lines.join(lineBreak));
};

/**
* Updates the whitespace of a line by passing split lines to a callback function
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.isOnTheSameLine"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>isOnTheSameLine (tokenBefore, tokenAfter)](#apidoc.element.jscs.js_file.prototype.isOnTheSameLine)
- description and source-code
```javascript
isOnTheSameLine = function (tokenBefore, tokenAfter) {
    if (tokenBefore === tokenAfter) {
        return true;
    }
    tokenBefore = tokenBefore instanceof Token ? tokenBefore : tokenBefore.getLastToken();
    tokenAfter = tokenAfter instanceof Token ? tokenAfter : tokenAfter.getFirstToken();
    var currentToken = tokenBefore;
    while (currentToken) {
        if (currentToken === tokenAfter) {
            return true;
        }
        if (currentToken !== tokenBefore && currentToken.getNewlineCount() > 0) {
            return false;
        }
        currentToken = currentToken.getNextToken();
    }
    return false;
}
```
- example usage
```shell
...

if (!token || !nextToken) {
    return false;
}

this._validateOptions(options);

if (!options.disallowNewLine && !this._file.isOnTheSameLine(token, nextToken)) {
    return false;
}

// Only attempt to remove or add lines if there are no comments between the two nodes
// as this prevents accidentally moving a valid token onto a line comment ed line
var fixed = !options.token.getNextNonWhitespaceToken().isComment;
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.iterate"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterate (cb, tree)](#apidoc.element.jscs.js_file.prototype.iterate)
- description and source-code
```javascript
iterate = function (cb, tree) {
    return treeIterator.iterate(tree || this._program, cb);
}
```
- example usage
```shell
...
 * Iterates through the token tree using tree iterator.
 * Calls passed function for every token.
 *
 * @param {Function} cb
 * @param {Object} [tree]
 */
iterate: function(cb, tree) {
    return treeIterator.iterate(tree || this._program, cb);
},

/**
 * Returns nodes by type(s) from earlier built index.
 *
 * @param {String|String[]} type
 * @returns {Object[]}
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.iterateNodesByType"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterateNodesByType (type, cb, context)](#apidoc.element.jscs.js_file.prototype.iterateNodesByType)
- description and source-code
```javascript
iterateNodesByType = function (type, cb, context) {
    return this.getNodesByType(type).forEach(cb, context || this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.iterateTokensByType"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterateTokensByType (type, cb)](#apidoc.element.jscs.js_file.prototype.iterateTokensByType)
- description and source-code
```javascript
iterateTokensByType = function (type, cb) {
    var tokens;

    if (Array.isArray(type)) {
        tokens = [];
        for (var i = 0; i < type.length; i++) {
            var items = this._program.selectTokensByType(type[i]);
            tokens = tokens.concat(items);
        }
    } else {
        tokens = this._program.selectTokensByType(type);
    }

    tokens.forEach(cb);
}
```
- example usage
```shell
...
iterateTokensByTypeAndValue: function(type, value, cb) {
    var values = (typeof value === 'string') ? [value] : value;
    var valueIndex = {};
    values.forEach(function(type) {
        valueIndex[type] = true;
    });

    this.iterateTokensByType(type, function(token) {
        if (valueIndex[token.value]) {
            cb(token);
        }
    });
},

getFirstTokenOnLineWith: function(element, options) {
...
```

#### <a name="apidoc.element.jscs.js_file.prototype.iterateTokensByTypeAndValue"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>iterateTokensByTypeAndValue (type, value, cb)](#apidoc.element.jscs.js_file.prototype.iterateTokensByTypeAndValue)
- description and source-code
```javascript
iterateTokensByTypeAndValue = function (type, value, cb) {
    var values = (typeof value === 'string') ? [value] : value;
    var valueIndex = {};
    values.forEach(function(type) {
        valueIndex[type] = true;
    });

    this.iterateTokensByType(type, function(token) {
        if (valueIndex[token.value]) {
            cb(token);
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.render"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>render ()](#apidoc.element.jscs.js_file.prototype.render)
- description and source-code
```javascript
render = function () {
    return this._program.getSourceCode();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.js_file.prototype.setWhitespaceBefore"></a>[function <span class="apidocSignatureSpan">jscs.js_file.prototype.</span>setWhitespaceBefore (token, whitespace)](#apidoc.element.jscs.js_file.prototype.setWhitespaceBefore)
- description and source-code
```javascript
setWhitespaceBefore = function (token, whitespace) {
    var prevToken = token.getPreviousToken();
    var ws = new Token('Whitespace', whitespace);
    var fragment = new Fragment(ws);

    if (prevToken && prevToken.isWhitespace) {
        if (whitespace === '') {
            prevToken.remove();
            return;
        }

        prevToken.parentElement.replaceChild(fragment, prevToken);
        return;
    }

    this._setTokenBefore(token, fragment);
}
```
- example usage
```shell
...

    // Only attempt to remove or add lines if there are no comments between the two nodes
    // as this prevents accidentally moving a valid token onto a line comment ed line
    var fixed = !options.token.getNextNonWhitespaceToken().isComment;

    var emitError = function(countPrefix, spaceCount) {
var fix = function() {
    this._file.setWhitespaceBefore(nextToken, new Array(spaceCount + 1).join(' '));
}.bind(this);

var msgPostfix = token.value + ' and ' + nextToken.value;

if (!options.message) {
    if (exactly === 0) {
        // support noWhitespaceBetween
...
```



# <a name="apidoc.module.jscs.super_"></a>[module jscs.super_](#apidoc.module.jscs.super_)

#### <a name="apidoc.element.jscs.super_.super_"></a>[function <span class="apidocSignatureSpan">jscs.</span>super_ ()](#apidoc.element.jscs.super_.super_)
- description and source-code
```javascript
super_ = function () {
    this._configuredRules = [];

    this._errorsFound = 0;
    this._maxErrorsExceeded = false;

    this._configuration = this._createConfiguration();
    this._configuration.registerDefaultPresets();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.super_.prototype"></a>[module jscs.super_.prototype](#apidoc.module.jscs.super_.prototype)

#### <a name="apidoc.element.jscs.super_.prototype._addParseError"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_addParseError (errors, parseError, file)](#apidoc.element.jscs.super_.prototype._addParseError)
- description and source-code
```javascript
_addParseError = function (errors, parseError, file) {
    if (this._maxErrorsExceeded) {
        return;
    }

    errors.add(parseError, file.getProgram());

    if (this.maxErrorsEnabled()) {
        this._errorsFound += 1;
        this._maxErrorsExceeded = this._errorsFound >= this._maxErrors;
    }
}
```
- example usage
```shell
...
     *
     * @param {String | Error} message
     * @param {cst.types.Element} element
     * @param {Number} [offset] relative offset
     */
    add: function(message, element, offset) {
if (message instanceof Error) {
    this._addParseError(message);
    return;
}

this._addError({
    message: message,
    element: element,
    offset: offset
...
```

#### <a name="apidoc.element.jscs.super_.prototype._checkJsFile"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_checkJsFile (file, errors)](#apidoc.element.jscs.super_.prototype._checkJsFile)
- description and source-code
```javascript
_checkJsFile = function (file, errors) {
    if (this._maxErrorsExceeded) {
        return;
    }

    var errorFilter = this._configuration.getErrorFilter();

    this._configuredRules.forEach(function(rule) {
        errors.setCurrentRule(rule.getOptionName());

        try {
            rule.check(file, errors);
        } catch (e) {
            errors.setCurrentRule('internalError');
            errors.add(getInternalErrorMessage(rule.getOptionName(), e), file.getProgram());
        }
    }, this);

    this._configuration.getUnsupportedRuleNames().forEach(function(rulename) {
        errors.add('Unsupported rule: ' + rulename, file.getProgram());
    });

    var program = file.getProgram();
    var tokenIndex = new TokenIndex(program.getFirstToken());
    errors.calculateErrorLocations(tokenIndex);
    errors.filter(function(error) {
        if (error.element) {
            return tokenIndex.isRuleEnabled(error.rule, error.element);
        } else {
            return true;
        }
    });

    // sort errors list to show errors as they appear in source
    errors.getErrorList().sort(function(a, b) {
        return (a.line - b.line) || (a.column - b.column);
    });

    if (errorFilter) {
        errors.filter(errorFilter);
    }

    if (this.maxErrorsEnabled()) {
        if (this._maxErrors === -1 || this._maxErrors === null) {
            this._maxErrorsExceeded = false;

        } else {
            this._maxErrorsExceeded = this._errorsFound + errors.getErrorCount() > this._maxErrors;
            errors.stripErrorList(Math.max(0, this._maxErrors - this._errorsFound));
        }
    }

    this._errorsFound += errors.getErrorCount();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype._createConfiguration"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_createConfiguration ()](#apidoc.element.jscs.super_.prototype._createConfiguration)
- description and source-code
```javascript
_createConfiguration = function () {
    return new Configuration();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype._createJsFileInstance"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_createJsFileInstance (filename, source)](#apidoc.element.jscs.super_.prototype._createJsFileInstance)
- description and source-code
```javascript
_createJsFileInstance = function (filename, source) {
    return new JsFile({
        filename: filename,
        source: source,
        es3: this._configuration.isES3Enabled()
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype._fixCommonError"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_fixCommonError (error)](#apidoc.element.jscs.super_.prototype._fixCommonError)
- description and source-code
```javascript
_fixCommonError = function (error) {
    if (error.fix) {
        // "error.fixed = true" should go first, so rule can
        // decide for itself (with "error.fixed = false")
        // if it can fix this particular error
        error.fixed = true;
        error.fix();
    }

    return !!error.fixed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype._fixJsFile"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_fixJsFile (file, errors)](#apidoc.element.jscs.super_.prototype._fixJsFile)
- description and source-code
```javascript
_fixJsFile = function (file, errors) {
    errors.getErrorList().forEach(function(error) {
        if (error.fixed) {
            return;
        }

        try {
            // Try to apply fixes for common errors
            var isFixed = this._fixCommonError(error);

            // Apply specific fix
            if (!isFixed) {
                this._fixSpecificError(file, error);
            }
        } catch (e) {
            error.fixed = false;
            errors.add(
                getInternalErrorMessage(error.rule, e),
                file.getProgram()
            );
        }
    }, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype._fixSpecificError"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>_fixSpecificError (file, error)](#apidoc.element.jscs.super_.prototype._fixSpecificError)
- description and source-code
```javascript
_fixSpecificError = function (file, error) {
    var configuration = this.getConfiguration();
    var instance = configuration.getConfiguredRule(error.rule);

    if (instance && instance._fix) {
        // "error.fixed = true" should go first, so rule can
        // decide for itself (with "error.fixed = false")
        // if it can fix this particular error
        error.fixed = true;
        instance._fix(file, error);
    }

    return !!error.fixed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.checkString"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>checkString (source, filename)](#apidoc.element.jscs.super_.prototype.checkString)
- description and source-code
```javascript
checkString = function (source, filename) {
    filename = filename || 'input';

    var file = this._createJsFileInstance(filename, source);

    var errors = new Errors(file);

    file.getParseErrors().forEach(function(parseError) {
        if (!this._maxErrorsExceeded) {
            this._addParseError(errors, parseError, file);
        }
    }, this);

    if (!file._program || file._program.firstChild.type === 'EOF') {
        return errors;
    }

    this._checkJsFile(file, errors);

    return errors;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.configure"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>configure (config)](#apidoc.element.jscs.super_.prototype.configure)
- description and source-code
```javascript
configure = function (config) {
    this._configuration.load(config);

    this._configuredRules = this._configuration.getConfiguredRules();
    this._maxErrors = this._configuration.getMaxErrors();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.fixString"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>fixString (source, filename)](#apidoc.element.jscs.super_.prototype.fixString)
- description and source-code
```javascript
fixString = function (source, filename) {
    filename = filename || 'input';

    var file = this._createJsFileInstance(filename, source);
    var errors = new Errors(file);

    var parseErrors = file.getParseErrors();
    if (parseErrors.length > 0) {
        parseErrors.forEach(function(parseError) {
            this._addParseError(errors, parseError, file);
        }, this);

        return {output: source, errors: errors};
    } else {
        var attempt = 0;
        do {

            // Fill in errors list
            this._checkJsFile(file, errors);

            // Apply fixes
            this._fixJsFile(file, errors);

            var hasFixes = errors.getErrorList().some(function(err) {
                return err.fixed;
            });

            if (!hasFixes) {
                break;
            }

            file = this._createJsFileInstance(filename, file.render());
            errors = new Errors(file);
            attempt++;
        } while (attempt < MAX_FIX_ATTEMPTS);

        return {output: file.getSource(), errors: errors};
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.getConfiguration"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>getConfiguration ()](#apidoc.element.jscs.super_.prototype.getConfiguration)
- description and source-code
```javascript
getConfiguration = function () {
    return this._configuration;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.getProcessedConfig"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>getProcessedConfig ()](#apidoc.element.jscs.super_.prototype.getProcessedConfig)
- description and source-code
```javascript
getProcessedConfig = function () {
    return this._configuration.getProcessedConfig();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.maxErrorsEnabled"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>maxErrorsEnabled ()](#apidoc.element.jscs.super_.prototype.maxErrorsEnabled)
- description and source-code
```javascript
maxErrorsEnabled = function () {
    return this._maxErrors !== null && this._maxErrors !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.maxErrorsExceeded"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>maxErrorsExceeded ()](#apidoc.element.jscs.super_.prototype.maxErrorsExceeded)
- description and source-code
```javascript
maxErrorsExceeded = function () {
    return this._maxErrorsExceeded;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.registerDefaultRules"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>registerDefaultRules ()](#apidoc.element.jscs.super_.prototype.registerDefaultRules)
- description and source-code
```javascript
registerDefaultRules = function () {
    this._configuration.registerDefaultRules();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.super_.prototype.registerRule"></a>[function <span class="apidocSignatureSpan">jscs.super_.prototype.</span>registerRule (rule)](#apidoc.element.jscs.super_.prototype.registerRule)
- description and source-code
```javascript
registerRule = function (rule) {
    this._configuration.registerRule(rule);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.token_assert"></a>[module jscs.token_assert](#apidoc.module.jscs.token_assert)

#### <a name="apidoc.element.jscs.token_assert.token_assert"></a>[function <span class="apidocSignatureSpan">jscs.</span>token_assert (file)](#apidoc.element.jscs.token_assert.token_assert)
- description and source-code
```javascript
function TokenAssert(file) {
    EventEmitter.call(this);

    this._file = file;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_assert.super_"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.</span>super_ ()](#apidoc.element.jscs.token_assert.super_)
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



# <a name="apidoc.module.jscs.token_assert.prototype"></a>[module jscs.token_assert.prototype](#apidoc.module.jscs.token_assert.prototype)

#### <a name="apidoc.element.jscs.token_assert.prototype._augmentLineCount"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_augmentLineCount (options, lineCount)](#apidoc.element.jscs.token_assert.prototype._augmentLineCount)
- description and source-code
```javascript
_augmentLineCount = function (options, lineCount) {
    var token = options.nextToken;
    if (lineCount === 0) {
        if (options.stickToPreviousToken) {
            var nextToken = this._file.getNextToken(token, {
                includeComments: true
            });
            this._file.setWhitespaceBefore(nextToken, this._file.getWhitespaceBefore(token));
        }

        this._file.setWhitespaceBefore(token, ' ');
        return;
    }

    this._updateWhitespaceByLine(token, function(lines) {
        var currentLineCount = lines.length;
        var lastLine = lines[lines.length - 1];

        if (currentLineCount <= lineCount) {
            // add additional lines that maintain the same indentation as the former last line
            for (; currentLineCount <= lineCount; currentLineCount++) {
                lines[lines.length - 1] = '';
                lines.push(lastLine);
            }
        } else {
            // remove lines and then ensure that the new last line maintains the previous indentation
            lines = lines.slice(0, lineCount + 1);
            lines[lines.length - 1] = lastLine;
        }

        return lines;
    });
}
```
- example usage
```shell
...

    var linesBetween = this._file.getLineCountBetween(token, nextToken);

    var emitError = function(countPrefix, lineCount) {
var msgPrefix = token.value + ' and ' + nextToken.value;

var fix = function() {
    this._augmentLineCount(options, lineCount);
}.bind(this);

if (!options.message) {
    if (exactly === 0) {
        // support sameLine
        options.message = msgPrefix + ' should be on the same line';
    } else if (atLeast === 1 && atMost === undefined) {
...
```

#### <a name="apidoc.element.jscs.token_assert.prototype._updateCommentWhitespace"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_updateCommentWhitespace (token, indentChar, actual, expected)](#apidoc.element.jscs.token_assert.prototype._updateCommentWhitespace)
- description and source-code
```javascript
_updateCommentWhitespace = function (token, indentChar, actual, expected) {
    var difference = expected - actual;
    var tokenLines = token.value.split(/\r\n|\r|\n/);
    var i = 1;
    if (difference >= 0) {
        var lineWhitespace = (new Array(difference + 1)).join(indentChar);
        for (; i < tokenLines.length; i++) {
            tokenLines[i] = tokenLines[i] === '' ? '' : lineWhitespace + tokenLines[i];
        }
    } else {
        for (; i < tokenLines.length; i++) {
            tokenLines[i] = tokenLines[i].substring(-difference);
        }
    }

    var newComment = new Token('CommentBlock', tokenLines.join(this._file.getLineBreakStyle()));
    token.parentElement.replaceChild(newComment, token);
}
```
- example usage
```shell
...

            this._updateWhitespaceByLine(token, function(lines) {
                lines[lines.length - 1] = newWhitespace;
                return lines;
            });

            if (token.isComment) {
                this._updateCommentWhitespace(token, indentChar, actual, expected);
            }
        }.bind(this)
    });

    return true;
};
...
```

#### <a name="apidoc.element.jscs.token_assert.prototype._updateWhitespaceByLine"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_updateWhitespaceByLine (token, callback)](#apidoc.element.jscs.token_assert.prototype._updateWhitespaceByLine)
- description and source-code
```javascript
_updateWhitespaceByLine = function (token, callback) {
    var lineBreak = this._file.getLineBreakStyle();
    var lines = this._file.getWhitespaceBefore(token).split(/\r\n|\r|\n/);

    lines = callback(lines);
    this._file.setWhitespaceBefore(token, lines.join(lineBreak));
}
```
- example usage
```shell
...
    this.emit('error', {
        message: 'Expected indentation of ' + expected + ' characters',
        line: lineNumber,
        column: expected,
        fix: function() {
var newWhitespace = (new Array(expected + 1)).join(indentChar);

this._updateWhitespaceByLine(token, function(lines) {
    lines[lines.length - 1] = newWhitespace;
    return lines;
});

if (token.isComment) {
    this._updateCommentWhitespace(token, indentChar, actual, expected);
}
...
```

#### <a name="apidoc.element.jscs.token_assert.prototype._validateOptions"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>_validateOptions (options)](#apidoc.element.jscs.token_assert.prototype._validateOptions)
- description and source-code
```javascript
_validateOptions = function (options) {
    var token = options.token;
    var nextToken = options.nextToken;
    var atLeast = options.atLeast;
    var atMost = options.atMost;
    var exactly = options.exactly;

    if (token === nextToken) {
        throw new Error('You cannot specify the same token as both token and nextToken');
    }

    if (atLeast === undefined &&
        atMost === undefined &&
        exactly === undefined) {
        throw new Error('You must specify at least one option');
    }

    if (exactly !== undefined && (atLeast !== undefined || atMost !== undefined)) {
        throw new Error('You cannot specify atLeast or atMost with exactly');
    }

    if (atLeast !== undefined && atMost !== undefined && atMost < atLeast) {
        throw new Error('atLeast and atMost are in conflict');
    }
}
```
- example usage
```shell
...
var atMost = options.atMost;
var exactly = options.exactly;

if (!token || !nextToken) {
    return false;
}

this._validateOptions(options);

if (!options.disallowNewLine && !this._file.isOnTheSameLine(token, nextToken)) {
    return false;
}

// Only attempt to remove or add lines if there are no comments between the two nodes
// as this prevents accidentally moving a valid token onto a line comment ed line
...
```

#### <a name="apidoc.element.jscs.token_assert.prototype.differentLine"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>differentLine (options)](#apidoc.element.jscs.token_assert.prototype.differentLine)
- description and source-code
```javascript
differentLine = function (options) {
    options.atLeast = 1;

    return this.linesBetween(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_assert.prototype.indentation"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>indentation (options)](#apidoc.element.jscs.token_assert.prototype.indentation)
- description and source-code
```javascript
indentation = function (options) {
    var token = options.token;
    var lineNumber = options.lineNumber;
    var actual = options.actual;
    var expected = options.expected;
    var indentChar = options.indentChar;

    if (actual === expected) {
        return false;
    }

    this.emit('error', {
        message: 'Expected indentation of ' + expected + ' characters',
        line: lineNumber,
        column: expected,
        fix: function() {
            var newWhitespace = (new Array(expected + 1)).join(indentChar);

            this._updateWhitespaceByLine(token, function(lines) {
                lines[lines.length - 1] = newWhitespace;
                return lines;
            });

            if (token.isComment) {
                this._updateCommentWhitespace(token, indentChar, actual, expected);
            }
        }.bind(this)
    });

    return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_assert.prototype.linesBetween"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>linesBetween (options)](#apidoc.element.jscs.token_assert.prototype.linesBetween)
- description and source-code
```javascript
linesBetween = function (options) {
    var token = options.token;
    var nextToken = options.nextToken;
    var atLeast = options.atLeast;
    var atMost = options.atMost;
    var exactly = options.exactly;

    if (!token || !nextToken) {
        return false;
    }

    this._validateOptions(options);

    // Only attempt to remove or add lines if there are no comments between the two nodes
    // as this prevents accidentally moving a valid token onto a line comment ed line
    var fixed = !options.token.getNextNonWhitespaceToken().isComment;

    var linesBetween = this._file.getLineCountBetween(token, nextToken);

    var emitError = function(countPrefix, lineCount) {
        var msgPrefix = token.value + ' and ' + nextToken.value;

        var fix = function() {
            this._augmentLineCount(options, lineCount);
        }.bind(this);

        if (!options.message) {
            if (exactly === 0) {
                // support sameLine
                options.message = msgPrefix + ' should be on the same line';
            } else if (atLeast === 1 && atMost === undefined) {
                // support differentLine
                options.message = msgPrefix + ' should be on different lines';
            } else {
                // support linesBetween
                options.message = msgPrefix + ' should have ' + countPrefix + ' ' + lineCount + ' line(s) between them';
            }
        }

        this.emit('error', {
            message: options.message,
            element: token,
            offset: token.getSourceCodeLength(),
            fix: fixed ? fix : undefined
        });
    }.bind(this);

    if (atLeast !== undefined && linesBetween < atLeast) {
        emitError('at least', atLeast);
        return true;
    }

    if (atMost !== undefined && linesBetween > atMost) {
        emitError('at most', atMost);
        return true;
    }

    if (exactly !== undefined && linesBetween !== exactly) {
        emitError('exactly', exactly);
        return true;
    }

    return false;
}
```
- example usage
```shell
...
* @param {Boolean} [options.stickToPreviousToken]
* @param {String} [options.message]
* @return {Boolean} whether an error was found
*/
TokenAssert.prototype.sameLine = function(options) {
   options.exactly = 0;

   return this.linesBetween(options);
};

/**
* Requires tokens to be on different lines.
*
* @param {Object} options
* @param {Object} options.token
...
```

#### <a name="apidoc.element.jscs.token_assert.prototype.noWhitespaceBetween"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>noWhitespaceBetween (options)](#apidoc.element.jscs.token_assert.prototype.noWhitespaceBetween)
- description and source-code
```javascript
noWhitespaceBetween = function (options) {
    options.exactly = 0;
    return this.spacesBetween(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_assert.prototype.sameLine"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>sameLine (options)](#apidoc.element.jscs.token_assert.prototype.sameLine)
- description and source-code
```javascript
sameLine = function (options) {
    options.exactly = 0;

    return this.linesBetween(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_assert.prototype.spacesBetween"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>spacesBetween (options)](#apidoc.element.jscs.token_assert.prototype.spacesBetween)
- description and source-code
```javascript
spacesBetween = function (options) {
    var token = options.token;
    var nextToken = options.nextToken;
    var atLeast = options.atLeast;
    var atMost = options.atMost;
    var exactly = options.exactly;

    if (!token || !nextToken) {
        return false;
    }

    this._validateOptions(options);

    if (!options.disallowNewLine && !this._file.isOnTheSameLine(token, nextToken)) {
        return false;
    }

    // Only attempt to remove or add lines if there are no comments between the two nodes
    // as this prevents accidentally moving a valid token onto a line comment ed line
    var fixed = !options.token.getNextNonWhitespaceToken().isComment;

    var emitError = function(countPrefix, spaceCount) {
        var fix = function() {
            this._file.setWhitespaceBefore(nextToken, new Array(spaceCount + 1).join(' '));
        }.bind(this);

        var msgPostfix = token.value + ' and ' + nextToken.value;

        if (!options.message) {
            if (exactly === 0) {
                // support noWhitespaceBetween
                options.message = 'Unexpected whitespace between ' + msgPostfix;
            } else if (exactly !== undefined) {
                // support whitespaceBetween (spaces option)
                options.message = spaceCount + ' spaces required between ' + msgPostfix;
            } else if (atLeast === 1 && atMost === undefined) {
                // support whitespaceBetween (no spaces option)
                options.message = 'Missing space between ' + msgPostfix;
            } else {
                options.message = countPrefix + ' ' + spaceCount + ' spaces required between ' + msgPostfix;
            }
        }

        this.emit('error', {
            message: options.message,
            element: token,
            offset: token.getSourceCodeLength(),
            fix: fixed ? fix : undefined
        });
    }.bind(this);

    var spacesBetween = this._file.getDistanceBetween(token, nextToken);

    if (atLeast !== undefined && spacesBetween < atLeast) {
        emitError('at least', atLeast);
        return true;
    }

    if (atMost !== undefined && spacesBetween > atMost) {
        emitError('at most', atMost);
        return true;
    }

    if (exactly !== undefined && spacesBetween !== exactly) {
        emitError('exactly', exactly);
        return true;
    }

    return false;
}
```
- example usage
```shell
...
* @param {Object} options.nextToken
* @param {String} [options.message]
* @param {Number} [options.spaces] Amount of spaces between tokens.
* @return {Boolean} whether an error was found
*/
TokenAssert.prototype.whitespaceBetween = function(options) {
   options.atLeast = 1;
   return this.spacesBetween(options);
};

/**
* Requires to have no whitespace between specified tokens.
*
* @param {Object} options
* @param {Object} options.token
...
```

#### <a name="apidoc.element.jscs.token_assert.prototype.whitespaceBetween"></a>[function <span class="apidocSignatureSpan">jscs.token_assert.prototype.</span>whitespaceBetween (options)](#apidoc.element.jscs.token_assert.prototype.whitespaceBetween)
- description and source-code
```javascript
whitespaceBetween = function (options) {
    options.atLeast = 1;
    return this.spacesBetween(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.token_categorizer"></a>[module jscs.token_categorizer](#apidoc.module.jscs.token_categorizer)

#### <a name="apidoc.element.jscs.token_categorizer.categorizeCloseParen"></a>[function <span class="apidocSignatureSpan">jscs.token_categorizer.</span>categorizeCloseParen (token)](#apidoc.element.jscs.token_categorizer.categorizeCloseParen)
- description and source-code
```javascript
categorizeCloseParen = function (token) {
    assert(token.value === ')', 'Input token must be a parenthesis');
    var node = token.parentElement;
    var nodeType = node.type;
    var nextToken = token.getNextCodeToken();

    // Terminal statement
    if (nextToken.type === 'EOF') {
        switch (nodeType) {
            case 'DoWhileStatement':
                return 'Statement';
            case 'CallExpression':
            case 'NewExpression':
                return 'CallExpression';
            default:
                return 'ParenthesizedExpression';
        }
    }

    // Part of a parentheses-bearing statement (if, with, while, switch, etc.)
    if (PAREN_KEYWORD_TYPE_RE.test(nodeType) && !NO_PAREN_KEYWORD_TYPE_RE.test(nodeType)) {
        // Closing parentheses for 'switch' and 'catch' must be followed by "{"
        // Closing parentheses for 'do..while' may be the last punctuation inside a block
        if (nextToken.value === '{' || nextToken.value === '}') {
            return 'Statement';
        }

        // Closing parentheses for other statements must be followed by a statement or declaration
        var nextNode = nextToken.parentElement;
        while (!nodeContains(nextNode, token)) {
            if (QUASI_STATEMENT_TYPE_RE.test(nextNode.type)) {
                return 'Statement';
            }
            nextNode = nextNode.parentElement;
        }
    }

    // Part of a function definition (declaration, expression, method, etc.)
    if (nextToken.value === '{' && FUNCTION_TYPE_RE.test(nodeType)) {
        return 'Function';
    }

    // Part of a call expression
    if ((nodeType === 'CallExpression' || nodeType === 'NewExpression')) {
        var openParen = node.callee.getNextToken();
        if (openParen.parentElement === node && node.lastChild === token) {
            return 'CallExpression';
        }
    }

    // All remaining cases are grouping parentheses
    return 'ParenthesizedExpression';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.token_categorizer.categorizeOpenParen"></a>[function <span class="apidocSignatureSpan">jscs.token_categorizer.</span>categorizeOpenParen (token)](#apidoc.element.jscs.token_categorizer.categorizeOpenParen)
- description and source-code
```javascript
categorizeOpenParen = function (token) {
    assert(token.value === '(', 'Input token must be a parenthesis');
    var node = token.parentElement;
    var nodeType = node.type;
    var prevToken = token.getPreviousCodeToken();

    // Outermost grouping parenthesis
    if (!prevToken) {
        return 'ParenthesizedExpression';
    }

    // Part of a parentheses-bearing statement (if, with, while, switch, etc.)
    if (prevToken.type === 'Keyword' && PAREN_KEYWORD_TYPE_RE.test(nodeType) &&
        !NO_PAREN_KEYWORD_TYPE_RE.test(nodeType)) {

        return 'Statement';
    }

    // Part of a function definition (declaration, expression, method, etc.)
    if (FUNCTION_TYPE_RE.test(nodeType) &&

        // Name is optional for function expressions
        (prevToken.type === 'Identifier' || prevToken.value === 'function')) {

        return 'Function';
    }

    // Part of a call expression
    var prevNode = prevToken.parentElement;
    if ((nodeType === 'CallExpression' || nodeType === 'NewExpression') &&

        // Must not be inside an arguments list or other grouping parentheses
        prevToken.value !== ',' && prevToken.value !== '(' &&

        // If the callee is parenthesized (e.g., '(foo.bar)()'), prevNode will match node
        // Otherwise (e.g., 'foo.bar()'), prevToken must be the last token of the callee node
        (prevNode === node || prevToken === node.callee.getLastToken())) {

        return 'CallExpression';
    }

    // All remaining cases are grouping parentheses
    return 'ParenthesizedExpression';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.jscs.tree_iterator"></a>[module jscs.tree_iterator](#apidoc.module.jscs.tree_iterator)

#### <a name="apidoc.element.jscs.tree_iterator.iterate"></a>[function <span class="apidocSignatureSpan">jscs.tree_iterator.</span>iterate (node, cb)](#apidoc.element.jscs.tree_iterator.iterate)
- description and source-code
```javascript
function iterate(node, cb) {
    if ('type' in node) {
        estraverse.traverse(node, {
            enter: function(node, parent) {
                var parentCollection = [];

                // parentCollection support
                var path = this.path();
                if (path) {
                    var collectionKey;
                    while (path.length > 0) {
                        var pathElement = path.pop();
                        if (typeof pathElement === 'string') {
                            collectionKey = pathElement;
                            break;
                        }
                    }

                    parentCollection = parent[collectionKey];
                    if (!Array.isArray(parentCollection)) {
                        parentCollection = [parentCollection];
                    }
                }

                if (cb(node, parent, parentCollection) === false) {
                    return estraverse.VisitorOption.Skip;
                }
            },
            keys: VISITOR_KEYS
        });
    }
}
```
- example usage
```shell
...
 * Iterates through the token tree using tree iterator.
 * Calls passed function for every token.
 *
 * @param {Function} cb
 * @param {Object} [tree]
 */
iterate: function(cb, tree) {
    return treeIterator.iterate(tree || this._program, cb);
},

/**
 * Returns nodes by type(s) from earlier built index.
 *
 * @param {String|String[]} type
 * @returns {Object[]}
...
```



# <a name="apidoc.module.jscs.utils"></a>[module jscs.utils](#apidoc.module.jscs.utils)

#### <a name="apidoc.element.jscs.utils.getFunctionNodeFromIIFE"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>getFunctionNodeFromIIFE (node)](#apidoc.element.jscs.utils.getFunctionNodeFromIIFE)
- description and source-code
```javascript
getFunctionNodeFromIIFE = function (node) {
    if (node.type !== 'CallExpression') {
        return null;
    }

    var callee = node.callee;

    if (callee.type === 'FunctionExpression') {
        return callee;
    }

    if (callee.type === 'MemberExpression' &&
        callee.object.type === 'FunctionExpression' &&
        callee.property.type === 'Identifier' &&
        (callee.property.name === 'call' || callee.property.name === 'apply')
    ) {
        return callee.object;
    }

    return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.utils.isPragma"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>isPragma (additionalExceptions)](#apidoc.element.jscs.utils.isPragma)
- description and source-code
```javascript
isPragma = function (additionalExceptions) {
    var pragmaKeywords = [
        'eslint',
        'eslint-env',
        'eslint-enable',
        'eslint-disable',
        'eslint-disable-line',
        'eslint-disable-next-line',
        'global',
        'jshint',
        'jslint',
        'globals',
        'falls through',
        'exported',
        'jscs:',
        'jscs:enable',
        'jscs:disable',
        'jscs:ignore',
        'istanbul'
    ];
    if (additionalExceptions && Array.isArray(additionalExceptions)) {
        pragmaKeywords = pragmaKeywords.concat(additionalExceptions);
    }

    return function(comment) {
        // pragmaKeywords precede a space or the end of the comment
        var trimmedComment = comment.trim() + ' ';
        for (var i = 0; i < pragmaKeywords.length; i++) {
            if (trimmedComment.indexOf(pragmaKeywords[i] + ' ') === 0) {
                return true;
            }
        }
        return false;
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.utils.isRelativePath"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>isRelativePath (path)](#apidoc.element.jscs.utils.isRelativePath)
- description and source-code
```javascript
isRelativePath = function (path) {
    // Logic from: https://github.com/joyent/node/blob/4f1ae11a62b97052bc83756f8cb8700cc1f61661/lib/module.js#L237
    var start = path.substring(0, 2);
    return start === './' || start === '..';
}
```
- example usage
```shell
...
 * or just returns the filepath if not relative
 *
 * @param  {String} filepath
 * @param  {String} basePath
 * @return {String}
 */
exports.normalizePath = function(filepath, basePath) {
    if (this.isRelativePath(filepath)) {
        return path.resolve(basePath, filepath);
    }

    return filepath;
};

/**
...
```

#### <a name="apidoc.element.jscs.utils.isSnakeCased"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>isSnakeCased (name)](#apidoc.element.jscs.utils.isSnakeCased)
- description and source-code
```javascript
isSnakeCased = function (name) {
    return SNAKE_CASE_RE.test(name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.utils.isValidIdentifierName"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>isValidIdentifierName (name, dialect)](#apidoc.element.jscs.utils.isValidIdentifierName)
- description and source-code
```javascript
isValidIdentifierName = function (name, dialect) {
    dialect = dialect || 'es5';
    var identifierRegex = dialect === 'es5' ? IDENTIFIER_NAME_ES5_RE : IDENTIFIER_NAME_ES6_RE;
    return !reservedWords.check(name, dialect, true) && identifierRegex.test(name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.utils.normalizePath"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>normalizePath (filepath, basePath)](#apidoc.element.jscs.utils.normalizePath)
- description and source-code
```javascript
normalizePath = function (filepath, basePath) {
    if (this.isRelativePath(filepath)) {
        return path.resolve(basePath, filepath);
    }

    return filepath;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.utils.promisify"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>promisify (fn)](#apidoc.element.jscs.utils.promisify)
- description and source-code
```javascript
promisify = function (fn) {
    return function() {
        var deferred = Vow.defer();
        var args = [].slice.call(arguments);

        args.push(function(err, result) {
            if (err) {
                deferred.reject(err);
            } else {
                deferred.resolve(result);
            }
        });

        fn.apply(null, args);

        return deferred.promise();
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.jscs.utils.trimUnderscores"></a>[function <span class="apidocSignatureSpan">jscs.utils.</span>trimUnderscores (name)](#apidoc.element.jscs.utils.trimUnderscores)
- description and source-code
```javascript
trimUnderscores = function (name) {
    var res = name.replace(TRAILING_UNDERSCORES_RE, '');
    return res ? res : name;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
