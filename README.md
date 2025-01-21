# Students-records-using-access-modifier-constructor-
class Student {
    
    private String name;
    private int rollNumber;
    private double mark;
    public Student(String name, int rollNumber, double marks) {
        this.name = name;
        this.rollNumber = rollNumber;
        this.marks = marks;
    }

 
    public void displayDetails() {
        System.out.println("Student Name: " + name);
        System.out.println("Roll Number: " + rollNumber);
        System.out.println("Marks: " + marks);
    }

   
    public double getMarks() {
        return marks;
    }

    public void setMarks(double marks) {
        if (marks >= 0 && marks <= 100) {
            this.marks = marks;
        } else {
            System.out.println("Invalid marks! Please enter marks between 0 and 100.");
        }
    }
}


public class StudentRecord {
    public static void main(String[] args) {
      
        Student student1 = new Student("Alice", 101, 85.5);
        Student student2 = new Student("Bob", 102, 92.0);
        System.out.println("Student 1 Details:");
        student1.displayDetails();

        System.out.println("\nStudent 2 Details:");
        student2.displayDetails();
        System.out.println("\nUpdating Student 1 Marks...");
        student1.setMarks(88.0);
        System.out.println("Updated Marks for Student 1: " + student1.getMarks());
        System.out.println("\nTrying to set invalid marks for Student 2...");
        student2.setMarks(105.0); // Invalid marks
    }
}
 
Output 

Student 1 Details:
Student Name: Alice
Roll Number: 101
Marks: 85.5

Student 2 Details:
Student Name: Bob
Roll Number: 102
Marks: 92.0

Updating Student 1 Marks...
Updated Marks for Student 1: 88.0

Trying to set invalid marks for Student 2...
Invalid marks! Please enter marks between 0 and 100.
