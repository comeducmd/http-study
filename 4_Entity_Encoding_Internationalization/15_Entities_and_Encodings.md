# 15. 엔터티와 인코딩

### 15.1 메세지는 컨테이너, 엔터티는 화물 

1. 엔터티 헤더로 정의되어 있지는 않지만 엔터티와 관련된 많은 동작을 위해 중요한 헤더는?
2. 데이터가 압축되었거나 혹은 추가적인 인코딩이 되었는지 말해주는 헤더는?
<details><summary>정답</summary>


1. ETag
2. Content-Encoding
</details>

### 15.2 Content-Length : 엔터티의 길이

1. Content-Length 헤더는 엔터티 본문의 크기를 1Bit 단위로 나타낸다. (O/X)
2. 클라이언트는 메세지 잘림을 검출하기 위해 Content-Length를 필요로 한다. (O/X) 
3. 인코딩된 콘텐츠의 Content-Length 헤더는 인코딩 되지 않는 원본 콘텐츠의 길이이다. (O/X)
4. 본문을 갖는 것이 허용되지 않는 타입의 HTTP 메세지에서 Content-Length 헤더는 어떤 기능을 하는가?
5. Transfer-Encoding 헤더를 포함하고 있는 메세지는 어떤 패턴으로 메세지가 끝나는가?
<details><summary>정답</summary>
    1. X 1바이트
    2. O
    3. X 인코딩 된거임
    4. 아무런 기능도 하지 않음
    5. 0바이트 청크

</details>

### 15.3 엔터티 요약

1. 어떤 문서를 압축하여 청크 인코딩으로 보냈다면, MD5 알고리즘은 원본 문서에 대해 수행된다. (O/X)
2. Quality Value를 ㅇㅣ용해 여러 요약 알고리즘을 제안하고 선호도를 지정할 수 있는 새로운 헤더는?
<details><summary>정답</summary>

1. X
2. Want-Digest
</details>

### 15.4 미디어 타입과 차셋

1. HTTP 폼을 채워서 제출하면 HTTP는 그러한 요청을 ________나 ________헤더에 멀티파트 본문을 함께 보낸다.
<details><summary>정답</summary>

1. Content-Type: multipart/form-data나 Content-Type: multipart/mixed
</details>

### 15.5 콘텐츠 인코딩

1. 콘텐츠 인코딩 과정을 순서 대로 나열하시오.
    1. 콘텐츠 인코딩 서버(아마 원 서버이거나 다운스트림 프락시일 것이다)가 인코딩된 메시지를 생성한다. 인코딩된 메시지는 Content-Type은 같지만 (본문이 압축되었거나 했다면) Content-Length는 다르다. 콘텐츠 인코딩 서버는 Content-Encoding헤더를 인코딩된 메시지에 추가하여, 수신 측 애플리케이션이 그것을 디코딩할수 있도록한다.
    2. 웹 서버가 원본 Content-Type과 Content-Length 헤더를 수반한 원본 응답 메시지를 생성한다.
    3. 수신 측 프로그램은 인코딩된 메시지를 받아서 디코딩하고 원본을 얻는다.
2. 다음 중 HTTP에서 쓰이는 콘텐츠 인코딩 토큰이 아닌 것은?
    1. gzip
    2. compress
    3. 7zip
    4. targz
    5. deflate
    6. identity
    7. alzip
3. 2번의 인코딩 토큰 중, 일반적으로 가장 효율적이고 가장 널리 쓰이는 압축 알고리즘은?
4. HTTP Request에 Accept-Encoding 헤더를 포함하지 않는다면 서버는 이를 어떻게 받아들이는가?
<details><summary>정답</summary>
    1. 213
    2. 347
    3. gzip
    4. 어떤 인코딩이든 받아들일 수 있다. 
</details>

### 15.6 전송 인코딩과 청크 인코딩

1. JPEG 파일은 주로 gzip 방식으로 압축한다. (O/X)
2. 수신자에게 메세지가 청크 인코딩으로 전송 인코딩되었음을 알려주기 위해 _______ 헤더를 포함한다.
3. 청크 인코딩이란?
4. 콘텐츠 인코딩과 전송 인코딩은 동시에 사용될 수 없다. (O/X)
<details><summary>정답</summary>
    1. X 잘 압축되지 않는다고 함
    2. Transfer-Encoding( : chunked)
    3. 메세지를 일정 크기의 청크 여럿으로 쪼개는 것 
    4. O ㅆㄱㄴ
</details>

### 15.7 시간에 따라 바뀌는 인스턴스

1. HTTP 프로토콜에서 정의된 특정한 종류의 요청이나 응답을 다루는 방법들은?
<details><summary>정답</summary>
    1. 인스턴스 조작(instance manipulation)
</details>

### 15.8 검사기와 신선도는 7장에서 다루었습니다. 


### 15.9 범위 요청

1. 서버는 클라이언트에게 자신이 범위를 받아들일 수 있는지 응답에 ________________ 헤더를 포함시키는 방법으로 알려줄 수 있다.
<details><summary>정답</summary>

1. Accept-Range
</details>

### 15.10 델타 인코딩

1. 델타 인코딩은 어떻게 전송량을 최적화 하는지 간단하게 서술하시오.
<details><summary>정답</summary>

1. 객체 전체가 아닌 변경된 부분에 대해서만 통신
</details>