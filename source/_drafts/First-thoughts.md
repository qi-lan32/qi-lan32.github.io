---
title: First_thoughts
tags:
---
# First Week 

- deep work sessions
- canvas 101: UMPIRE, practice 
- sat staff/team meet 
- expression evaluaton - stack

## Data Structures: Expression Evaluation

One data structure problem I revisited this past week is expression evaluation using stack. In this problem, we are given expression, like (((15 / (7 - (1 + 1))) * 3) - (2 + (1 + 1))), and using stack, we are to turn this expression into Reverse Polish notation and then evaluate the expression. **Reverse Polish notation** is when we write the numbers of an inner expression (e.g. (1 + 1)), in the format of '1 1 +', with the numbers in front and the operand at the end. We would move through the parentheses on the level of priority until all have been converted. 

One major change I made in my solution is to change from using string and directly manipulate the expression in string format to using scanner and tokenize each character for interation. I realized that if I manipulated string directly, the program would not be able to recognize numbers with multiple digits

MAJOR CHANGES: [convertToReversePolish]
        * at first used string, but realize it couldn't tell apart numbers with multiple digits
        * then I changed to using string[] and planned to join it at the end, but the final string end up with
            extra slots from the initialization of the string[]
        * my final decision was to use stack, just like my previous implementation of the problem, then use String.join()
            to convert to string

        [calculateResult]
        * transform string into scanner (similar process in convertToReversePolish), perform arithmetic on the expression
