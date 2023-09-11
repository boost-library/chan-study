[필요성](#필요성)

[커널](#커널)

[이중모드](#이중모드)

[시스템호출](#시스템호출)

[핵심서비스](#핵심서비스)

[pcb](#pcb)

[문맥교환](#문맥교환)

[메모리영역](#메모리영역)

[프로세스 상태](#프로세스상태)

[프로세스 생성](#프로세스생성)

[스레드](#스레드)

[스케줄링](#스케줄링)





### 필요성
<details>
<summary></summary>

- 자원관리를 신경쓸 필요가 없다.
- 하드웨어를 조작하는 코드를 직접 작성할 필요가 없다.
- 문제해결의 실마리

</details>

### 커널
<details>
<summary></summary>

- 운영체제 핵심 서비스를 담당하는 부분
- UI는 커널에 속하지 않지만 운영체제에는 속한다.

</details>

### 이중모드
<details>
<summary></summary>

- CPU가 명령어를 실행하는 모드
- 사용자 모드 : 커널 영역 코드 실행 불가
- 커널 모드 : 운영체제의 서비스 제공

</details>

### 시스템호출
<details>
<summary></summary>

- 소프트웨어 인터럽트
- 커널 모드로 전환하여 실행하기 위해 호출

</details>

### 핵심서비스
<details>
<summary></summary>

- 프로세스 관리
- 자원 접근 및 할당
- 파일 시스템 관리

</details>

### pcb
<details>
<summary></summary>

- 프로세스를 관리하기 위한 자료구조
- 프로세스 생성 시 커널영역에 생성

</details>


### 문맥교환
<details>
<summary></summary>

- 다른 프로세스로 실행 순서 넘어갈때 정보 백업, 복구

</details>


### 메모리영역
<details>
<summary></summary>

- 코드
  - 실행할 수 있는 코드, 기게어
  - cpu가 실행할 명령어가 담김
  - read only
- 데이터
  - 프로그램이 실행되는 동안 유지할 데이터 저장
  - ex 전역 변수
- 힙
  - 사용자가 할당할 수 있는 공간
- 스택
  - 데이터가 일시적으로 저장되는 공간
  - 매개 변수, 지역변수 

</details>

### 프로세스상태
<details>
<summary></summary>

- 생성
- 준비 : CPU 할당 X
- 실행 : CPU 할당 O
- 대기 : 요청 사건 대기
- 종료 
  

</details>

### 프로세스생성
<details>
<summary></summary>

- fork
- 생성한 쪽 부모
- 만들어진 쪽 자식
- 계층구조

</details>


### 스레드
<details>
<summary></summary>

- CPU 제어의 흐름
- 실행 단위
- 프로세스 자원 공유

</details>

### 스케줄링
<details>
<summary></summary>

- 우선순위
- 스케줄링 큐
- 준비 큐 : CPU 사용
- 대기 큐 : 입출력 장치 사용

</details>
