**Topic:** Evaluation of Postfix Expression Using Stack

**AIM:**  
To evaluate a user-given postfix expression containing multiplication and addition operators using a stack.

**ALGORITHM:**  
1. Start  
2. Create an empty stack  
3. Read the postfix expression from the user  
4. Traverse each character in the expression:  
   a. If the character is a digit, push it onto the stack as an integer  
   b. If the character is an operator (+, *):  
      - Pop the top two elements from the stack (operand2 then operand1)  
      - Perform the operation (operand1 + operand2 or operand1 * operand2)  
      - Push the result back onto the stack  
5. After traversal, the final result is the only element left in the stack  
6. Display the postfix expression and the evaluation result  
7. End  

**PROGRAM:**  
```
def evaluate_postfix(expression):
    stack = []
    for char in expression:
        if char.isdigit():
            stack.append(int(char))
        elif char == '+':
            operand2 = stack.pop()
            operand1 = stack.pop()
            stack.append(operand1 + operand2)
        elif char == '*':
            operand2 = stack.pop()
            operand1 = stack.pop()
            stack.append(operand1 * operand2)
    return stack.pop()

expression = input()
print(f"postfix expression:  {expression}")
result = evaluate_postfix(expression)
print(f"Evaluation result:  {result}")
```

**OUTPUT:**  
```
23+45+*
postfix expression:  23+45+*
Evaluation result:  45
```

**RESULT:**  
The program successfully evaluates the given postfix expression containing addition and multiplication operators using stack operations. For the expression "23+45+*", the computed result is 45, which matches the expected output.
