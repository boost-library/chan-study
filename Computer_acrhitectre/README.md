## 목차
|day one | day two |
|--- | --- |
|[필요성](#필요성)|[비트](#비트)|
|[데이터](#데이터)|[워드](#워드)|
|[명령어](#명령어)|[이진법](#이진법)|
|[프로그램](#프로그램)|[플래그](#플래그)|
|[cpu](#cpu)|[십육진법](#십육진법)|
|[메모리](#메모리)|[문자 집합](#문자집합)|
|[보조기억장치](#보조기억장치)|[인코딩](#인코딩)|
|[입출력장치](#입출력장치)|[디코딩](#디코딩)|
|[메인보드](#메인보드)|[아스키](#아스키)|
|[시스템버스](#시스템버스)|[유니코드](#유니코드)|
||[utf](#utf)|
||[고급 언어](#고급언어)|
||[저급 언어](#저급언어)|
||[기계어](#기계어)|
||[어셈블리어](#어셈블리어)|
||[컴파일](#컴파일)|
||[인터프리터](#인터프리터)|
||[명령어](#명령어)|
||[연산코드](#연산코드)|
||[오퍼랜드](#오퍼랜드)|
||[주소 지정 방식](#주소지정방식)|


### 필요성
<details>
<summary></summary>

전공과목과 기업에서 요구하는 컴퓨터과학의 가장 근본적이고 기초적인 지식이다.
정확하게 이해한다면 설계,개발에서 효율, 성능, 비용부분에서 이득을 볼수있으며 문제발생시 근본적인 해결에 도움을 준다.

</details>

### 데이터
<details>
<summary></summary>

정적인 정보

</details>

### 명령어
<details>
<summary></summary>

컴퓨터를 실질적으로 움직이는 정보

</details>

### 프로그램
<details>
<summary></summary>

명령어들의 모음

</details>

### cpu
<details>
<summary></summary>

- 메모리에 저장된 값을 읽고, 해석, 실행하는 장치
- 내부에 ALU, 레지스터,제어장치
- ALU : 계산하는 장치
- 레지스터 : 임시 저장장치
- 제어장치 : 제어 신호를 발생시키고 명령어를 해석하는 장치

</details>

### 메모리
<details>
<summary></summary>

- 현재 실행되는 프로그램의 명령어와 데이터를 저장
- 주소개념이 있다
- 휘발성

</details>

### 보조기억장치
<details>
<summary></summary>

- 비휘발성
- 하드 디스크, ssd, cd등등

</details>

### 입출력장치
<details>
<summary></summary>

컴퓨터 외부에 연결되어 내부와 정보를 교환하는 장치

</details>

### 메인보드
<details>
<summary></summary>

- 컴퓨터 부품을 부착
- 내부에 버스 존재

</details>

### 시스템버스
<details>
<summary></summary>

- 주소버스 : 주소 통로
- 데이터 버스 : 명령어, 데이터 통로
- 제어버스 : 제어신호 통로

</details>

### 비트
<details>
<summary></summary>

- 0과 1을 표현하는 가장 작은 정보단위
- n 비트로 2^n개 정보 표현 가능
  
</details>

### 워드
<details>
<summary></summary>

- CPU가 한 번에 처리할 수 있는 정보의 크기 단위
  
</details>

### 이진법
<details>
<summary></summary>

- 0, 1로 수를 표현하는 방법
- 음수 표현법 : 2의 보수
  
</details>

### 플래그
<details>
<summary></summary>

- cpu내부 특별한 레지스터
- 음수와 양수 구분에 사용
  
</details>

### 십육진법
<details>
<summary></summary>

- 0-9, A-F를 사용해 수를 표현하는 방법
- 이진수 4자리씩 변환 용이
  
</details>

### 문자집합
<details>
<summary></summary>

- 컴퓨터가 이해할 수 있는 문자의 모음
  
</details>

### 인코딩
<details>
<summary></summary>

- 문자를 코드화 하는 과정
  
</details>

### 디코딩
<details>
<summary></summary>

- 코드를 문자화 하는 과정
  
</details>

### 아스키
<details>
<summary></summary>

- 초창기 문자 집합
- 7비트 + 1비트(오류 검출 패리티 비트)
- 다양한 문자 표현 불가능
  
</details>

### 유니코드
<details>
<summary></summary>

- 통일된 문자 집합
  
</details>

### utf
<details>
<summary></summary>

- 유니코드를 인코딩하는 방식 8,16,32.. 등
  
</details>

### 고급언어
<details>
<summary></summary>

- 일반적인 프로그래밍언어
- 개발자가 이해가 편하다.
  
</details>

### 저급언어
<details>
<summary></summary>

- 컴퓨터가 이해하기 편하다.
- 기계어, 어셈블리어가 있다.
  
</details>

### 기계어
<details>
<summary></summary>

- 0,1로 이루어진 명령어 모음
  
</details>

### 어셈블리어
<details>
<summary></summary>

- 기계어를 읽기 편한 형태로 변환한 언어
  
</details>

### 컴파일
<details>
<summary></summary>

- 소스코드를 컴파일러가 컴파일 하면 목적코드가 나온다.
  
</details>

### 인터프리터
<details>
<summary></summary>

- 인터프리터에 의해 소스코드를 한 줄씩 실행한다.
- 소스코드 전체를 저급 언어로 변환하는 시간을 기다릴 필요없다.
  
</details>

### 명령어
<details>
<summary></summary>

- operation code 와 operand로 구성되어있다.
  
</details>

### 연산코드
<details>
<summary></summary>

- 명령어가 수행할 연산
  1) 데이터 전송 : MODE,STORE,LOAD(FETCH),PUSH,POP
  3) 산술/논리 연산 : 사칙연산, 증감, 논리, 참거짓
  4) 제어 흐름 변경 : JUMP, CONDITIONAL JUMP, HALT, CALL, RETURN
  5) 입출력 제어 : READ, WRITE, START IO, TEST IO
  
</details>

### 오퍼랜드
<details>
<summary></summary>

- 연산에 사용할 데이터 or 연산에 사용할 데이터가 저장된 위치
- 주소필드라고도 부른다.
  
</details>

### 주소지정방식
<details>
<summary></summary>

- 연상에 사용할 데이터가 지정된 위치(유효 주소)를 찾는법
    1) 즉지 주소 지정 방식 : 데이터를 오러랜드 필드에 직접명시
    2) 직접 주소 지정 방식 : 유효주소를 명시
    3) 간접 주소 지정 장식 : 유효주소의 주소를 명시
    4) 레지스터 주소 지정 방식 : 데이터가 저장된 레지스터 명시
    5) 레지스터 간접 주소 지정 방식 : 데이터가 저장된 메모리의 주소를 레지스터에 명시
  
</details>
