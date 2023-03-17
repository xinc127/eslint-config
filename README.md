# @xxxxinc/eslint-config

Forked from [antfu/eslint-config](https://github.com/antfu/eslint-config)

## Usage

### Install

```bash
pnpm add -D eslint @xxxxinc/eslint-config
```

### Config `.eslintrc`

```json
{
  "extends": "@xxxxinc"
}
```

> You don't need `.eslintignore` normally as it has been provided by the preset.

### Add script for package.json

For example:

```json
{
  "scripts": {
    "lint": "eslint .",
    "lint:fix": "eslint . --fix"
  }
}
```

### Config VS Code auto fix

Install [VS Code ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) and create `.vscode/settings.json`

```json
{
  "prettier.enable": false,
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

### TypeScript Aware Rules

Type aware rules are enabled when a `tsconfig.eslint.json` is found in the project root, which will introduce some stricter rules into your project. If you want to enable it while have no `tsconfig.eslint.json` in the project root, you can change tsconfig name by modifying `ESLINT_TSCONFIG` env. 

```js
// .eslintrc.js
process.env.ESLINT_TSCONFIG = 'tsconfig.json'

module.exports = {
  extends: '@xxxxinc'
}
```

## License

[MIT](./LICENSE) License &copy; 2023-PRESENT [xxxxinc](https://github.com/xxxxinc)
