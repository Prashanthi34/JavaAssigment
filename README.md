//1Question
package wiprotraining;

public class BufferReader {


	public static void main(String[] args) 
	{
		// TODO Auto-generated method stubpublic static void main(String[] args) {
		        int num = 2345;
		        num += 8;                  // Step 1
		        int quotient = num / 3;   // Step 2
		        int mod = quotient % 5;   // Step 3
		        int result = mod * 5;     // Step 4

		        System.out.println("Final result: " + result); // Output: 20
		    }
		}

//3Question
package wiprotraining;

public class GradeACalculator {
    public static void main(String[] args) {
        int totalStudents = 90;
        int totalBoys = 45;
        int gradeAStudents = totalStudents / 2;     // 50% of total students
        int gradeABoys = 20;

        int gradeAGirls = gradeAStudents - gradeABoys;

        System.out.println("Number of girls with Grade 'A': " + gradeAGirls); // Output: 25
    }
}

//4 
import java.util.Scanner;

public class PersonalInfo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Enter your roll number: ");
        String roll = sc.nextLine();

        System.out.print("Enter your field of interest: ");
        String interest = sc.nextLine();

        System.out.println("Hey, my name is " + name + " and my roll number is " + roll + ". My field of interest are " + interest + ".");
    }
} // output: Enter your name: Batta
             Enter your roll number: 101
             Enter your field of interest: Java and testing
             Hey, my name is Batta and my roll number is 101. My field of interest are Java and testing.

//5
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your salary: ");
        double salary = sc.nextDouble();

        System.out.print("Enter years of service: ");
        int years = sc.nextInt();

        if (years > 20) {
            double bonus = salary * 0.10;
            System.out.println("Net bonus amount: ₹" + bonus);
        } else {
            System.out.println("No bonus awarded.");
        }
    }
} // Enter your salary: 50000
     Enter years of service: 7
     Net bonus amount: ₹5000.0

//6
import java.util.Scanner;

public class GradeSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter your marks: ");
        int marks = sc.nextInt();

        char grade;
        if (marks < 25) grade = 'F';
        else if (marks <= 45) grade = 'E';
        else if (marks <= 50) grade = 'D';
        else if (marks <= 60) grade = 'C';
        else if (marks <= 80) grade = 'B';
        else grade = 'A';

        System.out.println("Your grade is: " + grade);
    }
}     // Enter your marks: 67
         Your grade is: B

  //7 
  import java.util.Scanner;

public class AttendanceCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Number of classes held: ");
        int held = sc.nextInt();

        System.out.print("Number of classes attended: ");
        int attended = sc.nextInt();

        double percentage = (attended * 100.0) / held;
        System.out.println("Attendance Percentage: " + percentage + "%");

        if (percentage >= 70) {
            System.out.println("Allowed to sit in exam ✅");
        } else {
            System.out.println("Not allowed to sit in exam ❌");
        }
    }
}   // Number of classes held: 60
       Number of classes attended: 45
       Attendance Percentage: 75.0%
       Allowed to sit in exam ✅

//8 
import java.util.Scanner;

public class AttendanceWithMedical {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Number of classes held: ");
        int held = sc.nextInt();

        System.out.print("Number of classes attended: ");
        int attended = sc.nextInt();

        sc.nextLine(); // consume newline
        System.out.print("Do you have a medical cause? (Y/N): ");
        char medical = sc.nextLine().trim().toUpperCase().charAt(0);

        double percentage = (attended * 100.0) / held;
        System.out.println("Attendance Percentage: " + percentage + "%");

        if (percentage >= 70 || medical == 'Y') {
            System.out.println("Allowed to sit in exam ✅");
        } else {
            System.out.println("Not allowed to sit in exam ❌");
        }
    }
}     Number of classes held: 50
      Number of classes attended: 32
      Do you have a medical cause? (Y/N): Y
      Attendance Percentage: 64.0%
      Allowed to sit in exam ✅

	//9 
 import java.util.Scanner;

public class RetailCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double total = 0.0;

        while (true) {
            System.out.print("Enter product number (1-3) or 0 to finish: ");
            int product = sc.nextInt();

            if (product == 0) break;

            System.out.print("Enter quantity sold: ");
            int quantity = sc.nextInt();

            switch (product) {
                case 1: total += quantity * 22.50; break;
                case 2: total += quantity * 44.50; break;
                case 3: total += quantity * 9.98; break;
                default: System.out.println("Invalid product number!");
            }
        }

        System.out.printf("Total retail value of products sold: ₹%.2f\n", total);
    }
}     Enter product number (1-3) or 0 to finish: 1
      Enter quantity sold: 2
      Enter product number (1-3) or 0 to finish: 3
      Enter quantity sold: 5
      Enter product number (1-3) or 0 to finish: 0
      Total retail value of products sold: ₹97.40

// 10
package wiprotraining;

public class EggCounter {
    public static void main(String[] args) {
        int eggs = 1342;  // You can also use Integer.parseInt(args[0]) for command-line input

        int gross = eggs / 144;
        eggs %= 144;

        int dozen = eggs / 12;
        int leftover = eggs % 12;

        System.out.println("Your number of eggs is " + gross + " gross, " + dozen + " dozen, and " + leftover);
    }
}     output: Your number of eggs is 9 gross, 3 dozen, and 10

//11
package wiprotraining;
public class Calculator {
    public void add(int a, int b) {
        System.out.println("Sum = " + (a + b));
    }

    public void diff(int a, int b) {
        System.out.println("Difference = " + (a - b));
    }

    public void mul(int a, int b) {
        System.out.println("Product = " + (a * b));
    }

    public void div(int a, int b) {
        if (b != 0)
            System.out.println("Quotient = " + (a / b));
        else
            System.out.println("Cannot divide by zero!");
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();
        calc.add(20, 5);
        calc.diff(20, 5);
        calc.mul(20, 5);
        calc.div(20, 5);
    }
}   output: Sum = 25
            Difference = 15
            Product = 100
            Quotient = 4

//12 
import java.util.*;

class Student {
    private static int nextRoll = 101;
    private int rollNo;
    private String name;
    private int eng, maths, science;

    public Student(String name, int eng, int maths, int science) {
        this.rollNo = nextRoll++;
        this.name = name;
        this.eng = eng;
        this.maths = maths;
        this.science = science;
    }

    public int getRollNo() { return rollNo; }
    public String getName() { return name; }
    public int getEng() { return eng; }
    public int getMaths() { return maths; }
    public int getScience() { return science; }
    public int getTotal() { return eng + maths + science; }
    public double getPercentage() { return getTotal() / 3.0; }
}

public class Standard {
    public static void main(String[] args) {
        List<Student> students = Arrays.asList(
            new Student("Ravi", 78, 82, 90),
            new Student("Sneha", 85, 88, 92),
            new Student("Vikram", 65, 90, 77),
            new Student("Asha", 72, 60, 68),
            new Student("Manoj", 91, 84, 89),
            new Student("Priya", 95, 86, 93),
            new Student("Kiran", 60, 75, 72),
            new Student("Geeta", 88, 80, 79)
        );

        System.out.println("1️⃣ Students in ascending roll number:");
        students.stream()
            .sorted(Comparator.comparingInt(Student::getRollNo))
            .forEach(s -> System.out.println(s.getRollNo() + " - " + s.getName()));

        System.out.println("\n2️⃣ Topper by percentage:");
        Student topper = Collections.max(students, Comparator.comparingDouble(Student::getPercentage));
        System.out.println(topper.getRollNo() + " - " + topper.getName());

        System.out.println("\n3️⃣ Highest marks in Mathematics:");
        Student mathTopper = Collections.max(students, Comparator.comparingInt(Student::getMaths));
        System.out.println(mathTopper.getRollNo() + " - " + mathTopper.getName());

        System.out.println("\n4️⃣ Sorted by (Maths + Science):");
        students.stream()
            .sorted(Comparator.comparingInt(s -> s.getMaths() + s.getScience()))
            .forEach(s -> System.out.println(s.getRollNo() + " - " + s.getName()));

        System.out.println("\n5️⃣ Ranking by percentage:");
        students.stream()
            .sorted((a, b) -> Double.compare(b.getPercentage(), a.getPercentage()))
            .forEachOrdered(s -> System.out.printf("Roll: %d Name: %s Total: %d %%: %.2f\n",
                    s.getRollNo(), s.getName(), s.getTotal(), s.getPercentage()));
    }
}  output:  1️⃣ Students in ascending roll number:
101 - Ravi
102 - Sneha
103 - Vikram
104 - Asha
105 - Manoj
106 - Priya
107 - Kiran
108 - Geeta

2️⃣ Topper by percentage:
106 - Priya

3️⃣ Highest marks in Mathematics:
103 - Vikram

4️⃣ Sorted by (Maths + Science):
104 - Asha
107 - Kiran
101 - Ravi
108 - Geeta
102 - Sneha
103 - Vikram
105 - Manoj
106 - Priya

5️⃣ Ranking by percentage:
Roll: 106 Name: Priya Total: 274 %: 91.33
Roll: 102 Name: Sneha Total: 265 %: 88.33
Roll: 105 Name: Manoj Total: 264 %: 88.00
Roll: 108 Name: Geeta Total: 247 %: 82.33
Roll: 101 Name: Ravi Total: 250 %: 83.33
Roll: 103 Name: Vikram Total: 232 %: 77.33
Roll: 107 Name: Kiran Total: 207 %: 69.00
Roll: 104 Name: Asha Total: 200 %: 66.67

//14 
package wiprotraining;

class Shape {
    // Area overloads
    public double area(int side) {
        return side * side;
    }

    public double area(int length, int breadth) {
        return length * breadth;
    }

    // Perimeter overloads
    public int perimeter(int side) {
        return 4 * side;
    }

    public int perimeter(int length, int breadth) {
        return 2 * (length + breadth);
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s = new Shape();

        int squareSide = 5;
        int rectLength = 10;
        int rectBreadth = 4;

        System.out.println("🔲 Square Area: " + s.area(squareSide));
        System.out.println("🔲 Square Perimeter: " + s.perimeter(squareSide));
        System.out.println("⬛ Rectangle Area: " + s.area(rectLength, rectBreadth));
        System.out.println("⬛ Rectangle Perimeter: " + s.perimeter(rectLength, rectBreadth));
    }
} output: 🔲 Square Area: 25.0
          🔲 Square Perimeter: 20
          ⬛ Rectangle Area: 40.0
          ⬛ Rectangle Perimeter: 28

//15
