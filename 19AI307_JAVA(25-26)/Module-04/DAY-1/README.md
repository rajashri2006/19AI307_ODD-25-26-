# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.


## AIM:
To write a program that reads two integers and divides the first by the second, handling division-by-zero safely.


## ALGORITHM :
1.	Start the program.

2. Create a Scanner object to take user input.

3. Read two integers a and b from the user.

4. Enter a try block and attempt to divide a by b.

5. If division succeeds, display the result.

6. If an ArithmeticException occurs (such as division by zero), move to the catch       block.

7. In the catch block, print "Error: Division by zero".

8. End the program.



## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber:  212223230208
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        try{
            int a = sc.nextInt();
            int b = sc.nextInt();
            System.out.println("Result: "+a/b);
        }
        catch (ArithmeticException e){
            System.out.println("Error: Division by zero");
        }
    }
}
```





## OUTPUT:


<img width="719" height="319" alt="image" src="https://github.com/user-attachments/assets/491afef4-c4e3-4700-982d-8498c94529c6" />


## RESULT:

The program outputs the quotient when possible, otherwise displays an error message for division by zero.


