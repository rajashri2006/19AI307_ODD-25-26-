# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

<img width="155" height="139" alt="image" src="https://github.com/user-attachments/assets/15a5a1b4-a8ad-4c75-87d6-1c2c4ee9f379" />



## AIM:
To read two integer values from the user, use a synchronized block to safely swap them, and display the swapped values.


## ALGORITHM :
1.	Here is the **algorithm** for the given Java program:

### **Algorithm**

1. Start the program.

2. Create a Scanner object to read input from the user.


3. Read the first integer value and store it in variable a.


4. Read the second integer value and store it in variable b.


5. Create a lock object for synchronization.


6. Enter a synchronized block using the lock object.


7. Inside the synchronized block, swap the values of a and b using a temporary         variable temp.


8. Exit the synchronized block.


9. Print the updated value of a.


10. Print the updated value of b.


11. Close the scanner.


12. End the program.


   





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber:  212223230208
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = Integer.parseInt(sc.nextLine().trim());
        int b = Integer.parseInt(sc.nextLine().trim());

        Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);

        sc.close();
    }
}
```





## OUTPUT:

<img width="350" height="238" alt="image" src="https://github.com/user-attachments/assets/6026fce5-b134-4040-b61b-11d35b4c9b68" />


## RESULT:
The program successfully swaps the values of variables a and b using synchronization and prints the updated values.


