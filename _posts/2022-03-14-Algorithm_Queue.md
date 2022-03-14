---
layout : single
title : "Algorithm_Queue"
categories : Algorithm
tag : [Python,Algorithm]
toc : true
author_profile: true
serach: false
---

# ⚙️ ALGORITHM_QUEUE ⚙️
<br>

> 1️⃣ __What Is Queue?__
 
 - 先入先出
 - FIFO - First-In-First-Out methodology
 - Like stack, queue is a linear data structure that stores items in First In First Out manner. With a queue the least recently added item is removed first.
 - 먼저 들어간(enqueue) 데이터가 먼저 삭제(dequeue)됩니다. 

> 2️⃣ __Method__

 * ▶️ *Basic*
   * <br><img src="https://github.com/KangMingyu0503/KangMingyu0503.github.io/blob/master/_posts/assets/images/queue.png?raw=True" alt="Markdown Monster icon"/><br>
   * Enqueue: Adds an item to the queue. If the queue is full, then it is said to be an Overflow condition – Time Complexity : O(1)
   * Dequeue: Removes an item from the queue. The items are popped in the same order in which they are pushed. If the queue is empty, then it is said to be an Underflow condition – Time Complexity : O(1)
   * Front: Get the front item from queue – Time Complexity : O(1)
   * Rear: Get the last item from queue – Time Complexity : O(1)
   
 * ▶️ *Implementation*
   * maxsize – Number of items allowed in the queue.
   * empty() – Return True if the queue is empty, False otherwise.
   * full() – Return True if there are maxsize items in the queue. If the queue was initialized with maxsize=0 (the default), then full() never returns True.
   * get() – Remove and return an item from the queue. If the queue is empty, wait until an item is available.
   * get_nowait() – Return an item if one is immediately available, else raise QueueEmpty.
   * put(item) – Put an item into the queue. If the queue is full, wait until a free slot is available before adding the item.
   * put_nowait(item) – Put an item into the queue without blocking.
   * qsize() – Return the number of items in the queue. If no free slot is immediately available, raise QueueFull.

> 3️⃣ __Code__

* ▶️ *Input1*
  * ```python
    # Python program to
    # demonstrate queue implementation
    # using list

    # Initializing a queue
    queue = []

    # Adding elements to the queue
    queue.append('a')
    queue.append('b')
    queue.append('c')
    
    print("Initial queue")
    print(queue)
    
    # Removing elements from the queue
    print("\nElements dequeued from queue")
    print(queue.pop(0))
    print(queue.pop(0))
    print(queue.pop(0))
    
    print("\nQueue after removing elements")
    print(queue)
    
    # Uncommenting print(queue.pop(0))
    # will raise and IndexError
    # as the queue is now empty

    ```
* ▶️ *Output1*
  * ```python
    Initial queue
    ['a', 'b', 'c']
    
    Elements dequeued from queue
    a
    b
    c
    
    Queue after removing elements
    []

    ```
* ▶️ *Input2*
  * ```python
    # Python program to
    # demonstrate implementation of
    # queue using queue module
    
    
    from queue import Queue
    
    # Initializing a queue
    q = Queue(maxsize = 3)
    
    # qsize() give the maxsize
    # of the Queue
    print(q.qsize())
    
    # Adding of element to queue
    q.put('a')
    q.put('b')
    q.put('c')
    
    # Return Boolean for Full
    # Queue
    print("\nFull: ", q.full())
    
    # Removing element from queue
    print("\nElements dequeued from the queue")
    print(q.get())
    print(q.get())
    print(q.get())
    
    # Return Boolean for Empty
    # Queue
    print("\nEmpty: ", q.empty())
    
    q.put(1)
    print("\nEmpty: ", q.empty())
    print("Full: ", q.full())
    
    # This would result into Infinite
    # Loop as the Queue is empty.
    # print(q.get())

    ```
* ▶️ *Output2*
  * ```python
    0
    
    Full:  True
    
    Elements dequeued from the queue
    a
    b
    c
    
    Empty:  True
    
    Empty:  False
    Full:  False


    ```


  
