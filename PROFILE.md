Welcome to my GitHub profile!
package main.java;
import java.util.Scanner;

import main.java.Beverage.Size;

/**
 * VendingMachine.
 * this is a driver/main class for Assignment 1 of the Java course
 */
public class VendingMachine {
    static Beverage b; 
    
    public static void main(String[] args) {
        System.out.println("Enter c for coffee and t for tea: ");
        Scanner s = new Scanner(System.in);
        char choice = s.nextLine().charAt(0);

        if (choice == 't') {
            b = new Tea(Size.SMALL);
            b.drink();
        } else if (choice == 'c') {
            b = new Coffee(Size.SMALL);
            b.drink();
        }

        s.close();
    }

}
