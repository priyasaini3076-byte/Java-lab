[Program 1 WAP for arithmetic logic](#Assi-1)      

 ## Assi-1
 '''

 import java.util.Scanner;

public class ArithmeticLogic {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double a, b;

        System.out.print("Enter first number: ");
        a = sc.nextDouble();

        System.out.print("Enter second number: ");
        b = sc.nextDouble();

        // Arithmetic operations
        System.out.println("Addition: " + (a + b));
        System.out.println("Subtraction: " + (a - b));
        System.out.println("Multiplication: " + (a * b));

        if (b != 0) {
            System.out.println("Division: " + (a / b));
        } else {
            System.out.println("Division: Not possible (divide by zero)");
        }
    }
}
'''

 Enter first number: 10
Enter second number: 5

Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2
