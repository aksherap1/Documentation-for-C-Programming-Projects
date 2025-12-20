Writeup for ECE13\_ExtraCredit

**My Issue was the operand order in stack pops for RPN:**  
When evaluating Reverse Polish Notation (RPN) expressions for ECE13 Lab05, I kept getting incorrect results, especially with subtraction and division. Basically, expressions like:

    **5 6 \-**

were giving me “1” instead of the correct answer, “-1”.

Before, I was popping values from the stack and applying the operation like this:

    StackPop(\&stack, \&operand1);  
    StackPop(\&stack, \&operand2);  
    result \= operand1 \- operand2;

However, this turned out to be the reverse of what is actually accurate. This bug caused many test cases to fail. Subtraction and division consistently returned incorrect results and since there were no warnings, I was not even able to figure out exactly what was wrong. This made debugging difficult because everything looked right, but there was a logic issue somewhere within that code. Then I realized that the first value popped from the stack is the second operand and the second value popped is the first operand. Consequently, this made me realize that in RPN, you push numbers onto the stack, then when you reach an operator, you pop the top two numbers, and then you apply the operator in the order they were pushed.

**For Example:**  
So, for \`5 6 \-\`:  
\- Push 5 → Stack: \[5\]  
\- Push 6 → Stack: \[5, 6\]  
\- Encounter \`-\`:  
  \- Pop 6 → operand1  
  \- Pop 5 → operand2  
  \- Compute: operand2 \- operand1 \= 5 \- 6 \= \-1

**My Steps to Resolution:**  
    StackPop(\&stack, \&operand1); // Top of stack  
    StackPop(\&stack, \&operand2); // Second from top  
    result \= operand2 \- operand1; // Correct order

WHen I realized that the most recently pushed value (top of stack) is actually the second operand, everything made sense. I corrected the operand order for subtraction and division and my test cases finally passed. I also learned how to add debug printf()s in general like for example I used test known expressions like "10 2 /" and "5 6 \-" to catch logic errors earlier and have my code be more efficient. 

**Code Example:**  
    if (StackGetSize(\&stack) \< 2\) {  
        return RPN\_ERROR\_STACK\_UNDERFLOW;  
    }

    double operand1, operand2;  
    StackPop(\&stack, \&operand1);  
    StackPop(\&stack, \&operand2);  
    double result \= 0;

    if (token\[0\] \== '-') {  
        result \= operand2 \- operand1;  
    } else if (token\[0\] \== '/') {  
        if (operand1 \== 0\) {  
            return RPN\_ERROR\_DIVIDE\_BY\_ZERO;  
        }  
        result \= operand2 / operand1;  
    } else if (token\[0\] \== '+') {  
        result \= operand2 \+ operand1;  
    } else if (token\[0\] \== '\*') {  
        result \= operand2 \* operand1;  
    }

    StackPush(\&stack, result);

**Reflection:**   
This was one of my many difficult issues I dealt with in this class ECE13. Understanding the operand order in stack-based evaluation helped me fix my implementation and it also prepared me for later labs involving expression parsing, recursion, and abstract data types.

