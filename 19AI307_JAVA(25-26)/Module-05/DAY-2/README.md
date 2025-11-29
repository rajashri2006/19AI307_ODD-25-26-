# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.


<img width="391" height="287" alt="image" src="https://github.com/user-attachments/assets/74856b04-04de-4cc0-be34-66c72cf59903" />



## AIM:
To demonstrate serialization and deserialization of Student objects in Java, storing and retrieving them from a file.


## ALGORITHM :
1.	Read the number of students.

2. For each student, read id, name, and marks, and add to ArrayList.

3. Serialize the ArrayList to "students.dat" using ObjectOutputStream.

4. Deserialize the ArrayList from "students.dat" using ObjectInputStream.

5. Display all deserialized student details.

6. End the program.




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: SINGAMALA VENKATA SAI KUMAR REDDY
RegisterNumber: 212223230208
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class SerializeStudents {

    @SuppressWarnings("unchecked")
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            ArrayList<Student> students = new ArrayList<>();

            int n = sc.nextInt(); 
            for (int i = 0; i < n; i++) {
                int id = sc.nextInt();
                sc.nextLine(); 
                String name = sc.nextLine();
                double marks = sc.nextDouble();
                students.add(new Student(id, name, marks));
            }

            String filename = "students.dat";

            ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename));
            oos.writeObject(students);
            oos.close();
            System.out.println("Students serialized successfully into: " + filename);

            ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename));
            ArrayList<Student> deserializedStudents = (ArrayList<Student>) ois.readObject();
            ois.close();

            System.out.println("Students deserialized successfully from: " + filename);
            System.out.println();
            System.out.println("Deserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }

        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```





## OUTPUT:


<img width="1031" height="653" alt="image" src="https://github.com/user-attachments/assets/d1fa3d47-f392-4282-87cb-fac03af09cc7" />


## RESULT:
The program successfully writes a list of students to a file (students.dat) and reads it back, displaying the deserialized student details.ALGORITHM 


