# HTTP 스터디 21장
## 21. 로깅과 사용 추적

1. 애플리케이션이 더 다양한 표준 로그 포맷을 지원함으로써 얻는 이점은?

    <details>
          <summary> 정답</summary>
          <div markdown="1">


          직접 지정한 필드를 포함한 로그 포맷을 통해 필요한 통계를 추출할 수 있어 더 잘 활용할 수 있다.


    </details>
    <br><br>


    
   

2. 다음 중 혼합 로그 포맷에만 있는 필드를 모두 고르시오.
    - `username`
    - `reponse-code`
    - `Referer`
    - `client-request-size`
    - `proxy-timestamp`
    - `User-Agent`
    
    <br>
    <details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    

      `Referer` : 이 URL을 요청자가 어디서 찾았는지에 대한 정보 제공

      `User-Agent` : 요청을 만든 HTTP 애플리케이션이 무엇인지 알아볼 수 있음

      `username` , `reponse-code` 는 일반 로그 포맷에도 있는 필드이며

      `client-request-size` 와 `proxy-timestamp` 는 혼합 로그 포맷에 없고 넷스케이프 확장 로그 포맷에만 있는 필드이다. 일반 로그 포맷에는 `request-size` 와 `timestamp` 필드가 있다.


</details>
<br><br>

3. 다음은 일반 로그 포맷 엔트리의 예시이다. 엔트리에서 `username` , `timestamp` , `request-line` 필드를 찾고, 해당 필드가 무슨 의미인지 해석하시오.


    `209.1.32.44 - - [03/Oct/1999:14:16:00 -0400] "GET/HTTP/1.0" 200 1024`
    
    <details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
      
        username

        - *-*
        - `username` 필드에는 만약 ident 검색을 수행했다면 인증된사용자의 이름이 있게 된다. 여기서의 `username` 필드는 비어있다. 즉 ident 검색을 수행하지 않았다는 것을 의미한다.

        timestamp

        - *[03/Oct/1999:14:16:00 -0400]*
        - 요청 날짜와 시간

        request-line

        - *"GET/HTTP/1.0"*
        - HTTP 요청의 행을 그대로 기술한다.

</details>
<br><br>

   
4. 다음은 로깅에 대한 설명이다.

    원 서버는 결산을 하기 위해 상세 로그를 저장한다. 하지만 `(a)`에 의해 로그 파일에 누락이 발생하게 되어, 결국 콘텐츠 제공자는 `(b)` 를 파기하게 된다. 이 방법으로 로깅에는 문제가 생기지 않지만, 요청에 대한 응답 속도는 느려지고, 원 서버와 네트워크의 부하가 가중된다. 따라서 이러한 문제를 해결하기 위해 `(c)` 를 제시하였다.
  
  
    <details>
          <summary> 정답</summary>
          <div markdown="1">

          (a) : 캐시

          클라이언트와 서버 사이에 캐시가 있어 많은 요청이 서버까지 오지 않고 캐시되어 있는 리소스로 처리된다.

          (b) : 캐시

          캐시를 파기 하면 모든 요청이 원 서버로 가기 때문에 속도가 느려지게 된다.

          (c) : 적중 규약

    </details>
    <br><br>

    
    


5. `(c)` 가 어떠한 방식으로 `(a)`에 의한 로깅 문제를 해결하는지 설명하시오.

    
    <details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	    
        프락시 캐시들은 자체 로그를 유지하기 때문에, 적중 계량 규약에서는 캐시가 정기적으로 캐시 접근 통계를 서버에 보고하도록 해 서버가 원하는 통계 정보를 받아볼 수 있게 한다.
	    
</details>
<br><br>



6. `(c)` 를 사용하기 위해 추가한 헤더의 이름은?

    <details>
          <summary> 정답</summary>
          <div markdown="1">

             `Meter` 헤더

    </details>
    <br><br>



# 그동안 수고하셨습니다!
# 개강도 축하드려요~
 
