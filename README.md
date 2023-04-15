## Learning Data Structure and Algorithms.
This repository contains my practice lessons and implementations for learning data structures.
### Day 1- Big O Notation :
#### Time complexity 
Time complexity is a measure of how the running time of an algorithm grows as the input size increases.
Here are some common time complexities and their corresponding Big O notations in JavaScript:

<b> O(1) - Constant Time Complexity:</b>
 The running time of the algorithm remains constant, regardless of the input size. Examples include basic arithmetic operations, assignment, accessing an element in an array etc
 ``` 
const displayName=(name)=>{
 console.log(name) } 
displayName("john doe")
 ```
In this example function requires same time for any name input. 

<b> O(n) - Linear Time Complexity: </b> The running time of the algorithm increases linearly with the input size. Examples include iterating over an array.
 ``` 
const myLoop=(arr){
for(let i=0;i<arr.length;i++){
console.log(arr[i])
}}
myLoop(["apple","orange",banana"])
```
In this example time required to run the " myLoop " function will increase when length of the array increases.
<br><b> O(n^2) - Quadratic Time Complexity:</b> 
The running time of the algorithm increases quadratically with the input size. Examples include nested loops that iterate over a 2D array.

```

function concatenateStrings(arr) {
  let result = "";

  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      result += arr[i] + arr[j];
    }
  }

  return result;
}

const input = ["a", "b", "c"];
const concatenated = concatenateStrings(input);
console.log(`Concatenated String:`, concatenated);
```
