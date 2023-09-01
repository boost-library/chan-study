
## 18258

```python
import sys

input = sys.stdin.readline

n: int = int(input().rstrip())
queue = []
head:int = 0

for i in range(n):
    cmd = input().rstrip().split()
    if cmd[0] == "push":
        queue.append(cmd[1])
    elif cmd[0] == "pop":
        if len(queue) > head:
            print(queue[head])
            head+=1
        else:
            print(-1)
    elif cmd[0] == "size":
        print(len(queue)-head)
    elif cmd[0] == "empty":
        if len(queue) == head:
            head=0
            queue.clear()
            print(1)
        else:
            print(0)
    elif cmd[0] == "front":
        if len(queue) >head:
            print(queue[head])
        else:
            print(-1)
    elif cmd[0] == "back":
        if len(queue) >head:
            print(queue[-1])
        else:
            print(-1)
```
<details>
<summary></summary>

- 일반적인 queue
- pop index와 함께 사용시 O(N)
- deque을 사용해도 무방하지만 heaed의 위치를 계산해서 풀이함
  
</details>

## 2164

```python
import sys
from collections import deque

input = sys.stdin.readline

n: int = int(input().rstrip())
dq = deque(maxlen=n)

for i in range(1,n+1):
    dq.append(i)

while(len(dq)!=1):
    dq.popleft()
    dq.append(dq.popleft())

print(dq[0])
```
<details>
<summary></summary>

- 일반적인 queue
- deque에 maxlen 설정가능

  
</details>