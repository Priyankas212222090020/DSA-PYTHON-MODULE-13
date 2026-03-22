**Topic:** Evaluation of Postfix Expression Using Stack

**AIM:**  
To evaluate a user-given postfix expression containing multiplication and addition operators using stack concept.

**ALGORITHM:**  
1. Start  
2. Create an empty stack  
3. Read the postfix expression from the user  
4. Traverse each character in the expression:  
   a. If the character is a digit, push it onto the stack as an integer  
   b. If the character is '+', pop two elements, add them, and push the result  
   c. If the character is '*', pop two elements, multiply them, and push the result  
5. After processing all characters, the final result is the top element of the stack  
6. Display the postfix expression and evaluation result  
7. End  

**PROGRAM:**  
```
def evaluate_postfix(exp):
    stack = []
    for ch in exp:
        if ch.isdigit():
            stack.append(int(ch))
        elif ch == '+':
            b = stack.pop()
            a = stack.pop()
            stack.append(a + b)
        elif ch == '*':
            b = stack.pop()
            a = stack.pop()
            stack.append(a * b)
    return stack.pop()

exp = input()
print(f"postfix expression:  {exp}")
result = evaluate_postfix(exp)
print(f"Evaluation result:  {result}")
```

**OUTPUT:**  
```
23+45+*
postfix expression:  23+45+*
Evaluation result:  45
```

**RESULT:**  
The program successfully evaluates the postfix expression containing addition and multiplication operators using stack operations. For the input "23+45+*", the evaluation result is 45, matching the expected output.
