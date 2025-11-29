# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to write a string to a text file named output.txt.

<img width="275" height="126" alt="image" src="https://github.com/user-attachments/assets/28fcb1e8-2159-47b0-88e1-fe124b5381a9" />


## AIM:
To write a given string into a text file named output.txt using Java.




## ALGORITHM :
1.	Start the program.

2. Declare a string variable and store the content to be written into the file.

3. Create a FileWriter object with the filename output.txt inside a try-with-           resources block.

4. Use the write() method to write the string content into the file.

5. Display a success message after writing.

6. If an exception occurs, catch the IOException and display an error message.

7. End the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: SINGAMALA VENKATA SSAI KUMAR REDDY
RegisterNumber: 212223230208 
*/
```

## SOURCE CODE:

```
import java.io.FileWriter;
import java.io.IOException;

public class WriteStringToFile {
    public static void main(String[] args) {
        String content = "Hello, this is a sample text."; 

        try (FileWriter writer = new FileWriter("output.txt")) {
            writer.write(content);
            System.out.println("Successfully wrote to the file.");
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}

```





## OUTPUT:


<img width="719" height="148" alt="image" src="https://github.com/user-attachments/assets/06a16717-1b84-45e6-9453-2bf4b61f14a5" />


## RESULT:

The program successfully creates output.txt and writes the specified content into it.


