### Create a function that takes two numbers as arguments and returns their sum.

```javascript 
function addition(a, b) {
	return a + b
}
addition(2,4);
```

### #2. Seven Boom
```javascript
function sevenBoom(arr) {
  let isSeven = ""
  // Iterate through array and convert to string
  arr.forEach(element =>{
    let strNum = element.toString()

    // Seperate string int into single digit
    let numSplit = strNum.split("")
    // Check if single digits contains '7'
    numSplit.forEach(number => {
      if(number == '7') {
      isSeven = "Boom!"
        console.log("boom")
    } else if(number != '7'){
        isSeven = "there is no 7 in the array";
    }
    })
  })
  console.log(isSeven);
}
sevenBoom([71, 61, 71, 91, 3]);
```
