# Java_Lab_5
/**
 * Loops: do, do while, and for. manipulates input numbers, gives odd/even,, shows all evens between
 * the two, totals the sum of all odd numbers between the two, shows all prime numbers between the
 * two, and asks if you would like to do it again with different numbers.
 * 
 * @author Kyle Meek
 * @version 10/29/2015
 */

import java.util.Scanner;
public class LoopPrimes
{
    public static void main (String [] args)
    {
        Scanner keyIn = new Scanner(System.in);
        int x;
        int y;
        int z;
        String answer;
        System.out.println("Programmer: Kyle Meek");
        System.out.println("Course:     COSC 111, Fall 2015");
        System.out.println("Lab#:       5");
        System.out.println("Due Date:   10-22-2015");
        System.out.println("");
        do{
            System.out.print("Enter a whole number: ");
            x = keyIn.nextInt();
            System.out.print("Enter another whole number: ");
            y = keyIn.nextInt();
            System.out.println("");
            if ((x % 2) == 0)
                System.out.println(x + " is even.");
            else
                System.out.println(x + " is odd.");
            if ((y % 2) == 0)
                System.out.println(y + " is even.");
            else
                System.out.println(y + " is odd.");
            System.out.println("");
            if (x > y){
                System.out.println(x + " and " + y + " are swapped.");
                System.out.println("");
                z = x;
                x = y;
                y = z;
            }
            else
                System.out.println("");
            System.out.println("Even numbers between " + x + " and " + y + " are:");
            for(int a = x; a <= y; a++){
                if(a % 2 == 0){
                    System.out.print(a + "\t");
                }
            }
            System.out.println("");
            int c = x;
            int sum = 0;
            while(x <= y){
                if(x % 2 == 1){
                    sum += x;
                }
                x++;
            }
            System.out.println("");
            System.out.println("The sum of the odd numbers between " + c + " and " + y + " is: " + sum);
            System.out.println("");
            System.out.println("Numbers between " + c + " and " + y + " (3 numbers per line):");
            int ret = 0;
            for(int numz = c; numz <= y; numz++){
                System.out.print(numz + "\t");
                ret ++;
                if(ret % 3 == 0)
                    System.out.print("\n");
            }
            System.out.println("");
            System.out.println("");
            System.out.println("Prime numbers from " + 3 + " to " + y + ":");
            for(int p = 3; p <= y; p++){
                for(int j = 2; j <= p; j++){
                    if(j == p){
                        System.out.print(p + "\t");
                    }
                    if(p % j == 0){
                        break;
                    }
                }
            }
            System.out.println("");
            System.out.println("");
            System.out.print("Do it again? (yes or no)");
            answer = keyIn.next();
            System.out.println("");
        }while(answer.equalsIgnoreCase("yes"));
    }
}
