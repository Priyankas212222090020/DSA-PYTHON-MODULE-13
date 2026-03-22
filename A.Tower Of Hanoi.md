**AIM:**  
To implement the Tower of Hanoi problem using a recursive function in Python and display all moves of disks between pegs A, B, and C for a given number of disks.

**ALGORITHM:**  
1. Start  
2. Define a recursive function `tower_of_hanoi(n, source, target, auxiliary)`  
3. If `n == 1`, move disk from source to target and print the move  
4. Else:  
   a. Move `n-1` disks from source to auxiliary using target as helper  
   b. Move the nth disk from source to target and print the move  
   c. Move `n-1` disks from auxiliary to target using source as helper  
5. Get the number of disks from the user  
6. Call the recursive function with pegs A (source), C (target), B (auxiliary)  
7. End  

**PROGRAM:**  
```
def tower_of_hanoi(n, source, target, auxiliary):
    if n == 1:
        print(f"Move disk from {source} to {target}")
        return
    tower_of_hanoi(n-1, source, auxiliary, target)
    print(f"Move disk from {source} to {target}")
    tower_of_hanoi(n-1, auxiliary, target, source)

n = int(input())
print(f"No. of disks = {n}")
tower_of_hanoi(n, 'A', 'C', 'B')
```

**OUTPUT:**  
```
2
No. of disks = 2
Move disk from A to B
Move disk from A to C
Move disk from B to C
```

```
3
No. of disks = 3
Move disk from A to C
Move disk from A to B
Move disk from C to B
Move disk from A to C
Move disk from B to A
Move disk from B to C
Move disk from A to C
```

```
4
No. of disks = 4
Move disk from A to B
Move disk from A to C
Move disk from B to C
Move disk from A to B
Move disk from C to A
Move disk from C to B
Move disk from A to B
Move disk from A to C
Move disk from B to C
Move disk from B to A
Move disk from C to A
Move disk from B to C
Move disk from A to B
Move disk from A to C
Move disk from B to C
```

**RESULT:**  
The program successfully implements the Tower of Hanoi using recursion and displays all disk moves for any given number of disks. The moves follow the optimal solution of \(2^n - 1\) steps, ensuring the rules of the puzzle are satisfied.
