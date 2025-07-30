# StringCode

1. Reverse a String

import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String reversed = new StringBuilder(s).reverse().toString();
        System.out.println("Reversed: " + reversed);
        sc.close();
    }
}
2. Check if String is Palindrome

import java.util.Scanner;

public class PalindromeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String rev = new StringBuilder(s).reverse().toString();
        if (s.equalsIgnoreCase(rev))
            System.out.println("Palindrome");
        else
            System.out.println("Not a palindrome");
        sc.close();
    }
}
3. Count Vowels in String

import java.util.Scanner;

public class CountVowels {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toLowerCase().toCharArray()) {
            if("aeiou".indexOf(c) != -1) count++;
        }
        System.out.println("Number of vowels: " + count);
        sc.close();
    }
}
4. Count Consonants in String

import java.util.Scanner;

public class CountConsonants {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toLowerCase().toCharArray()) {
            if (c >= 'a' && c <= 'z' && "aeiou".indexOf(c) == -1) count++;
        }
        System.out.println("Number of consonants: " + count);
        sc.close();
    }
}
5. Count Words in a String

import java.util.Scanner;

public class CountWords {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine().trim();
        if (s.isEmpty()) {
            System.out.println("Word count: 0");
        } else {
            String[] words = s.split("\\s+");
            System.out.println("Word count: " + words.length);
        }
        sc.close();
    }
}
6. Find Largest Word in String

import java.util.Scanner;

public class LargestWord {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine();
        String[] words = s.split("\\s+");
        String largest = "";
        for(String w : words) {
            if (w.length() > largest.length()) largest = w;
        }
        System.out.println("Largest word: " + largest);
        sc.close();
    }
}
7. Check if Two Strings are Anagrams
import java.util.Arrays;
import java.util.Scanner;

public class AnagramCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first string: ");
        String s1 = sc.nextLine().replaceAll("\\s", "").toLowerCase();
        System.out.print("Enter second string: ");
        String s2 = sc.nextLine().replaceAll("\\s", "").toLowerCase();
        
        if (s1.length() != s2.length()) {
            System.out.println("Not anagrams");
        } else {
            char[] a1 = s1.toCharArray();
            char[] a2 = s2.toCharArray();
            Arrays.sort(a1);
            Arrays.sort(a2);
            if (Arrays.equals(a1, a2))
                System.out.println("Anagrams");
            else
                System.out.println("Not anagrams");
        }
        sc.close();
    }
}
8. Remove Duplicates from String
import java.util.LinkedHashSet;
import java.util.Scanner;

public class RemoveDuplicates {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        LinkedHashSet<Character> set = new LinkedHashSet<>();
        for(char c : s.toCharArray()) set.add(c);
        StringBuilder sb = new StringBuilder();
        for(char c : set) sb.append(c);
        System.out.println("Without duplicates: " + sb);
        sc.close();
    }
}
9. Count Occurrences of Character
import java.util.Scanner;

public class CharOccurrences {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter character to count: ");
        char ch = sc.nextLine().charAt(0);
        int count = 0;
        for(char c : s.toCharArray()) {
            if(c == ch) count++;
        }
        System.out.println(ch + " occurs " + count + " times.");
        sc.close();
    }
}
10. Replace Spaces with Underscores
import java.util.Scanner;

public class ReplaceSpaces {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String replaced = s.replace(' ', '_');
        System.out.println("Modified string: " + replaced);
        sc.close();
    }
}
11. Convert String to Uppercase
import java.util.Scanner;

public class ToUpperCase {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("Uppercase: " + s.toUpperCase());
        sc.close();
    }
}
12. Convert String to Lowercase
import java.util.Scanner;

public class ToLowerCase {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("Lowercase: " + s.toLowerCase());
        sc.close();
    }
}
13. Capitalize First Letter of Each Word
import java.util.Scanner;

public class CapitalizeWords {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine();
        String[] words = s.split("\\s+");
        StringBuilder sb = new StringBuilder();
        for(String w : words) {
            if (w.length() > 0) {
                sb.append(Character.toUpperCase(w.charAt(0)))
                  .append(w.substring(1).toLowerCase())
                  .append(" ");
            }
        }
        System.out.println("Capitalized: " + sb.toString().trim());
        sc.close();
    }
}
14. Check if String Contains Only Digits
import java.util.Scanner;

public class IsNumeric {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        if(s.matches("\\d+"))
            System.out.println("String contains only digits");
        else
            System.out.println("String contains non-digit characters");
        sc.close();
    }
}
15. Remove All Whitespaces
import java.util.Scanner;

public class RemoveWhitespaces {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String result = s.replaceAll("\\s+", "");
        System.out.println("Without whitespaces: " + result);
        sc.close();
    }
}
16. Find the First Non-Repeating Character
import java.util.LinkedHashMap;
import java.util.Map;
import java.util.Scanner;

public class FirstNonRepeatingChar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        Map<Character, Integer> countMap = new LinkedHashMap<>();
        for (char c : s.toCharArray()) {
            countMap.put(c, countMap.getOrDefault(c, 0) + 1);
        }
        char result = 0;
        for (Map.Entry<Character, Integer> entry : countMap.entrySet()) {
            if (entry.getValue() == 1) {
                result = entry.getKey();
                break;
            }
        }
        if (result != 0)
            System.out.println("First non-repeating character: " + result);
        else
            System.out.println("No non-repeating character found");
        sc.close();
    }
}
17. Check if Two Strings are Rotations

import java.util.Scanner;

public class RotationCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first string: ");
        String s1 = sc.nextLine();
        System.out.print("Enter second string: ");
        String s2 = sc.nextLine();
        if (s1.length() == s2.length() && (s1 + s1).contains(s2))
            System.out.println("Strings are rotations of each other");
        else
            System.out.println("Strings are NOT rotations");
        sc.close();
    }
}
18. Count Number of Sentences in a String
import java.util.Scanner;

public class SentenceCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter text: ");
        String s = sc.nextLine().trim();
        if (s.isEmpty()) {
            System.out.println("Sentence count: 0");
        } else {
            String[] sentences = s.split("[.!?]+");
            System.out.println("Sentence count: " + sentences.length);
        }
        sc.close();
    }
}
19. Find the Index of First Vowel

import java.util.Scanner;

public class FirstVowelIndex {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine().toLowerCase();
        int index = -1;
        for (int i = 0; i < s.length(); i++) {
            if ("aeiou".indexOf(s.charAt(i)) != -1) {
                index = i;
                break;
            }
        }
        if (index != -1)
            System.out.println("First vowel at index: " + index);
        else
            System.out.println("No vowels found");
        sc.close();
    }
}
20. Count Occurrences of Each Character

import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class CharOccurrencesCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        Map<Character, Integer> map = new HashMap<>();
        for(char c : s.toCharArray()) {
            map.put(c, map.getOrDefault(c, 0) + 1);
        }
        System.out.println("Character occurrences:");
        for(Map.Entry<Character, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
        sc.close();
    }
}
21. Remove All Non-Alphanumeric Characters
import java.util.Scanner;

public class RemoveNonAlphanumeric {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String cleaned = s.replaceAll("[^a-zA-Z0-9]", "");
        System.out.println("Cleaned string: " + cleaned);
        sc.close();
    }
}
22. Count Number of Digits in String
import java.util.Scanner;

public class DigitCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toCharArray()) {
            if (Character.isDigit(c)) count++;
        }
        System.out.println("Number of digits: " + count);
        sc.close();
    }
}
23. Remove Duplicate Words from Sentence
import java.util.LinkedHashSet;
import java.util.Scanner;

public class RemoveDuplicateWords {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine();
        String[] words = s.split("\\s+");
        LinkedHashSet<String> set = new LinkedHashSet<>();
        for(String w : words) set.add(w);
        System.out.println("After removing duplicates: " + String.join(" ", set));
        sc.close();
    }
}
24. Reverse Each Word in Sentence
import java.util.Scanner;

public class ReverseEachWord {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine();
        String[] words = s.split("\\s+");
        StringBuilder result = new StringBuilder();
        for(String w : words) {
            result.append(new StringBuilder(w).reverse().toString()).append(" ");
        }
        System.out.println("Reversed words: " + result.toString().trim());
        sc.close();
    }
}
25. Check if String is a Valid Email (Simple Regex)
import java.util.Scanner;

public class EmailValidator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter email: ");
        String email = sc.nextLine();
        if(email.matches("^[\\w.-]+@[\\w.-]+\\.\\w{2,}$"))
            System.out.println("Valid email");
        else
            System.out.println("Invalid email");
        sc.close();
    }
}
26. Count Number of Special Characters
import java.util.Scanner;

public class SpecialCharCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toCharArray()) {
            if(!Character.isLetterOrDigit(c) && !Character.isWhitespace(c)) count++;
        }
        System.out.println("Special characters count: " + count);
        sc.close();
    }
}
27. Check if String is a Valid IPv4 Address
import java.util.Scanner;

public class IPv4Validator {
    public static boolean isValidIPv4(String ip) {
        String[] parts = ip.split("\\.");
        if(parts.length != 4) return false;
        for(String p : parts) {
            try {
                int val = Integer.parseInt(p);
                if(val < 0 || val > 255) return false;
            } catch(NumberFormatException e) {
                return false;
            }
        }
        return true;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter IP address: ");
        String ip = sc.nextLine();
        System.out.println(isValidIPv4(ip) ? "Valid IPv4" : "Invalid IPv4");
        sc.close();
    }
}
28. Find the Longest Palindromic Substring (Simple Approach)
import java.util.Scanner;

public class LongestPalindromeSubstring {
    public static String longestPalindrome(String s) {
        if(s == null || s.length() < 1) return "";
        int start = 0, end = 0;
        for(int i=0; i < s.length(); i++) {
            int len1 = expandAroundCenter(s, i, i);
            int len2 = expandAroundCenter(s, i, i+1);
            int len = Math.max(len1, len2);
            if(len > end - start) {
                start = i - (len -1)/2;
                end = i + len/2;
            }
        }
        return s.substring(start, end+1);
    }
    private static int expandAroundCenter(String s, int left, int right) {
        while(left >=0 && right < s.length() && s.charAt(left) == s.charAt(right)) {
            left--;
            right++;
        }
        return right - left -1;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("Longest palindromic substring: " + longestPalindrome(s));
        sc.close();
    }
}
29. Check if String Ends With Another String
import java.util.Scanner;

public class EndsWithCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter main string: ");
        String main = sc.nextLine();
        System.out.print("Enter suffix string: ");
        String suffix = sc.nextLine();
        System.out.println(main.endsWith(suffix) ? "Ends with suffix" : "Does not end with suffix");
        sc.close();
    }
}
30. Count the Number of Lines in a Multiline String
public class LineCount {
    public static void main(String[] args) {
        String multiline = "Hello\nWorld\nThis is a test\nJava";
        String[] lines = multiline.split("\\r?\\n");
        System.out.println("Number of lines: " + lines.length);
    }
}
31. Check if String Starts with Another String
import java.util.Scanner;

public class StartsWithCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter main string: ");
        String main = sc.nextLine();
        System.out.print("Enter prefix string: ");
        String prefix = sc.nextLine();
        System.out.println(main.startsWith(prefix) ? "Starts with prefix" : "Does not start with prefix");
        sc.close();
    }
}
32. Count Number of Uppercase Letters
import java.util.Scanner;

public class UppercaseCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toCharArray()) {
            if(Character.isUpperCase(c)) count++;
        }
        System.out.println("Uppercase letters: " + count);
        sc.close();
    }
}
33. Count Number of Lowercase Letters
import java.util.Scanner;

public class LowercaseCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toCharArray()) {
            if(Character.isLowerCase(c)) count++;
        }
        System.out.println("Lowercase letters: " + count);
        sc.close();
    }
}
34. Find All Indexes of a Character
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class AllIndexesOfChar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter character: ");
        char ch = sc.nextLine().charAt(0);
        List<Integer> indexes = new ArrayList<>();
        for(int i=0; i<s.length(); i++) {
            if(s.charAt(i) == ch) indexes.add(i);
        }
        if(indexes.isEmpty())
            System.out.println("Character not found");
        else
            System.out.println("Character found at indexes: " + indexes);
        sc.close();
    }
}
35. Convert String to Char Array
import java.util.Arrays;
import java.util.Scanner;

public class StringToCharArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        char[] chars = s.toCharArray();
        System.out.println("Char array: " + Arrays.toString(chars));
        sc.close();
    }
}
36. Check if String Contains Another String (Substring)
import java.util.Scanner;

public class ContainsSubstring {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter main string: ");
        String main = sc.nextLine();
        System.out.print("Enter substring: ");
        String sub = sc.nextLine();
        System.out.println(main.contains(sub) ? "Contains substring" : "Does not contain substring");
        sc.close();
    }
}
37. Remove First and Last Character
import java.util.Scanner;

public class RemoveFirstLastChar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string (length >= 2): ");
        String s = sc.nextLine();
        if (s.length() < 2) {
            System.out.println("String too short");
        } else {
            System.out.println("Result: " + s.substring(1, s.length() - 1));
        }
        sc.close();
    }
}
38. Swap First and Last Characters
import java.util.Scanner;

public class SwapFirstLastChar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string (length >= 2): ");
        String s = sc.nextLine();
        if(s.length() < 2) {
            System.out.println("String too short");
        } else {
            String swapped = s.charAt(s.length()-1) + s.substring(1, s.length()-1) + s.charAt(0);
            System.out.println("Swapped string: " + swapped);
        }
        sc.close();
    }
}
39. Repeat a String N Times
import java.util.Scanner;

public class RepeatString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter number of repetitions: ");
        int n = sc.nextInt();
        StringBuilder sb = new StringBuilder();
        for(int i=0; i<n; i++) {
            sb.append(s);
        }
        System.out.println("Repeated string: " + sb.toString());
        sc.close();
    }
}
40. Check if String Contains Only Letters
import java.util.Scanner;

public class OnlyLettersCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        if(s.matches("[a-zA-Z]+"))
            System.out.println("String contains only letters");
        else
            System.out.println("String contains other characters");
        sc.close();
    }
}
41. Remove Leading and Trailing Spaces
import java.util.Scanner;

public class TrimSpaces {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string with spaces: ");
        String s = sc.nextLine();
        System.out.println("Trimmed string: '" + s.trim() + "'");
        sc.close();
    }
}
42. Print String in Alternate Characters

import java.util.Scanner;

public class AlternateCharacters {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        StringBuilder sb = new StringBuilder();
        for(int i=0; i<s.length(); i+=2) {
            sb.append(s.charAt(i));
        }
        System.out.println("Alternate characters: " + sb.toString());
        sc.close();
    }
}
43. Check if String is Empty or Blank
import java.util.Scanner;
public class EmptyOrBlank {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        if(s.isEmpty())
            System.out.println("String is empty");
        else if(s.isBlank())
            System.out.println("String is blank");
        else
            System.out.println("String is not empty or blank");
        sc.close();
    }
}
44. Extract Substring from Index i to j
import java.util.Scanner;

public class SubstringExtract {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter start index: ");
        int start = sc.nextInt();
        System.out.print("Enter end index: ");
        int end = sc.nextInt();
        if(start < 0 || end > s.length() || start > end) {
            System.out.println("Invalid indexes");
        } else {
            System.out.println("Substring: " + s.substring(start, end));
        }
        sc.close();
    }
}
45. Compare Two Strings Ignoring Case
import java.util.Scanner;

public class CompareIgnoreCase {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first string: ");
        String s1 = sc.nextLine();
        System.out.print("Enter second string: ");
        String s2 = sc.nextLine();
        System.out.println(s1.equalsIgnoreCase(s2) ? "Strings are equal ignoring case" : "Strings are not equal");
        sc.close();
    }
}
46. Insert a String into Another String at Given Position

import java.util.Scanner;

public class InsertString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter original string: ");
        String original = sc.nextLine();
        System.out.print("Enter string to insert: ");
        String insert = sc.nextLine();
        System.out.print("Enter position (0-based index): ");
        int pos = sc.nextInt();
        if(pos < 0 || pos > original.length()) {
            System.out.println("Invalid position");
        } else {
            String result = original.substring(0, pos) + insert + original.substring(pos);
            System.out.println("Result: " + result);
        }
        sc.close();
    }
}
47. Remove All Occurrences of a Character
import java.util.Scanner;

public class RemoveCharacter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter character to remove: ");
        char ch = sc.nextLine().charAt(0);
        String result = s.replace(String.valueOf(ch), "");
        System.out.println("Result: " + result);
        sc.close();
    }
}
48. Convert String to ASCII Values Array
import java.util.Scanner;

public class StringToAscii {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int[] ascii = new int[s.length()];
        for(int i=0; i<s.length(); i++) {
            ascii[i] = (int) s.charAt(i);
        }
        System.out.print("ASCII values: ");
        for(int val : ascii) System.out.print(val + " ");
        sc.close();
    }
}
49. Check if String is a Valid URL (Simple Regex)
import java.util.Scanner;

public class URLValidator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter URL: ");
        String url = sc.nextLine();
        String regex = "^(https?://)?([\\w.-]+)\\.([a-z]{2,6})([/\\w .-]*)*/?$";
        System.out.println(url.matches(regex) ? "Valid URL" : "Invalid URL");
        sc.close();
    }
}
50. Extract Numbers from String
import java.util.Scanner;

public class ExtractNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String numbers = s.replaceAll("[^0-9]", "");
        System.out.println("Extracted numbers: " + numbers);
        sc.close();
    }
}
51. Count Number of Words Starting with Vowel

import java.util.Scanner;

public class WordsStartingWithVowel {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine().toLowerCase();
        String[] words = s.split("\\s+");
        int count = 0;
        for(String w : words) {
            if(w.length() > 0 && "aeiou".indexOf(w.charAt(0)) != -1) count++;
        }
        System.out.println("Words starting with vowel: " + count);
        sc.close();
    }
}
52. Count Number of Words Ending with Consonant
import java.util.Scanner;

public class WordsEndingWithConsonant {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine().toLowerCase();
        String[] words = s.split("\\s+");
        int count = 0;
        for(String w : words) {
            if(w.length() > 0) {
                char last = w.charAt(w.length()-1);
                if("bcdfghjklmnpqrstvwxyz".indexOf(last) != -1) count++;
            }
        }
        System.out.println("Words ending with consonant: " + count);
        sc.close();
    }
}
53. Reverse Words in a Sentence

import java.util.Scanner;

public class ReverseWordsInSentence {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine();
        String[] words = s.split("\\s+");
        StringBuilder sb = new StringBuilder();
        for(int i=words.length-1; i>=0; i--) {
            sb.append(words[i]).append(" ");
        }
        System.out.println("Reversed words: " + sb.toString().trim());
        sc.close();
    }
}
54. Capitalize First Letter of Each Word

import java.util.Scanner;

public class CapitalizeWords {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String s = sc.nextLine().toLowerCase();
        String[] words = s.split("\\s+");
        StringBuilder sb = new StringBuilder();
        for(String w : words) {
            if(w.length() > 0) {
                sb.append(Character.toUpperCase(w.charAt(0))).append(w.substring(1)).append(" ");
            }
        }
        System.out.println("Capitalized sentence: " + sb.toString().trim());
        sc.close();
    }
}
55. Remove Duplicate Characters from String

import java.util.LinkedHashSet;
import java.util.Scanner;
import java.util.Set;

public class RemoveDuplicateChars {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        Set<Character> set = new LinkedHashSet<>();
        for(char c : s.toCharArray()) set.add(c);
        StringBuilder sb = new StringBuilder();
        for(char c : set) sb.append(c);
        System.out.println("String without duplicates: " + sb.toString());
        sc.close();
    }
}
56. Find Frequency of Each Character

import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class CharFrequency {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        Map<Character, Integer> freq = new HashMap<>();
        for(char c : s.toCharArray()) {
            freq.put(c, freq.getOrDefault(c, 0) + 1);
        }
        for(Map.Entry<Character, Integer> entry : freq.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
        sc.close();
    }
}
57. Check if Two Strings are Anagrams
import java.util.Arrays;
import java.util.Scanner;

public class AnagramCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first string: ");
        String s1 = sc.nextLine().replaceAll("\\s", "").toLowerCase();
        System.out.print("Enter second string: ");
        String s2 = sc.nextLine().replaceAll("\\s", "").toLowerCase();
        char[] arr1 = s1.toCharArray();
        char[] arr2 = s2.toCharArray();
        Arrays.sort(arr1);
        Arrays.sort(arr2);
        System.out.println(Arrays.equals(arr1, arr2) ? "Anagrams" : "Not anagrams");
        sc.close();
    }
}
58. Count Vowels and Consonants
import java.util.Scanner;

public class VowelConsonantCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine().toLowerCase();
        int vowels = 0, consonants = 0;
        for(char c : s.toCharArray()) {
            if(c >= 'a' && c <= 'z') {
                if("aeiou".indexOf(c) != -1) vowels++;
                else consonants++;
            }
        }
        System.out.println("Vowels: " + vowels);
        System.out.println("Consonants: " + consonants);
        sc.close();
    }
}
59. Find First Non-Repeated Character
import java.util.LinkedHashMap;
import java.util.Map;
import java.util.Scanner;

public class FirstNonRepeatedChar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        Map<Character, Integer> countMap = new LinkedHashMap<>();
        for(char c : s.toCharArray()) {
            countMap.put(c, countMap.getOrDefault(c, 0) + 1);
        }
        for(Map.Entry<Character, Integer> entry : countMap.entrySet()) {
            if(entry.getValue() == 1) {
                System.out.println("First non-repeated character: " + entry.getKey());
                break;
            }
        }
        sc.close();
    }
}
60. Check if String Contains Only Digits

import java.util.Scanner;

public class OnlyDigitsCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println(s.matches("\\d+") ? "String contains only digits" : "String contains non-digit characters");
        sc.close();
    }
}
61. Count Number of Sentences in a String

import java.util.Scanner;

public class SentenceCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter text: ");
        String text = sc.nextLine();
        String[] sentences = text.split("[.!?]+");
        System.out.println("Number of sentences: " + sentences.length);
        sc.close();
    }
}
62. Check if Two Strings are Rotations of Each Other
java
Copy
Edit
import java.util.Scanner;

public class RotationCheck {
    public static boolean isRotation(String s1, String s2) {
        if(s1.length() != s2.length()) return false;
        String temp = s1 + s1;
        return temp.contains(s2);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first string: ");
        String s1 = sc.nextLine();
        System.out.print("Enter second string: ");
        String s2 = sc.nextLine();
        System.out.println(isRotation(s1, s2) ? "Strings are rotations" : "Not rotations");
        sc.close();
    }
}
63. Remove All Spaces from a String
java
Copy
Edit
import java.util.Scanner;

public class RemoveSpaces {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string with spaces: ");
        String s = sc.nextLine();
        System.out.println("String without spaces: " + s.replace(" ", ""));
        sc.close();
    }
}
64. Find the Longest Word in a Sentence
java
Copy
Edit
import java.util.Scanner;

public class LongestWord {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String sentence = sc.nextLine();
        String[] words = sentence.split("\\s+");
        String longest = "";
        for(String w : words) {
            if(w.length() > longest.length()) longest = w;
        }
        System.out.println("Longest word: " + longest);
        sc.close();
    }
}
65. Convert String to Title Case
java
Copy
Edit
import java.util.Scanner;

public class TitleCase {
    public static String toTitleCase(String input) {
        String[] words = input.toLowerCase().split("\\s+");
        StringBuilder sb = new StringBuilder();
        for(String w : words) {
            if(w.length() > 0) {
                sb.append(Character.toUpperCase(w.charAt(0))).append(w.substring(1)).append(" ");
            }
        }
        return sb.toString().trim();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String input = sc.nextLine();
        System.out.println("Title Case: " + toTitleCase(input));
        sc.close();
    }
}
66. Check if String Contains Only Alphabet and Numbers
java
Copy
Edit
import java.util.Scanner;

public class AlphaNumericCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println(s.matches("[a-zA-Z0-9]+") ? "Alphanumeric only" : "Contains other characters");
        sc.close();
    }
}
67. Find the Smallest Word in a Sentence
java
Copy
Edit
import java.util.Scanner;

public class SmallestWord {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String sentence = sc.nextLine();
        String[] words = sentence.split("\\s+");
        String smallest = words[0];
        for(String w : words) {
            if(w.length() < smallest.length()) smallest = w;
        }
        System.out.println("Smallest word: " + smallest);
        sc.close();
    }
}
68. Check if String is Palindrome (Ignore Case and Spaces)
java
Copy
Edit
import java.util.Scanner;

public class PalindromeIgnoreCaseSpaces {
    public static boolean isPalindrome(String s) {
        s = s.replaceAll("\\s+", "").toLowerCase();
        int left = 0, right = s.length()-1;
        while(left < right) {
            if(s.charAt(left) != s.charAt(right)) return false;
            left++; right--;
        }
        return true;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println(isPalindrome(s) ? "Palindrome" : "Not a palindrome");
        sc.close();
    }
}
69. Count the Number of Digits in a String
java
Copy
Edit
import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int count = 0;
        for(char c : s.toCharArray()) {
            if(Character.isDigit(c)) count++;
        }
        System.out.println("Number of digits: " + count);
        sc.close();
    }
}
70. Reverse Each Word in a Sentence
java
Copy
Edit
import java.util.Scanner;

public class ReverseEachWord {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String sentence = sc.nextLine();
        String[] words = sentence.split("\\s+");
        StringBuilder sb = new StringBuilder();
        for(String w : words) {
            sb.append(new StringBuilder(w).reverse().toString()).append(" ");
        }
        System.out.println("Reversed each word: " + sb.toString().trim());
        sc.close();
    }
}
71. Remove All Non-Alphanumeric Characters
java
Copy
Edit
import java.util.Scanner;

public class RemoveNonAlphanumeric {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        String result = s.replaceAll("[^a-zA-Z0-9]", "");
        System.out.println("After removing non-alphanumeric: " + result);
        sc.close();
    }
}
72. Check if String Contains Any Special Characters
java
Copy
Edit
import java.util.Scanner;

public class SpecialCharCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println(s.matches(".*[^a-zA-Z0-9 ].*") ? "Contains special characters" : "No special characters");
        sc.close();
    }
}
73. Find the Index of First Vowel
java
Copy
Edit
import java.util.Scanner;

public class FirstVowelIndex {
    public static int firstVowelIndex(String s) {
        s = s.toLowerCase();
        for(int i = 0; i < s.length(); i++) {
            if("aeiou".indexOf(s.charAt(i)) != -1) return i;
        }
        return -1;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int index = firstVowelIndex(s);
        System.out.println(index != -1 ? "First vowel at index: " + index : "No vowel found");
        sc.close();
    }
}
74. Remove Consecutive Duplicate Characters
java
Copy
Edit
import java.util.Scanner;

public class RemoveConsecutiveDuplicates {
    public static String removeDuplicates(String s) {
        if(s.length() < 2) return s;
        StringBuilder sb = new StringBuilder();
        sb.append(s.charAt(0));
        for(int i=1; i<s.length(); i++) {
            if(s.charAt(i) != s.charAt(i-1)) sb.append(s.charAt(i));
        }
        return sb.toString();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("After removing duplicates: " + removeDuplicates(s));
        sc.close();
    }
}
75. Find the Second Most Frequent Character
java
Copy
Edit
import java.util.*;

public class SecondMostFrequentChar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        Map<Character, Integer> freq = new HashMap<>();
        for(char c : s.toCharArray()) {
            freq.put(c, freq.getOrDefault(c, 0) + 1);
        }
        List<Map.Entry<Character, Integer>> list = new ArrayList<>(freq.entrySet());
        list.sort((a,b) -> b.getValue() - a.getValue());
        if(list.size() < 2)
            System.out.println("No second most frequent character");
        else
            System.out.println("Second most frequent character: " + list.get(1).getKey());
        sc.close();
    }
}
76. Convert String to Binary Representation
java
Copy
Edit
import java.util.Scanner;

public class StringToBinary {
    public static String toBinary(String s) {
        StringBuilder sb = new StringBuilder();
        for(char c : s.toCharArray()) {
            sb.append(String.format("%8s", Integer.toBinaryString(c)).replace(' ', '0')).append(" ");
        }
        return sb.toString().trim();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("Binary representation: " + toBinary(s));
        sc.close();
    }
}
77. Count Occurrences of Each Word
java
Copy
Edit
import java.util.*;

public class WordFrequency {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String sentence = sc.nextLine().toLowerCase();
        String[] words = sentence.split("\\s+");
        Map<String, Integer> freq = new HashMap<>();
        for(String w : words) {
            freq.put(w, freq.getOrDefault(w, 0) + 1);
        }
        for(Map.Entry<String, Integer> e : freq.entrySet()) {
            System.out.println(e.getKey() + ": " + e.getValue());
        }
        sc.close();
    }
}
78. Count Number of Palindromic Words in a Sentence
java
Copy
Edit
import java.util.Scanner;

public class PalindromicWordsCount {
    public static boolean isPalindrome(String s) {
        int left=0, right=s.length()-1;
        while(left < right) {
            if(s.charAt(left) != s.charAt(right)) return false;
            left++; right--;
        }
        return true;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String sentence = sc.nextLine().toLowerCase();
        String[] words = sentence.split("\\s+");
        int count=0;
        for(String w : words) {
            if(isPalindrome(w)) count++;
        }
        System.out.println("Number of palindromic words: " + count);
        sc.close();
    }
}
79. Replace First Occurrence of a Substring
java
Copy
Edit
import java.util.Scanner;

public class ReplaceFirstOccurrence {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter substring to replace: ");
        String target = sc.nextLine();
        System.out.print("Enter replacement: ");
        String replacement = sc.nextLine();
        System.out.println("Result: " + s.replaceFirst(target, replacement));
        sc.close();
    }
}
80. Check if String is Valid Email Format (Basic)
java
Copy
Edit
import java.util.Scanner;

public class EmailValidation {
    public static boolean isValidEmail(String email) {
        return email.matches("^[\\w._%+-]+@[\\w.-]+\\.[a-zA-Z]{2,6}$");
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter email: ");
        String email = sc.nextLine();
        System.out.println(isValidEmail(email) ? "Valid Email" : "Invalid Email");
        sc.close();
    }
}
81. Find All Duplicate Words in a Sentence
java
Copy
Edit
import java.util.*;

public class DuplicateWords {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String[] words = sc.nextLine().toLowerCase().split("\\s+");
        Map<String, Integer> freq = new HashMap<>();
        for(String w : words) freq.put(w, freq.getOrDefault(w, 0) + 1);
        System.out.println("Duplicate words:");
        for(Map.Entry<String, Integer> e : freq.entrySet()) {
            if(e.getValue() > 1) System.out.println(e.getKey());
        }
        sc.close();
    }
}
82. Count Number of Uppercase and Lowercase Letters
java
Copy
Edit
import java.util.Scanner;

public class CaseCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        int upper=0, lower=0;
        for(char c : s.toCharArray()) {
            if(Character.isUpperCase(c)) upper++;
            else if(Character.isLowerCase(c)) lower++;
        }
        System.out.println("Uppercase letters: " + upper);
        System.out.println("Lowercase letters: " + lower);
        sc.close();
    }
}
83. Insert a Character at a Given Position
java
Copy
Edit
import java.util.Scanner;

public class InsertChar {
    public static String insertChar(String s, char c, int pos) {
        if(pos < 0 || pos > s.length()) return s;
        return s.substring(0, pos) + c + s.substring(pos);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.print("Enter character to insert: ");
        char c = sc.nextLine().charAt(0);
        System.out.print("Enter position: ");
        int pos = sc.nextInt();
        System.out.println("Result: " + insertChar(s, c, pos));
        sc.close();
    }
}
84. Find the Longest Palindromic Substring (Brute Force)
java
Copy
Edit
import java.util.Scanner;

public class LongestPalindromicSubstring {
    public static boolean isPalindrome(String s) {
        int left=0, right=s.length()-1;
        while(left < right) {
            if(s.charAt(left) != s.charAt(right)) return false;
            left++; right--;
        }
        return true;
    }
    public static String longestPalindrome(String s) {
        String longest = "";
        for(int i=0; i<s.length(); i++) {
            for(int j=i+1; j<=s.length(); j++) {
                String sub = s.substring(i,j);
                if(isPalindrome(sub) && sub.length() > longest.length()) {
                    longest = sub;
                }
            }
        }
        return longest;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("Longest palindromic substring: " + longestPalindrome(s));
        sc.close();
    }
}
85. Count Number of Words Starting with a Vowel
java
Copy
Edit
import java.util.Scanner;

public class WordsStartingWithVowel {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter sentence: ");
        String[] words = sc.nextLine().toLowerCase().split("\\s+");
        int count=0;
        for(String w : words) {
            if(w.length() > 0 && "aeiou".indexOf(w.charAt(0)) != -1) count++;
        }
        System.out.println("Words starting with vowel: " + count);
        sc.close();
    }
}
86. Toggle Case of Each Character
java
Copy
Edit
import java.util.Scanner;

public class ToggleCase {
    public static String toggleCase(String s) {
        StringBuilder sb = new StringBuilder();
        for(char c : s.toCharArray()) {
            if(Character.isUpperCase(c)) sb.append(Character.toLowerCase(c));
            else if(Character.isLowerCase(c)) sb.append(Character.toUpperCase(c));
            else sb.append(c);
        }
        return sb.toString();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("Toggled case: " + toggleCase(s));
        sc.close();
    }
}
87. Check if String Contains Only Whitespaces

import java.util.Scanner;

public class OnlyWhitespace {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println(s.trim().isEmpty() ? "Contains only whitespaces" : "Contains non-whitespace characters");
        sc.close();
    }
}
88. Remove Leading and Trailing Zeros from a String

import java.util.Scanner;

public class RemoveLeadingTrailingZeros {
    public static String removeZeros(String s) {
        return s.replaceAll("^0+|0+$", "");
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println("After removing leading and trailing zeros: " + removeZeros(s));
        sc.close();
    }
}
89. Count Number of Sentences Ending with a Question Mark
import java.util.Scanner;

public class CountQuestionSentences {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter text: ");
        String text = sc.nextLine();
        String[] sentences = text.split("[.!?]");
        int count = 0;
        for(char c : text.toCharArray()) {
            if(c == '?') count++;
        }
        System.out.println("Number of question sentences: " + count);
        sc.close();
    }
}
90. Check if String Contains Balanced Parentheses

import java.util.Scanner;
import java.util.Stack;

public class BalancedParentheses {
    public static boolean isBalanced(String s) {
        Stack<Character> stack = new Stack<>();
        for(char c : s.toCharArray()) {
            if(c == '(') stack.push(c);
            else if(c == ')') {
                if(stack.isEmpty()) return false;
                stack.pop();
            }
        }
        return stack.isEmpty();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter string: ");
        String s = sc.nextLine();
        System.out.println(isBalanced(s) ? "Balanced parentheses" : "Not balanced");
        sc.close();
    }
}
