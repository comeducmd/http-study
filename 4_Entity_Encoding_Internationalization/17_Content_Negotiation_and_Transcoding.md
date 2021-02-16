# 17. 내용 협상과 트랜스코딩

### 17.1 내용 협상 기법

1. 웹 콘텐츠의 서로 다른 버전을 ________라 한다. 
<details><summary>정답</summary>


1. 배리언트
</details>

### 17.2 클라이언트 주도 협상

1. 클라이언트 주도 협상의 단점과 단점이 발생하는 이유를 서술하시오. 
2. 클라이언트 주도 협상을 위해 서버가 클라이언트에 돌려주는 응답 코드는 300__________ 이다. 

<details><summary>정답</summary>
1. 두번의 요청을 해야하기 때문에 요청 시간이 증가하고, 여러개의 URL을 요구한다.  
2. Multiple Choices


</details>

### 17.3 서버 주도협상

1. 클라이언트가 자신의 선호 정보를 전달하는 HTTP 헤더가 아닌 것은?
    1. Accept
    2. Accept-Language
    3. Accept-Entity
    4. Accept-Charset
    5. Accept-Encoding
2. HTTP가 클라이언트의 선호를 표기하기 위해 제공하는 값은?
3. Apache 웹 서버가 서버 주도 협상을 위해 생성하는 파일은?
<details><summary>정답</summary>

1. 3
2. 품질값 또는 Qualirt Value 또는 Q값
3. type-map 파일
</details>

### 17.4 투명 협상

1. 투명 협상의 장점을 서술하시오.
2. 제공된 문서가 User-Agent 헤더에 의존한다면, Vary 헤더는 반드시 "User-Agent" 를 포함해야 한다. (O/X)
<details><summary>정답</summary>

1. 클라이언트와 메세지 교환을 최소화 하고, 서버 주도 협상으로 인한 부하를 서버에서 제가한다.
2. O / 그것이 Vary 헤더의 이유
</details>

### 17.5 트랜스코딩

1. 데이터를 클라이언트가 볼 수 있도록 변환하는 것을 정보 합성이라 한다. (O/X)
2. 콘텐츠 주입 트랜스코딩은 광고를 삽입하는 데 사용될 수 있다. (O/X)
3. 트랜스 코딩을 사용하지 않고 여러 가지 사본을 만드는 것의 단점을 서술하시오.
<details><summary>정답</summary>
    1. O
    2. O
    3. 대기 시간 증가로 인한 비용을 초래할 수 있다. 
</details>