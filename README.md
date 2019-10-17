1. Follow steps from [How To Set Up ESLint, TypeScript, Prettier with Create React App](https://dev.to/benweiser/how-to-set-up-eslint-typescript-prettier-with-create-react-app-3675)

2. Remove all traces of `prettier` from `.eslintrc.json`, this is dumb since prettier will fix all these lint errors:

3. Add to `.eslintignore`:

```
src/serviceWorker.ts
src/react-app-env.d.ts
src/**/__tests__/**
```

4. Add to VSCode config:

```json
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    {
      "language": "typescript",
      "autoFix": true
    },
    {
      "language": "typescriptreact",
      "autoFix": true
    }
  ],
```
