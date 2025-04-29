# Ex5 Stack Operations
## DATE:28-4-2025
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1.First Start scanning the expression from left to right.
2.If the scanned character is an operand, output it, i.e. print it.
3.Else. ...
4.If the scanned character is an '(', push it to the stack.
5.If the scanned character is an ')', pop the stack and output it until a '(' is encountered, and discard both the parenthesis. 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by:Divya R V 
RegisterNumber:212223100005  
*/
```
```
#include<stdio.h>

char stack[100];
int top = -1;

void push(char x)
{
   if (top >= 99) {  // Stack overflow check
        printf("Stack overflow\n");
        return;
    }
    stack[++top] = x;
}

char pop()
{
   if (top == -1) {  // Stack underflow check
        printf("Stack underflow\n");
        return '\0';  // Return null character if stack is empty
    }
    return stack[top--]; 
}
```
## Output:

![Screenshot 2025-04-29 090410](https://github.com/user-attachments/assets/07ca4f22-52a2-4e6a-9f8c-408cda0cefd0)


## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
