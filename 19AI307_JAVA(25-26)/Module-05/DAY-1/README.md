# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.


<img width="324" height="130" alt="image" src="https://github.com/user-attachments/assets/cebb029d-8392-4547-afbe-efc2287aa147" />



## AIM:
To write characters to a file in Java using the FileWriter class.


## ALGORITHM :
1.	Read the file name and content from the user.

2. Create a FileWriter object with the given file name.

3. Write the content to the file using write().

4. Close the FileWriter.

5. Print success message if no exception occurs; otherwise, print an error message.

6. AIMM End the program.




## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber: 212223230208 
*/
```

## SOURCE CODE:

```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteToFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        String fileName = sc.nextLine();
        String content = sc.nextLine();

        try {
            
            FileWriter writer = new FileWriter(fileName);

            
            writer.write(content);

            
            writer.close();

            
            System.out.println("File written successfully.");
        } 
        catch (IOException e) {
            System.out.println("An error occurred.");
        }

        sc.close();
    }
}
```





## OUTPUT:



<img width="672" height="245" alt="image" src="https://github.com/user-attachments/assets/69796d46-8c78-42ce-9ac2-d8d023285317" />


## RESULT:
The program successfully writes the user-provided content to the specified file and confirms completion.


