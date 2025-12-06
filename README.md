### 0.2.0
version: R++ #2
- New library sys.io with only one function os_()
- New variations for the following functions:
1. print() has --> print(), pt(), console_log()
2. input() has --> input(), ipt()

- Added null but with specific function:
>>> definition: null has rol as a value of a variable: e.g.' int b = null; ' and as a variable type: e.g. ' null a; '
>>> you could add value for null in 2 different ways:
-1- if it should be a number or decimal just type:
>>
null x;
x --> x += 2; // '-->' means that variable x will gain 2 for its value.
pt(x); // output will be: 2
-2- As a text
null x;
x <-- "Question"; // or Question // '<--' means that x will accept only string-type
console_log(x); //output will be: Question
---
>>> null as its value:
int a = null;

- Added return for functions of type func & void

- break if () and continue if () --> conditional for loops

You can download rplusplus.vsix on clicking the link in documentation.

Link to digital document:

https://docs.google.com/document/d/1ZCzdmiSYzHkU3jgZGLPcZSw2sGpNjPXnrZKLs-2Vcz0/edit?usp=sharing
