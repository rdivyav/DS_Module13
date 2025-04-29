# EX3 Implementation of Tower of Hanoi
## DATE: 28-04-2025
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1.Define the hanoi function 
2. Base case 
3.Recursive move to the auxiliary peg
4.Move the largest disk  
5. Recursive move from the auxiliary to the destination   

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by:Divya R V 
RegisterNumber:212223100005  
*/
```
```
#include <stdio.h>

// Function to solve Tower of Hanoi
void towerOfHanoi(int n, char from_peg, char to_peg, char aux_peg) {
    if (n == 1) {
        printf("%c to %c\n", from_peg, to_peg);
        return;
    }
    
    towerOfHanoi(n - 1, from_peg, aux_peg, to_peg); // Move n-1 disks to auxiliary peg
    printf("%c to %c\n", from_peg, to_peg); // Move nth disk to destination peg
    towerOfHanoi(n - 1, aux_peg, to_peg, from_peg); // Move n-1 disks to destination peg
}

int main() {
    int num_disks = 4;
    towerOfHanoi(num_disks, 'A', 'B', 'C'); // A is source, B is destination, C is auxiliary
    return 0;
}

```

## Output:

![Screenshot 2025-04-29 084208](https://github.com/user-attachments/assets/fa60a291-9492-4265-8f01-6a91cc771c52)

## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
