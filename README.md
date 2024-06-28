Reverse String 

import java.util.*;

public class ReverseString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String input = sc.nextLine();
        char[] ch = input.toCharArray();
        int left = 0;
        int right = ch.length- 1;

        while (left < right) {
            char temp = ch[left];
            ch[left] = ch[right];
            ch[right] = temp;
            left++;
            right--;
        }

        String reversed = new String(ch);
        System.out.println("Reversed string: " + reversed);
    }
}


Email Validation

import java.util.*;

public class EmailValidation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter an email address: ");
        String email = sc.nextLine();

        if (isValidEmail(email)) {
            System.out.println("Valid email address!");
        } else {
            System.out.println("Invalid email address!");
        }
    }

    public static boolean isValidEmail(String email) {
        return email.contains("@") && email.contains(".") && email.contains("gmail");
        		
    }
}

Palindrome

import java.util.*;

public class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String A= sc.nextLine();

        
        A= A.toLowerCase();

        if (isPalindrome(A)) {
            System.out.println("Yes, it's a palindrome!");
        } else {
            System.out.println("No, it's not a palindrome.");
        }
    }

    public static boolean isPalindrome(String str) {
        int left = 0;
        int right = str.length() - 1;

        while (left < right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false; 
            }
            left++;
            right--;
        }
        return true; 
    }
}

Replace Character

import java.util.*;

public class ReplaceCharacter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String originalString = sc.next();

        System.out.print("Enter the index where you want to replace a character: ");
        int index = sc.nextInt();

        System.out.print("Enter the new character: ");
        char newChar = sc.next().charAt(0);

        StringBuilder newstring = new StringBuilder(originalString);
        newstring.setCharAt(index, newChar);

        System.out.println("Modified string: " + newstring.toString());
    }
}

String_methods

import java.util.*;

public class String_methods{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String H = "HEMANSU";

        int length = H.length();
        System.out.println("Length of the string: " + length);

        boolean isEmpty = H.isEmpty();
        System.out.println("Is the string empty? " + isEmpty);

        int index = 1;
        char Index = H.charAt(index);
        System.out.println("Character at index " + index + ": " + Index);

        String uppercase = H.toUpperCase();
        System.out.println("Uppercase string: " + uppercase);

        char oldChar = 'E'; 
        char newChar = 'I'; 
        String replacedString = H.replace(oldChar, newChar);
        System.out.println("String after replacing '" + oldChar + "' with '" + newChar + "': " + replacedString);

    }
}
