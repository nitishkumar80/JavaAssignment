
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

----------------------------------------------------------------------------------------


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


----------------------------------------------------------------------------------------

3. Menu-Driven Calculator
   
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean exit = false;

        while (!exit) {
            System.out.println("Choose an operation: 1-Add 2-Subtract 3-Multiply 4-Divide 5-Exit");
            int choice = scanner.nextInt();
            
            if (choice == 5) break;

            System.out.print("Enter two numbers: ");
            double num1 = scanner.nextDouble();
            double num2 = scanner.nextDouble();

            switch (choice) {
                case 1: System.out.println("Result: " + (num1 + num2)); break;
                case 2: System.out.println("Result: " + (num1 - num2)); break;
                case 3: System.out.println("Result: " + (num1 * num2)); break;
                case 4: 
                    if (num2 != 0) System.out.println("Result: " + (num1 / num2));
                    else System.out.println("Cannot divide by zero");
                    break;
                default: System.out.println("Invalid choice");
            }
        }
    }
}
----------------------------------------------------------------------------------------

4. Palindrome Check

import java.util.Scanner;

public class PalindromeCheck {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String str = scanner.nextLine();
        
        if (isPalindrome(str)) System.out.println("The string is a palindrome.");
        else System.out.println("The string is not a palindrome.");
    }
    
    public static boolean isPalindrome(String str) {
        String reversed = new StringBuilder(str).reverse().toString();
        return str.equals(reversed);
    }
}

----------------------------------------------------------------------------------------

5. Fibonacci Sequence
java
Copy code
import java.util.Scanner;

public class FibonacciSequence {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of terms: ");
        int n = scanner.nextInt();

        int[] fibonacci = new int[n];
        fibonacci[0] = 0;
        if (n > 1) fibonacci[1] = 1;
        
        for (int i = 2; i < n; i++) fibonacci[i] = fibonacci[i - 1] + fibonacci[i - 2];
        
        System.out.println("Fibonacci sequence:");
        for (int num : fibonacci) System.out.print(num + " ");
    }
}
----------------------------------------------------------------------------------------

6. Second Largest in Array
java
Copy code
import java.util.Scanner;
import java.util.Arrays;

public class SecondLargest {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of elements: ");
        int n = scanner.nextInt();
        int[] numbers = new int[n];
        
        System.out.println("Enter the numbers:");
        for (int i = 0; i < n; i++) numbers[i] = scanner.nextInt();
        
        System.out.println("Second largest: " + findSecondLargest(numbers));
    }
    
    public static int findSecondLargest(int[] arr) {
        Arrays.sort(arr);
        return arr[arr.length - 2];
    }
}

----------------------------------------------------------------------------------------

7. Pyramid of Numbers
import java.util.Scanner;

public class NumberPyramid {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of rows: ");
        int rows = scanner.nextInt();

        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) System.out.print(j + " ");
            System.out.println();
        }
    }
}

----------------------------------------------------------------------------------------

8. Inverted Triangle of Numbers
java
Copy code
import java.util.Scanner;

public class InvertedTriangle {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of rows: ");
        int rows = scanner.nextInt();

        for (int i = rows; i >= 1; i--) {
            for (int j = 1; j <= i; j++) System.out.print(j + " ");
            System.out.println();
        }
    }
}

----------------------------------------------------------------------------------------

9. Floyd's Triangle

import java.util.Scanner;

public class FloydsTriangle {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of rows: ");
        int rows = scanner.nextInt();
        
        int number = 1;
        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) System.out.print(number++ + " ");
            System.out.println();
        }
    }
}

----------------------------------------------------------------------------------------
10. Count Character Occurrences

import java.util.Scanner;

public class CharacterCount {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String str = scanner.nextLine();
        
        System.out.print("Enter a character to count: ");
        char ch = scanner.next().charAt(0);

        int count = countOccurrences(str, ch);
        System.out.println("Occurrences of '" + ch + "': " + count);
    }
    
    public static int countOccurrences(String str, char ch) {
        int count = 0;
        for (int i = 0; i < str.length(); i++) if (str.charAt(i) == ch) count++;
        return count;
    }
}
