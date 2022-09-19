_Box.js_
```js
import styled from 'styled-components';  
import { color, layout, typography, flexbox } from 'styled-system';  
  
export const Box = styled.div(  
  {    boxSizing: 'border-box',  
	    minWidth: 0,  
  },  
  color,  
  layout,  
  typography,  
  flexbox  
);
```

_App.js_
```js
import './App.css';  
import { Box } from 'components/Box';  
  
function App() {  
  return (  
    <Box as="main" bg="white" color="accent">  
      Hello  
    </Box>  
  );  
}  
  
export default App;
```