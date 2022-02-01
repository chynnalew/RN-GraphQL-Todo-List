# To do list 

## created to learn GraphQL with Apollo in React Native

#### Updates by: Chynna Lew

#### created with https://hasura.io/learn/graphql/react-native/introduction/

### Updates to instructions

- many npm dependencies deprecated, npm install with --force tag
- update expo to 41.0.0 to use with expo app, v 39.0.0 incompatible
- add metro.config.js file to handle bundling main.cjs.js file with the following code: 
```
const { getDefaultConfig } = require("metro-config");
const { resolver: defaultResolver } = getDefaultConfig.getDefaultValues();
exports.resolver = {
  ...defaultResolver,
  sourceExts: [
    ...defaultResolver.sourceExts,
    "cjs",
  ],
};
```
- @apollo/react-hooks is deprecated, import from react-apollo for {useMutation, useQuery} instead