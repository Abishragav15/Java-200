
// 1. Check whether a number is positive or negative.
import java.util.Scanner;
class PositiveNegative {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        if (num > 0) System.out.println("Positive");
        else if (num < 0) System.out.println("Negative");
        else System.out.println("Zero");
    }
}

// 2. Check whether a number is even or odd.
import java.util.Scanner;
class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(num % 2 == 0 ? "Even" : "Odd");
    }
}

// 3. Check whether a number is divisible by 3 and 5.
import java.util.Scanner;
class DivisibleBy3And5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(num % 3 == 0 && num % 5 == 0 ? "Divisible" : "Not Divisible");
    }
}

// 4. Find the largest of three numbers.
import java.util.Scanner;
class LargestOfThree {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt(), b = sc.nextInt(), c = sc.nextInt();
        System.out.println(Math.max(a, Math.max(b, c)));
    }
}

// 5. Check whether a number is a prime number.
import java.util.Scanner;
class PrimeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        boolean isPrime = num > 1;
        for (int i = 2; i * i <= num; i++) if (num % i == 0) isPrime = false;
        System.out.println(isPrime ? "Prime" : "Not Prime");
    }
}

// 6. Check whether a year is a leap year.
import java.util.Scanner;
class LeapYear {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int year = sc.nextInt();
        System.out.println((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0) ? "Leap Year" : "Not Leap Year");
    }
}

// 7. Find the greatest of four numbers.
import java.util.Scanner;
class LargestOfFour {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt(), b = sc.nextInt(), c = sc.nextInt(), d = sc.nextInt();
        System.out.println(Math.max(Math.max(a, b), Math.max(c, d)));
    }
}

// 8. Check if a number is a palindrome.
import java.util.Scanner;
class PalindromeNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt(), rev = 0, temp = num;
        while (temp > 0) { rev = rev * 10 + temp % 10; temp /= 10; }
        System.out.println(num == rev ? "Palindrome" : "Not Palindrome");
    }
}

// 9. Check whether a character is a vowel or consonant.
import java.util.Scanner;
class VowelConsonant {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().toLowerCase().charAt(0);
        System.out.println("aeiou".indexOf(ch) != -1 ? "Vowel" : "Consonant");
    }
}

// 10. Find the smallest of three numbers.
import java.util.Scanner;
class SmallestOfThree {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt(), b = sc.nextInt(), c = sc.nextInt();
        System.out.println(Math.min(a, Math.min(b, c)));
    }
}

// 11. Check if a number is prime using a simple loop.
import java.util.Scanner;
class PrimeSimple {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        boolean isPrime = true;
        for (int i = 2; i < num; i++) if (num % i == 0) isPrime = false;
        System.out.println(isPrime && num > 1 ? "Prime" : "Not Prime");
    }
}

// 12. Check if a number is perfect.
import java.util.Scanner;
class PerfectNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt(), sum = 0;
        for (int i = 1; i <= num / 2; i++) if (num % i == 0) sum += i;
        System.out.println(sum == num ? "Perfect Number" : "Not Perfect");
    }
}

// 13. Find whether a number is Armstrong or not.
import java.util.Scanner;
class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt(), sum = 0, temp = num;
        while (temp > 0) { int d = temp % 10; sum += d * d * d; temp /= 10; }
        System.out.println(sum == num ? "Armstrong" : "Not Armstrong");
    }
}

// 14. Calculate the factorial of a number using recursion.
import java.util.Scanner;
class FactorialRecursion {
    static int factorial(int n) { return n == 0 ? 1 : n * factorial(n - 1); }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(factorial(num));
    }
}

// 15. Check whether a string is a palindrome.
import java.util.Scanner;
class PalindromeString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        System.out.println(str.equals(new StringBuilder(str).reverse().toString()) ? "Palindrome" : "Not Palindrome");
    }
}

// 16. Check if a string is an anagram of another string.
import java.util.Scanner;
import java.util.Arrays;
class AnagramCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str1 = sc.next(), str2 = sc.next();
        char[] arr1 = str1.toCharArray(), arr2 = str2.toCharArray();
        Arrays.sort(arr1); Arrays.sort(arr2);
        System.out.println(Arrays.equals(arr1, arr2) ? "Anagram" : "Not Anagram");
    }
}

// 17. Find if a number is a Fibonacci number.
import java.util.Scanner;
class FibonacciCheck {
    static boolean isPerfectSquare(int x) {
        int s = (int) Math.sqrt(x);
        return s * s == x;
    }
    static boolean isFibonacci(int n) {
        return isPerfectSquare(5 * n * n + 4) || isPerfectSquare(5 * n * n - 4);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(isFibonacci(num) ? "Fibonacci" : "Not Fibonacci");
    }
}

// 18. Determine if a number is a perfect square.
import java.util.Scanner;
class PerfectSquareCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int sqrt = (int) Math.sqrt(num);
        System.out.println(sqrt * sqrt == num ? "Perfect Square" : "Not Perfect Square");
    }
}

// 19. Count the number of digits in a number.
import java.util.Scanner;
class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt(), count = 0;
        while (num > 0) { count++; num /= 10; }
        System.out.println(count);
    }
}

// 20. Check if a number is an automorphic number.
import java.util.Scanner;
class AutomorphicNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int square = num * num;
        System.out.println(square % Math.pow(10, String.valueOf(num).length()) == num ? "Automorphic" : "Not Automorphic");
    }
}

// 21. Check whether a number is a prime number within a range.
import java.util.Scanner;
class PrimeInRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt(), end = sc.nextInt();
        for (int num = start; num <= end; num++) {
            boolean isPrime = num > 1;
            for (int i = 2; i * i <= num; i++) if (num % i == 0) isPrime = false;
            if (isPrime) System.out.print(num + " ");
        }
    }
}

// 22. Find the largest number among n numbers using a nested if-else.
import java.util.Scanner;
class LargestAmongN {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(), max = sc.nextInt();
        for (int i = 1; i < n; i++) {
            int num = sc.nextInt();
            if (num > max) max = num;
        }
        System.out.println(max);
    }
}

// 23. Print all prime numbers in a range using nested loops.
import java.util.Scanner;
class PrimeNumbersRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt(), end = sc.nextInt();
        for (int num = start; num <= end; num++) {
            boolean isPrime = num > 1;
            for (int i = 2; i < num; i++) if (num % i == 0) isPrime = false;
            if (isPrime) System.out.print(num + " ");
        }
    }
}

// 24. Find all the divisors of a number.
import java.util.Scanner;
class FindDivisors {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        for (int i = 1; i <= num; i++) if (num % i == 0) System.out.print(i + " ");
    }
}

// 25. Find the GCD and LCM of two numbers.
import java.util.Scanner;
class GCDLCM {
    static int gcd(int a, int b) { return b == 0 ? a : gcd(b, a % b); }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt(), b = sc.nextInt();
        int gcd = gcd(a, b), lcm = (a * b) / gcd;
        System.out.println("GCD: " + gcd + " LCM: " + lcm);
    }
}

// 26. Check if a number is a perfect number within a range.
import java.util.Scanner;
class PerfectNumberRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt(), end = sc.nextInt();
        for (int num = start; num <= end; num++) {
            int sum = 0;
            for (int i = 1; i <= num / 2; i++) if (num % i == 0) sum += i;
            if (sum == num) System.out.print(num + " ");
        }
    }
}

// 27. Check whether an integer is positive, negative, or zero.
import java.util.Scanner;
class IntegerCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(num > 0 ? "Positive" : num < 0 ? "Negative" : "Zero");
    }
}

// 28. Determine the type of a triangle based on its angles.
import java.util.Scanner;
class TriangleType {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt(), b = sc.nextInt(), c = sc.nextInt();
        System.out.println(a + b + c == 180 ? (a == 90 || b == 90 || c == 90 ? "Right-angled" : (a > 90 || b > 90 || c > 90 ? "Obtuse" : "Acute")) : "Invalid");
    }
}

// 29. Find whether a number is a Fibonacci number within a range.
import java.util.Scanner;
class FibonacciInRange {
    static boolean isFibonacci(int n) {
        int a = 0, b = 1;
        while (b < n) { int temp = b; b = a + b; a = temp; }
        return b == n;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt(), end = sc.nextInt();
        for (int i = start; i <= end; i++) if (isFibonacci(i)) System.out.print(i + " ");
    }
}

// 30. Print all leap years within a given range.
import java.util.Scanner;
class LeapYearsInRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt(), end = sc.nextInt();
        for (int year = start; year <= end; year++)
            if ((year % 4 == 0 && year % 100 != 0) || year % 400 == 0)
                System.out.print(year + " ");
    }
}

// 31. Check whether a string is a valid palindrome.
import java.util.Scanner;
class ValidPalindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine().replaceAll("[^a-zA-Z0-9]", "").toLowerCase();
        System.out.println(str.equals(new StringBuilder(str).reverse().toString()) ? "Valid Palindrome" : "Not a Palindrome");
    }
}

// 32. Check for a specific pattern in a string using if-else.
import java.util.Scanner;
class PatternCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.next();
        System.out.println(str.contains("abc") ? "Pattern Found" : "Pattern Not Found");
    }
}

// 33. Check if a given day is a weekend or weekday.
import java.util.Scanner;
class WeekendWeekday {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String day = sc.next().toLowerCase();
        System.out.println(day.equals("saturday") || day.equals("sunday") ? "Weekend" : "Weekday");
    }
}

// 34. Check if a number is divisible by 7 or 11.
import java.util.Scanner;
class DivisibleBy7Or11 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        System.out.println(num % 7 == 0 || num % 11 == 0 ? "Divisible" : "Not Divisible");
    }
}

// 35. Print prime numbers within a range using nested conditions.
import java.util.Scanner;
class PrimeNumbersNested {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int start = sc.nextInt(), end = sc.nextInt();
        for (int num = start; num <= end; num++) {
            boolean isPrime = num > 1;
            for (int i = 2; i < num; i++) if (num % i == 0) isPrime = false;
            if (isPrime) System.out.print(num + " ");
        }
    }
}

// 36. Identify if an alphabet character is uppercase, lowercase, or non-alphabet.
import java.util.Scanner;
class AlphabetType {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0);
        System.out.println(Character.isUpperCase(ch) ? "Uppercase" : Character.isLowerCase(ch) ? "Lowercase" : "Not an Alphabet");
    }
}

// 37. Determine if a given number is a valid credit card number.
import java.util.Scanner;
class ValidCreditCard {
    static boolean isValid(long num) {
        String s = Long.toString(num);
        return s.length() >= 13 && s.length() <= 19;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        long num = sc.nextLong();
        System.out.println(isValid(num) ? "Valid Credit Card" : "Invalid Credit Card");
    }
}

// 38. Check if a given date is valid or invalid.
import java.util.Scanner;
class ValidDate {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int day = sc.nextInt(), month = sc.nextInt(), year = sc.nextInt();
        boolean valid = day > 0 && month > 0 && month <= 12 && year > 0 && day <= 31;
        System.out.println(valid ? "Valid Date" : "Invalid Date");
    }
}

// 39. Find the day of the week for a given date.
import java.time.LocalDate;
import java.util.Scanner;
class DayOfWeek {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int day = sc.nextInt(), month = sc.nextInt(), year = sc.nextInt();
        System.out.println(LocalDate.of(year, month, day).getDayOfWeek());
    }
}

// 40. Print multiplication tables for a given number using nested loops.
import java.util.Scanner;
class MultiplicationTable {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        for (int i = 1; i <= 10; i++) System.out.println(num + " x " + i + " = " + (num * i));
    }
}

// 41. Implement a simple calculator using switch case.
import java.util.Scanner;
class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a = sc.nextDouble(), b = sc.nextDouble();
        char op = sc.next().charAt(0);
        switch (op) {
            case '+': System.out.println(a + b); break;
            case '-': System.out.println(a - b); break;
            case '*': System.out.println(a * b); break;
            case '/': System.out.println(b != 0 ? a / b : "Cannot divide by zero"); break;
            default: System.out.println("Invalid operator");
        }
    }
}

// 42. Convert a number to its word equivalent (1 to 10) using switch.
import java.util.Scanner;
class NumberToWord {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        switch (num) {
            case 1: System.out.println("One"); break;
            case 2: System.out.println("Two"); break;
            case 3: System.out.println("Three"); break;
            case 4: System.out.println("Four"); break;
            case 5: System.out.println("Five"); break;
            case 6: System.out.println("Six"); break;
            case 7: System.out.println("Seven"); break;
            case 8: System.out.println("Eight"); break;
            case 9: System.out.println("Nine"); break;
            case 10: System.out.println("Ten"); break;
            default: System.out.println("Invalid number");
        }
    }
}

// 43. Find the day of the week using switch statement.
import java.util.Scanner;
class DayOfWeekSwitch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int day = sc.nextInt();
        switch (day) {
            case 1: System.out.println("Monday"); break;
            case 2: System.out.println("Tuesday"); break;
            case 3: System.out.println("Wednesday"); break;
            case 4: System.out.println("Thursday"); break;
            case 5: System.out.println("Friday"); break;
            case 6: System.out.println("Saturday"); break;
            case 7: System.out.println("Sunday"); break;
            default: System.out.println("Invalid day");
        }
    }
}

// 44. Convert a number to its Roman numeral equivalent using switch.
import java.util.Scanner;
class NumberToRoman {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        switch (num) {
            case 1: System.out.println("I"); break;
            case 2: System.out.println("II"); break;
            case 3: System.out.println("III"); break;
            case 4: System.out.println("IV"); break;
            case 5: System.out.println("V"); break;
            case 6: System.out.println("VI"); break;
            case 7: System.out.println("VII"); break;
            case 8: System.out.println("VIII"); break;
            case 9: System.out.println("IX"); break;
            case 10: System.out.println("X"); break;
            default: System.out.println("Invalid number");
        }
    }
}

// 45. Implement a basic menu-driven program using switch-case.
import java.util.Scanner;
class MenuProgram {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("1. Say Hello\n2. Say Goodbye\n3. Exit");
        int choice = sc.nextInt();
        switch (choice) {
            case 1: System.out.println("Hello!"); break;
            case 2: System.out.println("Goodbye!"); break;
            case 3: System.out.println("Exiting..."); break;
            default: System.out.println("Invalid choice");
        }
    }
}

// 46. Print all numbers from 1 to n in reverse using switch.
import java.util.Scanner;
class ReverseNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        switch (1) {
            case 1:
                for (int i = n; i >= 1; i--) System.out.print(i + " ");
                break;
        }
    }
}

// 47. Grade student marks using a switch-case statement.
import java.util.Scanner;
class GradeStudent {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();
        switch (marks / 10) {
            case 10:
            case 9: System.out.println("A"); break;
            case 8: System.out.println("B"); break;
            case 7: System.out.println("C"); break;
            case 6: System.out.println("D"); break;
            default: System.out.println("Fail");
        }
    }
}

// 48. Perform simple arithmetic operations using switch.
import java.util.Scanner;
class ArithmeticSwitch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a = sc.nextDouble(), b = sc.nextDouble();
        char op = sc.next().charAt(0);
        switch (op) {
            case '+': System.out.println(a + b); break;
            case '-': System.out.println(a - b); break;
            case '*': System.out.println(a * b); break;
            case '/': System.out.println(b != 0 ? a / b : "Cannot divide by zero"); break;
            default: System.out.println("Invalid operator");
        }
    }
}

// 49. Convert temperature from Celsius to Fahrenheit or vice versa using switch.
import java.util.Scanner;
class TemperatureConverter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char choice = sc.next().charAt(0);
        double temp = sc.nextDouble();
        switch (choice) {
            case 'C': System.out.println("Fahrenheit: " + (temp * 9/5 + 32)); break;
            case 'F': System.out.println("Celsius: " + ((temp - 32) * 5/9)); break;
            default: System.out.println("Invalid choice");
        }
    }
}

// 50. Find the number of days in a month using switch-case.
import java.util.Scanner;
class DaysInMonth {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int month = sc.nextInt();
        switch (month) {
            case 2: System.out.println("28 or 29 days"); break;
            case 4: case 6: case 9: case 11: System.out.println("30 days"); break;
            case 1: case 3: case 5: case 7: case 8: case 10: case 12: System.out.println("31 days"); break;
            default: System.out.println("Invalid month");
        }
    }
}

// 51. Implement a simple banking system with switch-case.
import java.util.Scanner;
class BankingSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double balance = 1000.0;
        System.out.println("1. Deposit\n2. Withdraw\n3. Check Balance");
        int choice = sc.nextInt();
        switch (choice) {
            case 1: balance += sc.nextDouble(); System.out.println("New Balance: " + balance); break;
            case 2: double amount = sc.nextDouble();
                    if (amount <= balance) balance -= amount;
                    else System.out.println("Insufficient funds");
                    System.out.println("New Balance: " + balance); break;
            case 3: System.out.println("Balance: " + balance); break;
            default: System.out.println("Invalid choice");
        }
    }
}

// 52. Determine the month name based on its number using switch-case.
import java.util.Scanner;
class MonthName {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int month = sc.nextInt();
        switch (month) {
            case 1: System.out.println("January"); break;
            case 2: System.out.println("February"); break;
            case 3: System.out.println("March"); break;
            case 4: System.out.println("April"); break;
            case 5: System.out.println("May"); break;
            case 6: System.out.println("June"); break;
            case 7: System.out.println("July"); break;
            case 8: System.out.println("August"); break;
            case 9: System.out.println("September"); break;
            case 10: System.out.println("October"); break;
            case 11: System.out.println("November"); break;
            case 12: System.out.println("December"); break;
            default: System.out.println("Invalid month");
        }
    }
}

// 53. Calculate the area of different shapes using switch-case.
import java.util.Scanner;
class AreaCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("1. Circle\n2. Rectangle\n3. Triangle");
        int choice = sc.nextInt();
        switch (choice) {
            case 1: double r = sc.nextDouble(); System.out.println("Area: " + (Math.PI * r * r)); break;
            case 2: double l = sc.nextDouble(), w = sc.nextDouble(); System.out.println("Area: " + (l * w)); break;
            case 3: double b = sc.nextDouble(), h = sc.nextDouble(); System.out.println("Area: " + (0.5 * b * h)); break;
            default: System.out.println("Invalid choice");
        }
    }
}

// 54. Implement a basic calculator with multiple operations.
import java.util.Scanner;
class BasicCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a = sc.nextDouble(), b = sc.nextDouble();
        char op = sc.next().charAt(0);
        switch (op) {
            case '+': System.out.println(a + b); break;
            case '-': System.out.println(a - b); break;
            case '*': System.out.println(a * b); break;
            case '/': System.out.println(b != 0 ? a / b : "Cannot divide by zero"); break;
            case '%': System.out.println(a % b); break;
            default: System.out.println("Invalid operator");
        }
    }
}

// 55. Determine if a given character is a vowel or consonant using switch-case.
import java.util.Scanner;
class VowelConsonant {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0);
        switch (Character.toLowerCase(ch)) {
            case 'a': case 'e': case 'i': case 'o': case 'u': System.out.println("Vowel"); break;
            default: System.out.println("Consonant");
        }
    }
}

// 56. Implement a simple menu system for shopping.
import java.util.Scanner;
class ShoppingMenu {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("1. Buy Shirt\n2. Buy Pants\n3. Exit");
        int choice = sc.nextInt();
        switch (choice) {
            case 1: System.out.println("Shirt added to cart"); break;
            case 2: System.out.println("Pants added to cart"); break;
            case 3: System.out.println("Exiting..."); break;
            default: System.out.println("Invalid choice");
        }
    }
}

// 57. Convert a time duration in minutes to hours and minutes.
import java.util.Scanner;
class TimeConverter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int minutes = sc.nextInt();
        System.out.println((minutes / 60) + " hours " + (minutes % 60) + " minutes");
    }
}

// 58. Implement a number to word converter (1-10) using switch.
import java.util.Scanner;
class NumberToWordSwitch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        switch (num) {
            case 1: System.out.println("One"); break;
            case 2: System.out.println("Two"); break;
            case 3: System.out.println("Three"); break;
            case 4: System.out.println("Four"); break;
            case 5: System.out.println("Five"); break;
            case 6: System.out.println("Six"); break;
            case 7: System.out.println("Seven"); break;
            case 8: System.out.println("Eight"); break;
            case 9: System.out.println("Nine"); break;
            case 10: System.out.println("Ten"); break;
            default: System.out.println("Invalid number");
        }
    }
}

// 59. Implement a traffic light system using switch.
import java.util.Scanner;
class TrafficLight {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String color = sc.next().toLowerCase();
        switch (color) {
            case "red": System.out.println("Stop"); break;
            case "yellow": System.out.println("Get Ready"); break;
            case "green": System.out.println("Go"); break;
            default: System.out.println("Invalid color");
        }
    }
}

// 60. Solve a quadratic equation using switch-case for the discriminant.
import java.util.Scanner;
class QuadraticEquation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double a = sc.nextDouble(), b = sc.nextDouble(), c = sc.nextDouble();
        double d = b * b - 4 * a * c;
        switch (d > 0 ? 1 : (d == 0 ? 0 : -1)) {
            case 1: System.out.println("Two real roots"); break;
            case 0: System.out.println("One real root"); break;
            case -1: System.out.println("No real roots"); break;
        }
    }
}


// 61. Print numbers from 1 to 10 using for loop.
class PrintNumbers {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) System.out.println(i);
    }
}

// 62. Print the multiplication table of a number using for loop.
import java.util.Scanner;
class MultiplicationTable {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for (int i = 1; i <= 10; i++) System.out.println(n + " x " + i + " = " + (n * i));
    }
}

// 63. Calculate the factorial of a number using a for loop.
import java.util.Scanner;
class Factorial {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        long fact = 1;
        for (int i = 1; i <= n; i++) fact *= i;
        System.out.println(fact);
    }
}

// 64. Print Fibonacci series up to n terms using for loop.
import java.util.Scanner;
class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(), a = 0, b = 1;
        for (int i = 0; i < n; i++) {
            System.out.print(a + " ");
            int temp = a + b;
            a = b;
            b = temp;
        }
    }
}

// 65. Sum of digits of a number using a for loop.
import java.util.Scanner;
class SumOfDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(), sum = 0;
        for (; n > 0; n /= 10) sum += n % 10;
        System.out.println(sum);
    }
}

// 66. Print prime numbers up to a given number using for loop.
import java.util.Scanner;
class PrimeNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for (int i = 2; i <= n; i++) {
            boolean isPrime = true;
            for (int j = 2; j * j <= i; j++) if (i % j == 0) { isPrime = false; break; }
            if (isPrime) System.out.print(i + " ");
        }
    }
}

// 67. Reverse a number using for loop.
import java.util.Scanner;
class ReverseNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(), rev = 0;
        for (; n > 0; n /= 10) rev = rev * 10 + n % 10;
        System.out.println(rev);
    }
}

// 68. Check whether a number is prime or not using a for loop.
import java.util.Scanner;
class PrimeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        boolean isPrime = n > 1;
        for (int i = 2; i * i <= n; i++) if (n % i == 0) { isPrime = false; break; }
        System.out.println(isPrime ? "Prime" : "Not Prime");
    }
}

// 69. Calculate the sum of even numbers from 1 to n using a for loop.
import java.util.Scanner;
class SumEvenNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(), sum = 0;
        for (int i = 2; i <= n; i += 2) sum += i;
        System.out.println(sum);
    }
}
