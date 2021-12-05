---
title: Nested Lists
published: true
---

### Question:

Given the names and grades for each student in a class of _N_ students, store them in a nested list and print the name(s) of any student(s) having the second lowest grade.

**Note**: If there are multiple students with the second lowest grade, order their names alphabetically and print each name on a new line.


**Input Format**

The first line contains an integer, _N_, the number of students.
The _2N_ subsequent lines describe each student over lines.
- The first line contains a student's name.
- The second line contains their grade. 

**Output Format**

Print the name(s) of any student(s) having the second lowest grade in. If there are multiple students, order their names alphabetically and print each one on a new line.


### Python Solution:

```python
if __name__ == '__main__':
    records=[]
    scores=[]
    
    for _ in range(int(input())):
        name = input()
        score = float(input())
        
        records.append([name,score])
        scores.append(score)
    
    second_lowest_grade = sorted(set(scores), reverse=False)[1];
    students_second_lowest_grade=sorted([record[0] for record in records 
        if (record[1] == second_lowest_grade)])    
    print("\n".join(students_second_lowest_grade))
```

Source: HackerRank