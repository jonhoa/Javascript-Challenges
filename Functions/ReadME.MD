### #1.Create a function that takes two numbers as arguments and returns their sum.

```javascript 
function addition(a, b) {
	return a + b
}
addition(2,4);
```

### #2. Seven Boom
Create a function that takes an array of numbers and return "Boom!" if the digit 7 appears in the array. Otherwise, return "there is no 7 in the array".
```javascript 
sevenBoom([1, 2, 3, 4, 5, 6, 7]) ➞ "Boom!"
// 7 contains the number seven.

sevenBoom([8, 6, 33, 100]) ➞ "there is no 7 in the array"
// None of the items contain 7 within them.

sevenBoom([2, 55, 60, 97, 86]) ➞ "Boom!"
// 97 contains the number seven.
``` 
Solution:
```javascript
function sevenBoom(arr) {
  let isSeven = "there is no 7 in the array"
  // Iterate through array and convert to string
  arr.forEach(element =>{
    let strNum = element.toString()

    // Seperate string int into single digit
    let numSplit = strNum.split("")
    // Check if single digits contains '7'
    numSplit.forEach(number => {
      if(number == '7') {
      isSeven = "Boom!"
    }
    })
  })
  return isSeven;
}
sevenBoom([01, 61, 1, 91, 3])
```
