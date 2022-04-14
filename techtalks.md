{% include navigation.html %}

# Week 3
- Sorts 
- Build custom Bubble Sort, Selection Sort, Insertion Sort and Merge Sort. 25%
- Build a GitHub page that describes Sort implementations and the Big O complexity of these Sorts. 25%
- Analysis 25%
   - Establish analytics including: time, comparisons and swaps.
   - Average the results for each each Sort, run each at least 12 times and 5000 elements.  You should throw out High and Low when doing analysis.
   - Make your final/judgement on best sort considering Data Structure loading, Comparisons, Swaps, Big O complexity, and Time.


# Week 2
- In coding languages, Reverse Polish Notation is used to calculate math expressions by using Stacks and the Shunting-yard algorithm to parse through the inputed data
   - Ex: 6 * 15 becomes 6 15 
- Operators are stored in a hash map based off of order of operations - which ones come first and thus take precedence


# Week 1
* Linked Lists
   - Circle queues
   - Stacks
     - push (enqueue, push/add)
     - pop (dequeue, remove/pop/delete)
* Queue
   - Has a linked list
   - Full with test data
   - As we add to the queue, the head remains constant 
   - Dequeue = tail remains constant
   - Add = remove from tail
   - Remove = remove from head 
* Challenge 
   - Set up 2 queues
   - Dequeue 2 queues, make 3rd queue in-between the 2 queues
   - Build a queue

public class Queue<T> implements Iterable<T> {
    LinkedList<T> head, tail;
 - Generic data type



# Week 0 
* Data Structure
   - method of organizing data
   - table & databases
* Programming Paradigms
   - array list & fibonacci
* Data Structures Project 
   - Review the requirements for Replit to GitHub version control. Spend some time reviewing comments in the Menu code below, you need to "Comment the Heck out of your Project". Adapt this menu code for your "Individual Data Structures Project" and some things from Tri 2 or before.

