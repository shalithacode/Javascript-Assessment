### HackerLand University has the following grading policy:

- Every student receives a grade in the inclusive range from 0 to 100.
- Any grade less than 40 is a failing grade.

### Sam is a professor at the university and likes to round each student's grade according to these rules:

### If the difference between the grade and the next multiple of 5 is less than 3, round grade up to the next multiple of 5.

### If the value of grade is less than 38, no rounding occurs as the result will still be a failing grade.

### For example, grade = 84 will be rounded to 85 but grade = 29 will not be rounded because the rounding would result in a number that is less than 40.

### Given the initial value of grade for each of Sam’s n students, write code to automate the rounding process.

<br>

#### **Function Description:**

#### Complete the function gradingStudents in the editor below. It should return an integer array consisting of rounded grades.

#### **gradingStudents has the following parameter(s):**

- grades: an array of integers representing grades before rounding

<br>

---

 <br>

## Solution 👇🏼

 <br>

```
function gradingStudents(grades) {
    let RdGrades = [];
    for (let i = 0; i < grades.length; i++) {
        if (grades[i] < 38) {
            RdGrades.push(grades[i]);
        } else {
            let nextMultiple = Math.ceil(grades[i] / 5) * 5;
            if (nextMultiple - grades[i] < 3) {
                RdGrades.push(nextMultiple);
            } else {
                RdGrades.push(grades[i]);
            }
        }
    }
    return RdGrades;
}


gradingStudents([73,67,38,37,33]);
```
