# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. Scan the expression
2. Identify operators and their precedence
3. Evaluate within parentheses
4. Apply precedence and associativity 
5. Repeat until complete  

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: 
RegisterNumber:  
*/
```
```
#include <stdio.h>
#include<string.h>

 /* Hint:
 int priority(char x)
{
 switch (x) {
        case '%':
        case '*': return 3; // Second highest priority
        case '-':
        case '+': return 2; // Second lowest priority
        case '^': return 4; // Highest priority
        default: return 0; // Ignore non-operator characters
    }
} Hint */

int main()
{
  char expression[] = "K%L-M*N+(O^P)";
    int i, j;
    
 
    
    for (i = 0; expression[i] != '\0'; i++) {
        if (expression[i] == '%' || expression[i] == '-' || expression[i] == '*' || expression[i] == '+' || expression[i] == '^') {
            j = priority(expression[i]);
            printf("%c  ----> ", expression[i]);
            switch (j) {
                case 2: printf("Second Lowest Priority\n"); break;
                case 3: printf("Second Highest Priority\n"); break;
                case 4: printf("Highest Priority\n"); break;
            }
        }
    }
    return 0;
   
}
   
```

## Output:

![Screenshot 2025-04-29 084926](https://github.com/user-attachments/assets/c016bcd3-7281-4280-9931-8fb565bbc394)


## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
