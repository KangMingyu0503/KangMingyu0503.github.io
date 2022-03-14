---
layout : single
title : "Algorithm_Stack"
categories : Algorithm
tag : [Python,Algorithm]
toc : true
author_profile: true
serach: false
---

# ⚙️ ALGORITHM_STACK ⚙️
<br>

> 1️⃣ __What Is Stack?__
 
 -  後入先出
 -  LIFO - Last In, First Out
 -  Stack is a linear data structure which follows a particular order in which the operations are performed.
 -  스택은 데이터의 삽입과 삭제가 데이터의 가장 한쪽 끝에서만 일어나는 자료구조 입니다.
    가장 마지막에 삽입된 데이터가 가장 먼저 사용되거나 삭제됩니다.
    
    <br>
    
> 2️⃣ __Method__

 * ▶️ *Push , Pop*
   * <br><img src="https://github.com/KangMingyu0503/KangMingyu0503.github.io/blob/master/_posts/assets/images/push,pop.png?raw=True" alt="Markdown Monster icon"/><br>
   * push() − Pushing (storing) an element on the stack.
   * pop()  − Removing (accessing) an element from the stack.
   * 데이터를 삽입하는 과정을 push, 가장 마지막에 삽입한 데이터를 삭제하는 과정을 pop이라고 부릅니다. 
   * ❗️ 데이터를 삭제하는 pop의 경우 현재 스택에 데이터가 비어있는지 여부를 먼저 확인한 후에 실행합니다.

 * ▶️ *Top*
   * <br><img src="https://github.com/KangMingyu0503/KangMingyu0503.github.io/blob/master/_posts/assets/images/top.png?raw=True" alt="Markdown Monster icon"/><br>
   * pop이 가장 마지막에 삽입한 데이터를 삭제하는 것이라면 top은 가장 마지막에 삽입한 데이터를 삭제하지 않고 return 해주는 메소드입니다.
 
 * ▶️ *isEmpty*
   * <br><img src="https://github.com/KangMingyu0503/KangMingyu0503.github.io/blob/master/_posts/assets/images/isEmpty.png?raw=True" alt="Markdown Monster icon"/><br>
   * peek() − get the top data element of the stack, without removing it.
   * isFull() − check if stack is full.
   * isEmpty() − check if stack is empty.
   * peek은 현재 스택의 요소를 제거하지않고 가져오는 메소드 입니다.
   * isFull은 현재 스택이 가득차있는지 여부를 확인하는 메소드 입니다.
   * isEmpty는 현재 스택이 비어있는지 여부를 확인하는 메소드 입니다.

> 3️⃣ __Code__

* ▶️ *List*
  * ```python
    class Stack():
    def __init__(self):
        self.stack = []
        
    def push(self, data):
        self.stack.append(data)
        
    def pop(self):
        pop_object = None
        if self.isEmpty():
            print("Stack is Empty")
        else:
            pop_object = self.stack.pop()
            
        return pop_object
            
    def top(self):
        top_object = None
        if self.isEmpty():
            print("Stack is Empty")
        else:
            top_object = self.stack[-1]
            
        return top_object
            
            
    def isEmpty(self):
        is_empty = False
        if len(self.stack) == 0:
            is_empty = True
            
        return is_empty
    ```
    
    

 

