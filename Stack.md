# Stack

- A stack is a linear data structure that follows the Last-In-First-Out (LIFO) principle.
- A stack has two primary operations: push and pop.
  - Push: Adds an element to the top of the stack.
  - Pop: Removes the top element from the stack.

- Stacks can be implemented using arrays or linked lists.
  - Array Implementation: In this approach, a fixed-size array is used to store the stack elements. Push and pop operations modify the top index of the array.
  - Linked List Implementation: Here, a linked list is used to implement the stack. Each node in the linked list represents an element, and the top of the stack is the head of the list.

## Stack Implementation

```py
class Stack:
    MAX_SIZE = 100

    def __init__(self):
        self.top = -1
        self.item = [0] * self.MAX_SIZE

    def push(self, element):
        if self.top >= self.MAX_SIZE - 1:
            print("Stack is full on push")
        else:
            self.top += 1
            self.item[self.top] = element

    def is_empty(self):
        return self.top < 0

    def pop(self):
        if self.is_empty():
            print("Stack is empty on pop")
        else:
            self.top -= 1

    def get_top(self):
        if self.is_empty():
            print("Stack is empty on getTop")
            return None
        else:
            stack_top = self.item[self.top]
            print(stack_top)
            return stack_top

    def print_stack(self):
        print("[", end="")
        for i in range(self.top, -1, -1):
            print(self.item[i], end=" ")
        print("]")

if __name__ == "__main__":
    s = Stack()

    # Push elements onto the stack
    s.push(5)
    s.push(10)
    s.push(15)
    s.push(20)

    # Print the stack
    s.print_stack()

    # Get and print the top element of the stack
    y = s.get_top()

    # Pop an element from the stack
    s.pop()

    # Push another element onto the stack
    s.push(7)

    # Print the stack again
    s.print_stack()
```
