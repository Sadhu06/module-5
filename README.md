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
```
#include <stdio.h>

int main() 
{
    float length, breadth, area;
    float *x, *y;
    x = &length;
    y = &breadth;
    scanf("%f", x);  
    scanf("%f", y);  
    area = (*x) * (*y);
    printf("Area of the rectangle = %.2f\n", area);
    return 0;
}
```
## OUTPUT
		       	
![Screenshot 2025-05-28 142118](https://github.com/user-attachments/assets/8d555f36-6847-44af-9b47-f71e7ce43ad7)


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
```
#include <stdio.h>
#include <stdlib.h>  

int main() 
{
    char *str;
    str = (char *)malloc(8 * sizeof(char));
    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;  
    }
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0';  
    printf("The string is: %s\n", str);
    free(str);
    return 0;
}
```

## OUTPUT

![Screenshot 2025-05-28 142435](https://github.com/user-attachments/assets/dfb1da2a-10b7-41c4-b0c5-e7de5e637357)


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
```
#include <stdio.h>
struct Student {
    char name[50];
    int rollNumber;
    float marks;
};

int main() 
{
    struct Student s;
    scanf("%s", s.name);  
    scanf("%d", &s.rollNumber);
    scanf("%f", &s.marks);
    printf("Student Information\n");
    printf("Name       : %s\n", s.name);
    printf("Roll Number: %d\n", s.rollNumber);
    printf("Marks      : %.2f\n", s.marks);
    return 0;
}
```

## OUTPUT

![Screenshot 2025-05-28 142738](https://github.com/user-attachments/assets/3a17594c-a8b9-482a-9be8-cf98b89ff1c9)


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
```
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basicSalary;
    float grossSalary;
};

int main() 
{
    struct Employee emp[3];
    for (int i = 0; i < 3; i++) {
        scanf("%s", emp[i].name);  
        scanf("%d", &emp[i].id);
        scanf("%f", &emp[i].basicSalary);
        float hra = 0.20f * emp[i].basicSalary;
        float da = 0.10f * emp[i].basicSalary;
        emp[i].grossSalary = emp[i].basicSalary + hra + da;
    }
    printf("Employee Details\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d\n", i + 1);
        printf("Name        : %s\n", emp[i].name);
        printf("ID          : %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basicSalary);
        printf("Gross Salary: %.2f\n", emp[i].grossSalary);
    }
    return 0;
}
```


 ## OUTPUT

 ![Screenshot 2025-05-28 143311](https://github.com/user-attachments/assets/175ac6fc-5008-4290-a031-b962828726b9)


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
```
#include <stdio.h>
struct student {
    int subject[5];
    int total;
};
int main() 
{
    struct student s[2];
    int i, j;
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        printf("%d:\n", i + 1);
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }
    }
    for (i = 0; i < 2; i++) {
        printf("\nStudent %d Total = %d, Average = %.2f\n", 
               i + 1, s[i].total, s[i].total / 5.0);
    }
    return 0;
}
```


## OUTPUT

 ![Screenshot 2025-05-28 144145](https://github.com/user-attachments/assets/abe621cc-6956-433f-8fe0-90df244bcf4b)


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


