## 10808

```python
str = input()
arr = [0]*26

for i in str:
    arr[ord(i)-97]+=1
    
print(*arr)
```
<details>
<summary></summary>

- 유니코드값을 통한 인덱스
- 
</details>

## 10807

```python
n = int(input())

numbers = list(map(int,input().split()))
v = int(input())

print(numbers.count(v))

```

<details>
<summary></summary>

- 배열에 값을 추가 or 값을 인덱스로
- 결과적으로는 배열에 값을 추가하고 count 사용

</details>

## 13300

```python
n,k = map(int,input().split())
current = {0:[0]*7,1:[0]*7}
cnt = 0

for i in range(0,n):
    s,g = map(int,input().split())
    tmp = current[s][g] +1
    
    if(tmp>k):
        current[s][g] =1
        cnt+=1
    else:
        if(tmp==1):
            cnt+=1
        current[s][g] = tmp

print(cnt)

```

<details>
<summary></summary>

- 총 학생수
- 한방 최대인원
- 성별과 학년
- 학생을 성별과 학년, 한방 최대인원에 알맞게 방배정하기

1) 남자와 여자는 다른방
2) 한방에 최대인원 있다.
3) 같은 학년끼리 배정
-> 남자와 여자를 학년별로 방을 구분하여 현재인원 상태확인
- 0:[0,0,0,0,0,0], 1:[0,0,0,0,0,0]
- +1씩 하면서 최대인원일 경우 방 카운트 +1, 그방의 상태 초기화

추가
- 편의를 위해 배열 크기는 7로
- 방 카운트는 최대인원이 찰때뿐만 아니라 최초에 방에 입장할때도 추가해야함

</details>




