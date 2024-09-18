```
All methods I used/researched can be found at https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
```

## Return Negative

```js

// Using the 'sign method' from the Class Math, I can differentiate wether a number is zero, negative, or positive
// Then using the ternary operator, which is another way of writing an if-statement, I can return the disired results
function makeNegative(num) {
  return Math.sign(num) === 1 ? num * -1 : num
}
```

## Sum of Positive

```js

// Using the filter() I can create a new array depending the code I write between the parenthesis
// I also used the Math.sign() to only include positive numbers in my filter()
// With my new array I can use the reduce() to get the sum of the array starting at index 0
function positiveSum(arr) {
  let posNum = arr.filter(num => Math.sign(num) === 1)
  if(posNum.length) {
    return posNum.reduce((a,b)=>a+b, 0)
  } else {
    return 0
  }
}

```

## Function 2

```js

// Using the arrow function I can create a simple line of code where function will return the number squared
const square = (num) => num ** 2 

```

## Sum Arrays

```js

// Similar to the 'Sum of Positive', I will be using the reduce() to add the sum of the array.
// Using the ternary operator I check if the array is empty or not. Then return the desired result
function sum (numbers) {
  return numbers.length ? numbers.reduce((a,b) => a+b, 0) : 0
};

```

## Reversed Strings

```js

//In this solution I first split my string into an array using the split() making sure I do split('') so to separate each letter
//Then using a for-loop I have my 'i' start at the end of the split-letter-array and decrement down by 1
//Using push() I add the letter at position 'i' into a new array
//Finally using the join() I join the value and make the array into a string
function solution1(str){
    let splitArr = str.split('');
    let reverseArr = [];
    for(let i=splitArr.length-1; i>=0; i--) {
        reverseArr.push(splitArr[i])
    }
    return reverseArr.join('')
}

//This solution is cleaner as there is already a reverse()
//Taking advantage that you can string javascript methods together properly, the solution can be one line of code
function solution2(str){
  return str.split('').reverse().join('')
}

```
