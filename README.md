# Armstrong-Numbers
Find Armstrong Numbers From 100 to 10000.
package Prog;

public class ArmstrongNumbers {
    public static void main(String[] args) {
        System.out.println("Amstrong numbers between 100 and 10000:");
        for (int num = 100; num <= 10000; num++) {
            if (isAmstrong(num)) {
                System.out.println(num);
            }
        }
    }

    public static boolean isAmstrong(int num) {
        int originalNumber = num;
        int numDigits = String.valueOf(num).length();
        int sum = 0;

        while (num != 0) {
            int digit = num % 10;
            sum += Math.pow(digit, numDigits);
            num /= 10;
        }

        return sum == originalNumber;
    }
}

