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
### #3. Create a function that takes a number as an argument, increments the number by +1 and returns the result.
```javascript
function addition(num) {
	return num + 1;
}
addition(0)
```
### #4. Tower of Hanoi
https://edabit.com/challenge/3ZtykTsx3GSoPHyBb
solution(not solved yet)
```javascript
function towerHanoi(discs) {
  // size of discs with 3 at the bottom
  size = [1, 2, 3]
  // poles with first pole[0] holding all discs
  let poles = [size, 0 , 0]
  let min = Math.min
  // test methods
	console.log(`There are ${discs} discs in the game`)
  console.log(`There are ${poles.length} poles in the game`)
console.log(poles)
  // Moving the discs into the empty poles

 
  for(i = size.length; i >= 0; i--) {
  // Checking if poles are empty
    if(poles[i - 1] == 0) {
      console.log(`pole ${i} is empty`)
  // if empty move smallest disc to furthest pole..if poles[2](0) is less than 1 then move 1 to poles[2]
      if(poles[i-1] < min(...poles[0])) {
         poles[i - 1] = poles[0].splice(0,1)
        console.log(poles)
      }
    
    }  
    
  }
   if(poles[size.length - 1] != 0) {
      console.log('not empty')
    }
}
towerHanoi(3)

// need 7 steps to complete 3 discs moving to position three


// How would I represent the poles?
```
