## React Navigation - Stack

A simple guide to implement navigation in your React Native app.

- `yarn add react-navigation`

- `yarn add react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view`

Run `pod install` in your `ios` folder

Create a `routes.js`
 
 - `yarn add @react-navigation/stack`

 Now add the navigation stack to the `routes.js`file

 ```js
import React from 'react';

import {NavigationContainer} from '@react-navigation/native';
import {createStackNavigator} from '@react-navigation/stack';

import Home from './pages/Home';

const Stack = createStackNavigator();

function Routes() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen
          name="Home"
          component={Home}
          options={{
            headerStyle: {
              backgroundColor: 'red',
            },
          }}
        />
      </Stack.Navigator>
    </NavigationContainer>
  );
}

export default Routes;
 ```

 Now in your `App.js`file you need to serve the navigation

 ```js
import React from 'react';

import 'react-native-gesture-handler';

import Routes from './routes';

const App: () => React$Node = () => {
  return <Routes />;
};

export default App;
 ```