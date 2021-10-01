```java
package ru.endurence;


import java.util.LinkedHashSet;
import java.util.Scanner;
import java.util.Set;

public class Main {

    public static boolean correctOrder(String string) {

        String str = new String();

        Set<Character> charSet = new LinkedHashSet<Character>();

        for (int i = 0; i < string.length() ; i++) {
            charSet.add(string.charAt(i));
        }

        for (char s:charSet) {
            str += s + "";
        }

        if (str.charAt(0) == 'a' && str.charAt(1) == 'b' && str.charAt(2) == 'c') {
            return true;
        } else {
            return false;
        }

    }

    public static int quantityChart(String string, char symbol){
        int a = 0;

        for (int i = 0; i < string.length(); i++) {
            if(string.charAt(i) == symbol){
                a++;
            }
        }

        return a;
    }


        public static void main(String[] args) {
            String str = new String();
            Scanner sr = new Scanner(System.in);

            str = sr.nextLine();

            int a,b,c;

            a = quantityChart(str, 'a');
            b = quantityChart(str,'b');
            c = quantityChart(str, 'c');

            if(correctOrder(str) && ((a == c) || (b == c))){
                System.out.println("YES");
            }else{
                System.out.println("NO");
            }


        }





    }

```
