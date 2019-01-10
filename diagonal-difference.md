# Diagonal Difference

Hacker Rank problem: https://www.hackerrank.com/challenges/diagonal-difference/problem

Given a square matrix, calculate the absolute difference between the sums of its diagonals. 

```js
function diagonalDifference(arr) {
    var LeftToRight = 0;
    var RightToLeft = 0;
    for (let i = 0; i < arr.length; i++) {
        LeftToRight += arr[i][i];
        RightToLeft += arr[i][Math.abs(i - (arr.length - 1))];
    }
    return Math.abs(LeftToRight - RightToLeft);
}
```

## Practical Application

The ability to solve this problem demonstrates the ability to work with multi-dimensional arrays. 

Ways this algorithm could be used: 
- pixel editing- [image kernels](http://setosa.io/ev/image-kernels/) images are often edited based on the pixels that surround them (their "neighborhood")
- computations related to coordinates (tracking objects in space) See: [Linear Algebra](https://en.wikipedia.org/wiki/Linear_algebra)
- 3-d graphics programming (https://en.wikipedia.org/wiki/Fundamental_matrix_(computer_vision)) - it allows a computer to add depth characteristic/perspective to a 2-d (flat) image. 
