### Below is the solution to the 3x3 matrix puzzle. Using javascript, calculate the least number of steps required to solve the puzzle and print the solved puzzle. Input can be any combination of numbers from 1-9 placed in a 3x3 matrix. To solve the puzzle you can only interchange/ switch numbers and each switch is calculated as a step.

- [1,5,6]

- [3,2,7]

- [8,4,9]

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function calculateStepCount(initialMatrix, targetMatrix) {
  let steps = 0;
  for (let i = 0; i < 9; i++) {
    if (initialMatrix[Math.floor(i / 3)][i % 3] !== targetMatrix[Math.floor(i / 3)][i % 3]) {
      for (let j = i + 1; j < 9; j++) {
        if (initialMatrix[Math.floor(j / 3)][j % 3] === targetMatrix[Math.floor(i / 3)][i % 3]) {
          [initialMatrix[Math.floor(j / 3)][j % 3], initialMatrix[Math.floor(i / 3)][i % 3]] = [initialMatrix[Math.floor(i / 3)][i % 3], initialMatrix[Math.floor(j / 3)][j % 3]];
          steps++;
          break;
        }
      }
    }
  }
  return steps;
}

calculateStepCount([[1, 2, 3], [5, 4, 6], [7, 8, 9]], [[1, 2, 3], [4, 5, 6], [7, 8, 9]]);
```
