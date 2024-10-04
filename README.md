import java.util.Scanner;
public class LeftRotateString {
public static void rotateLeft(char[] s, int k) {
int n = s.length;
k = k % n;
char[] temp = new char[n];
int j = 0;
for (int i = k; i < n; i++, j++) {
temp[j] = s[i];
}
for (int i = 0; i < k; i++, j++) {
temp[j] = s[i];
}for (int i = 0; i < n; i++) {
s[i] = temp[i];
}
}
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
System.out.print("Enter a string: ");
String input = scanner.nextLine();
System.out.print("Enter the number of positions to rotate left: ");
int k = scanner.nextInt();
char[] s = input.toCharArray();
rotateLeft(s, k);
String rotatedString = new String(s);
System.out.println("Rotated string: " + rotatedString);
}
}
