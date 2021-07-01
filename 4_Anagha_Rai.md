# Problem Statement 1: Strings in the box

## Submitted Code:

```
def codeathon(words):
    size = max(len(word) for word in words)
    print("*"*(size+4))

    for i in words:
        print("*"+" "+i+" "*((size+4)-len(i)-3)+"*")

    print("*"*(size+4))

codeathon(["I", "Participated", "in", "APSIT", "Codeathon"])

```

# Problem Statement 2: English to Morse

## Submitted Code:

```
import java.io.*;
import java.util.*;

public class Solution {

        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
    public static void englishToMorse(String[] code, String englishText, char[] letter){
        
        for (int i = 0; i < englishText.length(); i++) {
            for (int j = 0; j < letter.length; j++) {
                if (englishText.charAt(i) == letter[j]) {
                    System.out.print(code[j] + " ");
                    break;
                }
            }
        }
    }
 
    public static void main(String[] args)
    {
 
        // store the all the alphabet in an array
        char[] letter = { 'a', 'b', 'c', 'd', 'e', 'f',
                          'g', 'h', 'i', 'j', 'k', 'l',
                          'm', 'n', 'o', 'p', 'q', 'r',
                          's', 't', 'u', 'v', 'w', 'x',
                          'y', 'z', '1', '2', '3', '4',
                          '5', '6', '7', '8', '9', '0' };
        // Morse code by indexing
        String[] code
            = { ".-",   "-...", "-.-.", "-..",  ".",
                "..-.", "--.",  "....", "..",   ".---",
                "-.-",  ".-..", "--",   "-.",   "---",
                ".--.", "--.-", ".-.",  "...",  "-",
                "..-",  "...-", ".--",  "-..-", "-.--",
                "--..", "|" };
 
        String englishText = "school";
        englishToMorse(code, englishText, letter);
        System.out.println();
    }
}

```

# Problem Statement 3: ROT13 Cipher

## Submitted Code:

```
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
   
        String str,str1= "";
        char ch,ch1;
        int i,x,l;
        str = "APSITCODE";
        l= str.length();
        for(i=0;i<l;i++)
        {
            ch= str.charAt(i);
            x = (int) ch;
            if(x>=65&&x<78)
            {
                x= x+13;
                ch1= (char)x;
                str1= str1+ch1;
            }
            else if(x>=78&&x<91)
            {
                x= x-13;
                ch1= (char)x;
                str1= str1+ch1;
            }
            else if(x>=97&&x<110)
            {
                x= x+13;
                ch1= (char)x;
                str1= str1+ch1;
            }
            else if(x>=110&&x<123)
            {
                x= x-13;
                ch1= (char)x;
                str1= str1+ch1;
            }
        }
        System.out.println("Rot 13 converted Text: " +str1);
    }
}

```