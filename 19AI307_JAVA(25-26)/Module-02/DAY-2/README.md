# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class demo with two methods: square(int n) → returns n * n. cube(int n) → returns n * square(n) by calling the square() method internally.
4.	In the main class, read an integer input from the user.
5.	Create an object of the demo class.
6.	Call the cube() method using the object and print the result.
7.	End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.*;
class demo
{
    public int square(int n)
    {
        return n*n;
    }
    public int cube(int n)
    {
        return n*square(n);
    }
    
}
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        demo d=new demo();
        System.out.println(d.cube(n));
    }
}
```





## OUTPUT:


<img width="486" height="299" alt="image" src="https://github.com/user-attachments/assets/15a5327f-2f4a-4d6f-b187-8b912cff27dc" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
