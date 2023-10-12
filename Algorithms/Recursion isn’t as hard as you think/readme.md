# Recursion isn't as hard as you think
- Author : [Tashin Parvez](https://github.com/TashinParvez) 
- [United International University](https://www.uiu.ac.bd/)
- Sid : 011221437

![CoverPhoto](https://github.com/TashinParvez/My-Blogs-In-UIU-CP-COMMUNITY/blob/Tashin_Parvez_011221437/Algorithms/Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think/ImageFile/Cover.png?raw=true)

Recursion is a very used and powerful **functional programming**
concept. What is recursion? It's a technique in programming **where a
function calls itself,** like in front of a mirror you are calling your
mirror view by your name. It is also called a **recursive function**.
Why? When a function that calls itself is a recursive function.

<p>An image: <img src="[img/image.jpg](https://github.com/TashinParvez/My-Blogs-In-UIU-CP-COMMUNITY/blob/Tashin_Parvez_011221437/Algorithms/Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think/ImageFile/spider-man-pointing.jpg)" alt="gras" /></p>



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

    greet();  // Calling the greet() function without arguments

    int result = add(5, 3);   // Calling the add() function with arguments and storing the result

    return 0;
}
```

by this line " greet(); " in the main function we are calling the greet
function which is printing Hello, World! **Is this function calling
itself?**

No.

### What does calling itself in a function look like? {#12dc99b4-5378-4225-9a8f-8100f85286e0}

``` {#af2a1cc2-83d3-4907-86d7-396eb428a1cf .code}
void greet() {
    printf("Hello, World!\n");
        greet();  // Calling itself
}
```

See, in this Greet function calling itself by using " greet(); " this
line.

**Do you know what will happen if this greet function is called from the
main function?**

Yes, it will continuously print Hello World and it will not stop, and in
the end, our program will crash.

So, now we know that Recursion is a recursive function because it calls
itself. then **is the recursive function always crashes the program?**
like the greet function above?

The answer is No. Why?

Because It has the **base case** which [terminates the recursion
function]{.mark .highlight-yellow}.

### [Now the question is what is ]{.mark .highlight-default}[**base case**]{.mark .highlight-default}[?]{.mark .highlight-default} {#e200b01a-5235-4a6c-a815-6c14b9a636e6}

The \"**[base case]{.mark .highlight-yellow}**\" in recursion is like
the red-light signal on the road and you have to stop your car now. So
basically, it tells you when to stop. let\'s clear it up with an
**example**.

If I told you to calculate 4 factorials. What will you do?

You will calculate 4 into 3 into 2 into 1. then you will stop. why do
you stop? Because you know that while calculating the factorial of a
number you need to calculate the multiplication of all numbers between 1
and the given

::: {#5a996385-2087-4b42-b044-9f4cd39d247e .column-list}
::: {#d69e2d37-d9a0-4661-b15e-a67938da1c70 .column style="width:50%"}
number. so in this case 1 is your best case when you are getting 1 you
end the process.

This is the base case.

Now you know a recursion function has a base case and a recursive line
that calls itself. Let me tell you that this is the **main two parts of
the recursion**.

-   Base Case (terminates the recursion)

```{=html}
<!-- -->
```
-   Recursive Case
:::

::: {#f4ad0e37-6231-47d5-9b75-2f2a80c3b33f .column style="width:50%"}
![](Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think%20db0994d7a30a49ef99a7afceb2d79379/UnastitbaseCaseled.png){style="width:533px"}
:::
:::

``` {#e390fd70-7e19-4cd1-8e71-7b513997911f .code}
void recursion (int n)
{
    if(n==0)
    {
        return;
    }
    else{
        print("%d\n", n);
        recursion(n-1);
    }
}
```

### [Now a question occurs why do we need recursion in programming?]{.mark .highlight-gray_background} {#581de42b-205f-4b96-beda-f9e3a6d5dd05}

-   **Code Length Reduction:** Recursion helps reduce the length of code
    by breaking complex problems into simpler, recursive subproblems.

```{=html}
<!-- -->
```
-   **Enhanced Readability:** It contributes to code readability and
    makes it easier to write and understand.

```{=html}
<!-- -->
```
-   **Solving Recursive Structures:** It\'s essential for tasks
    involving recursive data structures like trees, graphs, and linked
    lists.

[Let me give you a real-life example so that you can relate the
recursion you are using in your life without knowing that this process
is called recursion. ]{.mark .highlight-blue_background}

Suppose your math teacher gives you an assignment. and it has 10
problems. You hardly solve one question, and you are not able to solve
the other 9 problems. Now you asked one of your friend to solve problems
for you. But your friend is only able to solve one and he refers your
problems to another friend of his. He solved one and referred it to his
friend. This is how you along with your 9 friends solved all the
problems.

Did you do this in your school or college life? I did.

**[Let\'s think about this scenario from the viewpoint of
recursion.]{.mark .highlight-brown}**

You solved one and handed over the rest to your other friend. (First
person)

::: {#cd0491aa-35fd-4929-ab18-dd89e269b588 .column-list}
::: {#61d17f04-84f7-4798-8fc9-4a3f36b34f42 .column style="width:56.25%"}
He also solved one and handed over the rest to your other friend.
(Second person)

He also solved one and handed over the rest to your other friend. (Third
person)

...

...

...

He solved the last one. (Tenth person) \[ the last problem is the Base
case\]

See in this case your all problems are solved but you didn\'t do all
those solutions.
:::

::: {#c343c60c-b673-4653-ac90-b42cdc4e3faa .column style="width:43.75000000000001%"}
![](Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think%20db0994d7a30a49ef99a7afceb2d79379/Square__Untitled.png){style="width:849px"}
:::
:::

In the recursion problem, we also do the same in one call we do
something and recall the function and hand over the left work. This
continues until we don\'t get the base case. In the above scenario, the
last problem was our best case.

We are not done yet. Let\'s say you send your problems to your friends
using email. then obviously your friend also sends you the solution by
using email. Imagine this.

The 10th person solves the last problem and sends it to the 9th person.

9th person sends the last 2 solutions to the 8th person \[9th person
solve one and get one solve from 10th person\]

::: {#71769b2b-238e-44eb-a906-8934729b5379 .column-list}
::: {#a5bcd303-e760-4221-aff4-41c62b88d6ae .column style="width:50%"}
The 8th person sends 3 solutions to the 7th person.

...

...

...

2nd person sends 9 solutions to you.

**Now you have all the solutions. This process is called**
**[backtracking]{style="border-bottom:0.05em solid"}.**

Sending the solution is the return value of the function in the view of
recursion.
:::

::: {#4691970f-de27-4690-abb9-a087a033caea .column style="width:49.99999999999999%"}
![](Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think%20db0994d7a30a49ef99a7afceb2d79379/back__Untitled.png){style="width:820px"}
:::
:::

Let\'s solve a problem using recursion.

**Problem:** Write a program using a recursive function to find the
Factorial of 5.

**Solution: First watch the given tree**

![](Recursion%20isn%E2%80%99t%20as%20hard%20as%20you%20think%20db0994d7a30a49ef99a7afceb2d79379/3181d.png){style="width:576px"}

Let\'s compare this problem with the teacher-given assignment scenario.

To get 5 factorials we need 4 factorials. \[ You don\'t know the value
of 4 factorials, so you give it to your friend \]

To get 4 factorials we need 3 factorials. \[ He doesn\'t know the value
of 3 factorials, so he gives it to his friend \]

To get 3 factorials we need 2 factorials. \[ He doesn\'t know the value
of 2 factorials, so he gives it to his friend \]

To get 2 factorials we need 1 factorial. \[ He doesn\'t know the value
of 1 factorial, so he gives it to his friend \]

1 factorial is 1 \[ He sends the solution of 1 factorial \]

``` {#bd8fa272-3d1e-4e38-9585-be6c8c26163b .code}
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

::: {#d333b6c0-d415-40bf-b6e4-47d167e394ca .column-list}
::: {#fd3914b9-2983-4c20-a1f5-e2e9ae41fe9a .column style="width:50%"}
``` {#5688f199-e2e7-4b18-b719-1f27df2351dd .code}
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
:::

::: {#d17991b6-3f8f-45f1-9615-699485518358 .column style="width:50%"}
:::
:::

I hope this article helps you to get an overview of* **Recursion***.

Thanks for your time,

-Tashin Parvez
:::
