import java.util.ArrayList;
import java.util.Scanner;

public class task1 {

    static ArrayList<String> history = new ArrayList<>();

    // Addition
    public static double add(double a, double b) {
        return a + b;
    }

    // Subtraction
    public static double subtract(double a, double b) {
        return a - b;
    }

    // Multiplication
    public static double multiply(double a, double b) {
        return a * b;
    }

    // Division
    public static double divide(double a, double b) {
        if (b == 0) {
            throw new ArithmeticException("Cannot divide by zero!");
        }
        return a / b;
    }

    // Modulus
    public static double modulus(double a, double b) {
        return a % b;
    }

    // Power
    public static double power(double a, double b) {
        return Math.pow(a, b);
    }

    // Square Root
    public static double squareRoot(double a) {
        if (a < 0) {
            throw new ArithmeticException(
                    "Cannot find square root of a negative number!");
        }
        return Math.sqrt(a);
    }

    // Safe number input
    public static double getNumber(Scanner sc, String message) {

        while (true) {
            System.out.print(message);

            if (sc.hasNextDouble()) {
                return sc.nextDouble();
            } else {
                System.out.println("Invalid input! Please enter a number.");
                sc.next();
            }
        }
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int choice;

        do {
            System.out.println("\n=================================");
            System.out.println("      ADVANCED CALCULATOR");
            System.out.println("=================================");
            System.out.println("1. Addition");
            System.out.println("2. Subtraction");
            System.out.println("3. Multiplication");
            System.out.println("4. Division");
            System.out.println("5. Modulus");
            System.out.println("6. Power");
            System.out.println("7. Square Root");
            System.out.println("8. View History");
            System.out.println("9. Clear History");
            System.out.println("10. Exit");
            System.out.print("Enter your choice: ");

            while (!sc.hasNextInt()) {
                System.out.println("Please enter a valid choice!");
                sc.next();
            }

            choice = sc.nextInt();

            try {

                double num1, num2, result;

                switch (choice) {

                    case 1:
                        num1 = getNumber(sc, "Enter first number: ");
                        num2 = getNumber(sc, "Enter second number: ");

                        result = add(num1, num2);

                        System.out.printf("Result = %.2f%n", result);
                        history.add(num1 + " + " + num2 + " = " + result);
                        break;

                    case 2:
                        num1 = getNumber(sc, "Enter first number: ");
                        num2 = getNumber(sc, "Enter second number: ");

                        result = subtract(num1, num2);

                        System.out.printf("Result = %.2f%n", result);
                        history.add(num1 + " - " + num2 + " = " + result);
                        break;

                    case 3:
                        num1 = getNumber(sc, "Enter first number: ");
                        num2 = getNumber(sc, "Enter second number: ");

                        result = multiply(num1, num2);

                        System.out.printf("Result = %.2f%n", result);
                        history.add(num1 + " * " + num2 + " = " + result);
                        break;

                    case 4:
                        num1 = getNumber(sc, "Enter first number: ");
                        num2 = getNumber(sc, "Enter second number: ");

                        result = divide(num1, num2);

                        System.out.printf("Result = %.2f%n", result);
                        history.add(num1 + " / " + num2 + " = " + result);
                        break;

                    case 5:
                        num1 = getNumber(sc, "Enter first number: ");
                        num2 = getNumber(sc, "Enter second number: ");

                        result = modulus(num1, num2);

                        System.out.printf("Result = %.2f%n", result);
                        history.add(num1 + " % " + num2 + " = " + result);
                        break;

                    case 6:
                        num1 = getNumber(sc, "Enter base number: ");
                        num2 = getNumber(sc, "Enter exponent: ");

                        result = power(num1, num2);

                        System.out.printf("Result = %.2f%n", result);
                        history.add(num1 + " ^ " + num2 + " = " + result);
                        break;

                    case 7:
                        num1 = getNumber(sc,
                                "Enter number for square root: ");

                        result = squareRoot(num1);

                        System.out.printf("Result = %.2f%n", result);
                        history.add("√" + num1 + " = " + result);
                        break;

                    case 8:
                        System.out.println("\n===== CALCULATION HISTORY =====");

                        if (history.isEmpty()) {
                            System.out.println("No calculations performed yet.");
                        } else {
                            for (int i = 0; i < history.size(); i++) {
                                System.out.println((i + 1) + ". "
                                        + history.get(i));
                            }
                        }
                        break;

                    case 9:
                        history.clear();
                        System.out.println("History cleared successfully!");
                        break;

                    case 10:
                        System.out.println(
                                "Thank you for using the calculator!");
                        break;

                    default:
                        System.out.println("Invalid choice! Try again.");
                }

            } catch (ArithmeticException e) {
                System.out.println("Error: " + e.getMessage());
            } catch (Exception e) {
                System.out.println("Unexpected Error: " + e.getMessage());
            }

        } while (choice != 10);

        sc.close();
    }
}
