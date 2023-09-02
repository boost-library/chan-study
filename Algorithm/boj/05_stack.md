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

----
# Stack plus

## 4949

```python
while True:
    text = input()
    stack= []
    if text == '.':
        break

    for i in text:
        if i=='(' or i=='[':
            stack.append(i)
        
        elif i == ')':
            if stack and stack[-1]=='(':
                stack.pop()
            else:
                stack.append(-1)
                break
        elif i == ']':
            if stack and stack[-1]=='[':
                stack.pop()
            else:
                stack.append(-1)
                break
    if stack:
        print("no")
    else :
        print("yes")
```
<details>
<summary></summary>

- 일반적인 stack
- if stack을 먼저하지 않을경우 stakc이 비어있을 경우에 index오류
  
</details>

## 3986

```python
n = int(input())
cnt = 0

for _ in range(n):
    text = input()
    stack = []

    for i in text:
        if stack and stack[-1] == i:
            stack.pop()
        else:
            stack.append(i)
    if not stack:
        cnt += 1
print(cnt)
```
<details>
<summary></summary>

- 일반적인 stack
- 괄호쌍 찾기와 동일, 동일한 문자가 head에 위치해야 한다.
  
</details>

## 9012

```python
n = int(input())

for _ in range(n):
    text = input()
    stack= []

    for i in text:
        if i=='(':
            stack.append(i)
        
        elif i == ')':
            if stack and stack[-1]=='(':
                stack.pop()
            else:
                stack.append(-1)
                break
    if stack:
        print("NO")
    else :
        print("YES")
```
<details>
<summary></summary>

- 일반적인 stack
- 4949문제와 동일
  
</details>

## 9012

```python
text = input()
stack = []
cnt = 0
flag = True

for i in text:
    if i == '(':
        stack.append(i)
        flag = True

    else:
        stack.pop()

        if flag:
            cnt += len(stack)
        else:
            cnt += 1

        flag = False

print(cnt)
```
<details>
<summary></summary>
    
- 괄호 하나로는 1개의 막대기도 발생X
- 최소 (()) 필요 
- ) 부분에 막대기의 끝부분이 위치하는지 파악
- depth
- () 하나짜리가 아닌 닫히는 부분에 막대기 개수 +1
  
</details>
