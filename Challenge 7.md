### Sunny and Johnny like to pool their money and go to the ice cream parlor. Johnny never buys the same flavor that Sunny does. The only other rule they have is that they spend all of their money.

### Given a list of prices for the flavors of ice cream, select the two that will cost all of the money they have.

### For example, they have m = 6 to spend and there are flavors costing cost = [1,3,4,5,6]. The two flavors costing 1 and 5 meet criteria. Using 1-based indexing, they are at indices 1 and 4.

<br>

#### **Function Description:**

#### Complete the icecreamParlor function in the editor below. It should return an array containing the indices of the prices of the two flavors they buy, sorted ascending.

#### **icecreamParlor has the following parameter(s):**

- m: an integer denoting the amount of money they have to spend.
- cost: an integer array denoting the cost of each flavor of ice cream.

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function icecreamParlor(m, cost) {
    for (var i = 0; i < cost.length; i++) {
        for (var j = i + 1; j < cost.length; j++) {
            if (cost[i] + cost[j] === m) {
                return [i + 1, j + 1];
            }
        }
    }
}
icecreamParlor(4,[6,3,5,1,2]);
```

### Sunny and Johnny like to pool their money and go to the ice cream parlor. Johnny never buys the same flavor that Sunny does. The only other rule they have is that they spend all of their money.

### Given a list of prices for the flavors of ice cream, select the two that will cost all of the money they have.

### For example, they have m = 6 to spend and there are flavors costing cost = [1,3,4,5,6]. The two flavors costing 1 and 5 meet criteria. Using 1-based indexing, they are at indices 1 and 4.

<br>

#### **Function Description:**

#### Complete the icecreamParlor function in the editor below. It should return an array containing the indices of the prices of the two flavors they buy, sorted ascending.

#### **icecreamParlor has the following parameter(s):**

- m: an integer denoting the amount of money they have to spend.
- cost: an integer array denoting the cost of each flavor of ice cream.

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function icecreamParlor(m, cost) {
    for (var i = 0; i < cost.length; i++) {
        for (var j = i + 1; j < cost.length; j++) {
            if (cost[i] + cost[j] === m) {
                return [i + 1, j + 1];
            }
        }
    }
}
icecreamParlor(4,[6,3,5,1,2]);
```
