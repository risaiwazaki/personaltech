## Week 2 Code
Below are some coding snippets.
<div markdown=“0”><a href=“https://replit.com/@risaiwazaki/risarefcode#.replit” class=“btn btn-info”> Click to Go Back</a></div>

http://p1-valid.me/personaltech/

## Calculator
package src.week2;

import java.util.Scanner;

public class Calc 
{
    static Scanner scan = new Scanner(System.in);

    public static void main(String[] args) 
    {
        displayMenu();

        int entryChoice = scan.nextInt();

        while (entryChoice != 7) 
        {
            System.out.println(userSelection(entryChoice));

            displayMenu();
            isInt(entryChoice);
            entryChoice = scan.nextInt();
        }

        scan.close();
        System.exit(0);
    }
    

    public static boolean isDouble(double x)
    {
        double userInput = x;
        try 
            {
                userInput = Double.parseDouble(scan.next());
                return true; 
            } 
            catch (NumberFormatException ignore) 
            {
                System.out.println("Invalid input.  Try again.");

                return false;
            }
    }
    public static boolean isInt(int x)
    {
        int userInput = x;
            try 
            {
                userInput = Integer.parseInt(scan.next());
                return true;
            } 
            catch (NumberFormatException ignore) 
            {
                System.out.println("Invalid input");
                return false;
            }
    }

    public static void displayMenu() 
    {
        System.out.println("Please select from the following choices:");
        System.out.println();
        System.out.println("1) Addition");
        System.out.println("2) Subtraction");
        System.out.println("3) Multiplication");
        System.out.println("4) Division");
        System.out.println("5) Raise to a Power");
        System.out.println("6) Square Root");
        System.out.println("7) Exit Program");
        System.out.println();
        System.out.println("Enter your choice here: ");
    }

    public static double userSelection(int entryChoice) 
    {
        double result = 0;
        double x = 0;
        double y = 0;

        if (entryChoice == 6) 
        {
            System.out.println("Enter one number: ");
            x = scan.nextDouble();
        } 
        else 
        {
            System.out.println("Enter two numbers seperated by a space");

            x = scan.nextDouble();
            y = scan.nextDouble();
        }
        switch (entryChoice) 
        {
            case 1:
                result = x + y;
                break;

            case 2:
                result = x - y;
                break;

            case 3:
                result = x * y;
                break;

            case 4:
                if (y == 0)
                {
                    System.out.println("Can't divide by zero.  Please enter another number.");
                    y = scan.nextDouble();
                    result = x / y;
                }
                else 
                {
                    result = x / y;
                }
            break;

            case 5:
                result = Math.pow(x, y);
                break;

            case 6:
                result = Math.sqrt(x);
                break;

            case 7:
                result = 0;
                break;
            default:

        }
        return result;
    }
}

## Menu
## IntByReference
package src;

import src.week0.*;
import src.week1.*;
import src.week2.*;

import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class Menu {
    Map<Integer, MenuRow> menu = new HashMap<>();

    public Menu(MenuRow[] rows) {
        int i = 0;
        for (MenuRow row : rows) {
            menu.put(i++, new MenuRow(row.getTitle(), row.getAction()));
        }
    }
  
    public MenuRow get(int i) {
        return menu.get(i);
    }

    public void print() {
        for (Map.Entry<Integer, MenuRow> pair : menu.entrySet()) {
            System.out.println(pair.getKey() + " ==> " + pair.getValue().getTitle());
        }
    }

    public static void main(String[] args) {
        Driver.main(args);
    }

}

class MenuRow {
    String title;
    Runnable action;

    public MenuRow(String title, Runnable action) {
        this.title = title;
        this.action = action;
    }

    public String getTitle() {
        return this.title;
    }
    public Runnable getAction() {
        return this.action;
    }

    public void run() {
        action.run();
    }
}

class Driver {
    public static void main(String[] args) {
        MenuRow[] rows = new MenuRow[]{
                new MenuRow("Exit", () -> main(null)),
                new MenuRow("Tech Talk 0", () -> Menu0.main(null)),
                new MenuRow("Tech Talk 1", () -> Menu1.main(null)),
                new MenuRow("Tech Talk 2", () -> Menu2.main(null)),
        };

        Menu menu = new Menu(rows);

        while (true) {
            System.out.println("Menu:");
            menu.print();

            try {
                Scanner sc = new Scanner(System.in);
              
                int selection = sc.nextInt();

                try {
                    MenuRow row = menu.get(selection);
                    if (row.getTitle().equals("Exit"))
                        return;
                    row.run();
                } catch (Exception e) {
                    System.out.printf("\nInvalid selection: %d \n\n", selection);
                }
            } catch (Exception e) {
                System.out.println("\nInput is not a number\n");
            }
        }
    }
}


