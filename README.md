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


