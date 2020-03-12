# AmplifyTest
Repo reproducting https://github.com/aws-amplify/amplify-js/issues/4025

## Steps to reproduce
1. npx react-native init AmplifyTest --template react-native-template-typescript
2. npm install aws-amplify aws-amplify-react-native
3. npm install --dev babel-plugin-module-resolver
4. Add module-resolver plugin to babel.config.js:
```plugins: [
    [
      'module-resolver',
      {
        root: ['./'],
        extensions: [
          '.ios.ts',
          '.android.ts',
          '.ts',
          '.ios.tsx',
          '.android.tsx',
          '.tsx',
          '.jsx',
          '.js',
          '.json',
        ],
        alias: {},
      },
    ],
  ],```
5. Run!
