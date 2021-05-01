# task
Task1
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package javaapplication92;

import java.util.Scanner;

/**
 *
 * @author Ahmed
 */
public class JavaApplication92 {

    /**
     * @param args the command line arguments
     */
    static int play(int a, int b) {
        if (b == 0) {
            return 0;
        }
        if (a / b > 1) {
            return 1;
        }
        return play(b, a - b) + 1;
    }

    public static void main(String[] args) {
        int a, b;
        Scanner sc = new Scanner(System.in);

        while (true) {
            a = sc.nextInt();
            b = sc.nextInt();
            if (a == 0 && b == 0) {
                break;
            }
            if (a < b) {
                int t = a;
                a = b;
                b = t;
            }
            int numTurns = play(a, b);
            if (numTurns ==1 ) {
                System.out.println("amr wins");
            } else {
                System.out.println("Diana wins");
            }
        }
    }

}
