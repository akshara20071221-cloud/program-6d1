# program-6d
# 🧪 C Programming Lab
## 📘 Experiment No: 6d
### 🔹
**Date:** 19/3/2026  
**Name:** AKshara.k 
**Register No:** 25003090 

---

## 🎯 AIM
Create a structure program to read(rego,3 subject markss) and store the details of 5 students and calculate the Total and Average
---

## 🧠 ALGORITHM
Define a structure Student with members: • regno (integer) • marks[3] (array for 3 subject marks) • total and average (float) Declare an array of 5 Student structures. For each student: • Read register number and marks for 3 subjects. • Calculate total = sum of marks. • Calculate average = total / 3. Display each student’s details, total, and average.
---

## 💻 PROGRAM
```
#include <stdio.h>

struct Student {
    int regno;
    float marks[3];
    float total;
    float average;
};

int main() {
    struct Student s[5];
    int i, j;

    // Read details of 5 students
    for (i = 0; i < 5; i++) {
        printf("\nEnter details of Student %d\n", i + 1);
        printf("Enter Register Number: ");
        scanf("%d", &s[i].regno);

        s[i].total = 0;
        for (j = 0; j < 3; j++) {
            printf("Enter mark for subject %d: ", j + 1);
            scanf("%f", &s[i].marks[j]);
            s[i].total += s[i].marks[j];
        }

        s[i].average = s[i].total / 3.0;
    }

    // Display results
    printf("\n--------------------------------------------\n");
    printf("RegNo\tSub1\tSub2\tSub3\tTotal\tAverage\n");
    printf("--------------------------------------------\n");

    for (i = 0; i < 5; i++) {
        printf("%d\t", s[i].regno);
        for (j = 0; j < 3; j++) {
            printf("%.1f\t", s[i].marks[j]);
        }
        printf("%.1f\t%.2f\n", s[i].total, s[i].average);
    }

    return 0;
}
```

## 🖼️ OUTPUT SCREENSHOT


<img width="568" height="802" alt="image" src="https://github.com/user-attachments/assets/404e2bb9-59fd-49ee-bac4-f7a2caab5bab" />


---

## ✅ RESULT
Thus the C program to store the student information and display it using structure is executed successfully.
