### Karl has an array of integers. He wants to reduce the array until all remaining elements are equal. Determine the minimum number of elements to delete to reach his goal.

### For example, if his array is arr = [1,2,2,3], we see that he can delete the 2 element 1 and 3 leaving arr = [2,2]. He could also delete both twos and either the 1 or the 3, but that would take 3 deletions. The minimum number of deletions is 2.

<br>

#### **Function Description:**

#### Complete the equalizeArray function in the editor below. It must return an integer that denotes the minimum number of deletions required.

#### **equalizeArray has the following parameter(s):**

- arr: an array of integers

<br>

---

 <br>

## Solution 👇🏼

 <br>

```

function equalizeArray(arr) {
    var map = {};
    var max = 0;
    for (var i = 0; i < arr.length; i++) {
        if (!map[arr[i]]) {
            map[arr[i]] = 1;
        } else {
            map[arr[i]]++;
        }
        max = Math.max(max, map[arr[i]]);
    }
    return arr.length - max;
}
equalizeArray([3, 3, 2, 1, 3]);
```
