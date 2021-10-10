## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/DarkEmbers/Java/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/DarkEmbers/Java/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

Alrighty, here's a tutorial on basic Java Programming!

```markdown
public class MyClass
{
    public static void main(String[] args)
    {
        // Your code goes here
        
    }

}
```

Here's the stuff you will see when starting your Java project:
1. A Class with the name of your project
2. A main function where you will write your code

The first thing to try is a simple Print Statement:
```markdown
System.out.println("Hello World");
```
This will print a statement onto the console.

Next are variables, these are important as you'll constantly use them in every program you write!

The main variable types to know are:
- Integer - A whole number e.g. 1, 2, 3. Takes 4 bytes of memory.
- Long - A whole number, but takes 8 bytes of memory.
- Short - A whole number, but takes 2 bytes of memory.
- Float - A decimal number e.g. 1.45, 9.992, 54.1642. Takes 4 bytes of memory.
- Double - A decimal number, but takes 8 bytes of memory.
- Boolean - Can either be true or false. Takes 1 byte of memory.
- Char - Contains a single character e.g. 1, a, c, 9. Takes 2 bytes of memory.
- String - A string of chars. Though it isn't a primitive type, Java has a native String class.

Different amounts of memory means they can hold different amounts of data.
E.g. a short can hold numbers between -32,768 and 32,767 (inclusive). But an int can hold numbers between -2,147,483,648 to 2,147,483,647 (inclusive).

Variables are defined by specifying the variable type and a variable name as such:
```markdown
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

In our main function, we'll create a String variable called Name and an int variable called Age, and assign it to "Bob" and 25 respectively:
```markdown
String Name = "Bob";
int Age = 25;
```
Now lets print out a scentence about Bob:
```markdown
System.out.println("Hello " + Name + ", you are " + Age + " years old.");
```
Note that the + sign allows you to concatenate variables and string scentences together in the Print Statement.
