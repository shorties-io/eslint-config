# eslint-config

This is the ESLint configuration for the shorties.io codebase(s), it is published to npmjs public registry as `@shorties-io/eslint-config`

To use this, add it as a dependency of your project and then it's as simple as creating an `.eslintrc` file with the following contents:

```
{
	"extends": "@shorties-io/eslint-config"
}
```

In order to use this with a CommonJS project, you should adjust the settings a bit.

```js
// .eslintrc.js
"use strict";

module.exports = {
  extends: ["@shorties-io/eslint-config"],
  env: {
    browser: false,
    node: true,
    worker: false
  },
  parserOptions: {
    sourceType: "script",
    ecmaFeatures: {}
  }
};
```
