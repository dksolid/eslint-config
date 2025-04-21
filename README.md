## Private ESLint config

[![npm](https://img.shields.io/npm/v/@dksolid/eslint-config)](https://www.npmjs.com/package/@dksolid/eslint-config)
[![license](https://img.shields.io/npm/l/@dksolid/eslint-config)](https://github.com/dksolid/eslint-config/blob/main/LICENSE)

### Usage

1. Add `@dksolid/eslint-config` to `devDependencies` in package.json
2. Create `eslint.config.cjs` with content:
```javascript
const path = require('path');

const { getEslintConfig } = require('@dksolid/eslint-config');

const eslintConfig = getEslintConfig({
  tsConfigPath: path.resolve(__dirname, './tsconfig.json'),
});

module.exports = eslintConfig;
```
3. Add scripts to package.json (example for formatting only pointed files but analyze all files):
```json
{
  "scripts": {
    "analyze:js": "eslint ./src",
    "format:js": "eslint --fix"
  }
}
```

Attach ESLint to your IDE, don't forget to enable auto-formatting on save.
