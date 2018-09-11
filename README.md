# Instructions

https://babeljs.io/docs/en/usage

https://css-tricks.com/why-npm-scripts/

```
1. $ npm init

2. Install modules:
    $ npm install --save-dev @babel/core @babel/cli @babel/preset-env
    $ npm install --save @babel/polyfill

3. Touch babel.config.js in project root and fill it with:

    const presets = [
      ["@babel/env", {
        targets: {
          edge: "17",
          firefox: "60",
          chrome: "67",
          safari: "11.1"
        },
        useBuiltIns: "usage"
      }]
    ];

    module.exports = { presets };

To run: $ ./node_modules/.bin/babel app --out-dir dist
    (or $ npx babel app --out-dir dist)

4. OR...add this to package.json, below the test script:
    "build:js": "babel app -d dist --presets @babel/preset-env"

To run: $ npm run build:js

5. Watch for file change and run scripts automatically:

$ npm node install --save-dev node-sass
$ node-sass --output-style compressed -o dist/css app/scss





```
