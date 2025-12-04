# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.

Input:

3 100 200 300

Output:

Final Balance: 600

## AIM:
To simulate multiple concurrent deposits into a shared bank account using threads, ensuring thread-safety by synchronizing the deposit method.

ALGORITHM :

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BankAccount class with a balance variable and a synchronized deposit(int amount) method.
4.	Create a DepositTask class extending Thread, storing a reference to BankAccount and the deposit amount, and call deposit() inside run().
5.	In main, read n (number of deposits), then read each deposit amount and create/start a thread for each.
6.	Use join() on all threads to ensure all deposits are completed.
7.	Print the final bank balance using getBalance().





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.*;

class BankAccount {
    private int balance = 0;

    public synchronized void deposit(int amount) {
        balance += amount;
    }

    public int getBalance() {
        return balance;
    }
}

class DepositTask extends Thread {
    BankAccount acc;
    int amount;

    DepositTask(BankAccount acc, int amount) {
        this.acc = acc;
        this.amount = amount;
    }

    public void run() {
        acc.deposit(amount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        BankAccount acc = new BankAccount();
        DepositTask[] t = new DepositTask[n];

        for (int i = 0; i < n; i++) {
            int amount = sc.nextInt();
            t[i] = new DepositTask(acc, amount);
            t[i].start();
        }

        for (int i = 0; i < n; i++) {
            try { t[i].join(); } catch(Exception e) {}
        }

        System.out.println("Final Balance: " + acc.getBalance());
    }
}

```





## OUTPUT:

<img width="628" height="450" alt="image" src="https://github.com/user-attachments/assets/3ec9e5f0-7563-44b0-912b-6514cd3e9418" />



## RESULT:
The program safely performs concurrent deposits using synchronized access and prints the correct final balance.
