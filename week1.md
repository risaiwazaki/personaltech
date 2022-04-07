{% include navigation.html %}

<--[Back to Home Page](/personaltech/)

## Week 1 Code

My week one code on Replit is [here](https://replit.com/@risaiwazaki/risachallenge#week_1/stack.java)

Below are some coding snippets.


http://p1-valid.me/personaltech/

## Queue

```
package week_1;

import java.util.ArrayList;

public class queue<T> {

    private ArrayList<T> list = new ArrayList<T>();

    public queue() {}

    public void push(T data){
        list.add(data);
    }

    //remove from queue (pop)
    public void pop(){
        //if list is not empty
        if(!list.isEmpty()){
            //remove item from list
            list.remove(0);
        }
        else{
            System.out.println("null");
        }
    }

    //view top of queue (peek)
    public T peek(){
        if(!list.isEmpty()){
            return list.get(0);
        }
        else{
            return null;
        }
    }

    //view entire queue
    public ArrayList<T> display(){
        return list;
    }

    //view length of queue
    public int length(){
        return list.size();
    }

    //clear queue
    public void clear(){
        list.clear();
    }
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
