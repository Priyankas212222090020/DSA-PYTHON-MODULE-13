**Topic:** Stack Implementation Using List

**AIM:**  
To implement a stack using Python list with `append()` and `pop()` methods, accept seven items from the user, display the stack, pop five items, and display the stack again.

**ALGORITHM:**  
1. Start  
2. Create an empty list `stack`  
3. Use a loop to accept 7 items from the user and append each to the stack  
4. Display the stack with the message "Stack before elements are popped"  
5. Use a loop to pop 5 items from the stack  
6. Display the remaining stack with the message "Stack after elements are popped:"  
7. End  

**PROGRAM:**  
```
stack = []
for i in range(7):
    stack.append(input())
print("Stack before elements are popped")
print(stack)
for i in range(5):
    stack.pop()
print("Stack after elements are popped:")
print(stack)
```

**OUTPUT:**  
```
Hello
Everyone!
Welcome
to
Python
World
!!!
Stack before elements are popped
['Hello', 'Everyone!', 'Welcome', 'to', 'Python', 'World', '!!!']
Stack after elements are popped:
['Hello', 'Everyone!']
```

**RESULT:**  
The program successfully implements a stack using Python list with `append()` and `pop()` methods. It accepts seven items, displays the stack, removes five items using pop, and displays the remaining two items correctly. All test cases passed with 1.00/1.00 marks.
