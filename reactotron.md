## React Native - Reactottron Configuration

- `yarn add reactotron-react-native reactotron-redux reactotron-redux-saga redux redux-saga react-redux`

In your soucer folder create `config/ReactotronConfig.js`

```js
import Reactotron from "reactotron-react-native";
import { reactotronRedux } from "reactotron-redux";
import reactotronSaga from "reactotron-redux-saga";

if (__DEV__) {
  const tron = Reactotron.configure()
    .useReactNative()
    .use(reactotronRedux())
    .use(reactotronSaga())
    .connect();

  tron.clear();

  console.tron = tron;
}
```

In your app index.js import the reactotronConfig

```js
import '~/config/ReactotronConfig';
```
