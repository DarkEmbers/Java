## Java

Alrighty, here's a tutorial on basic Java Programming!

Here's the stuff you will see when starting your Java project:
1. A Class with the same name of your project
2. A main function where you will write your code

```java
public class MyClass
{
    public static void main(String[] args)
    {
        // Your code goes here
        
    }

}
```
### Print Statements and Variables

The first thing to try is a simple Print Statement:
```java
System.out.println("Hello World");
```
This will print a statement onto the console.

Next are variables, these are important as you'll constantly use them in every program you write!

The main variable types to know are:
- ```Integer``` - A whole number e.g. 1, 2, 3. Takes 4 bytes of memory.
- ```Long``` - A whole number, but takes 8 bytes of memory.
- ```Short``` - A whole number, but takes 2 bytes of memory.
- ```Float``` - A decimal number e.g. 1.45, 9.992, 54.1642. Takes 4 bytes of memory.
- ```Double``` - A decimal number, but takes 8 bytes of memory.
- ```Boolean``` - Can either be true or false. Takes 1 byte of memory.
- ```Char``` - Contains a single character e.g. 1, a, c, 9. Takes 2 bytes of memory.
- ```String``` - A string of chars. Though it isn't a primitive type, Java has a native String class.

> Different amounts of memory means they can hold different amounts of data.
> E.g. a short can hold numbers between -32,768 and 32,767 (inclusive). But an int can hold numbers between -2,147,483,648 to 2,147,483,647 (inclusive).

Variables are defined by specifying the variable type and a variable name as such:
```java
int MyInt = 10;
long MyLong = 1304;
short MyShort = 3;
float MyFloat = 12.f;
double MyDouble = 53.13;
boolean MyBoolean = true;
char MyChar = 'a'; // You must use 'single quotes' when defining a char
String MyString = "Hello"; // You must use "Double quotes" when defining a String
```

Lets write some code with what we know so far!

In our main function, we'll create a String variable called Name and an int variable called Age, and assign them to "Bob" and 25 respectively:
```java
String Name = "Bob";
int Age = 25;
```
Now lets print out a scentence about Bob:
```java
System.out.println("Hello " + Name + ", you are " + Age + " years old.");
```
> Note: The + sign allows you to concatenate variables and string scentences together in the Print Statement.

Finally you should have something like this:
```java
public class MyClass
{
    public static void main(String[] args)
    {
        // Your code goes here
        String Name = "Bob";
        int Age = 25;

        System.out.println("Hello " + Name + ", you are " + Age + " years old.");
    }

}
```

This should result in the following output:
```markdown
Hello Bob, you are 25 years old.
```

Congrats, you've written your first Program!

### Inputs

Moving on, we will learn to take in user input from the console.
Inputs are taken using a Java class called Scanner. To import Scanner, at the top of your file add:
```java
import java.util.Scanner;
```
To create an instance of the Scanner class, we create a new variable of type Scanner.
```java
Scanner scan = new Scanner(System.in);
```
> Don't forget to close your Scanner after you're done using it by writing: ```scan.close()```

Scanner is a class that reads input streams and allows us to read data from those streams. To access functions from a class we must use:
```java
scan.YourFunctionName();
```
For this example we will have the user input their name and assign it to a String variable. Lucky for us, the Scanner class has a function to read different data type inputs.
```java
// Scanner methods to read user inputs:
scan.next(); // Reads the first word from the input
scan.nextLine(); // Reads the entire line from the input
scan.nextInt(); // Reads the next Integer
scan.nextFloat(); // Reads the next Float
scan.nextBoolean(); // Reads the next Boolean
// etc...
```

Although we can read input from the user, it needs to be stored for later use.
So we can create a variable and assign it to one of these Scanner functions.
Lets ask the user for their name:
```java
System.out.println("What is your name?");
String Name = scan.nextLine();
```
Lets break this down, first, we are using a print statement to ask the user for their name. We know that a Name is of type String, so we can use ```scan.nextLine()``` to read String input. Then we are assigning the value we got from the input to a String variable called Name.

Once we've stored the input we can use the variable as we normally would:
```java
System.out.println("Hello " + Name);
```

Similarly if you want to read int data and store it to a variable named Age, write:
```java
int Age = scan.nextInt();
```

So you should have something like this:
```java
import java.util.Scanner;

public class MyClass
{
    public static void main(String[] args)
    {
        // Your code goes here
        Scanner scan = new Scanner(System.in);

        System.out.println("What's your name?");
        String Name = scan.nextLine();

        System.out.println("What's your age");
        int Age = scan.nextInt();

        System.out.println("Heya " + Name + " you're " + Age + " years old, yowza!");

    }

}
```
Try running it and see what happens.

### If, Else if, and Else Statements

If Statements are one of the fundamentals of programming that allow you to change your code from a series of inputs and outputs, to a logical program with complex functionality!

#### Operators

Before we dive into if statements we need a good knowledge of the operators used.
```markdown
Basic arithmetic signs are used too: +, -, *, /, ()
Then logical operators:
1. == Equals
2. >= Greater than or Equal to
3. <= Less than or Equal to
4. || OR
5. && AND
```
> Note: The ```==``` sign is used to check equality in a condition while the ```=``` sign is used to assign values.

The body of an If Statement looks like this:
```java
if (/* Condition goes here */)
{

}
else if (/* Another condition goes here */)
{

}
else // Will run if all else fails
{

}
```
If Statements only run code if the conditions (in the parenthesis) is true.
Different operators are used to formulate conditions to be used in if statements.

To get an idea of how to use these operators in conjunction with If Statements, lets write a simple conditional statement. 
We will ask the user for their age, assign it to an int variable, and check if they're old enough to drive.
> It isn't neccesary to have ```else if``` and ```else``` in every conditional statement we make.

```java
/**
* You can also declare your variables and assign them 
* later. Though you will get an error if you try to use
* unassigned variables.
*/

int Age;

Scanner scan = new Scanner(System.in);
System.out.println("How old are ya:");
Age = scan.nextInt();

if (Age < 18)
{
    System.out.println("Yikes you're to young to drive, fella!");
}
else if (Age > 40)
{
    System.out.println("Wowee, you're old, of course you can drive.");
}
else if (Age >= 18)
{
    System.out.println("Woohooo You can drive! Enjoy the Nissan Sunny lol.");
}

scan.close();
```
The final else if:
```java
else if (Age >= 18)
{
    System.out.println("Woohooo You can drive! Enjoy the Nissan Sunny lol.");
}
```
can be replaced with:
```java
else
{
    System.out.println("Woohooo You can drive! Enjoy the Nissan Sunny lol.");
}
```
to achieve the same result, as ```(Age >= 18)``` is the only possibility left.
> If any of the conditions are true, then any of the other Else Ifs and Elses in the statement will be ignored. If you would like to check those conditions anyways, create seperate If Statements.

#### Equality of Strings

Since String is not a primitive data type and is instead a class built on top, all String variables will have available functions from the String class.

For Example, you may have noticed if you put a String variable == a value, the condition is always false. To check String equality you must use the String function ```equals()``` or ```equalsIgnoreCase()``` to ignore case sensitivity.
It's used like this:
```java
if (name.equals("Naruto"))
{

}
```
This check whether the variable ```name``` is equal to Naruto
