## 1406

```python
import sys

input = sys.stdin.readline

left: list = list(input().rstrip())
right: list = list()
n: int = int(input().rstrip())

for i in range(0, n):
    cmd = list(input().rstrip().split())
    if(cmd[0] == "L"):
        if(left):
            right.append(left.pop())
    elif(cmd[0] == "D"):
        if(right):
            left.append(right.pop())
    elif(cmd[0] == "B"):
        if(left):
            left.pop()
    else:
        left.append(cmd[1])

left_text = ''.join(left)
right_text = ''.join(right[::-1])
print(left_text+right_text)
```
<details>
<summary></summary>

- 2번 틀림(일반적인 시간초과,리스트 index err)
- 연결리스트로 다시 풀기
  
</details>


## 5397

```python
import sys

input = sys.stdin.readline
t: int = int(input().rstrip())

for i in range(t):
    text = input().rstrip()
    left: list = list()
    right: list = list()
    for i in text:
        if (i == "-"):
            if (left):
                left.pop()
        elif (i == "<"):
            if (left):
                right.append(left.pop())
        elif (i == ">"):
            if (right):
                left.append(right.pop())
        else:
            left.append(i)
    left_text = ''.join(left)
    right_text = ''.join(right[::-1])
    print(left_text+right_text)
```
<details>
<summary></summary>

- 1406문제와 동일
  
</details>

## 1158

```python
from collections import deque

n, k = map(int, input().split())
q = deque()
res = []

for i in range(1, n + 1):
    q.append(i)

while q:
    for i in range(1, k):
        q.append(q.popleft())
    res.append(q.popleft())

print("<{}>".format(", ".join(map(str, res))))
```
<details>
<summary></summary>

- deque를 통해 위에 2문제도 확인하기
- k, n은 5000이하
- 과거에 풀었던 문제
  
</details>
