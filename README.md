
### README for Basic Calculator

```markdown
# Basic Calculator

This is a simple calculator program implemented in Java. It performs basic arithmetic operations such as addition, subtraction, multiplication, and division.

## How to Use

1. The program will prompt you to enter the first number.
2. Enter the first number and press Enter.
3. The program will prompt you to enter an operator (+, -, *, /).
4. Enter the operator and press Enter.
5. The program will prompt you to enter the second number.
6. Enter the second number and press Enter.
7. The program will display the result of the operation.

## Code Example

```java
import java.util.Scanner;

public class BasicCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Enter first number: ");
        double num1 = scanner.nextDouble();
        
        System.out.println("Enter an operator (+, -, *, /): ");
        char operator = scanner.next().charAt(0);
        
        System.out.println("Enter second number: ");
        double num2 = scanner.nextDouble();
        
        double result;
        
        switch(operator) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 + num2;
                break;
            case '/':
                if(num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error! Division by zero.");
                    return;
                }
                break;
            default:
                System.out.println("Invalid operator.");
                return;
        }
        
        System.out.println("The result is: " + result);
        scanner.close();
    }
}
