# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

<img width="364" height="144" alt="image" src="https://github.com/user-attachments/assets/76e1cf66-7963-4865-99ff-b1118a65ceb9" />



## AIM:
To create two threads in Java, read their names from the user, set their priorities (t1 → 4, t2 → 2), and display the updated thread details.


## ALGORITHM :
1. Start the program.

2. Create a Scanner object to read input from the user.

3. Read the first thread name from the user and store it in name1.

4. Read the second thread name from the user and store it in name2.

5. Create thread object t1 using name1.

6. Create thread object t2 using name2.

7. Set the priority of t1 to 4.

8. Set the priority of t2 to 2.

9. Display the details of both threads using System.out.println().

10. Close the scanner.

11. End the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber: 212223230208
*/
```

## SOURCE CODE:


```
import java.util.Scanner;

class MyThread extends Thread {
    public MyThread(String name) {
        super(name); 
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        
        MyThread t1 = new MyThread(name1);
        MyThread t2 = new MyThread(name2);

        t1.setPriority(4);
        t2.setPriority(2);

        
        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```




## OUTPUT:

<img width="656" height="205" alt="image" src="https://github.com/user-attachments/assets/1d72aa01-5077-47f0-b72e-24f071d4a79d" />



## RESULT:
The program successfully accepts thread names from the user, assigns priorities, and displays the current thread information.


