## Learning Data Structure and Algorithms.
This repository contains my practice lessons and implementations for learning data structures.

- [Day 1- Big O Notation](#day-1--big-o-notation)
  - [Time complexity](#time-complexity)
    - [O(1) - Constant Time Complexity](#o1---constant-time-complexity)
    - [O(n) - Linear Time Complexity](#on---linear-time-complexity)
    - [O(n^2) - Quadratic Time Complexity](#on2---quadratic-time-complexity)
  - [Space Complexity in JavaScript](#space-complexity-in-javascript)
    - [Constant Space Complexity (O(1))](#constant-space-complexity-o1)
    - [Linear Space Complexity (O(n))](#linear-space-complexity-on)
    - [Quadratic Space Complexity (O(n^k))](#quadratic--space-complexity-onk)


### Day 1- Big O Notation :
#### Time complexity 
Time complexity is a measure of how the running time of an algorithm grows as the input size increases.
common time complexities and their corresponding Big O notations in JavaScript:

#### O(1) - Constant Time Complexity:
 The running time of the algorithm remains constant, regardless of the input size. Examples include basic arithmetic operations, assignment, accessing an element in an array etc
 ``` 
const addTwo=(num)=>{
 Let sum=num+2
Return sum} 
addTwo(8)
 ```
In this example function requires same time for any name input. 

#### O(n) - Linear Time Complexity: 
The running time of the algorithm increases linearly with the input size. Examples include iterating over an array.
 ``` 
const myLoop=(arr){
for(let i=0;i<arr.length;i++){
console.log(arr[i])
}}
myLoop(["apple","orange",banana"])
```
In this example time required to run the " myLoop " function will increase when length of the array increases.
#### O(n^2) - Quadratic Time Complexity 
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

### Space Complexity in JavaScript

In JavaScript, space complexity refers to the amount of memory or storage required by an algorithm or data structure during its execution. It is typically measured in terms of the amount of memory used by the algorithm or data structure to store and manipulate data, and it can vary depending on the specific implementation and the size of the input data.

common space complexity scenarios in JavaScript:

##### Constant Space Complexity (O(1)):
 An algorithm or data structure has a constant space complexity if the amount of memory used does not depend on the size of the input data. For example, simple arithmetic operations, variable declarations, and assignment statements in JavaScript generally have constant space complexity because they use a fixed amount of memory regardless of the size of the input.
Example:
```
function add(a, b) {
  return a + b;
}
```
No matter how large the input numbers a and b are, the amount of memory used by the add function remains constant
##### Linear Space Complexity (O(n)):
 An algorithm or data structure has a linear space complexity if the amount of memory used increases linearly with the size of the input data. 
```
function sumArray(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}
```
In this example, if the input array arr has 5 elements, the function will use 5 units of memory to store the elements in the array, and the loop will iterate 5 times to calculate the sum. If the input array arr has 10 elements, the function will use 10 units of memory for the array elements, and the loop will iterate 10 times. 
##### Quadratic  Space Complexity (O(n^k)):
 An algorithm or data structure has a quadratic or polynomial space complexity if the amount of memory used increases with the size of the input data raised to some constant power. For example, nested arrays or matrices with n elements would have a quadratic or polynomial space complexity because the amount of memory used increases with the square or higher power of the number of elements in the data structure.
```
function generatePyramid(n) {
  const pyramid = [];
  for (let i = 0; i < n; i++) {
    pyramid[i] = [];
    for (let j = 0; j <= i; j++) {
      pyramid[i][j] = j + 1;
    }
  }
  return pyramid;
}

```
