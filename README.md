# Day25-with-java

Today I practiced How to print the index of a character in a given string.
Here is the code ...

import java.util.Scanner;
public class CharacterIndex {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = scanner.nextLine();

        System.out.print("Enter a character: ");
        char ch = scanner.next().charAt(0);

        int index = findCharacterIndex(str, ch);
        if (index != -1) {
            System.out.println("Index of '" + ch + "' in the string is: " + index);
        } else {
            System.out.println("Character '" + ch + "' not found in the string.");
        }
        scanner.close();
    }
    public static int findCharacterIndex(String str, char ch) {
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == ch) {
                return i;
            }
        }
        return -1;
    }
}

output:
Enter a string: hello
Enter character : o
The index of o is 4
