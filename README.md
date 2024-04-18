
# Ch 1 컴퓨터 구조 시작하기


### 1.1  컴퓨터 구조를 알아야하는 이유

컴퓨터 구조를 이해하고 있다면, 코드 및 언어의 문법만으로 알기 어려운 성능, 비용, 용량을 고려하며 개발할 수 있다.

### 1.2  컴퓨터 구조의 큰 그림

컴퓨터 구조는 크게 두가지로 아래 두 가지로 나뉜다. 

- 컴퓨터가 이해하는 정보

컴퓨터가 이해하는 정보는 **Data, 명령어** 두가지로 나뉨

컴퓨터가 이해하는 숫자, 문자, 이미지 동영상과 같은 정적인 정보를 가리켜 **Data**라고 한다. 

**Data**를 바탕으로 컴퓨터를 작동시키는 것을 **명령어**라고 한다. 

- 컴퓨터의 네 가지 핵심 부품
1. 중앙처리장치(CPU)
2. 주 기억장치(Main Memory)
3. 보조 기억장치(Secondary Storage)
4. 입출력장치(I/O Device)

<br>

# Ch 2 데이터

### 2.1 0과 1로 숫자를 표현하는 방법

**정보 단위**

- 비트(bit): 1 bit
- 바이트(byte): 8 bit
- 킬로바이트(kB): 1000 byte
- 메가바이트(MB): 1000kB
- 기가바이트(GB): 1000MB
- 테라바이트(TB): 1000GB

**워드:** CPU가 한번에 처리할 수 있는 데이터의 크기

Ex x86은 32비트 x64는 64비트

**이진법**

0과 1만으로 숫자를 표현하는 방법

**십진법**

0부터 9 까지의 숫자만으로 숫자를 표현하는 방법

**십육진법**

0부터 9 , A B C D E F 16가지의 글자로 숫자를 표현하는 방법

**이진수의 음수 표현**

0과 1만으로 음수를 표현하는 방법은 **2의 보수**

0과 1을 모두 반전시키고 1을 더해준다!

**2의 보수 표현방법의 한계**

 2^n 형태의 이진수를 2의 보수로 표현한다면 원하는 음수값을 찾아내기 힘들다.

### 2.2 0과 1로 문자를 표현하는 방법

컴퓨터가 인식하고 표현할 수 있는 문자의 모음을 **문자 집합(Character Set)**이라고 한다. 

문자를 0과 1로 변환해서 컴퓨터가 읽을 수 있게하는 것을 **문자 인코딩(Character Encoding)**

0과 1을 사람이 이해할 수 있게 만드는 과정을 **문자 디코딩(Character Decoding)**이라고 한다.

**아스키 코드**

2^7 의 문자를 표현할 수 있다.

**EUC-KR**

KS X 1001 KS X 1003이라는 문자 집합을 기반으로 하는 대표적인 완성형 인코딩

**유니코드**

모든 언어를 아우르는 문자 집합과 통일된 표준 인코딩 방식을 위해 만들어진 문자 집합

현대 문자를 표현할 때 가장 많이 사용되는 표준 문자 집합.

**UTF-8**

가장 대중적인 유니코드를 사용한 인코딩 방식

<br>

# Ch 3 명령어

### 3.1 소스 코드와 명령어

- 고급언어(High Level Programming Language)

컴퓨터가 이해하는 언어가 아닌 사람이 이해하고 작성하기 쉽게 만들어진 언어. 

Ex) Java, Python, C, C++

- 저급언어(Low Level Programming Language)

컴퓨터가 이해하고 실행할 수 있는 언어. **고급 언어로 작성된 소스 코드가 실행되려면 반드시 저급언어, 즉 명령어로 변환되어야 한다.**

Ex) 어셈블리어

**컴파일 언어와 인터프리터 언어**

- 컴파일 언어

컴파일러에 의해 소스 코드 전체가 저급 언어로 변환되어  실행되는 고급 언어.

소스 코드 전체가 저급언어로 변환 되는 과정을 **컴파일**이라고 하고 컴파일을 수행해 주는 도구를 **컴파일러**라고 한다.

Ex) C

- 인터프리터 언어

인터프리터에 의해 소스 코드가 한 줄씩 실행되는 고급 언어. 

실행해 주는  도구는 **인터프리터**라고 한다. 

Ex) Python

**고급 언어가 저급 언어로 변환되는 대표적인 방법에는 인터프리트 방식과 컴파일 방식이 있다!!**

### 3.2 명령어의 구조

명령어는 연산 코드와 오퍼랜드로 구성되어 있다.

- 연산 코드(Operation Code)

<aside>
💡 가장 기본적인 연산코드 유형
1. 데이터 전송
2. 산술/ 논리 연산
3. 제어 흐름 변경
4. 입출력 제어

</aside>

- 오퍼랜드(Operand)

연산에 사용할 데이터 또는 연산에 사용할 데이터가 저장된 위치를 의미한다.

연산에 사용할 데이터를 직접 명시하기 보다는 메모리 주소나 레지스터 이름이 담긴다.

오퍼랜드 필드를 주소필드라고 부르기도 함.

<aside>
💡 오퍼랜드가 
하나도 없는 명령어를 0 - 주소 명령어, 
하나인 명령어를 1 - 주소 명령어
두 개인 명령어를 2 - 주소 명령어
세 개인 명령어를 3 - 주소 명령어

</aside>

**주소 지정 방식:** 오퍼랜드 필드에 데이터가 저장된 위치를 명시할 때  연산에 사용할 데이터의 위치를 찾는 방법**.**

1. **즉시 주소 지정 방식**
데이터를 직접 명시하는 방법 다른 주소 지정 방식들보다 빠름
2. **직접 주소 지정 방식**
유효 주소에 제한이 생길 수가 있음.
3. **간접 주소 지정 방식**
일반적으로 느린 방식
4. **레지스터 주소 지정 방식**
    
    직접 주소 지정 방식보다 빠르게 데이터에 접근할 수 있다. 다만, 레지스터 크기에 제한이 생길 수 있다.
    
5. **레지스터 간접 주소 지정 방식**
    
    연산에 사용할 데이터를 메모리에 저장하고, 그 주소를 저장한레지스터를 오퍼랜드 필드에 명시하는 방법
    
    간접 주소 지정 방식보다 빠르다.

<br>

# Ch 4. CPU의 작동 원리

### 4.1 ALU와 제어장치

- ALU
    
    레지스터를 통해 피연산자를 받아들이고 제어장치로부터 수행할 연산을 알려주는 제어신호를 받아들인다.
    
- 제어장치
    
    제어 신호를 내보내고 명령어를 해석하는 부품. 
    
    1. 제어장치는 클럭 신호를 받아들인다.
    2. 제어장치는 해석해야 할 명령어를 받아들인다.
    3. 제어장치는 플래그 값을 받아들인다
    4. 제어장치는 시스템 버스, 제어버스로 전달된 제어 신호를 받아들인다.

### 4.2 레지스터

레지스터의 종류

1. 프로그램 카운터(PC)
    
    메모리에서 가져올 명령어의 주소 즉 메모리에서 읽어 들일 명령어의 주소를 저장한다.
    
2. 명령어 레지스터(IR)
    
    해석할 명령어 즉 방금 메모리에서 읽어 들인 명령어를 저장하는 레지스터. 제어장치는 명령어 레지스터 속 명령어를 받아들이고 이를 해석한 뒤 제어 신호를 내보낸다.
    
3. 메모리 주소 레지스터(MAR) 
    
    메모리의 주소를 저장하는 레지스터.
    
4. 메모리 버퍼 레지스터(MBR)
    
    메모리와 주고받을 값을 저장하는 레지스터
    
5. 범용 레지스터
    
    일반적인 상황에서 자유롭게 사용할 수 있는 레지스터
    
6. 플래그 레지스터
    
    ALU 연산 결과에 따른 플래그를 플래그 레지스터에 저장한다.
    
- 특정 레지스터를 이용한 주소 지정 방식
    1. 스택 주소 지정 방식
        
        스택 포인터는 스택 주소 지정 방식이라는 주소 지정 방식에 사용되고 프로그램 카운터와 베이스 레지스터는 변위 주소 지정 방식이라는 주소 지정 방식에 사용된다.
        
    2. 변위 주소 지정 방식
        
        오퍼랜드 필드 값과 특정 레지스터의 값을 더하여 유효 주소를 얻어내는 주소 지정 방식
        
    3. 상대 주소 지정 방식
        
        프로그래밍 언어의 IF문과 유사하게 모든 코드를 실행하는 것이 아닌 분기하여 특정 주소의 코드를 실행할 때 사용된다.
        
    4. 베이스 레지스터 주소 지정 방식
        
        베이스 레지스터 속 기준 주소로부터 얼마나 떨어져있는 주소에 접근할 것인지를 연산하여 유효 주소를 얻어내는 방식.
        

### 4.3 명령어 사이클과 인터럽트

- 명령어 사이클: 하나의 명령어를 처리하는 정형화된 흐름.
    - 인출 사이클: 명령어를 메모리에서 CPU로 가지고 오는 단계.
    - 실행 사이클: 제어장치가 명령어 레지스터에 담긴 값을 해석하고 제어 신호를 발생시키는 단계.
    - 간접 사이클: 명령어를 실행하기 위해서 메모리 접근을 한번 더 해야하는 단계.
- 인터럽트: CPU의 정상적인 작업을 방해하는 신호
    - 동기 인터럽트(예외): CPU에 의해 발생하는 인터럽트.
    - 비동기 인터럽트(하드웨어 인터럽트): 입출력장치에 의해 발생하는 인터럽트
- 하드웨어 인터럽트 처리 순서
    1. CPU에 인터럽트 요청 신호
    2. CPU는 명령어를 인출하기 전 인터럽트 여부 확인
    3. 인터럽트 플래그를 통해 현재 인터럽트를 받아들일 수 있는 지 확인
    4. 인터럽트를 받아들일 수 있다면 CPU는 작업 백업
    5. 인터럽트 벡터를 참조하여 서비스 루틴 실행
    6. 실행 재개
    

<br>

# Ch 5. CPU 성능 향상 기법

### 5.1 빠른 CPU를 위한 설계 기법

- **클럭**
    
    클럭 신호가 빠르게 반복되면 CPU를 비롯한 컴퓨터 부품들은 그만큼 빠른 박자에 맞춰 움직인다. 클럭 속도가 높아지면 CPU는 명령어 사이클을 더 빠르게 반복할 것이고, 다른 부품들도 그에 발맞춰 더 빠르게 작동할 것이다.
    
    **클럭** 속도가 높은 CPU는 일반적으로 성능이 좋다. 클럭 속도는 CPU 속도 단위로 간주되기도 한다.
    
    **클럭 속도**는 헤르츠(Hz) 단위로 측정한다. 이는 1초에 클럭이 몇 번 반복되는지를 나타낸다. Ex) 클럭이 1초에 100번 반복되면 CPU 클럭 속도는 100Hz인 셈.
    
    <aside>
    💡 클럭 속도는 일정하지 않다.
    
    CPU는 계속 일정한 클럭 속도를 유지하기 보다는 고성능을 요할 때 클럭 속도를 높이고 그렇지 않을 때는 유연하게 클럭 속도를 낮춘다.
    최대 클럭 속도를 강제로 더 끌어올릴 수도 있는데, 이런 기법을 
    **오버 클러킹**이라고 한다.
    
    </aside>
    
    클럭 속도를 높이는 것은 CPU를 빠르게 만들지만 발열의 이유로 클럭 속도로 빠르게 한다는 것은 무리가 있다.
    
- **코어와 멀티 코어**
**코어**라는 용어는 명령어를 실행하는 부품. **멀티 코어**는 명령어를 실행하는 부품을 여러개 둔다는 뜻으로 CPU를 빠르게 만드는 것이다. 8코어는 명령어를 실행하는 부품이다. 
코어를 여러 개 포함하고 있는 CPU를 멀티코어CPU, 멀티코어 프로세서라고 부른다.
싱글, 듀얼, 트리플, 쿼드 ++
코어를 늘린다고만해서 CPU의 성능이 비례해서 좋아지는 것이 아니다. 처리할 연산이 적절히 분배되지 않는다면 코어 수에 비례하여 연산 속도가 증가하지 않는다.
- **스레드와 멀티 스레드**
**스레드(thread)**의 사전적 의미는 ‘실행 흐름의 단위’ 스레드는 하드웨어적 스레드와 소프트웨어적 스레드로 나뉜다.
    
    
    하나의 코어로 여러 명령어를 동시에 처리하는 CPU를 **멀티스레드(Multithread)프로세서** 또는 **멀티 스레드 CPU** 라고 한다. 
    
    1. 하드웨어적 스레드
        1. 하나의 코어로 여러 명령어를 동시에 처리하는 CPU를 **멀티스레드(Multithread)프로세서** 또는 **멀티 스레드 CPU** 라고 한다. 
        2. **하이퍼 스레딩**: 인텔의 멀티스레드 기술을 의미한다.
    2. 소프트웨어적 스레드
        1. 하나의 프로그램에서 독립적으로 실행되는 단위
    
    <aside>
    💡 논리 프로세서(logical processor) 
    2코어 4스레드 CPU는 한번에 네 개의 명령어를 처리할 수 있는데 프로그램 입장에서 봤을 때 한번에 하나의 명령어를 처리하는 CPU가 네 개 있는 것 처럼 보인다. 이러한 하드웨어 스레드를 논리 프로세서라고 부른다.
    
    </aside>
    

### 5.2 명령어 병렬 처리 기법

CPU의 여유시간 없이 작동하게 만드는 방법.

- 명령어 파이프라인: 명령어들을 명령어 파이프라인에 넣고 동시에 처리하는 기법
    1. 명령어 인출
    2. 명령어 해석
    3. 명령어 실행
    4. 결과 저장
    
    파이프 라이닝이 높은 성능을 가져오지만 특정 상황에서는 성능 향상에 실패하는 경우도 있다. 이러한 상황을 **파이프라인 위험 이라고 한다.**
    

- **파이프라인 위험**
    - **데이터 위험**
        
        명령어 간 데이터 의존성에 의해 발생된다.
        
        ![Untitled](https://github.com/choijw1004/Computer-Architecture/assets/117329752/7cdb587e-24b0-4b60-ac01-b4bf8b5b8c7d)
        
    - **제어 위험**
        
        분기 등으로 인한 프로그램 카운터의 갑작스러운 변화에 의해 발생한다.
        
        ![Untitled 1](https://github.com/choijw1004/Computer-Architecture/assets/117329752/75b8686e-e904-4d68-9b76-a8bfb34f19b9)
        
        이러한 분기에 의한 갑작스러운 변화를 방지하기 위해 **분기 예측**을 사용한다.
        
    - **구조적 위험**
        
        구조적 위험은 명령어들을 겹쳐 실행하는 과정에서 서로 다른 명령어가 동시에 CPU 부품을 사용할 때 발생한다. = **자원 위험**
        
    - **슈퍼 스칼라**
        
        여러개의 명령어 파이프라인을 두는 기법. 매 클럭 주기마다 동시에 여러 명령어를 인출할 수도, 실행할 수도 있어야 한다.
        
    - 비순차적 명령어 처리(Out - of - erder execution)
        
        명령어들을 순차적으로 실행하지 않는 기법.
        
        파이프라인의 중단을 방지하기 위해 명령어들을 순차적으로 처리하지 않는 명령어 병렬 처리 기법.
        

### 5.3 CISC와 RISC

- 명령어 집합 = ISA(Instruction Set Architecture)
    
    명령어의 기본적인 구조와 작동원리는 명령어의 세세한 생김세, 명령어로 할 수 있는 연산, 주소 지정 방식 등은 CPU마다 조금씩 차이가 있다. CPU가 이해할 수 있는 명령어들의 모음.
    
- CISC(Complex Instruction Set Computer)
    
    복잡하고 다양한 명령어들을 활용하는 CPU 설계 방식.
    
    가변 길이 명령어를 활용한다
    
    - 장점: 적은 수의 명령어만으로도 프로그램을 동작시킬 수 있어 메모리 공간을 절약할 수 있다는 장점이 있다.
    - 단점: 명령어가 복잡하고 다양한 기능을 제공하는 탓에 크기와 실행되기 까지의  시간이 일정하지 않다. 규걱화 되지 않는 명령어가 파이프라이닝을 어렵게 만든다. 복잡한 명령어는 실제로 20프로의 명령어만 사용되고 80프로는 간단한 명령어를 차지함. 사용 빈도가 낮다.
- RISC(Reduced Instruction Set Computer)
    
    RISC는 CISC에 비해 명령어의 종류가 적다. CISC보다 길이가 짧고 규격화된 명령어, 되도록 1클럭 내외로 실행되는 명령어를 지향한다.
    
    고정 길이 명령어를 활용한다. LOAD - STORE 구조
    
   ![Untitled 2](https://github.com/choijw1004/Computer-Architecture/assets/117329752/f641c3be-5a06-4c31-8155-09c57f2c95c0)
    

<br>

# Ch 6. 메모리와 캐시 메모리

### 6.1 RAM의 특징과 종류

- RAM의 특징
    - 실행할 프로그램의 명령어와 데이터가 저장된다. but 휘발성 저장 장치
    - HDD, SSD, CD-ROM ,USB와 같은 보조기억장치가 대표적인 비휘발성 저장 장치
- RAM의 용량과 성능
    
    RAM의 용량이 작다면 CPU가 적재적소에 저장하고 싶은 프로그램을 갖고오는 시간이 오래 걸린다.
    
- RAM의 종류
    - DRAM(Dynamic RAM): 데이터가 동적으로 변하는 RAM을 의미한다.
        
        시간이 지나면 저장된 데이터가 점차 사라지는 RAM 데이터의 소멸을 막기 위해 일정 주기로 데이터를 재활성화해야 한다. 일반적으로 메모리로 사용하는 RAM. 전력 소비가 낮고, 저렴, 집적도가 높다.
        
    - SRAM(Static RAM): 시간이 지나도 저장된 데이터가 사라지지 않는다. 주기적으로 데이터를 재활성할 필요가 없어서 일반적으로 속도가 빠름.
        
        but 집적도가 낮고, 소비 전력이 크며, 가격도 비싸다 → 캐시 메모리에서 사용
        
    - SDRAM(Synchronous Dynamic RAM): 클럭 타이밍에 맞춰 CPU와 정보를 주고받을 수 있음을 의미한다. DRAM
    - DDR SDRAM(Double Data Rate SDRAM)은 가장 흔히 사용되는 RAM. 대역폭을 넓혀 속도를 빠르게 만든 SDRAM **대역폭**이란 데이터를 주고받는 길의 너비를 의미한다. <> SDR SDRAM
    - SDR SDRAM*4 → DDR2*4 → DDR4

### 6.2 메모리의 주소 공간

- 물리주소: 메모리 하드웨어 상의 주소
- 논리주소: CPU와 실행 중인 프로그램이 사용하는 주소
- 메모리 관리 장치(Memory Management Unit) 논리 주소와 물리 주소 간의 변환을 하게 해주는 하드웨어
- 논리 주소: 프로그램의 시작점으로부터 떨어진 거리
- 메모리 보호 기법
- 한계 레지스터: 다른 프로그램을 침범할 수 있는(논리 주소 범위를 벗어나는) 명령어 실행을 방지하고 실행 중인 다른 프로그램에 영향을 받지 않도록 보호할 방법이 필요하다. 이를 위한 레지스터 논리주소의 최대 크기를 저장한다.

### 6.3 캐시 메모리

CPU의 연산속도보다 메모리에 접근하는 속도가 느리기때문에 이를 극복하기 위한 저장 장치.

- 저장 장치 계층 구조의 명제
    - CPU와 가까운 저장 장치는 빠르고, 멀리 있는 저장 장치는 느리다.
    - 속도가 빠른 저장 장치는 저장 용량이 작고 가격이 비싸다.
    
    ![Untitled 3](https://github.com/choijw1004/Computer-Architecture/assets/117329752/dab425be-6d19-4716-9680-e597f0408ed5)
    
- 캐시 메모리: CPU와 메모리 사이에 위치하고, 레지스터보다 용량이 크고 메모리보다 빠른 SRAM 기반의 저장 장치.
    - Level1 캐시 메모리: CPU와 가장 가까운 캐시메모리
    - Level2 캐시 메모리: 그 다음
    - Level3 캐시 메모리: 그 다음
- 참조 지역성 원리
    1. CPU는 최근에 접근했던 메모리 공간에 다시 접근하려는 경향이 있다.
    2. CPU는 접근한 메모리 공간 근처를 접근하려는 경향이 있다. 
    - 캐시 히트: 자주 사용될 것으로 예측한 데이터가 실제로 들이맞아 캐시 메모리 내 데이터가 CPU에서 활용될 경우.
    - 캐시 미스: 자주 사용될 것으로 예측하여 캐시 메모리에 저장했지만, 예측이 틀려 메모리에서 필요한 데이터를 직접 가져와야 하는 경우.
    - 캐시 적중률: 캐시 히트 횟수 / 캐시 히트 + 캐시 미스 횟수
    
    <br>

# Ch 7. 보조 기억장치

### 7.1 다양한 보조 기억장치

- 하드 디스크(HDD): 자기적인 방식의 데이터를 저장하는 보조기억장치.
    - 플래터: 실질적으로 데이터가 저장되는 곳
    - 스핀들: 플래터를 회전시키는 구성 요소
    - RPM: 스핀들이 플래터를 돌리는 분당 회전수
    - 헤드: 플래터를 대상으로 데이터를 읽고 쓰는 구성 요소
    - 디스크 암: 헤드가 원하는 위치로 헤드를 이동시키는 디스크 암
    - 트랙: 플래터를 동심원으로 나누었을 때 그중 하나의 원
    - 섹터: 트랙 중 한 조각
    - 실린더: 플래터 상에서 같은 트랙이 위치한 곳을 모아 연결한 논리적 단위.
- 하드 디스크가 저장된 데이터에 접근하는 시간
    - 탐색 시간: 접근하려는 데이터가 저장된 트랙까지 헤드를 이동시키는 시간
    - 회전 지연: 헤드가 있는 곳으로 플래터를 회전시키는 시간.
    - 전송 시간: 하드 디스크와 컴퓨터 간에 데이터를 전송하는 시간
- 플래시 메모리: 전기적으로 데이터를 읽고 쓸 수 있는 반도체 기반의 저장 장치.
    - NAND 플래시 메모리
    - NOR 플래시 메모리
    - 셀; 플래시 메모리에서 데이터를 저장하는 가장 작은 단위.
        - SLC: 한 셀에 1비트를 저장할 수 있는 플래시 메모리
            - 다른 타입에 비해 비트의 빠른 입출력이 가능하다.
            - 용량 대비 가격이 높다. 고성능 장치가 필요한 경우에 SLC타입을 사용한다.
        - MLC: 한 셀에 2비트를 저장할 수 있는 플래시 메모리
        - TLC: 한 셀에 3비트를 저장할 수 있는 플래시 메모리
            - SLC의 반대.

- 페이지: 셀들이 모여 만들어진 단위
    - Free 상태: 어떠한 데이터도 저장하고 있지 않아 새로운 데이터를 저장할 수 있는 상태를 의미한다.
    - Valid 상태: 유효한 데이터를 저장하고 있는 상태를 의미한다.
    - InValid 상태: 쓰레기값이라 불리는 유효하지 않은 데이터를 저장하고 있는 상태.
    - 가비지 컬렉션: 사용되지 않은 메모리를 정리하기 위해 SSD를 비롯한 플래시 메모리에서 제공하는 기능
- 블록: 페이지가 모여 만들어진 단위
- 플레인: 블록이 모여 만들어진 단위
- 다이: 플레인이 모여 만들어진 단위

### 7.2  RAID의 정의와 종류

- RAID의 정의
    - 하드디스크와  SSD를 사용하는 기술로 데이터의 안전성 혹은 높은 성능을 위해 여러 개의 물리적 보조 기억장치를 마치 하나의 논리적 보조 기억장치처럼 사용하는 기술.
- RAID의 종류
    - RAID 0
        - 4TB 저장장치라고 가정했을 때 저장장치 한 개를 사용하는 것보다 네 개를 이용하는 것이 이론상 4배 빠르다. BUT 저장된 정보가 안전하지 않고, 하나에 문제가 생긴다면 모든 하드 디스크의 정보를 읽는 데 문제가 생길 수 있다.
    - RAID 1
        - 복사본을 만드는 방식 RAID 0 보다 느리다.
        - 복구가 매우 간단하다는 장점이 있다. 사용 가능한 용량이 적어지는 단점이 있다.
    - RAID 2
    - RAID 3
    - RAID 4
        - RAID 1처럼 복사본을 만드는 대신 오류를 검출하고 복구하기 위한 정보를 저장한 장치를 두는 구성 방식. 이때 오류를 검출하고 복구하기 위한 정보를 패리티 비트라고 한다.
    - RAID 5
        - RAID 4의 병목현상을 방지하기 위해서 패리티 비트를 분산하여 저장하는 방식
    - RAID 6
        - RAID 5보다 속도는 느리지만 데이터를 안전하게 보관하고 싶을 때 사용하는 방식

---