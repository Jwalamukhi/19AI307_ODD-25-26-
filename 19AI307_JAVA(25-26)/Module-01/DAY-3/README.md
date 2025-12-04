# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Construct a right-angled triangle star pattern using for loop

## AIM:
To write a Java program using looping statements to print a right-angled triangle star pattern based on user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of rows from the user.
4.	Use an outer loop to iterate through each row.
5.	Use an inner loop to print stars (*) for each row.
6.	Move to the next line after printing stars for each row.
7.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.*;
public class prog
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        for (int i = 1; i <= n; i++){         
            for (int j = 1; j <= i; j++) {      
                System.out.print("* ");
            }
            System.out.println();              
        }
    }
}
```





## OUTPUT:

<img width="495" height="488" alt="image" src="https://github.com/user-attachments/assets/aa7f7546-e940-4829-a284-c5a35a0e40ae" />


## RESULT:

Thus, the Java program using looping statements to print a right-angled triangle star pattern was successfully written, executed, and verified.
