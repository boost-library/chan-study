## 10828

```python
import sys

input = sys.stdin.readline
n: int = int(input().rstrip())
stack = []

for i in range(n):
    cmd = input().rstrip().split()
    if cmd[0] == "push":
        stack.append(cmd[1])
        pass
    elif cmd[0] == "pop":
        if len(stack) != 0:
            print(stack.pop())
        else:
            print(-1)
    elif cmd[0] == "size":
        print(len(stack))
    elif cmd[0] == "empty":
        if len(stack) != 0:
            print(0)
        else:
            print(1)
    elif cmd[0] == "top":
        if len(stack) != 0:
            print(stack[len(stack)-1])
        else:
            print(-1)
```
<details>
<summary></summary>

- 일반적인 stack
- 파이썬 list의 시간복잡도 숙지
  
</details>

## 10773

```python
import sys
input = sys.stdin.readline

k: int = int(input().rstrip())
stack = []

for i in range(k):
    num = int(input().rstrip())
    stack.pop() if num==0 else stack.append(num)

print(sum(stack))
```
<details>
<summary></summary>

- 일반적인 stack
- 파이썬 if else를 삼항 연산자처럼 사용
  
</details>