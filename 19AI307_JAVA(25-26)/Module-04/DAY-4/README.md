# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types


<img width="236" height="123" alt="image" src="https://github.com/user-attachments/assets/40109d12-a9d9-49cb-8897-832e2e27b31f" />



## AIM:
To implement the Abstract Factory design pattern in Java for creating UI components (Button and Checkbox) for multiple themes (dark and light).


## ALGORITHM :
1.	Read theme input from the user.

2. Create the corresponding factory (DarkFactory or LightFactory).

3. Use the factory to create a Button and Checkbox.

4. Call create() on both to display their types.

5. End the program.ort the necessary package 'java.util'
   3.	





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber: 212223230208
*/
```

## SOURCE CODE:

```
import java.util.*;

interface Button { void create(); }
interface Checkbox { void create(); }

class DarkButton implements Button {
    public void create() { 
        System.out.println("Dark Button created"); } 
    
}

class DarkCheckbox implements Checkbox 
{
    public void create() 
{ System.out.println("Dark Checkbox created"); }
}
class LightButton implements Button
{ 
    public void create() 
{ System.out.println("Light Button created"); } 
    
}
class LightCheckbox implements Checkbox
{ 
    public void create() 
{
    System.out.println("Light Checkbox created"); } 
    
}

interface UIFactory { Button createButton(); Checkbox createCheckbox(); }

class DarkFactory implements UIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}

class LightFactory implements UIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine().trim().toLowerCase();
        UIFactory factory;

        if (theme.equals("dark")) factory = new DarkFactory();
        else if (theme.equals("light")) factory = new LightFactory();
        else { System.out.println("Invalid theme"); sc.close(); return; }

        factory.createButton().create();
        factory.createCheckbox().create();
        sc.close();
    }
}
```





## OUTPUT:


<img width="482" height="228" alt="image" src="https://github.com/user-attachments/assets/90c0d97a-778a-4f49-bb50-98662c1d3679" />


## RESULT:
The program generates and displays UI components based on the chosen theme, demonstrating theme-specific object creation without changing client code.


