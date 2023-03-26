### Sami's spaceship crashed on Mars! She sends a series of SOS messages to Earth for help.

### Letters in some of the SOS messages are altered by cosmic radiation during transmission. Given the signal received by Earth as a string, s, determine how many letters of Sami's SOS have been changed by radiation.

### For example, Earth receives SOSTOT. Sami's original message was SOSSOS. Two of the message characters were changed in transit.

<br>

#### **Function Description:**

#### Complete the marsExploration function in the editor below. It should return an integer representing the number of letters changed during transmission.

#### **marsExploration has the following parameter(s):**

- s: the string as received on Earth

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function marsExploration(s) {
    let count = 0;
    let goal = "SOS";
    for (let i = 0; i < s.length; i++) {
        if (s[i] !== goal[i % 3]) {
            count++;
        }
    }
    return count;
}
marsExploration("SOSSOT");
```
