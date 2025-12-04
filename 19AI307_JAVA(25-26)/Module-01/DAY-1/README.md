# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely has mastered printing in Java, and now she wants to learn how arithmetic operators work. She’s curious about how Java can add, subtract, multiply, divide, and find remainders of two numbers.

Write a Java program that:

Accepts two integer numbers from the user.

Demonstrates all 5 arithmetic operations:

Addition (+)

Subtraction (-)

Multiplication (*)

Division (/)

Modulus (%)

Displays the result of each operation in a separate line with a clear message.

Input Format
First line: Integer → first number

Second line: Integer → second number

Output Format
Each line shows the result of an arithmetic operation in this format:

Sum = Difference = Product = Quotient = Remainder = Ensure integer division and modulus are correctly handled. Assume the second number will not be 0.



## AIM:
To write a Java program that reads two integer numbers from the user and performs basic arithmetic operations such as addition, subtraction, multiplication, division, and modulus, and displays the results

## ALGORITHM :
1.	Start
2.Create a Scanner object to read input from the user.
3.Read two integer values a and b from the user.
4.Compute sum=a+b , diff=a-b, prod=a*b, quo=a/b and rem=a%b.
5.Display the results and end.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## Sourcecode.java:

```
import java.util.*;
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println("Sum = "+(a+b));
        System.out.println("Difference = "+(a-b));
        System.out.println("Product = "+(a*b));
        System.out.println("Quotient = "+(a/b));
        System.out.println("Remainder = "+(a%b));
    }
}
```





## OUTPUT:
<img width="558" height="330" alt="image" src="https://github.com/user-attachments/assets/b03a4ee0-886c-4788-91f5-7e0abe04894e" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.
