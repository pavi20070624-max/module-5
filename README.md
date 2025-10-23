# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

int main() {
    float length, breadth, area;
    float *ptr1, *ptr2;

    // Assign addresses to pointers
    ptr1 = &length;
    ptr2 = &breadth;

    // Input length and breadth
    printf("Enter the length of the rectangle: ");
    scanf("%f", ptr1);

    printf("Enter the breadth of the rectangle: ");
    scanf("%f", ptr2);

    // Calculate area using pointer dereferencing
    area = (*ptr1) * (*ptr2);

    // Display result
    printf("Area of the rectangle = %.2f\n", area);

    return 0;
}
```
## OUTPUT
		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```c
#include <stdio.h>
#include <stdlib.h>   // for malloc() and free()

int main() {
    char *str;

    // Allocate memory for the string "WELCOME"
    str = (char *)malloc(8 * sizeof(char));  // 7 letters + 1 for '\0'

    if (str == NULL) {  // Always check if malloc succeeded
        printf("Memory allocation failed!\n");
        return 1;
    }

    // Store the string in allocated memory
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0';  // null terminator for string end

    // Print the string
    printf("%s\n", str);

    // Free allocated memory
    free(str);

    return 0;
}
```

## OUTPUT



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

// Define structure for student
struct Student {
    int roll_no;
    char name[50];
    float marks;
};

int main() {
    struct Student s1;  // Declare a structure variable

    // Input student details
    printf("Enter student roll number: ");
    scanf("%d", &s1.roll_no);

    printf("Enter student name: ");
    scanf("%s", s1.name);  // no '&' needed for string

    printf("Enter student marks: ");
    scanf("%f", &s1.marks);

    // Display student details
    printf("\n--- Student Information ---\n");
    printf("Roll Number : %d\n", s1.roll_no);
    printf("Name        : %s\n", s1.name);
    printf("Marks       : %.2f\n", s1.marks);

    return 0;
}
```


## OUTPUT


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```c
#include <stdio.h>

// Define a structure for employee
struct Employee {
    int emp_id;
    char name[50];
    float basic, hra, da, gross;
};

int main() {
    struct Employee e[3]; // Array of 3 employees
    int i;

    // Read details of 3 employees
    for (i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);

        printf("Enter Employee ID: ");
        scanf("%d", &e[i].emp_id);

        printf("Enter Employee Name: ");
        scanf("%s", e[i].name);

        printf("Enter Basic Salary: ");
        scanf("%f", &e[i].basic);

        printf("Enter HRA: ");
        scanf("%f", &e[i].hra);

        printf("Enter DA: ");
        scanf("%f", &e[i].da);

        // Calculate Gross Salary
        e[i].gross = e[i].basic + e[i].hra + e[i].da;
    }

    // Display employee details
    printf("\n--- Employee Salary Details ---\n");
    for (i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("ID           : %d\n", e[i].emp_id);
        printf("Name         : %s\n", e[i].name);
        printf("Basic Salary : %.2f\n", e[i].basic);
        printf("HRA          : %.2f\n", e[i].hra);
        printf("DA           : %.2f\n", e[i].da);
        printf("Gross Salary : %.2f\n", e[i].gross);
    }

    return 0;
}
```


 ## OUTPUT

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```c
#include <stdio.h>

// Define structure for student
struct Student {
    int roll_no;
    char name[50];
    float marks1, marks2, marks3; // three subjects
    float total;
    float average;
};

int main() {
    struct Student s;

    // Read student details
    printf("Enter student roll number: ");
    scanf("%d", &s.roll_no);

    printf("Enter student name: ");
    scanf("%s", s.name);

    printf("Enter marks in 3 subjects: ");
    scanf("%f %f %f", &s.marks1, &s.marks2, &s.marks3);

    // Calculate total and average
    s.total = s.marks1 + s.marks2 + s.marks3;
    s.average = s.total / 3;

    // Display result
    printf("\n--- Student Details ---\n");
    printf("Roll Number : %d\n", s.roll_no);
    printf("Name        : %s\n", s.name);
    printf("Total Marks : %.2f\n", s.total);
    printf("Average     : %.2f\n", s.average);

    return 0;
}
```

## OUTPUT

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


