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

## 2577

```python
a = int(input())
b = int(input())
c = int(input())

arr = [0]*10
sum = a*b*c

for i in str(sum):
    arr[int(i)]+=1

for i in arr:
    print(i)
```

<details>
<summary></summary>

- 숫자 곱하고 각자리수 인덱스값을 통해 값 +1씩 전체 반복

</details>

## 1919

```python
a = input()
b = input()
cnt = [0]*26

for i in a:
    cnt[ord(i)-97]+=1

for i in b:
    cnt[ord(i)-97]-=1

print(sum(map(abs,cnt)))
```

<details>
<summary></summary>

- 소문자 각각 길이 1000이하
- 에너그램 -> 구성하는 문자의 개수가 각각 동일해야함
- 문자열1의 각 알파벳 개수 - 문자열2 의 각 알파벳 개수
- 문자열2에 있는게 a에 없을수도 -> 절대값으로 계산

</details>


## 11328

```python
n = int(input())

for i in range(0,n):
    a,b = map(str,input().split())
    cnt = [0]*26

    for i in a:
        cnt[ord(i)-97]+=1

    for i in b:
        cnt[ord(i)-97]-=1
        
    if sum(map(abs,cnt))==0:
        print("Possible")
    else:
        print("Impossible")
```

<details>
<summary></summary>

- 에너그램 문제와 동일
- 구성하는 알파뱃의 개수가 동일해야함

</details>


## 1475

```python
n = input()
arr = [1]*10
cnt =1

for i in n:
    idx = int(i)
    if(arr[idx]>0):
        arr[idx] -=1
    elif(idx==6 and arr[9]>0):
        arr[9]-=1
    elif(idx==9 and arr[6]>0):
        arr[6]-=1
    else:
        for i, value in enumerate(arr):
            arr[i] = value+1
        cnt+=1
        arr[idx]-=1

print(cnt)
```

<details>
<summary></summary>

- 0~9까지 1set
- 6,9는 뒤집어서 공유가능
- 최소 set의 개수
</details>



