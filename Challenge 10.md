### Monica wants to buy a keyboard and a USB drive from her favorite electronics store. The store has several models of each. Monica wants to spend as much as possible for the 2 items, given her budget.

### Given the price lists for the store's keyboards and USB drives, and Monica's budget, find and print the amount of money Monica will spend. If she doesn't have enough money to both a keyboard and a USB drive, print -1 instead. She will buy only the two required items.

### For example, suppose she has b = 60 to spend. Three types of keyboards cost keyboards = [40,50,60].Two USB drives cost drives = [5,8,12]. She could purchase a 40 keyboard + 12 USB drive = 52, or a 50 keyboard + 8 USB drive = 58. She chooses the latter. She can’t buy more than 2 items so she can't spend exactly 60.

<br>

#### **Function Description:**

#### Complete the getMoneySpent function in the editor below. It should return the maximum total price for the two items within Monica's budget, or -1 if she cannot afford both items.

#### **getMoneySpent has the following parameter(s):**

- keyboards: an array of integers representing keyboard prices
- drives: an array of integers representing drive prices
- b: the units of currency in Monica's budget

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function getMoneySpent(keyboards, drives, b) {
    let max_spend = -1;
    for (let i = 0; i < keyboards.length; i++) {
        for (let j = 0; j < drives.length; j++) {
            let total_price = keyboards[i] + drives[j];
            if (total_price <= b && total_price > max_spend) {
                max_spend = total_price;
            }
        }
    }
    return max_spend;
}

getMoneySpent([1, 2], [7, 6], 10);
```
