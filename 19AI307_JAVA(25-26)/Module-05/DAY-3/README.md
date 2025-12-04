# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:
To write user information (name, age, email) into a text file using FileWriter and then read the same content using BufferedReader, demonstrating basic file handling in Java.



## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Accept name, age, and email from the user using Scanner.
4.	Create a FileWriter object, write formatted user information into the file userdata.txt, and close the writer.
5.	Create a BufferedReader wrapped around FileReader to open the same file.
6.	Read each line using readLine() inside a loop and print it to the console.
7.	Use a try–catch block to manage errors related to file operations or invalid user input.






## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.io.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String fn = "userdata.txt";
        
        try
        {
            String name = sc.nextLine();
            int age = sc.nextInt();
            sc.nextLine();
            String mail = sc.nextLine();
            
            FileWriter fw = new FileWriter(fn);
            fw.write("User Information\n");
            fw.write("================\n");
            fw.write("Name  : "+name+"\n");
            fw.write("Age   : "+age+"\n");
            fw.write("Email : "+mail+"\n");
            fw.close();
            
            BufferedReader br = new BufferedReader(new FileReader(fn));
            String line;
            while((line = br.readLine())!=null)
            {
                System.out.println(line);
            }
            br.close();
        }
        catch(Exception e)
        {
            System.out.println("Error");
        }
    }
}
```






## OUTPUT:


<img width="681" height="247" alt="image" src="https://github.com/user-attachments/assets/428ba612-25ac-414d-9465-e755c17a5648" />


## RESULT:
The program successfully stores user details into a text file and reads them back line by line, displaying the stored content in the console.
