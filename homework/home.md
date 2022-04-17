보수 연산


존, 팩

보수연상 괴정

1의 보수 2의 보수 표현 범위

# 문자 자료표현

# 알고리즘 성능 분석 방법 2가지

시간 복잡도

    특정한 크기의 입력에 대하여 알고리즘이 소요하는 시간

공간 복잡도

    특정한 크기의 입력에 대하여 알고리즘이 사용하는 컴퓨터 자원(메모리)

# 알고리즘의 조건 5가지

유한성(Finiteness)

    알고리즘은 단계들을 반드시 유한한 횟수로 거친 후에 종료해야 함.

명확성(definiteness)

    알고리즘의 각 단계는 반드시 명확하게 정의되어야 함.

입력(input)

    알고리즘은 0 또는 그 이상의 입력들을 가짐.

출력(output)

    알고리즘은 하나나 그 이상의 출력들을 가짐.

효과점(effectiveness)

    효과적이라는 말은, 이론적으로 알고리즘의 모든 연산들이 사람이 종이와 연필을 이용해서 유한한 시간 안에 정확하게 수행할 수 있을 정도로 충분히 단순해야 한다는 의미임.

--------

# 알고리즘 분석 기준

----

# 빅오 빅미가 빅세타 표현법

빅오 (big-O) 표기법

    시간의 상한 (최악의 경우)
    해당 알고리즘은 big-O 보다 더 오래 걸릴 수 없다.

 

빅오메가 (big-Omega) 표기법

    시간의 하한 (최선의 경우)
    해당 알고리즘은 big-Omega 보다 더 빠를 수 없다.

 

빅세타 (big-theta) 표기법

    평균적인 경우, 딱 맞는 수행 시간
    big-O 와 big-Omega 를 하나로 합쳐 표현한것과 같다. 


------


f(n)

-----

--------------------------------
# 빅오 표기법

    O(1) : 입력값에 상관없이 일정한 실행시간을 최고!의 알고리즘이라 할 수 있다. 하지만 상수 시간에 실행된다 해도 상수값이 상상 이상으로 클 경우 사실상 일정한 시간의 의미가 없다. 최고의 알고리즘이 될 수 있지만 그만큼 신중해야 한다.

    O(log n) : 로그는 매우 큰 입력값에서도 크게 영향을 받지 않는 편이다. 매우 견고한 알고리즘으로 이진 탐색의 경우가 이에 해당한다.

    O(n) : 알고리즘을 수행하는데 걸리는 시간은 입력값에 비례한다. 이러한 알고리즘을 선형 시간 알고리즘이라 부른다. 정렬되지 않은리스트에서 최대 또는 최솟값을 찾는 경우가 해당되며 모든 입렵값을 적어도 한 번 이상은 살펴봐야 한다.

    O (n log n) : 병합 정렬등의 대부분 효율이 좋은 알고리즘이 이에 해당 한다. 아무리 좋은 알고리즘이라 할지라도 n log n 보다 빠를 수 없다. 입력값이 최선일 경우, 비교를 건너 뛰어 O(n)이 될 수 있다.

    O(n^2)  : 버블 정렬 같은 비효율저긴 정렬 알고리즘이 이에 해당 한다.

    O(2^n) : 피보나치의 수를 재귀로 계산하는 알고리즘이 이에 해당 한다. n^2와 혼동되는 경우가 있는데 2^n이 훨씬 더 크다.

    O(n!) : 가장 느린 알고리즘으로 입력값이 조금만 커져도 계산이 어렵다.

----

# 빅오 자료구조 적용

-------

# 배열의 정의

    배열은 같은 타입의 변수들로 이루어진 유한한 집합

    배열을 구성하는 각각의 값을 배열의 요소(element)라 하고, 배열에서 위치를 가리키는 숫자는 인덱스(index)라 한다.

----

---

알고리즘 문제



---

# 배열과 구조체 차이

    배열은 동일한 타입의 데이터를 묶는 구조

    구조체는 하나 이상의 자료형을 기반으로 "사용자 정의 자료형"을 만들 수 있는 문법 요소

---

------

# 재귀 호출이란 

    함수란 하나의 작업을 수행하기 위해 독립적으로 설계된 프로그램 코드의 집합입니다

    재귀 호출(recursive call)이란 함수 내부에서 함수가 자기 자신을 또다시 호출하는 행위를 의미합니다.

    이러한 재귀 호출은 자기가 자신을 계속해서 호출하므로, 끝없이 반복되게 됩니다.

    따라서 함수 내에 재귀 호출을 중단하도록 조건이 변경될 명령문을 반드시 포함해야 합니다.

    만약 빠져나오지 못한다면은 스택오버플로우가 발생한다. 

    재귀호출은 반드시 메서드의 복사본 메모리가 만들어진다.
    
    메서드가 종료되면 메서드 복사본이 삭제된다.

------

재귀구조 문제 해결 방법

    재귀구조는 비 재귀보다 느리고, 메모리 사용량도 상대적으로 많고, 코드분석,
    시 공간 복잡도 면에서 좋지 않다.

    해결방법
    간단한 문제는 재귀구조로 프로그래밍 시간을 줄이는 대신에
    복잡하거나 시공간 복잡도가 중요한 문제에선 다른 루프를 이용한 알고리즘을 사용한다.

----

---

# 순차와 연결 자료구조의 개념

    선형 리스트: 배열과 같이 연속되는 기억 장소에 저장되는 리스트

    연결 리스트: 자료들이 반드시 연속적으로 배열되어있지 않아도 노드 포인터 부분을 이용하여 서로 연결된 구조

# 선형리스트 연결리스트 장단점



|구분|순차(선형) 자료구조|연결 자료구조|
| --- | --- | --- |
|메모리 저장 방식|모든 데이터가 메모리에 연속적으로 저장|데이터는 노드에 저장되고, 노드는 메모리 곳곳에 흩어짐|
|연산 특징|임의의 데이터에 즉각 접근 가능|임의 데이터에 접근하는 것은 O(n) 복잡도를 가짐|
|프로그램 기법|배열을 이용하여 구현|포인터를 이용하여 구현|

---


스텍구조

큐 구조

스텍의 삽입 삭제 알고리즘

전위 중위 후위법

# 자료구조 표현

![img](./img/자료의표현.png)

# 자료구조의 표현단위

![img](./img/자료의단위.png)


부호