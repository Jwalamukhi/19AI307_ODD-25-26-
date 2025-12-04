# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To write a Java program that initializes object variables using a constructor and overrides the toString() method to display object details in a readable format.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class Student with two instance variables: String name int age
4.	Create a parameterized constructor to initialize these variables.
5.	Override the toString() method to return the student details in a formatted string.
6.	In the main() method:
   
   :Read the name and age from the user.

   :Create a Student object using the constructor.

7.Print the object, which automatically calls the overridden toString() method.

8.End the program.

  





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.*;
class student{
    private String name;
    private int age;
    public student(String name,int age){ 
        this.name=name;
        this.age=age;
    }
    @Override
    public String toString(){
        return "Student{name='"+name+"', age="+age+"}";
    }
}
public class prog{
    public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    String name = sc.nextLine();
    int age = sc.nextInt();
    student st = new student(name,age);
    System.out.print(st);
    }
}
```





## OUTPUT:


<img width="689" height="363" alt="image" src="https://github.com/user-attachments/assets/f3d94c5f-5773-4398-b67b-80052c8e0e84" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.

