# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array

## AIM:
To write a Java program that reads an array of integers and finds the index of a given element within the array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the size of the array n.
4.	Read n integer elements and store them in the array a[].
5.	Read the element x whose index needs to be found.
6.	Traverse the array from index 0 to n-1: If a[i] == x, print the index i and terminate the program.
7.	If the loop finishes without a match, print "Element not found".
8.	End.
   







## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a[] = new int[n];
        for (int i = 0; i < n; i++) 
        {
            a[i] = sc.nextInt();
        }
        
        int x = sc.nextInt();
        for (int i = 0; i < n; i++) {
            if (a[i] == x) {
                System.out.println(i);
                return;
            }  
        }
        System.out.println("Element not found");
    }
}
```





## OUTPUT:
<img width="593" height="549" alt="image" src="https://github.com/user-attachments/assets/10f1a424-af2c-4d62-9cc4-47a3aa28fd68" />


## RESULT:
Therefore the program successfully searches the array for the given element.

