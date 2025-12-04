# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types.

## AIM:
To implement the Abstract Factory Design Pattern in Java by creating UI components (Buttons and Checkboxes) for two different themes—Dark and Light.
Based on user input, the appropriate factory should generate the correct themed UI elements.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define two interfaces:
Button with method render()
Checkbox with method render()

4.Create concrete classes for Dark and Light themes:
DarkButton, LightButton
DarkCheckbox, LightCheckbox

5.Define the UIFactory interface with:
createButton()
createCheckbox()

6.Create concrete factories:
DarkThemeFactory implements UIFactory
Returns dark-themed button and checkbox
LightThemeFactory implements UIFactory
Returns light-themed button and checkbox

7.In the main method:
Read the theme name from user input.
If theme is "dark" → use DarkThemeFactory
If theme is "light" → use LightThemeFactory
Otherwise print "Invalid theme" and exit.

8.Use the chosen factory to:
Create a button and render it.
Create a checkbox and render it.

9.End the program.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface Button
{ 
    void render();
}
interface Checkbox 
{ 
    void render();
}

class DarkButton implements Button 
{
    public void render()
    { 
        System.out.println("Dark Button created"); 
    }
}

class LightButton implements Button 
{
    public void render() 
    {
        System.out.println("Light Button created"); 
    }
}

class DarkCheckbox implements Checkbox
{
    public void render() 
    { 
        System.out.println("Dark Checkbox created"); 
    }
}

class LightCheckbox implements Checkbox
{
    public void render() 
    { 
        System.out.println("Light Checkbox created");
    }
}

interface UIFactory 
{
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory
{
    public Button createButton()
    {
        return new DarkButton(); 
    }
    public Checkbox createCheckbox() 
    { 
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory 
{
    public Button createButton() 
    {
        return new LightButton();
    }
    public Checkbox createCheckbox() 
    {
        return new LightCheckbox(); 
    }
}

public class Main 
{
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;
        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else
        {
            System.out.println("Invalid theme");
            return;
        }
        factory.createButton().render();
        factory.createCheckbox().render();
    }
}
```





## OUTPUT:

<img width="599" height="338" alt="image" src="https://github.com/user-attachments/assets/0fb61d80-efa6-427c-9038-b22ff00dbdb5" />



## RESULT:
The program successfully demonstrates the Abstract Factory Pattern by creating theme-specific UI components.

Based on user input, the correct factory is selected, and it generates:

A Dark Button and Dark Checkbox or
A Light Button and Light Checkbox

Both components are rendered in the output according to the selected theme.
