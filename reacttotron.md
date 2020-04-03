## Reactotron

A simple guide to configure Reacttotron in your React Native app.

- `yarn add reactotron-react-native`

In your `config` folder create a `ReactotronConfig.js` file with the followinf content

```js
import Reactotron from 'reactotron-react-native';

if (__DEV__) {
  const tron = Reactotron.configure().useReactNative().connect();

  console.tron = tron;

  tron.clear();
}
```


In your `App.js` import the `ReactotronConfig.js`

```js
import './config/ReactotronConfig';
```

And it's done!