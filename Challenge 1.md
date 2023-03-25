### A salesperson who walks door to door to sell goods carries a suitcase with him. Each morning he packs his suitcase with items from his inventory. Each item has a size (cm3), price (Rs) and weight (grams). Write a javascript programme to calculate the total price of the items he can carry in his suitcase without exceeding the max weight and size limits of the suitcase.

### Products list:

- Item 01: weight: 10, price: 20, size: 30
- Item 02: weight: 15, price: 25, size: 35
- Item 03: weight: 20, price: 30, size: 40
- Item 04: weight: 25, price: 35, size: 40

<br>

### **Test 01**

#### Inputs: maxWeight = 50, maxSize = 50

#### Expected Output: Total price: 35

<br>

### **Test 02**

#### Inputs: maxWeight = 30, maxSize = 100

#### Expected Output: Total price: 50

 <br>

---

 <br>

## Solution 👇🏼

 <br>

```
function getTotalPrice(items, curWeight, curSize, curIndex) {
  return false;
}
const itemList = [
  { weight: 10, price: 20, size: 30 },
  { weight: 15, price: 25, size: 35 },
  { weight: 20, price: 30, size: 40 },
  { weight: 25, price: 35, size: 40 },
];

getTotalPrice(itemList, 50, 50, itemList.length);
```
