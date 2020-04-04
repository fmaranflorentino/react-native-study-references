## React Native - styled components

- `yarn add styled-components`

In your page folder create `styles.js`

```js
import styled from 'styled-components/native';

export const Container = styled.View`
  flex: 1;
  padding: 30px;
`;
```

In your page `index.js` import the styled-component

```js
import { Container } from './styles';
```