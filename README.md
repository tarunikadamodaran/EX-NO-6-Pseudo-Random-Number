# EX-NO:6 Pseudo-Random-Number

## Name: Tarunika D
## Reg No.212223040227

## AIM: 

Implementation of Pseudorandom Number Generation Using Standard library

## ALGORITHM:
Step 1: Get the number of random numbers to generate from the user.

Step 2: Read the minimum and maximum values for the random number range.

Step 3: Initialize the random seed using the current time.

Step 4: Generate a random number by calculating the remainder of division with the range (max - min + 1) and adding the minimum value.

Step 5: Repeat the random number generation for the specified count.

Step 6: Print each generated random number.

Step 7: End the program.

## PROGRAM:
```
#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("  ***Pseudorandom number generator***\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```

## OUTPUT:
![384794730-23b1642d-4db1-4e66-a3ae-a900c26180af](https://github.com/user-attachments/assets/f5ed4af9-ca43-4216-91b7-c5bdac9558a5)

## RESULT:
The program for Pseudorandom Number Generation is executed successfully
