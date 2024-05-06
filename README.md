import java.util.Scanner;

public class Solution {

    static boolean isAnagram(String a, String b) {
        // Complete the function
        String s1 = a;
        String s2 = b;
        s1=s1.toLowerCase();
        s2=s2.toLowerCase();
        
        if(s1.length()==s2.length())

        {
            int[] arr = new int[256];
            int[] brr = new int[256];
            for (int i = 0; i < s1.length(); i++) {
                arr[(int) s1.charAt(i)] += 1;
                brr[(int) s2.charAt(i)] += 1;
            }
            for (int i = 0; i < 256; i++) {
                if (arr[i] != brr[i])
                    return false;

            }
            return true;
        }
        else
        {
            return false;
        }
    }

  public static void main(String[] args) {
    
        Scanner scan = new Scanner(System.in);
        String a = scan.next();
        String b = scan.next();
        scan.close();
        boolean ret = isAnagram(a, b);
        System.out.println( (ret) ? "Anagrams" : "Not Anagrams" );
    }
}
