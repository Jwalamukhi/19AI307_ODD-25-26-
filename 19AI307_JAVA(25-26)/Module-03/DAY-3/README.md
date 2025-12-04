# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
Subclasses: ArcadeGame: score = baseScore + (level × 100) PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To write a Java program that uses an abstract class to calculate final game scores for two types of games:
ArcadeGame and PuzzleGame, each implementing its own scoring logic.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class GameScore with the abstract method finalScore().
4.	Create subclass ArcadeGame with:
Attributes: base, level
Scoring rule: finalScore = base + (level × 100)

5.Create subclass PuzzleGame with:
Attribute: attempts
Scoring rule:
If attempts ≤ 3 → finalScore = 1000 - (attempts × 100)

Else → finalScore = 500

6.In the main method:
Read type (1 for ArcadeGame, 2 for PuzzleGame)

If type == 1:
Read base and level
Create ArcadeGame object

Else:
Read attempts
Create PuzzleGame object

Call finalScore() and print the result.

7.End the program.






## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.*;
abstract class GameScore{
    abstract int finalScore();
}
class ArcadeGame extends GameScore{
    int base,level;
    ArcadeGame (int base, int level){
        this.base=base;
        this.level=level;
    }
    int finalScore(){
        return base+level*100;
    }
}
class PuzzleGame extends GameScore{
    int attempts;
    PuzzleGame(int attempts){
        this.attempts=attempts;
    }
    int finalScore(){
        return attempts <=3?1000 - attempts * 100 : 500;
    }
}
public class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore score;
        if(type == 1){
            score = new ArcadeGame(sc.nextInt(),sc.nextInt());
        }
        else{
            score = new PuzzleGame(sc.nextInt());
        }
        System.out.println(score.finalScore());
    }
}
```





## OUTPUT:


<img width="434" height="305" alt="image" src="https://github.com/user-attachments/assets/4b324869-2132-402e-a344-e1f293e2b384" />


## RESULT:
The program successfully calculates and displays the final score based on game type and user input using abstract methods and dynamic method dispatch.
