With single char
```js
function isAlphaNumeric(char) {  
  const code = char.charCodeAt(0);  
  return !(  
    !(code > 47 && code < 58) &&  
    !(code > 64 && code < 91) &&  
    !(code > 96 && code < 123)  
  );  
}
```


with string
```js
function isAlphaNumeric(str) {
  var code, i, len;

  for (i = 0, len = str.length; i < len; i++) {
    code = str.charCodeAt(i);
    if (!(code > 47 && code < 58) && // numeric (0-9)
        !(code > 64 && code < 91) && // upper alpha (A-Z)
        !(code > 96 && code < 123)) { // lower alpha (a-z)
      return false;
    }
  }
  return true;
};

```