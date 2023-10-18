# Recursion isn't as hard as you think
- Author: [Tashin Parvez](https://github.com/TashinParvez) 
- [United International University](https://www.uiu.ac.bd/)
- Sid: 011221437
 
![CoverPhoto](https://github.com/TashinParvez/My-Blogs-In-UIU-CP-COMMUNITY/blob/Tashin_Parvez_011221437/Algorithms/Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think/ImageFile/Cover.png?raw=true)

 <img align="right" width="25%" height="25%" src="https://github.com/TashinParvez/My-Blogs-In-UIU-CP-COMMUNITY/blob/Tashin_Parvez_011221437/Algorithms/Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think/ImageFile/spider-man-pointing.jpg" alt="gras" />
<b>Recursion</b> is a very used and powerful <b>functional programming</b>
concept. What is <b>recursion</b>? <br/>
It's a technique in programming <b>where a function calls itself,</b> like in front of a mirror you are calling your
mirror view by your name. It is also called a <b>recursive function</b>.
Why? When a function that calls itself is a recursive function.



### How do we call a function in C programming?

``` {#37243b9a-b511-4341-8e31-7511fc90eeb6 .code}
#include <stdio.h>

void greet() {
    printf("Hello, World!\n");
}

int add(int a, int b) {
    return a + b;
}

int main() {

    greet();                   // Calling the greet() function without arguments

    int result = add(5, 3);    // Calling the add() function with arguments and storing the result

    return 0;
}
```

by this line " greet(); " in the main function we are calling the greet
function which is printing Hello, World! <br/>
**Is this function calling itself?**

<b>No.</b>

### What does calling itself in a function look like?

```
void greet() {
    printf("Hello, World!\n");
    greet();                     // Calling itself
}
```

See, in this Greet function calling itself by using " greet(); " this
line.


<br/>
<b><u>Do you know what will happen if this greet function is called from the main function?</u></b>
<br/><br/>

Yes, it will continuously print Hello World and it will not stop, and in the end, our program will crash.

So, now we know that recursion is a recursive function because it calls itself. Does the recursive function always crash the program, like the 'greet' function above?

The answer is **No**. Why?

Because It has the **base case** which terminates the recursion function.
<br/><br/>


### Now the question is what is the **base case?**
___

The "base case" in recursion is like the red-light signal on the road and you have to stop your car now. So basically, it tells you when to stop. let's clear it up with an example.

If I told you to calculate 4 factorials. What will you do?


You will calculate 4 into 3 into 2 into 1. then you will stop. why do
you stop? Because you know that while calculating the factorial of a
number you need to calculate the multiplication of all numbers between 1
and the given number. so in this case 1 is your best case when you are getting 1 you end the process.

This is the base case.

---
<br/>
<br/>
<img align="right" width="25%" height="25%" src="https://github.com/TashinParvez/My-Blogs-In-UIU-CP-COMMUNITY/blob/Tashin_Parvez_011221437/Algorithms/Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think/ImageFile/Recursion.png" alt="gras" />

Now you know a recursion function has a base case and a recursive line
that calls itself. Let me tell you that these is the **main two parts of
the recursion**.

-   Base Case (terminates the recursion)
-   Recursive Case


### Now a question occurs why do we need recursion in programming?
---
-   **Code Length Reduction:** Recursion helps reduce the length of code
    by breaking complex problems into simpler, recursive subproblems.
    
-   **Enhanced Readability:** It contributes to code readability and
    makes it easier to write and understand.
    
-   **Solving Recursive Structures:** It's essential for tasks
    involving recursive data structures like trees, graphs, and linked
    lists.

Let me give you a real-life example so that you can relate the
recursion you are using in your life without knowing that this process
is called recursion.
<br/><br/>

**Suppose** your math teacher gives you an assignment. and it has 10
problems. You hardly solve one question, and you are not able to solve
the other 9 problems. Now you asked one of your friends to solve problems
for you. But your friend can only solve one and he refers your
problems to another friend of his. He solved one and referred it to his
friend. This is how you along with your 9 friends solved all the problems.

Did you do this in your school or college life? I did.

<br/>

**Let's think about this scenario from the viewpoint of recursion.**

You solved one and handed over the rest to your other friend. &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;(First person)<br/>
He also solved one and handed over the rest to your other friend. &nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;(Second person)<br/>

<img align="right" width="25%" height="25%" src="https://github.com/TashinParvez/My-Blogs-In-UIU-CP-COMMUNITY/blob/Tashin_Parvez_011221437/Algorithms/Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think/ImageFile/PassingLeftWorks.png" alt="Pasing Problems" />

He also solved one and handed over the rest to your other friend. &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;(Third person)<br/>
...<br/>
...<br/>
...<br/>
He solved the last one. &nbsp;&nbsp;  &nbsp;&nbsp;   &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; (Tenth person) [ last problem is the Base case]

See in this case your all problems are solved but you didn't do all those solutions.<br/><br/>

In the recursion problem, we also do the same in one call we do
something and recall the function and hand over the left work. This
continues until we don't get the base case. In the above scenario, the
last problem was our best case.

We are not done yet. Let's say you send your problems to your friends
using email. then obviously your friend also sends you the solution by
using email. Imagine this.

The 10th person solves the last problem and sends it to the 9th person.

9th person sends the last 2 solutions to the 8th person [9th person solve one and get one solve from the 10th person]<br/>
The 8th person sends 3 solutions to the 7th person.<br/>
...<br/>
...<br/>
...<br/>
2nd person sends 9 solutions to you.

**Now you have all the solutions. This process is called backtracking.*

Sending the solution is the return value of the function in the view of recursion.*<br/><br/>


### Let's solve a problem using recursion.
---

**Problem: Write a program using a recursive function to find the Factorial of 5.**

**Solution: First watch the given tree**

Let's compare this problem with the teacher-given assignment scenario.

To get 5 factorials we need 4 factorials.   &nbsp;&nbsp;&nbsp;&nbsp;[ You don't know the value of 4 factorials, so you give it to your friend ]

To get 4 factorials we need 3 factorials.   &nbsp;&nbsp;&nbsp;&nbsp;[ He doesn't know the value of 3 factorials, so he gives it to his friend ]

To get 3 factorials we need 2 factorials.   &nbsp;&nbsp;&nbsp;&nbsp;[ He doesn't know the value of 2 factorials, so he gives it to his friend ]

To get 2 factorials we need 1 factorial.     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[ He doesn\'t know the value of 1 factorial, so he gives it to his friend ]

1 factorial is 1 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;[ He sends the solution of 1 factorial ]

```
factorial(5) = 5 * factorial(4)
              = 5 * (4 * factorial(3))
              = 5 * (4 * (3 * factorial(2)))
              = 5 * (4 * (3 * (2 * factorial(1))))
              = 5 * (4 * (3 * (2 * 1)))    // Base case is reached here

              = 5 * 4 * 3 * 2 * 1
              = 120
```

The last person sends 1 factorial value to the person who gonna solve 2
factorial and sends to who gonna solve 3 factorial and so on. you get 4
factorial values, you multiply 5 with it, and get your 5 factorial
solutions.

Code:

```
#include <stdio.h>

int factorial(int i) {

   if(i == 1) {     // base case
      return 1; 
   }
   return i * factorial(i - 1);  // recursive call
}

int  main() {
   int i = 5;

   int factorial_Of_Five = factorial(i);   // calling the function

   printf("Factorial of %d is %d\n", i, factorial_Of_Five );
   return 0;
}
```

<br/>
<br/>

I hope this article helps you to get an overview of **Recursion**.<br/>
Thanks for your time.
<p>- Tashin Parvez</p>
