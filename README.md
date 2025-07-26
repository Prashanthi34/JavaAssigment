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
package wiprotraining;

import java.util.Scanner;

public class StudentAverage {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int count = 0;
        int total = 0;

        while (count < 3) {
            System.out.print("Enter the mark (0-100) for student " + (count + 1) + ": ");
            int mark = sc.nextInt();

            if (mark >= 0 && mark <= 100) {
                total += mark;
                count++;
            } else {
                System.out.println("Invalid input, try again...");
            }
        }

        double avg = total / 3.0;
        System.out.printf("The average is: %.2f\n", avg);
    }
} output: Enter the mark (0-100) for student 1: 56
Enter the mark (0-100) for student 2: 101
Invalid input, try again...
Enter the mark (0-100) for student 2: -1
Invalid input, try again...
Enter the mark (0-100) for student 2: 99
Enter the mark (0-100) for student 3: 45
The average is: 66.67

//16
import java.util.Scanner;

public class StudentAverage {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int count = 0;
        int total = 0;

        while (count < 3) {
            System.out.print("Enter the mark (0-100) for student " + (count + 1) + ": ");
            int mark = sc.nextInt();

            if (mark >= 0 && mark <= 100) {
                total += mark;
                count++;
            } else {
                System.out.println("Invalid input, try again...");
            }
        }

        double avg = total / 3.0;
        System.out.printf("The average is: %.2f\n", avg);
    }
}  Enter the mark (0-100) for student 1: 56
Enter the mark (0-100) for student 2: 101
Invalid input, try again...
Enter the mark (0-100) for student 2: -1
Invalid input, try again...
Enter the mark (0-100) for student 2: 99
Enter the mark (0-100) for student 3: 45
The average is: 66.67

//17
class Vehicle {
    String color;
    int wheels;
    String model;

    public Vehicle(String color, int wheels, String model) {
        this.color = color;
        this.wheels = wheels;
        this.model = model;
    }

    public void display() {
        System.out.println("Color: " + color + ", Wheels: " + wheels + ", Model: " + model);
    }
}

class Truck extends Vehicle {
    public Truck() {
        super("Red", 6, "Tata Ace");
    }

    public void loadCapacity() {
        System.out.println("Truck can carry heavy loads.");
    }
}

class Bus extends Vehicle {
    public Bus() {
        super("Yellow", 4, "Volvo");
    }

    public void passengerCapacity() {
        System.out.println("Bus carries 50+ passengers.");
    }
}

class Car extends Vehicle {
    public Car() {
        super("Blue", 4, "Suzuki Swift");
    }

    public void speed() {
        System.out.println("Car goes up to 180 km/h.");
    }
}

public class Road {
    public static void main(String[] args) {
        Truck t = new Truck();
        Bus b = new Bus();
        Car c = new Car();

        t.display();
        t.loadCapacity();

        b.display();
        b.passengerCapacity();

        c.display();
        c.speed();
    }
}  Color: Red, Wheels: 6, Model: Tata Ace
Truck can carry heavy loads.
Color: Yellow, Wheels: 4, Model: Volvo
Bus carries 50+ passengers.
Color: Blue, Wheels: 4, Model: Suzuki Swift
Car goes up to 180 km/h.

//18 
class Animal {
    String name;
    String color;
    int age;
    double weight;

    public Animal(String name, String color, int age, double weight) {
        this.name = name;
        this.color = color;
        this.age = age;
        this.weight = weight;
    }

    public boolean isVegetarian() { return false; }
    public boolean canClimb() { return false; }
    public String sound() { return "Unknown sound"; }

    public void display() {
        System.out.println("Name: " + name);
        System.out.println("Color: " + color);
        System.out.println("Age: " + age + " years");
        System.out.println("Weight: " + weight + " kg");
        System.out.println("Vegetarian? " + isVegetarian());
        System.out.println("Can Climb? " + canClimb());
        System.out.println("Sound: " + sound());
        System.out.println("------------------------------");
    }
}

class Lion extends Animal {
    public Lion() { super("Lion", "Golden", 7, 190.5); }
    public String sound() { return "Roars"; }
}

class Tiger extends Animal {
    public Tiger() { super("Tiger", "Orange & Black", 6, 220.3); }
    public String sound() { return "Growls"; }
}

class Deer extends Animal {
    public Deer() { super("Deer", "Brown", 4, 85.0); }
    public boolean isVegetarian() { return true; }
    public String sound() { return "Bleats"; }
}

class Monkey extends Animal {
    public Monkey() { super("Monkey", "Grey", 3, 35.2); }
    public boolean isVegetarian() { return true; }
    public boolean canClimb() { return true; }
    public String sound() { return "Chatters"; }
}

class Elephant extends Animal {
    public Elephant() { super("Elephant", "Grey", 12, 500.0); }
    public boolean isVegetarian() { return true; }
    public String sound() { return "Trumpets"; }
}

class Giraffe extends Animal {
    public Giraffe() { super("Giraffe", "Yellow", 10, 800.0); }
    public boolean isVegetarian() { return true; }
    public String sound() { return "Hums"; }
}

public class VandalurZoo {
    public static void main(String[] args) {
        Animal[] zooAnimals = {
            new Lion(),
            new Tiger(),
            new Deer(),
            new Monkey(),
            new Elephant(),
            new Giraffe()
        };

        System.out.println("🐾 Welcome to Vandalur Zoo!");
        System.out.println("==============================");
        for (Animal a : zooAnimals) {
            a.display();
        }
    }
}  🐾 Welcome to Vandalur Zoo!
==============================
Name: Lion
Color: Golden
Age: 7 years
Weight: 190.5 kg
Vegetarian? false
Can Climb? false
Sound: Roars
------------------------------
Name: Tiger
Color: Orange & Black
Age: 6 years
Weight: 220.3 kg
Vegetarian? false
Can Climb? false
Sound: Growls
------------------------------
Name: Deer
Color: Brown
Age: 4 years
Weight: 85.0 kg
Vegetarian? true
Can Climb? false
Sound: Bleats
------------------------------
Name: Monkey
Color: Grey
Age: 3 years
Weight: 35.2 kg
Vegetarian? true
Can Climb? true
Sound: Chatters
------------------------------
Name: Elephant
Color: Grey
Age: 12 years
Weight: 500.0 kg
Vegetarian? true
Can Climb? false
Sound: Trumpets
------------------------------
Name: Giraffe
Color: Yellow
Age: 10 years
Weight: 800.0 kg
Vegetarian? true
Can Climb? false
Sound: Hums
------------------------------

//19 
abstract class Bank {
    String accNo;
    String custName;
    int custGender; // 1 = Male, 2 = Female
    String custJob;
    double curBal;

    Bank(String accNo, String custName, int custGender, String custJob, double curBal) {
        this.accNo = accNo;
        this.custName = custName;
        this.custGender = custGender;
        this.custJob = custJob;
        this.curBal = curBal;
    }

    public String toString() {
        return "Account No: " + accNo +
               "\nName: " + custName +
               "\nGender: " + (custGender == 1 ? "Male" : "Female") +
               "\nJob: " + custJob +
               "\nCurrent Balance: RM" + curBal;
    }

    public abstract double calcBalance();
}

class Saving extends Bank {
    double savRate;

    Saving(String accNo, String custName, int custGender, String custJob, double curBal, double savRate) {
        super(accNo, custName, custGender, custJob, curBal);
        this.savRate = savRate;
    }

    @Override
    public double calcBalance() {
        return curBal + (savRate * curBal);
    }
}

class Current extends Bank {
    boolean fixedDep;
    double curRate;

    Current(String accNo, String custName, int custGender, String custJob, double curBal, boolean fixedDep, double curRate) {
        super(accNo, custName, custGender, custJob, curBal);
        this.fixedDep = fixedDep;
        this.curRate = curRate;
    }

    @Override
    public double calcBalance() {
        double serviceFee = fixedDep ? 150.0 : 0.0;
        return (curBal + (curRate * curBal)) - serviceFee;
    }
}

public class BankDemo {
    public static void main(String[] args) {
        Bank[] customers = {
            new Saving("S1001", "Asha", 2, "Teacher", 5000.0, 0.04),
            new Current("C1002", "Raj", 1, "Engineer", 7000.0, true, 0.03),
            new Current("C1003", "Meena", 2, "Doctor", 12000.0, false, 0.025)
        };

        // b) Search customer by account number
        String searchAccNo = "C1003";
        boolean found = false;
        for (Bank b : customers) {
            if (b.accNo.equals(searchAccNo)) {
                System.out.println("🔎 Customer Found!");
                System.out.println(b);
                System.out.println("Calculated Balance: RM" + b.calcBalance());
                found = true;
                break;
            }
        }
        if (!found) {
            System.out.println("⚠️ Account number " + searchAccNo + " not found.");
        }

        // c) Count Current customers and total balance
        int currentCount = 0;
        double totalBalance = 0.0;
        for (Bank b : customers) {
            if (b instanceof Current) {
                currentCount++;
                totalBalance += b.calcBalance();
            }
        }
        System.out.println("\n🏦 Current Account Holders: " + currentCount);
        System.out.println("💰 Total Balance in Current Accounts: RM" + totalBalance);
    }
}  🔎 Customer Found!
Account No: C1003
Name: Meena
Gender: Female
Job: Doctor
Current Balance: RM12000.0
Calculated Balance: RM12300.0

🏦 Current Account Holders: 2
💰 Total Balance in Current Accounts: RM19290.0.

//20 
abstract class Vehicle {
    abstract void startEngine();
    abstract void stopEngine();
}

class Car extends Vehicle {
    @Override
    void startEngine() {
        System.out.println("🚗 Car engine started. Ready to cruise!");
    }

    @Override
    void stopEngine() {
        System.out.println("🚗 Car engine stopped. Parked safely.");
    }
}

class Motorcycle extends Vehicle {
    @Override
    void startEngine() {
        System.out.println("🏍️ Motorcycle engine started. Time to ride!");
    }

    @Override
    void stopEngine() {
        System.out.println("🏍️ Motorcycle engine stopped. Helmet off.");
    }
}

public class VehicleTest {
    public static void main(String[] args) {
        Vehicle v1 = new Car();
        Vehicle v2 = new Motorcycle();

        v1.startEngine();
        v1.stopEngine();

        System.out.println("-------------------------");

        v2.startEngine();
        v2.stopEngine();
    }
}   🚗 Car engine started. Ready to cruise!
🚗 Car engine stopped. Parked safely.
-------------------------
🏍️ Motorcycle engine started. Time to ride!
🏍️ Motorcycle engine stopped. Helmet off.

//21 
abstract class Person {
    abstract void eat();
    abstract void exercise();
}

class Athlete extends Person {
    void eat() {
        System.out.println("Athlete eats balanced meals and protein.");
    }
    void exercise() {
        System.out.println("Athlete works out daily.");
    }
}

class LazyPerson extends Person {
    void eat() {
        System.out.println("Lazy person prefers snacks and fast food.");
    }
    void exercise() {
        System.out.println("Lazy person rarely exercises.");
    }
}

public class PersonTest {
    public static void main(String[] args) {
        Person athlete = new Athlete();
        Person lazy = new LazyPerson();
        
        athlete.eat();
        athlete.exercise();
        System.out.println("---");
        lazy.eat();
        lazy.exercise();
    }
}  Athlete eats balanced meals and protein.
Athlete works out daily.
---
Lazy person prefers snacks and fast food.
Lazy person rarely exercises.

//22 
interface Drawable {
    void drawingColor();
    void thickness();
}

interface Fillable {
    void fillingColor();
    void size();
}

class Line implements Drawable, Fillable {
    public void drawingColor() {
        System.out.println("Line Color: Black");
    }
    public void thickness() {
        System.out.println("Line Thickness: 2px");
    }
    public void fillingColor() {
        System.out.println("Line Fill: None");
    }
    public void size() {
        System.out.println("Line Size: 100 units");
    }
}

class Circle implements Drawable, Fillable {
    public void drawingColor() {
        System.out.println("Circle Outline: Blue");
    }
    public void thickness() {
        System.out.println("Circle Border: 3px");
    }
    public void fillingColor() {
        System.out.println("Circle Fill: Yellow");
    }
    public void size() {
        System.out.println("Radius: 25 units");
    }
}

class Square implements Drawable, Fillable {
    public void drawingColor() {
        System.out.println("Square Border: Red");
    }
    public void thickness() {
        System.out.println("Square Border: 4px");
    }
    public void fillingColor() {
        System.out.println("Square Fill: Green");
    }
    public void size() {
        System.out.println("Side Length: 40 units");
    }
}

public class ShapeTest {
    public static void main(String[] args) {
        Drawable d;
        Fillable f;

        d = f = new Line();
        d.drawingColor(); d.thickness(); f.fillingColor(); f.size();
        System.out.println("---");

        d = f = new Circle();
        d.drawingColor(); d.thickness(); f.fillingColor(); f.size();
        System.out.println("---");

        d = f = new Square();
        d.drawingColor(); d.thickness(); f.fillingColor(); f.size();
    }
}  Line Color: Black
Line Thickness: 2px
Line Fill: None
Line Size: 100 units
---
Circle Outline: Blue
Circle Border: 3px
Circle Fill: Yellow
Radius: 25 units
---
Square Border: Red
Square Border: 4px
Square Fill: Green
Side Length: 40 units

//23 
doubt 

//24
import java.util.*;

public class BikerRace {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int[] speed = new int[5];
        int sum = 0;

        System.out.println("Enter speeds of 5 racers:");
        for (int i = 0; i < 5; i++) {
            speed[i] = sc.nextInt();
            sum += speed[i];
        }

        double avg = sum / 5.0;
        System.out.println("Average speed: " + avg);
        System.out.println("Qualifying racers:");

        for (int s : speed) {
            if (s > avg) {
                System.out.println(s);
            }
        }
    }
}  Enter speeds of 5 racers:
60 55 70 50 65
Average speed: 60.0
Qualifying racers:
70
65

//25 
import java.util.*;

public class MyTriangle {
    public static double area(double a, double b, double c) {
        double s = (a + b + c) / 2.0;
        return Math.sqrt(s * (s - a) * (s - b) * (s - c));
    }

    public static double perimeter(double a, double b, double c) {
        return a + b + c;
    }

    public static boolean isValid(double a, double b, double c) {
        return (a + b > c) && (b + c > a) && (a + c > b);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (true) {
            System.out.print("Enter side a: ");
            double a = sc.nextDouble();
            if (a == -1) {
                System.out.println("Bye~");
                break;
            }
            System.out.print("Enter side b: ");
            double b = sc.nextDouble();
            System.out.print("Enter side c: ");
            double c = sc.nextDouble();

            if (isValid(a, b, c)) {
                System.out.println("Valid Triangle ✅");
                System.out.println("Area: " + area(a, b, c));
                System.out.println("Perimeter: " + perimeter(a, b, c));
            } else {
                System.out.println("The input is invalid ❌");
            }
            System.out.println("---------------");
        }
    }
}  Enter side a: 3
Enter side b: 4
Enter side c: 5
Valid Triangle ✅
Area: 6.0
Perimeter: 12.0
---------------
Enter side a: -1
Bye~

//26
import java.util.*;

public class UniqueEvenSum {
    public static void main(String[] args) {
        int[] input = {2, 3, 54, 1, 6, 7, 7};

        Set<Integer> unique = new HashSet<>();
        int evenSum = 0;

        for (int num : input) {
            if (unique.add(num) && num % 2 == 0) {
                evenSum += num;
            }
        }

        System.out.println("Unique elements: " + unique);
        System.out.println("Sum of even numbers: " + evenSum);
    }
}  Unique elements: [1, 2, 3, 6, 7, 54]
Sum of even numbers: 62

//27 
enum Currency {
    ONE, FIVE, TEN, TWENTY, FIFTY, HUNDRED
}

public class CurrencyEnumTest {
    public static void main(String[] args) {
        for (Currency note : Currency.values()) {
            System.out.print(note + " - ");
            describeCurrency(note);
            System.out.println("----------------------");
        }
    }

    public static void describeCurrency(Currency currency) {
        switch (currency) {
            case ONE:
                System.out.println("Smallest denomination, useful for coins and minor purchases.");
                break;
            case FIVE:
                System.out.println("Often used for small change and snacks.");
                break;
            case TEN:
                System.out.println("Popular for moderate transactions like travel fare.");
                break;
            case TWENTY:
                System.out.println("Handy for routine shopping or fuel.");
                break;
            case FIFTY:
                System.out.println("Used for medium-scale payments like groceries.");
                break;
            case HUNDRED:
                System.out.println("High-value note, suitable for large purchases or saving.");
                break;
            default:
                System.out.println("Unknown currency type.");
        }
    }
}  ONE - Smallest denomination, useful for coins and minor purchases.
----------------------
FIVE - Often used for small change and snacks.
----------------------
TEN - Popular for moderate transactions like travel fare.
----------------------
TWENTY - Handy for routine shopping or fuel.
----------------------
FIFTY - Used for medium-scale payments like groceries.
----------------------
HUNDRED - High-value note, suitable for large purchases or saving.
----------------------







//28
interface PerformOperation {
    boolean check(int a);
}

public class LambdaCheck {
    public static PerformOperation isOdd() {
        return (n) -> n % 2 != 0;
    }

    public static PerformOperation isPrime() {
        return (n) -> {
            if (n < 2) return false;
            for (int i = 2; i <= Math.sqrt(n); i++) {
                if (n % i == 0) return false;
            }
            return true;
        };
    }

    public static PerformOperation isPalindrome() {
        return (n) -> {
            String s = String.valueOf(n);
            return s.equals(new StringBuilder(s).reverse().toString());
        };
    }

    public static void main(String[] args) {
        int testOdd = 7, testPrime = 17, testPal = 121;

        System.out.println("isOdd: " + isOdd().check(testOdd));          // true
        System.out.println("isPrime: " + isPrime().check(testPrime));    // true
        System.out.println("isPalindrome: " + isPalindrome().check(testPal)); // true
    }
}  isOdd: true
isPrime: true
isPalindrome: true

//29 
import java.util.*;

public class StudentValidation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter Register Number: ");
            String regNo = sc.nextLine();

            System.out.print("Enter Mobile Number: ");
            String mobNo = sc.nextLine();

            if (regNo.length() != 9 || mobNo.length() != 10) {
                throw new IllegalArgumentException("Invalid length");
            }

            if (!mobNo.matches("\\d+")) {
                throw new NumberFormatException("Mobile must contain only digits");
            }

            if (!regNo.matches("[a-zA-Z0-9]+")) {
                throw new NoSuchElementException("Register must be alphanumeric");
            }

            System.out.println("valid");

        } catch (Exception e) {
            System.out.println("invalid");
        }
    }
}  Enter Register Number: A1B2C3D4E
Enter Mobile Number: 9876543210
valid
     Enter Register Number: A1B#
Enter Mobile Number: 987654321A
invalid

//30
import java.util.Scanner;

@FunctionalInterface
interface Minimum3 {
    double min(double a, double b, double c);
}

public class MinTest {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Minimum3 findMin = (a, b, c) -> Math.min(a, Math.min(b, c));

        System.out.print("Enter first value: ");
        double a = sc.nextDouble();

        System.out.print("Enter second value: ");
        double b = sc.nextDouble();

        System.out.print("Enter third value: ");
        double c = sc.nextDouble();

        System.out.println("Smallest value: " + findMin.min(a, b, c));
    }
}  Enter first value: 3.5
Enter second value: 5.6
Enter third value: 2.1
Smallest value: 2.1
