```js
// ==================================== Second iteration, refactored ================================  
{  
  str1 = 'ieaiaio';  
  str2 = 'ieaiaio';  
  
  class AnagramValidator {  
    static isAnagram = (word01, word02) => {  
      // we will populate this objects with counts for each letter  
      const lookup = {};  
  
      // short circuit  
      if (word01.length !== word02.length) {  
        return false;  
      }  
  
      // populating 'lookup' object  
      [...word01].forEach(letter => {  
        lookup[letter] ? (lookup[letter] += 1) : (lookup[letter] = 1);  
      });  
  
      // Now we simply compare if we have a particular amount of letters from word02 in our "lookup" object from word01  
      for (let letter of word02) {  
        if (!lookup[letter]) {  
          return false;  
        } else {  
          lookup[letter] -= 1;  
        }  
      }  
  
      return true;  
    };  
  }  
  
  isAnagram = AnagramValidator.isAnagram(str1, str2);  
  console.log(isAnagram);  
}
```