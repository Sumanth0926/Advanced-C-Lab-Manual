EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

    #include <stdio.h>
    
    int main() {
        int num;

    printf("Enter a number between 1 and 9: ");
    scanf("%d", &num);
    switch(num) {
        case 1: printf("one\n"); break;
        case 2: printf("two\n"); break;
        case 3: printf("three\n"); break;
        case 4: printf("four\n"); break;
        case 5: printf("five\n"); break;
        case 6: printf("six\n"); break;
        case 7: printf("seven\n"); break;
        case 8: printf("eight\n"); break;
        case 9: printf("nine\n"); break;
        default: printf("Number out of range! Please enter a number between 1 and 9.\n");
    }

    return 0;
}





Output:


    Enter a number between 1 and 9: 3
    three









Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:



    #include <stdio.h>
    
    int main() {
        int num;
        int count[4] = {0}; 
    
    
    printf("Enter an integer: ");
    scanf("%d", &num);
    while (num != 0) {
        int digit = num % 10; // Extract the last digit
        if (digit >= 0 && digit <= 3) {
            count[digit]++; // Increment the count of that digit
        }
        num /= 10; 
    }

    for (int i = 0; i < 4; i++) {
        printf("%d ", count[i]);
    }

    return 0;
}





Output:


    Enter an integer: 123312
    2 2 2 2 







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

    #include <stdio.h>
    #include <string.h>
    #include <stdlib.h>
    
    int compare(const void *a, const void *b) {
        return (*(char *)a - *(char *)b);
    }
    
    int next_permutation(char str[], int length) {
        int i = length - 2;
        while (i >= 0 && str[i] >= str[i + 1]) i--;
        if (i < 0) return 0;
        int j = length - 1;
        while (str[j] <= str[i]) j--;
        char temp = str[i];
        str[i] = str[j];
        str[j] = temp;
        int left = i + 1, right = length - 1;
        while (left < right) {
            temp = str[left];
            str[left] = str[right];
            str[right] = temp;
            left++;
            right--;
        }
        return 1;
    }
    
    void printPermutations(char str[]) {
        qsort(str, strlen(str), sizeof(char), compare);
        do {
            printf("%s\n", str);
        } while (next_permutation(str, strlen(str)));
    }
    
    int main() {
        char str[100];
        printf("Enter a string: ");
        scanf("%s", str);
        printPermutations(str);
        return 0;
    }





Output:


    Enter a string: abc
    abc
    acb
    bac
    bca
    cab
    cba







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

    #include <stdio.h>
    
    int main() {
        int n;
        printf("Enter a number: ");
        scanf("%d", &n);

    for (int i = 1; i <= n; i++) {  
        for (int j = 1; j <= i; j++) {  
            printf("%d", j);
        }
        printf("\n");  
    }

    return 0;
}





Output:


    1
    12
    123
    1234
    12345







Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:


    #include <stdio.h>
    int square() {
        int num = 5;  // Predefined number for which we need the square
        return num * num; 
    }
    
    int main() {
        int result = square();
        printf("The square of the number is: %d\n", result);
        return 0;
    }





Output:





    The square of the number is: 25




Result:
Thus, the program is verified successfully



























