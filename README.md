# npmtest-howler

#### basic test coverage for  [howler (v2.0.3)](https://howlerjs.com)  [![npm package](https://img.shields.io/npm/v/npmtest-howler.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-howler) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-howler.svg)](https://travis-ci.org/npmtest/node-npmtest-howler)

#### Javascript audio library for the modern web.

[![NPM](https://nodei.co/npm/howler.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/howler)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-howler/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-howler/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-howler/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-howler/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-howler/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-howler/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-howler/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-howler/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-howler/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-howler/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-howler/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-howler/build/test-report.html](https://npmtest.github.io/node-npmtest-howler/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-howler/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-howler/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-howler/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-howler/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-howler/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-howler/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-howler/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-howler/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "James Simpson",
        "url": "http://goldfirestudios.com"
    },
    "bugs": {
        "url": "https://github.com/goldfire/howler.js/issues"
    },
    "dependencies": {},
    "description": "Javascript audio library for the modern web.",
    "devDependencies": {
        "uglify-js": "2.x"
    },
    "directories": {},
    "dist": {
        "shasum": "a76ab5a37ae5cc1e4a5a0f3ce279ca2c72b5efc7",
        "tarball": "https://registry.npmjs.org/howler/-/howler-2.0.3.tgz"
    },
    "files": [
        "src",
        "dist/howler.js",
        "dist/howler.min.js",
        "dist/howler.core.min.js",
        "dist/howler.spatial.min.js",
        "LICENSE.md"
    ],
    "gitHead": "4ebd1897b6c425befde7970c583999db663d2093",
    "homepage": "https://howlerjs.com",
    "keywords": [
        "howler",
        "howler.js",
        "audio",
        "sound",
        "web audio",
        "webaudio",
        "browser",
        "html5",
        "html5 audio",
        "audio sprite",
        "audiosprite"
    ],
    "license": {
        "type": "MIT",
        "url": "https://raw.githubusercontent.com/goldfire/howler.js/master/LICENSE.md"
    },
    "main": "dist/howler.js",
    "maintainers": [
        {
            "name": "goldfire"
        }
    ],
    "name": "howler",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/goldfire/howler.js.git"
    },
    "scripts": {
        "build": "VERSION='printf 'v' && node -e 'console.log(require(\"./package.json\").version)'' && sed -i '' '2s/.*/ *  howler.js '\"$VERSION\"'/' src/howler.core.js && sed -i '' '4s/.*/ *  howler.js '\"$VERSION\"'/' src/plugins/howler.spatial.js && uglifyjs --preamble \"/*! howler.js $VERSION | (c) 2013-2017, James Simpson of GoldFire Studios | MIT License | howlerjs.com */\" src/howler.core.js -c -m --screw-ie8 -o dist/howler.core.min.js && uglifyjs --preamble \"/*! howler.js $VERSION | Spatial Plugin | (c) 2013-2017, James Simpson of GoldFire Studios | MIT License | howlerjs.com */\" src/plugins/howler.spatial.js -c -m --screw-ie8 -o dist/howler.spatial.min.js && awk 'FNR==1{echo \"\"}1' dist/howler.core.min.js dist/howler.spatial.min.js | sed '3s~.*~/*! Spatial Plugin */~' | perl -pe 'chomp if eof' > dist/howler.min.js && awk '(NR>1 && FNR==1){printf (\"\\n\\n\")};1' src/howler.core.js src/plugins/howler.spatial.js > dist/howler.js",
        "release": "VERSION='printf 'v' && node -e 'console.log(require(\"./package.json\").version)'' && git tag $VERSION && git push && git push origin $VERSION && npm publish"
    },
    "version": "2.0.3",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
