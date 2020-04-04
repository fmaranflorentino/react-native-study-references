## React Native - StatusBar

A simple example of StatusBar configuration. 

In your `App.js` add the following code

```js
import React from 'react';
import {StatusBar} from 'react-native';

import 'react-native-gesture-handler';

import Routes from './routes';

const App: () => React$Node = () => {
  return (
    <>
      <StatusBar barStyle="light-content" backgroundColor="#7159c1" />
      <Routes />
    </>
  );
};

export default App;
```