






## 01-03 Emotion

```bash
npm i @emotion/styled @emotion/react
```

```js
import styled from '@emotion/styled';  
  
export const Heading = styled.h1`  
	margin-top: 0;
	text-align: center;
	text-transform: uppercase;
	`;
```

To make set up a theme

-  `import { ThemeProvider } from 'styled-components';`

- wrap you **<App/>** with  **ThemeProvider**
- Pass the _theme_ object to it

```js
import { ThemeProvider } from 'styled-components';  
import { theme } from './theme';  
  
const root = ReactDOM.createRoot(document.getElementById('root'));  
root.render(  
  <React.StrictMode>  
    <ThemeProvider theme={theme}>  
      <App />  
    </ThemeProvider>  
  </React.StrictMode>  
);
```

- Create a file with a theme using theme spec, follow the namings strictly
[theme spec](https://theme-ui.com/theme-spec)

```js
export const theme = {  
  colors: {  
    black: '#000',  
    white: '#fff',  
    text: '#2a2a2a',  
    background: '#fff',  
    primary: '#07c',  
    secondary: '#05a',  
    accent: '#609',  
    muted: '#f6f6f6',  
  },  
  space: [0, 2, 4, 8, 16, 32, 64, 128, 256],  
  fonts: {  
    body: 'system-ui, sans-serif',  
    heading: 'system-ui, sans-serif',  
    monospace: 'Menlo, monospace',  
  },  
  fontSizes: {  
    xs: '12px',  
    s: '14px',  
    m: '16px',  
    l: '32px',  
    xl: '64px',  
  },  
  fontWeights: {  
    normal: 400,  
    bold: 700,  
  },  
  lineHeights: {  
    body: 1.5,  
    heading: 1.125,  
  },  
  borders: {  
    none: 'none',  
    normal: '1px solid',  
  },  
  radii: {  
    none: '0',  
    normal: '4px',  
    round: '50%',  
  },  
};
```

Using styled components are similar to Emotion

```js
import './App.css';  
import styled from 'styled-components';  
  
const Text = styled.p`  
  color: ${p => `${p.theme.colors.accent}`};  
  font-size: ${p => `${p.theme.fontSizes.l}`};  
  padding-top: ${p => `${p.theme.space[4]}px`};  
  padding-bottom: ${p => `${p.theme.space[4]}px`};  
`;  
  
function App() {  
  return (  
    <div className="App">  
      <Text>Text</Text>  
    </div>  
  );  
}  
  
export default App;
```


- You whole app now can use all the theme properties.

Example with Button styled component

```js
 import styled from 'styled-components';  
  
const StyledButton = styled.button`  
  display: block;  padding-top: ${p => `${p.theme.space[2]}px`};  
  padding-bottom: ${p => `${p.theme.space[2]}px`};  
  padding-left: ${p => `${p.theme.space[3]}px`};  
  padding-right: ${p => `${p.theme.space[3]}px`};  
  margin: ${p => `${p.theme.space[0]}`};  
  
  // example with disabled property styles on and off
  background-color: ${p =>  
    p.disabled ? p.theme.colors.muted : p.theme.colors.primary}; 
     
  border: ${p => p.theme.borders.none};  
  border-radius: ${p => p.theme.radii.normal};  
  color: ${p => p.theme.colors.white};  
  
  :hover:not(:disabled),  
  :focus:not(:disabled) {  
    cursor: pointer;    background-color: ${p => p.theme.colors.secondary};  
  }  
`;  
  
export const Button = ({ children, type = 'button', disabled = false }) => {  
  return (  
    <StyledButton disabled={disabled} type={type}>  
      {children}  
    </StyledButton>  
  );  
};
```

#styledsystem
[styled system](https://styled-system.com/) for reusable components