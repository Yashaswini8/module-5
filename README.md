# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM:
#include <stdio.h>
int main() {
    float length = 5.0, width = 3.0;
    float *ptr_length = &length, *ptr_width = &width;
    float area;
    area = (*ptr_length) * (*ptr_width);
    printf("The area of the rectangle is: %.2f\n", area);
 return 0;
}
## OUTPUT
![Screenshot 2025-04-28 203105](https://github.com/user-attachments/assets/821ccbdf-5190-4a9d-ad37-bfd0bd328279)
		       	


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
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *str;
    str = (char *)malloc(8 * sizeof(char));
if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }
    sprintf(str, "WELCOME");
    printf("%s\n", str);
    free(str);

return 0;
}
## OUTPUT

![Screenshot 2025-04-28 203240](https://github.com/user-attachments/assets/a17af464-5a81-450d-a695-a503f88cf2e2)


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
#include <stdio.h>

struct student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    struct student s;
    printf("Enter student name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.roll_no);
    printf("Enter marks: ");
    scanf("%f", &s.marks);
    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll_no);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}

## OUTPUT
![Screenshot 2025-04-28 203342](https://github.com/user-attachments/assets/b5c3d8c4-c412-4946-9d6c-7c406c66dfaf)


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
#include <stdio.h>

struct employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct employee emp[3];
    for (int i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d\n", i + 1);
        printf("Enter name: ");
        scanf("%s", emp[i].name);
        printf("Enter ID: ");
        scanf("%d", &emp[i].id);
        printf("Enter basic salary: ");
        scanf("%f", &emp[i].basic_salary);
        emp[i].gross_salary = emp[i].basic_salary + (emp[i].basic_salary * 0.20);  // 20% increment
        printf("\nEmployee %d Details:\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }

  return 0;
}

 ## OUTPUT
![Screenshot 2025-04-28 203616](https://github.com/user-attachments/assets/7a0fb4a6-d463-4ea9-91d8-cbfa971fb5f6)

 

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
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};

int main() {
    struct student s[2] = {
        {"John", 101, {80, 85, 90, 70, 88}, 0, 0.0},
        {"Alice", 102, {75, 80, 65, 95, 90}, 0, 0.0}
    };
    for (int i = 0; i < 2; i++) {
        s[i].total = 0;
        for (int j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }
    printf("\nTotal and Average Marks for Each Student:\n");
    for (int i = 0; i < 2; i++) {
        printf("\nStudent %d:\n", i + 1);
        printf("Name: %s\n", s[i].name);
        printf("Roll No: %d\n", s[i].rollno);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", s[i].average);
    }

 return 0;
}

## OUTPUT
![Screenshot 2025-04-28 203817](https://github.com/user-attachments/assets/6bd7d587-227a-4bf9-bfe2-d44030c8ad94)

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


