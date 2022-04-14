{% include navigation.html %}

<--[Back to Home Page](/personaltech/)

## Week 0 Code

My week two code on Replit is [here](https://replit.com/@risaiwazaki/risachallenge#week_1/stack.java)

Below are some coding snippets.


http://p1-valid.me/personaltech/

## Matrix

```
package week_0;

import abstract_classes.funcMaster;

public class matrix extends funcMaster {
    public matrix(String selection) {
        super.selection = selection;
    }

    public String switchMatrix1(int[][] matrix, int rows, int columns) {
        int[][] newMatrix = new int[rows][columns];
        for(int i = 0; i < rows; i++) {
            for(int j = 0; j < columns; j++) {
                newMatrix[i][columns - j - 1] = matrix[i][j];
                System.out.println(matrix[i][j]);
            }
        }
        String output = newMatrix.toString();
        return output;
    }

```

## Menu
## IntByReference

```
import abstract_classes.funcMaster;

import java.util.Dictionary;
import java.util.Scanner;

public class menu {

    //Initialize variables
    private Dictionary<Integer, funcMaster> elements;
    Scanner input = new Scanner(System.in);

    //Constructor
    public menu(Dictionary<Integer, funcMaster> elements) {
        //Takes dictionary as input
        this.elements = elements;
    }

    //Iterate over dictionary and print all values
    public void print() {
        for(int i = 1; i <= this.elements.size(); i++) {
            System.out.print(i + " ");
            System.out.println(elements.get(i).getSelection());
        }
    }

    public void run(int x) {
        this.elements.get(x).run();
    }
}
```

