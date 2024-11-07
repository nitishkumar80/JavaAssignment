
1. Factorial and Sum of Digits
`import java.util.Scanner;

public class FactorialSum {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int num = scanner.nextInt();
        
        int factorial = calculateFactorial(num);
        System.out.println("Factorial: " + factorial);
        
        int sumOfDigits = calculateDigitSum(factorial);
        System.out.println("Sum of digits: " + sumOfDigits);
    }
    
    public static int calculateFactorial(int n) {
        int fact = 1;
        for (int i = 2; i <= n; i++) fact *= i;
        return fact;
    }
    
    public static int calculateDigitSum(int num) {
        int sum = 0;
        while (num > 0) {
            sum += num % 10;
            num /= 10;
        }
        return sum;
    }
}
`