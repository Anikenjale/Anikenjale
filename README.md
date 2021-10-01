import java.util.Arrays;
import java.util.Scanner;

class PalindromeDemo {
    public static void main(String[] args) {
        String s1;
        int m1;
        Scanner scan = new Scanner(System.in);
        System.out.println("Enter a string");
        s1 = scan.next();
        m1=s1.length();
        char org[] = new char[m1];
        char rev[] = new char[m1];
        int i, j;
        for (i = 0; i <=s1.length()-1; i++) {
            org[i] = s1.charAt(i);
        }
        i =m1-1;
        j = 0;
        while (i >= 0) {
            rev[j] = org[i];
            i--;
            j++;
        }
        boolean status;
        status = Arrays.equals(org, rev);
        if (status == true) {
            System.out.println("String is Palindrome");
        } else {
            System.out.println("String is not Palindrome");
        }
        scan.close();
    }
}
