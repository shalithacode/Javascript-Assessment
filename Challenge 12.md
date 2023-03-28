### Given an array of integers, find and print the maximum number of integers you can select from the array such that the absolute difference between any two of the chosen integers is less than or equal to 1. For example, if your array is a = [1,1,2,2,4,4,5,5,5], you can create two subarrays meeting the criterion: [1,1,2,2] and [4,4,5,5,5]. The maximum length subarray has 5 elements.

<br>

#### **Function Description:**

#### Complete the pickingNumbers function in the editor below. It should return an integer that represents

#### the length of the longest array that can be created.

#### **pickingNumbers has the following parameter(s):**

- a: an array of integers.
  <br>

---

 <br>

## Solution 👇🏼

 <br>

```
function pickingNumbers(a) {
    a.sort((a, b) => a - b);
    let Mlen = 0;
    for (let i = 0; i < a.length; i++) {
        let count = 1;
        for (let j = i + 1; j < a.length; j++) {
            if (Math.abs(a[i] - a[j]) <= 1) {
                count++;
            } else {
                break;
            }
        }
        Mlen = Math.max(Mlen, count);
    }
    return Mlen;
}

pickingNumbers([1, 2, 2, 3, 1, 2]);
```
