# Frequency Counter Pattern

This pattern uses object or sets to collect values/frequencies of values.

Usually is **O(n)** 


```js
  
const sameRefactored = (array1, array2) => {  
  if (array1.length !== array2.length) {  
    return 'Not the same';  
  }  
  
  const frequencyCounter1 = {};  
  const frequencyCounter2 = {};  
  
  array1.forEach(el => {  
    frequencyCounter1[el] = (frequencyCounter1[el] || 0) + 1;  
  });  
  
  array2.forEach(el => {  
    frequencyCounter2[el] = (frequencyCounter2[el] || 0) + 1;  
  });  
  
  for (let key in frequencyCounter1) {  
    if (!(key ** 2 in frequencyCounter2)) {  
      return 'Not the same';  
    }  
    if (frequencyCounter2[key ** 2] !== frequencyCounter1[key]) {  
      return 'Not the same';  
    }  
  }  
  
  return true;  
};  
  
console.log(sameRefactored([1, 2, 4, 5, 5], [4, 1, 16, 25, 25]));
```


# Multiple pointers pattern

```js
// create a function that accepts a sorted array of ints.  
// Function should find the first pair where the sum is 0.  
// Return an array of those two numbers or undefined if such pair don't exist*/  
  
function sumZero(array) {  
  let leftIndex = 0;  
  let rightIndex = array.length - 1;  
  console.log(leftIndex, rightIndex);  
  
  while (leftIndex < rightIndex) {  
    let sum = array[leftIndex] + array[rightIndex];  
  
    if (sum === 0) {  
      return [array[leftIndex], array[rightIndex]];  
    } else if (sum > 0) {  
      rightIndex -= 1;  
    } else {  
      leftIndex += 1;  
    }  
  }  
}  
  
console.log(sumZero([-4, -3, -2, -1, 0, 1, 2, 3, 3, 5]));
```