## Eslin, Prettier && EditorConfig

A simple guide to configure your code editor for working with React Native.

<hr>

### Eslint

- `yarn add eslint -D`

If you project already have a `.eslintrc.js` delete it in order to follow the next steps.

- `yarn eslint --init`

- `yarn add prettier eslint-config-prettier eslint-plugin-prettier babel-eslint -D`

In your .eslintrc add the following content

```js
module.exports = {
  env: {
    es6: true,
  },
  extends: [
    'plugin:react/recommended',
    'airbnb',
    'prettier',
    'prettier/react'
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
    __DEV__: 'readonly'
    React$Node: 'readonly',
  },
  parser: 'babel-eslint',
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: [
    'react',
    'prettier'
  ],
  rules: {
    'prettier/prettier': 'error',
    'react/jsx-filename-extension': ['error', { extensions: ['.js', '.jsx'] }],
    'import/prefer-default-export': 'off',
    'no-unused-vars': ['error', { argsIgnorePattern: '^_' }],
    'react/jsx-one-expression-per-line': 'off',
    'global-require': 'off',
    'react-native/no-raw-text': 'off',
    'no-param-reassign': 'off',
    'no-underscore-dangle': 'off',
    camelcase: 'off',
    'no-console': ['error', { allow: ['tron'] }],
  },
};
```

### Prettier

Create a `.prettierrc`file with the following content

```js
{
  "singleQuote": true,
  "trailingComma": "es5"
}
```

### EditorConfig

```js
root = true

[*]
enf_of_line = lf
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = false
insert_final_newline = false
```