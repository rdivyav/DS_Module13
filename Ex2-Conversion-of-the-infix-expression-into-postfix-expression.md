# Ex2 Conversion of the infix expression into postfix expression
## DATE:28-04-2025
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. Initialization 
2.Scanning 
3.Operand Handling 
4.Operator Handling  
5.Finalization   

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by:Divya R V 
RegisterNumber:212223100005  
*/
```
```
/*char stack[100];
int top = -1;

void push(char x)
{
    
}

char pop()
{
    }*/

char IntoPost(char *exp)
{
    char *e,x;
    e=exp;
    while(*e !='\0')
    {
        if(isalnum(*e))
        {
            printf("%c",*e);
        }
        else if(*e=='(')
        {
            push(*e);
        }
        else if(*e == ')')
        {
            while((x=pop())!= '(')
            printf("%c",x);
        }
        else
        {
            while(priority(stack[top])>=priority(*e))
            printf("%c",pop());
            push(*e);
        }
        e++;
    }
        while(top!= -1)
        {
            printf("%c",pop());
        }
        return 1;
    }
    

```
## Output:

![Screenshot 2025-04-29 085329](https://github.com/user-attachments/assets/6eea436e-535c-42ae-a69a-a96e4786ac73)


## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
