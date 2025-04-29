# Ex4 Evaluation of prefix expression
## DATE:28-4-2025
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1.Initialization 
2.Scan Right-to-Left 
3. Operand Found
4. Operator Found 
5.Perform Operation and Push   

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: Divya R V
RegisterNumber:212223100005  
*/
```
```
#include<stdio.h>
#include<string.h>
#include<ctype.h>

int s[50];
int top=0;

void push(int ch)
{
	top++;
	s[top]=ch;
}

int pop()
{
	int ch;
	ch=s[top];
	top=top-1;
	return(ch);
}

void evalprefix(char p[50])
{
  int a,b,c,i;
  for(i=strlen(p)-1;i>=0;i--)
  {
      if(p[i]=='+')
      {
          c=pop()+pop();
          push(c);
      }
      else if(p[i]=='/')
      {
         a=pop();
         b=pop();
         c=a/b;
         push(c);

      }
      else
      {
          push(p[i]-48);
      }
  }
  printf("%d",pop());
}
```
## Output:

![Screenshot 2025-04-29 085923](https://github.com/user-attachments/assets/e72a083e-9673-418e-9b10-69815cbb0513)


## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
