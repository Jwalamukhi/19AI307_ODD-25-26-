# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to define an enum named GameLevel with three constants: EASY, MEDIUM, and HARD.

## AIM:
To write a Java program that defines an enum named GameLevel with constants EASY, MEDIUM, and HARD, and allows the user to select a game level.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an enum GameLevel with constants: EASY, MEDIUM, HARD.
4.	Read user input as a string and convert it to uppercase.
5.	Use GameLevel.valueOf() to match the input with an enum constant.
6.	If the value matches, print the selected game level.
7.	If no match is found, catch IllegalArgumentException and show an error message.
8.	Close the scanner in the finally block.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

enum GameLevel {
    EASY, MEDIUM, HARD;
}

public class Game {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String userInput = scanner.nextLine().toUpperCase();

        try {
            GameLevel level = GameLevel.valueOf(userInput);
            System.out.println("You selected game level: " + level);
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid game level entered.");
        } finally {
            scanner.close();
        }
    }
}
```





## OUTPUT:


<img width="805" height="188" alt="image" src="https://github.com/user-attachments/assets/012fd46d-1caa-49bc-b40f-c5ad2a7fa158" />


## RESULT:

The program has been executed successfully and the desired output has been obtained.
