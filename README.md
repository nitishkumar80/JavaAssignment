
1. Factorial and Sum of Digits


import java.util.Scanner;

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




2. Prime Numbers in an Array

import java.util.Scanner;

public class PrimeArray {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] numbers = new int[10];
        
        System.out.println("Enter 10 integers:");
        for (int i = 0; i < 10; i++) numbers[i] = scanner.nextInt();
        
        System.out.println("Prime numbers:");
        for (int num : numbers) if (isPrime(num)) System.out.println(num);
    }
    
    public static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= Math.sqrt(num); i++) if (num % i == 0) return false;
        return true;
    }
}
