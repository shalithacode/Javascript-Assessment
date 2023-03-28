### Given a set of distinct integers, print the size of a maximal subset of S where the sum of any 2 numbers in s’ is not evenly divisible by k.

### For example, the array s = [19,10,12,10,24,25,22] and k = 4. One of the arrays that can be created is S’[0] = [10,12,25]. Another is S’[1] = [19,22,24]. After testing all permutations, the maximum length solution array has 3 elements.

<br>

#### **Function Description:**

#### Complete the nonDivisibleSubset function in the editor below. It should return an integer representing the length of the longest subset of S meeting the criteria.

#### **nonDivisibleSubset has the following parameter(s):**

- S: an array of integers
- k: an integer

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function nonDivisibleSubset(k, s){
   let remainders = s.map(function (x) {
    return x % k;
  });

  let freqCount = Array(k).fill(0);
  for (let i = 0; i < remainders.length; i++) {
    freqCount[remainders[i]]++;
  }

  var subset = 0;
  for (let i = 0; i <= k / 2; i++) {
    if (i == 0 || i == k / 2) {
      subset += freqCount[i] > 0 ? 1 : 0;
    } else {
      subset += Math.max(freqCount[i], freqCount[k - i]);
    }
  }
  return subset;
}

nonDivisibleSubset(4, [19,10,12,10,24,25,22]);
```
