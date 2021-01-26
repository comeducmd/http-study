# 7. 캐시

### 7.1 불필요한 데이터 전송

1. 캐시를 사용하면 불필요한 데이터 전송량을 늘릴 수 있다. (O/X)
<details><summary>정답</summary>


    X
</details>
### 7.2 대역폭 병목

1. 병목 현상에 대해 서술하시오.
2. 캐시는 병목 현상을 어떻게 해결하는지 서술하시오.
<details><summary>정답</summary>
    1. 네트워크에서 속도는 경로에 존재하는 네트워크의 속도 중 가장 느린 네트워크의 속도와 같은것
    2. 캐시되어있는 파일을 가져와서 해결
</details>
### 7.3 갑작스런 요청 쇄도

1. 트래픽 급증은 서버에 큰 부하를 준다.  (O/X)
<details><summary>정답</summary>

    O
</details>
### 7.4 거리로 인한 지연

1. ~~보스턴과 샌프란시스코 사이의 거리는?~~
<details><summary>정답</summary>

    약 4400킬로미터
</details>
### 7.5 재검사

1. HTTP 재검사에 대해 서술하시오.
2. 콘텐츠가 변경되지 않다면 서버는 (OOO) Not Modified의 응답을 보낸다. OOO은?
3. 콘텐츠가 변경되었다면 서버는 (OOO) 응답을 보낸다. OOO은?
4. 문서 적중률과 바이트 적중률이 달라지는 요인은 무엇인가?
<details><summary>정답</summary>
    1. 캐시 파일이 최신인지 검사하는 것
    2. 304
    3. 200
    4. 문서의 크기가 일정하지 않기 때문에
</details>
### 7.6 캐시 토폴로지

1. 한 명에게만 할당된 캐시를 (        )라 한다. 
<details><summary>정답</summary>

    개인 캐시
</details>
### 7.7 캐시 처리 단계

1. 다음 캐시 처리 단계를 순서 대로 나열하시오. (단, 이 처리 단계에서 아래의 모든 단계를 거쳤다고 가정한다.)
    1. 응답 생성
    2. 검색
    3. 요청 받기
    4. 로깅
    5. 파싱
    6. 신선도 검사
    7. 발송
2. 요청이 프락시 캐시를 거쳐갔음을 알려주기 위해 종종 Via 헤더를 포함하게 하는 단계는 (      ) 단계이다. 
<details><summary>정답</summary>
    1. 3526174
    2. 응답 생성
</details>
### 7.8 사본을 신선하게 유지하기

1. HTTP는 원 서버가 각 문서에 유효기간을 붙일 수 있게 해준다. 이때 사용되는 헤더 두개는?
2. IMS요청은 캐시된 태그가 서버에 있는 문서의 태그와 다를 때만 요청을 처리한다.  (O/X)
3. If-Modified-Since 헤더는 (          )헤더와 함께 동작한다. 
<details><summary>정답</summary>
    1. Cache-Control, Expires
    2. X
    3. Last-Modified
</details>
### 7.9 캐시 제어

1. no-cache로 표시된 응답은 캐시가 그 응답의 사본을 만드는 것을 금지한다. (O/X)
2. Expires 헤더에는 시간이 정수로 명시된다. (O/X)
3. Cache-Control : must-revalidate 헤더가 붙은 객체는 신선하지 않은 상태로 전달될 수 있다. (O/X)
<details><summary>정답</summary>

    XXX
</details>
### 7.10 캐시 제어 설정

1. HTML 콘텐츠 네에 삽입되어 캐시의 동작을 제어하는 태그는?
<details><summary>정답</summary>

    <META HTTP-EQUIV>
</details>
### 7.12 캐시와 광고

1. 광고 회사들이 캐시를 차단하는 이유를 서술하시오.
<details><summary>정답</summary>

    캐시가 적중되는 것이 서버에 전달되지 않기 때문에
</details>