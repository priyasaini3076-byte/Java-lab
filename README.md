 [Ass-1:create a class with 4 method (add,sub,div,mul) now test all 4 method in public static void main]{#xyz}
class Calculator {

     int add(int a, int b) {
        return a + b;
    }

     int sub(int a, int b) {
        return a - b;
    }

     int mul(int a, int b) {
        return a * b;
    }

     int div(int a, int b) {
        return a / b;
    }
}

public class Main {
    public static void main(String[] args) {

        Calculator calc = new Calculator();

        int a = 20;
        int b = 10;

        System.out.println("Addition: " + calc.add(a, b));
        System.out.println("Subtraction: " + calc.sub(a, b));
        System.out.println("Multiplication: " + calc.mul(a, b));
        System.out.println("Division: " + calc.div(a, b));
    }
}
