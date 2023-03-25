### Dothraki are planning an attack to usurp King Robert's throne. King Robert learns of this conspiracy from Raven and plans to lock the single door through which the enemy can enter his kingdom.

### But, to lock the door he needs a key that is an anagram of a palindrome. He starts to go through his box of strings, checking to see if they can be rearranged into a palindrome.

### For example, given the string s = [aabbccdd], one way it can be arranged into a palindrome is abcddcba.

<br>

#### **\*Function Description:**

#### Complete the gameOfThrones function below to determine whether a given string can be rearranged into a palindrome. If it is possible, return YES, otherwise return NO.

#### **gameOfThrones has the following parameter(s):**

- s: a string to analyze

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function gameOfThrones(s) {
  var map = {};
  var count = 0;
  for (var i = 0; i < s.length; i++) {
    if (!map[s[i]]) {
      map[s[i]] = 1;
    } else {
      map[s[i]]++;
    }
  }
  for (var key in map) {
    if (map[key] % 2 !== 0) {
      count++;
    }
  }
  return count <= 1 ? "YES" : "NO";
}


  gameOfThrones('aaabbbb');
```
