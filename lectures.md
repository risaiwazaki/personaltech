{% include navigation.html %}

# Unit 1: Primitive Data Types in Java
- Data manipulation is what computer programming does, taking in data, manipulates that data, outputs symbolic data. That manipulation happens because there are a specific set of instructions telling the computer exactly what to do. Programming is a way to articulate instructions that the computer can execute whatever you want to automate. In java, there are many ways to represent information, but a few that are atomic units: primitive data types. In java, there are 8. However, the most popular ones are integers (whole positive or negative numbers) and floating point numbers (numbers that have a fractional part). int is used to represent integers while double is used to represent floating point numbers. Both behave differently. 


```
Int num;

```
declares an integer called num as a type int. 

This line of codes tells java that we want a variable, a box that puts the integers in


```
num = 3;

```
This assigns the variable num a value. 

```
double otherNum = 4.0;

```
We are declaring and initializing a variable, it could have a fractional portion
It could be assigned “4” but since if it a double we want to make it extremely obvious that it is a fraction 

```
System.out.println(“The sum is: “ + sum);

```
When running this program, the value of sum will replace “sum”, which is 3+4.0


Java has six numeric types, 4 different types of integers, 2 different types of floating numbers. It has to do with memory. Each different type of integer uses a different amount of memory. When we declare the variable num, it tells Java that it is assigned a whole number. Java sets aside some memory for that variable and limits the size of the number. It is an integer that uses more memory so you could use bigger numbers. Since we want to conserve memory, we use memories that are not big such as byte, short, int. Memory requirements vary based on the task. If we want to be conservative about the memory we use, we can use these different types of integers. What if we want to represent a number bigger than long which is 8 bytes? In this situation, we don’t use a primitive type. With 64 bytes of memory, we can represent very big integers. However, the amount of memory varies based on the situation in Java. 


