```js
const generateColor = () => {
return Math.floor(Math.random()*16777215).toString(16);

```

or

```js
export function getRandomHexColor() {  
  return `#${Math.floor(Math.random() * 16777215)  
    .toString(16)  
    .padStart(6)}`;  
}
```