### Roy wanted to increase his typing speed for programming contests. His friend suggested that he type the sentence "The quick brown fox jumps over the lazy dog" repeatedly. This sentence is known as a pangram because it contains every letter of the alphabet.

### After typing the sentence several times, Roy became bored with it so he started to look for other pangrams.

### For example, Earth receives SOSTOT. Sami's original message was SOSSOS. Two of the message characters were changed in transit.

### Given a sentence, determine whether it is a pangram. Ignore case.

<br>

#### **Function Description:**

#### Complete the function pangrams in the editor below. It should return the string pangram if the input string is a pangram. Otherwise, it should return not pangram.

#### **pangrams has the following parameter(s):**

- s: a string to test

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function pangrams(s) {
  s = s.toLowerCase();
  var letters = "abcdefghijklmnopqrstuvwxyz";
  for (var i = 0; i < letters.length; i++) {
    if (s.indexOf(letters[i]) === -1) {
      return "not pangram";
    }
  }
  return "pangram";
}
pangrams("We promptly judged antique ivory buckles for the next prize");
```
