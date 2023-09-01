## 2164

```python
import sys
from collections import deque

input = sys.stdin.readline

n: int = int(input().rstrip())
dq = deque()

for i in range(n):
    cmd = input().rstrip().split()
    if cmd[0] == "push_front":
        dq.appendleft(cmd[1])
    elif cmd[0] == "push_back":
        dq.append(cmd[1])
    elif cmd[0] == "pop_front":
        print(dq.popleft() if dq else -1)
    elif cmd[0] == "pop_back":
        print(dq.pop() if dq else -1)
    elif cmd[0] == "size":
        print(len(dq))
    elif cmd[0] == "empty":
        print(0 if dq else 1)
    elif cmd[0] == "front":
        print(dq[0] if dq else -1)
    elif cmd[0] == "back":
        print(dq[-1] if dq else -1)
```
<details>
<summary></summary>

- 일반적인 deque
- if else 삼항연산자 처럼 사용함

  
</details>

## 1021

```python
import sys
from collections import deque

input = sys.stdin.readline
n, m = map(int, input().rstrip().split())
dq = deque(maxlen=n)

target = list(map(int, input().rstrip().split()))
for i in range(1, n+1):
    dq.append(i)

cnt = 0

for i in target:
    while True:
        if i == dq[0]:
            dq.popleft()
            break
    
        if dq.index(i) < len(dq)/2:
            while i != dq[0]:
                dq.append(dq.popleft())
                cnt += 1
        else:
            while i != dq[0]:
                dq.appendleft(dq.pop())
                cnt += 1
print(cnt)
```
<details>
<summary></summary>

- 일반적인 deque
- 문제를 이해하는게 중요한듯
- 왼쪽으로 돌려야하는지 오른쪽으로 돌려야하는지를 파악하는게 중요

  
</details>