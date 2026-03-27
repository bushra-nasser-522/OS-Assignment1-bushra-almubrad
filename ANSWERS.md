# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A process is a program in execution and has its own memory.  
A thread is a smaller unit inside the process.  
Threads share memory, but processes do not.  
Threads are faster and use fewer resources.  
We used threads because they are easier for scheduling.

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
Round-Robin scheduling, each process gets a fixed time quantum.  
If the process does not finish, it is stopped by the CPU.  
Then it is moved to the end of the ready queue.  
It waits until it gets another turn to run again.  
This helps all processes share the CPU fairly

Example from my output:

P1 yields CPU for context switch
P1 (Priority: 1) added to ready queue

**Explanation of example:**

 P1 was still not finished after its time quantum.  
So it was taken off the CPU.  
Then it was added again to the ready queue.  
It will get another chance to run later


*Why this is important for fairness:*
All processes get a chance to use the CPU.  
No process can take all the CPU time.  
This keeps the system fair


## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]
P1 is created as a thread before calling Thread.start().  

2. **Runnable**: [When does P1 become Runnable?]
P1 becomes runnable after calling Thread.start() and is added to the ready queue.  

3. **Running**: [When is P1 Running?]
P1 is running when the CPU executes its run() method.

4. **Waiting**: [When/why would P1 be Waiting?]
P1 goes to waiting when Thread.sleep() is called during execution.  
The main thread also uses Thread.join() to wait for it to finish.

5. **Terminated**: [When is P1 Terminated?]
P1 is terminated when it finishes execution and its remaining time becomes zero.
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
A download manager handles several file downloads at once.  
Each download works as a separate task.

**Why Round-Robin works well here**: 
Each download is given a short time to run.  
The CPU keeps switching between them.  
This helps all downloads progress together.  
This is similar to our program where processes run one after another.  
The scheduler controls them just like in our code.

### Example 2: [Name of application/scenario]

**Description**: 
Games run different tasks like movement, graphics, and network.  
All these tasks need to run continuously.

**Why Round-Robin works well here**:

Each task gets a small share of CPU time.  
The system switches between them very fast.  
This keeps the game running smoothly.  
This is similar to our simulation where tasks take turns.  
The scheduler manages them like in the program.

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
