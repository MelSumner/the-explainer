# Min-Max Sum

## Task
Given five positive integers, find the minimum and maximum values that can be calculated by summing exactly four of the five integers. Then print the respective minimum and maximum values as a single line of two space-separated long integers.


## Code

```js
function miniMaxSum(arr) {
    // Set the number of elements to sum
    let numElementsToSum = 4;

    // Declare the array for the minimum
    let miniSum = 0;

    // Declare the array for the maximum
    let maxSum = 0;

    // Sort the array
    // First 4 indices: smallest values, 
    // Last 4 indices: largest
    arr.sort();

    for (let ii = 0; ii < numElementsToSum; ii++) {
        miniSum += arr[ii];
    }

    for (let jj = (arr.length - numElementsToSum); jj < arr.length; jj++) {
        maxSum += arr[jj];
    }

    console.log(miniSum + ' ' + maxSum);
}

```

## Ok but why?!
This demonstrates the ability to work with data sets to calculate values that might be desired for analysis. 

## Practical Application(s)
- this could be used as part of a larger data analysis. Example: calculating the top N salary vs the bottom N salary. 

## Reference
Hacker Rank problem: https://www.hackerrank.com/challenges/mini-max-sum/problem
