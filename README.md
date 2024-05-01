# stylistic-default

To initialized the ESLint for a project:

```console
$ npm i -D eslint @stylistic/eslint-plugin @typescript-eslint/parser
```

Install this package using following command:

```console
$ npm i -D https://github.com/path-undefined/stylistic-default
```

An example `eslint.config.mjs` file:

```js
import stylistic from "@stylistic/eslint-plugin";
import typescriptEslintParser from "@typescript-eslint/parser";
import stylisticDefault from "stylistic-default";

export default [
  {
    files: [
      "src/**/*.ts",
      "eslint.config.mjs",
    ],

    plugins: {
      "@stylistic": stylistic,
    },

    languageOptions: {
      parser: typescriptEslintParser,
    },

    rules: {
      ...stylisticDefault,
    },
  },
];
```
