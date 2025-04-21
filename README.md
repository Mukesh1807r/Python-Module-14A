# Deleting an Element from Circular Queue

## 📌 Aim
To write a Python program that deletes an element from a **circular queue**. The queue will be implemented using the `deque` from the `collections` module, and the program will handle the insertion of elements and deletion from the queue.

---

## 🛠 Procedure
1. Define a function `insert_into_circular_queue(size, values)` to insert elements into the circular queue.
   - Initialize a queue with a maximum size using `deque`.
   - Insert values into the queue, ensuring that it doesn't exceed the defined size.
2. Define a function `delete_from_circular_queue(queue)` to delete the front element of the queue.
   - Remove the element from the front of the queue using `popleft()`.
3. After deleting an element, print the updated queue.

---

## 💻 Program

```python
from collections import deque

def insert_into_circular_queue(size, values):
    queue = deque(maxlen=size)
    for value in values:
        if len(queue) < size:
            queue.append(value)
        else:
            print("Queue is full")
            break
    return list(queue)

def delete_from_circular_queue(queue):
    if queue:
        queue.popleft()
    return list(queue)

size = int(input())
values = [int(input().strip()) for _ in range(size)]
queue = deque(values, maxlen=size)
print(list(queue))

queue = delete_from_circular_queue(queue)
print(list(queue))
```
---

##Output

![image](https://github.com/user-attachments/assets/11f4d1c8-5dde-4abd-9ca7-d6a0672b4b45)

##Result

Thus, the program was successfully created and executed to delete an element from the circular queue.






