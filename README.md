# Measuring Software Engineering

### Introduction
Measuring the capabilities of an employee is something trivial and obvious yet also very difficult to pinpoint the most effective way of doing so. It may be obvious for you or it may be something completely out of your realm of knowledge and capability but given the struggle so many have in measuring it meaningfully, it’s likely only obvious in hindsight. 

Managers in companies will often organise performance review meetings and other similar events in order to accurately measure an employee’s output. When we further narrow this down into the discipline of Software Engineering, we further make this question more difficult to answer.  Unlike some more traditional industries, the construction and study of metrics used to measure an employee is relatively straight forward but in software engineering there are first of all no obvious metrics which come to mind in order to form a meaningful analysis of an employee’s ability.

In the case of software engineering the ability to collect metrics in general is simple and routine due to the transparent nature of software engineering. Some of these metrics could be the total amount of commits, total amount of pull requests and total amount of lines of code written. These metrics each tell a story but none of them can accurately depict what is happening. In this essay I will discuss several metrics which are used in the professional landscape of software engineering. I will highlight the flaws and positives of each metric and then outline case studies and discuss their findings followed by a conclusion.

## Metrics

### Source Lines of Code (SLOC)
Also known as lines of code (LOC), is a very common software metric used to measure the size of a computer program by counting the total number of lines in the text of the program’s source code.  SLOC can be separated into two major types; physical SLOC and logical SLOC. 

* **Physical SLOC:** The most common definition of physical SLOC is a count of lines in the text of the program’s source code exempting the amount of comment lines. 

* **Logical SLOC:** Attempts to measure the number of executable statements.

Physical SLOC is much easier to measure as creating tools to measure physical SLOC is much easier. Physical SLOC’s definitions are also easier to explain. However, physical SLOC is not effective in cases of logically irrelevant formatting and conventions.
Logical SLOC is less sensitive to formatting and conventions but it is more complex to measure and create tools to measure. 

SLOC measures are usually stated without giving their definition and both measures often yield wildly different results. Here are some examples



**Example One:**
```java
for (int index = 0; index < 10; i++) System.out.println(“SLOC”); //This is a random comment
```

For this example:
* 1 physical line of code
* 2 logical lines of code
* 1 comment line


**Example Two:**
```java
//This is a random comment
for (int index=0; index<10;i++)
{
	System.out.println(“SLOC”);
}
```
For this example:
* 4 physical lines of code
* 2 logical lines of code
* 1 comment line

### Does it work?
>”Using SLOC to measure software progress is like using kg for measuring progress on aircraft manufacturing” – Bill Gates

This quote sums up the essence of the argument against using SLOC as a relevant and meaningful metric in measuring the progress and productivity of software engineering. The total lines of code and total amount of statements is an irrelevant metric for measuring software engineering as it encourages bad practises such as:

* Copy-Paste-Syndrome
* Discourages refactoring to make things more streamlined and similar
* Adding lines of code which adds to complexity
* Added complexity means it is harder to understand
* Understanding takes time and costs productivity

An example of the bad practice that SLOC encourages:
```java
// Print the number 1
System.out.println(1);
// Print the number 2
System.out.println(2);
// Print the number 3
System.out.println(3);
// Print the number 4
System.out.println(4);
// Print the number 5
System.out.println(5);
// Print the number 6
System.out.println(6);
// Print the number 7
System.out.println(7);
// Print the number 8
System.out.println(8);
// Print the number 9
System.out.println(9);
// Print the number 10
System.out.println(10);
```
As you can decipher from the above code, it carries out a simple task of printing out the numbers 1 to 10. The SLOC of the above code regardless of physical or logical is 10. Both examples I gave earlier were more efficient ways of approaching this problem yet both have lower SLOC. Any software engineer manager would rather the examples earlier as opposed to the hard coding of the above example. This is a very simple way of highlighting the inefficiency and discrepancies of SLOC as a metric.

Using SLOC as a metric also has its down sides when you are evaluating using different programming languages as different languages require different amounts of lines of code to achieve the same amount of functionality. For instances higher level languages such as Python, Java and GO allow programmers to write useful applications with only a handful amount of lines of code whereas a lower level language such as C would require many more lines of code to achieve the same functionality.
