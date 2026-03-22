**Topic:** Evaluation of Prefix Expression Using Stack

**AIM:**  
To evaluate a user-given prefix expression containing two-digit numbers and binary operators (+, -, *, /, %) using stack concept with space-separated tokens.

**ALGORITHM:**  
1. Start  
2. Define function `str_list(s)` to split the input string into a list of tokens  
3. Define function `prefix_Eval(x)` to evaluate the prefix expression:  
   a. Create an empty stack  
   b. Traverse the token list from right to left  
   c. If token is a number, convert to float and push onto stack  
   d. If token is an operator:  
      - Pop two elements from stack (operand1 then operand2)  
      - Perform operation (operand1 operator operand2)  
      - Push result back onto stack  
   e. After traversal, return the top element of stack  
4. Read the input expression  
5. Convert to list using `str_list()`  
6. Display the prefix expression  
7. Evaluate using `prefix_Eval()` and display the result  
8. End  

**PROGRAM:**  
```
def str_list(s):
    return s.split()

def prefix_Eval(x):
    stack = []
    for token in reversed(x):
        if token.lstrip('-').isdigit():
            stack.append(float(token))
        else:
            operand1 = stack.pop()
            operand2 = stack.pop()
            if token == '+':
                stack.append(operand1 + operand2)
            elif token == '-':
                stack.append(operand1 - operand2)
            elif token == '*':
                stack.append(operand1 * operand2)
            elif token == '/':
                stack.append(operand1 / operand2)
            elif token == '%':
                stack.append(operand1 % operand2)
    return stack.pop()

expression = input()
tokens = str_list(expression)
print(f"The prefix expression is {expression}")
result = prefix_Eval(tokens)
print(f"The result is {result}")
```

**OUTPUT:**  
```
- + 18 / 16 02 10
The prefix expression is - + 18 / 16 02 10
The result is 16.0

```
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/91ac0708-4490-4466-b614-a10e2887ba55" />

```
+ 09 * 12 06
The prefix expression is + 09 * 12 06
The result is 81.0
```

**RESULT:**  
The program successfully evaluates prefix expressions containing two-digit numbers and binary operators (+, -, *, /, %) using stack. It handles space-separated tokens and evaluates from right to left, producing accurate results for all test cases.
