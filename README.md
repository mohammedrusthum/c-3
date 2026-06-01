# MODULE-3
---
# EXP NO:11 C PROGRAM TO CONVERT DECIMAL TO BINARY

## Aim:

Write a C program to convert a given decimal integer value (228) into its binary representation using a loop and display the result.

## Algorithm:

1. Start.

2. Declare integer variables: dec (the decimal number), temp (a temporary copy), digit, and p (power counter, initialized to 0). Declare a long int called bin (binary result, initialized to 0).

3. The main logic is inside a while loop that runs as long as temp is not zero.

3. Inside the loop:
    - a.  Calculate the remainder: digit = temp % 2 (This is the next binary digit: 0 or 1).
    - b.  Build the binary number: bin = digit * pow(10, p) + bin. (This places the digit in the correct power-of-10 place, simulating a binary number).
    - c.  Update the decimal: temp = temp / 2.
    - d.  Increment the power counter: p++.

4. After the loop, print the original decimal value and the calculated binary value.

5. Stop.

## Program:
```
#include <stdio.h>
#include <math.h>
int main(){
    int dec=228;
    int digit,p=0,temp=dec;
    long int bin=0;
    while(temp!=0){
        digit=temp%2;
        bin=digit*pow(10,p) + bin;
        temp/=2;
        p++;
    }
    printf("%d in decimal = %ld in binary",dec,bin);
    return 0;
}
```

## Output:
<img width="1026" height="222" alt="image" src="https://github.com/user-attachments/assets/ac23853e-6e27-4ace-8639-b53b88328f4a" />

## Result:

The C program to convert a fixed decimal value into its binary equivalent was executed and verified successfully.

---
#
---
# EXP NO:12 C PROGRAM TO CHECK AUTOMORPHIC NUMBER

## Aim:

Write a C program to check if a number entered by the user is an Automorphic number (a number whose square ends with the same number) using a loop.

## Algorithm:

1. Start.

2. Declare an integer variable num to hold the input number.

3. Read the input number num from the user.

4. Calculate the square of the number: square = num * num.

5. Use a do-while loop to compare the last digit of the number with the last digit of its square.

6. Inside the loop:
    - a.  Get the last digit of the square: digit = square % 10.
    - b.  Check if digit is equal to num. If they are equal, the number is Automorphic.
    - c.  The loop terminates immediately after the first check because the provided code only checks the last digit.

7. Print the result: "Automorphic number" or "Not Automorphic".

8. Stop.

## Program:
```
#include <stdio.h>
int main(){
    int num;
    scanf("%d",&num);
    do{
        int digit= (num*num)%10;
        if (digit==num) printf("Automorphic number");
        else printf("Not Automorphic");
    }
    while(0);
    return 0;
}

```
## Output:
<img width="1039" height="280" alt="image" src="https://github.com/user-attachments/assets/2b990985-cd8c-4585-99da-42d066bf8442" />

## Result:

The C program to check if a number is an Automorphic number using a loop structure was executed and verified successfully.

---
#
---
# EXP NO:13 C PROGRAM TO PRINT FIRST ELEMENT OF EACH ROW IN MATRIX

## Aim:

Write a C program to read elements into an $n \times n$ matrix (2D array) and then display the element located at the start (index 0) of every row.

## Algorithm:

1. Start.

2. Declare integer variables i, j, and n.

3. Read the size of the square matrix, n, from the user.

4. Declare a Variable Length Array (VLA) for the matrix: int a[n][n].

5. Use nested for loops to read all $n \times n$ elements from the user, storing them in the array a.

6. Use a single for loop (variable i) to iterate through each row of the array (from $i=0$ to $i<n$).

7. Inside this loop, print the value of the first element of the current row: a[i][0].

8. Stop.

## Program:
```
#include <stdio.h>

int main()
{
    int i, j, n;
    
    scanf("%d", &n);
    
    int a[n][n];
    
    for (i = 0; i < n; i++)
    {
        for (j = 0; j < n; j++)
        {
            scanf("%d", &a[i][j]);
        }
    }
    
    for (i = 0; i < n; i++)
    {
        printf("a[%d][0] is %d\n", i, a[i][0]);
    }

    return 0;
}
```

## Output:
<img width="1035" height="460" alt="image" src="https://github.com/user-attachments/assets/8bbebee9-ecb6-492e-bc1a-45c217e1ecf0" />


## Result:

The C program to read an $n \times n$ matrix and successfully print the first element of every row was executed and verified.

---
#
---

# EXP NO:14 C PROGRAM TO SEARCH AN ELEMENT IN AN ARRAY (LINEAR SEARCH)

## Aim:

Write a C program to search for a specific number within a one-dimensional array and report its position (index) if found.

## Algorithm:

1. Start.

2. Declare integer variables n (array size), i (loop counter), and ind (index where the number is found).

3. Read the size of the array, n.

4. Declare the Variable Length Array (VLA): int num[n].

5. Use a for loop to read n elements from the user into the array num.

6. Use a second for loop to check each element in the array (num[i]).

7. If the current element is equal to the target value (5), store the current index i in ind and immediately break the loop.

8. Print the position where the number was found (ind + 1, since positions start at 1).

9. Stop.

## Program:
```
#include <stdio.h>
int main()
{
    int n, i, ind;
    
    scanf("%d", &n);
    
    int num[n];
    
    for (i = 0; i < n; i++)
    {
        scanf("%d", &num[i]);
    }
    
    for (i = 0; i < n; i++)
    {
        if (num[i] == 5) 
        {
            ind = i;
            break;
        }
    }
    
    printf("5 is found at position %d", ind + 1);

    return 0;
}

```
## Output:
<img width="1021" height="237" alt="image" src="https://github.com/user-attachments/assets/aa487c24-c85b-4dd9-82aa-fe7d87d959ac" />


The C program to perform a linear search to find the position of the target element (5) within the array was executed and the result was verified.

---
#
---
# EXP NO:15 C PROGRAM TO CALCULATE SUM AND COUNT EVEN/ODD IN ARRAY

## Aim:

Write a C program that takes an array of numbers as input and calculates the total sum, the count of even numbers, and the count of odd numbers within that array.

## Algorithm:

1. Start.

2. Declare integer variables n (array size), i (loop counter), and initialize o=0 (odd count), e=0 (even count), and sum=0.

3. Read the size of the array, n.

4. Declare the Variable Length Array (VLA): int num[n].

5. Use a for loop to read n elements into the array num.

6. Inside the loop, check if each element (num[i]) is divisible by 2 using the modulo operator (%).

7. If the remainder is 0, increment the even count (e++). Otherwise, increment the odd count (o++).

8. Add the current element to the running total (sum+=num[i]).

9. After the loop finishes, print the final sum, the count of even numbers (e), and the count of odd numbers (o).

10. Stop.

## Program:
```
#include <stdio.h>
int main()
{
    int n, i, o = 0, e = 0, sum = 0;
    
    scanf("%d", &n);
    
    int num[n];
    
    for (i = 0; i < n; i++)
    {
        scanf("%d", &num[i]);
        if (num[i] % 2 == 0) 
            e++;
        else 
            o++;
        sum += num[i];
    }
    
    printf("Total Sum: %d\n", sum);
    printf("Even numbers: %d\n", e);
    printf("Odd numbers: %d\n", o);

    return 0;
}

```
## Output:
<img width="1042" height="286" alt="image" src="https://github.com/user-attachments/assets/b71f209a-8663-4dda-ab32-b9b98321129f" />

## Result:

The C program to calculate the total sum of elements, and count the even and odd numbers within an array was successfully executed and verified.

---
