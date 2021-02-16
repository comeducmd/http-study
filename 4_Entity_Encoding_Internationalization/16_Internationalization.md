# 16장 국제화

1. 다음 헤더를 해석하시오.

    ```python
    Accept-Language : fr, en;q=0.8
    Accept-Charset : utf-8
    ```

    <details>
       <summary> 정답</summary>
       <div markdown="1">
       
        클라이언트는 프랑스어와 영어를 사용한다.

        영어보다는 프랑스어를 사용한다.

        UTF-8 유니코드 차셋 인코딩을 지원한다.
       
</details>
<br>


    

2. 다음은 웹 서버가 클라이언트에게 보내는 MIME 차셋 태그이다.

    ```html
    <HEAD>
    	<META HTTP-EQIV = "(A)" (B)="text/html; (C)=iso-2022-jp">
    ```

    (A) = `_________`

    (B) = `_________`

    (C) = `_________`

    <details>
       <summary> 정답</summary>
       <div markdown="1">
       
        (A) = Content-Type

        (B) = CONTENT

        (C) = charset
       
</details>
<br>



<br>

3. 브라우저 A와 브라우저 B가 서버에서 온 문자를 UTF-8를 사용하여 디코딩했더니 각각 가와 나가 되었다. 가와 나가 다르게 갖는 특성을 모두 고르시오.

![Untitled](https://user-images.githubusercontent.com/67185391/108041239-9b170000-7081-11eb-8ae8-9676bfb380c6.png)

  
    <보기>

    `문자` `글리프` `문자코드` `인코딩된 문자의 길이`
    
    <details>
       <summary> 정답</summary>
       <div markdown="1">

        
           - 문자

              둘 다 Z이므로 같은 문자이다.

          - 글리프

              모양이 다르므로 다른 글리프를 갖는다.

          - 문자 코드

              UFT-8은 ASCII와 완벽히 호환된다. 둘 다 문자 코드 90을 갖는다.

          - 문자 길이

              ASCII는 7비트의 고정 길이 인코딩 방식이다. Z를 인코딩하면 1011010이 된다.

              UTF-8에서 문자 코드 90인 Z를 인코딩하면 01011010이 된다. 8비트이다.
          
       
</details>

<br>




4. 어떤 헤더에 관한 설명인지 맞추시오.

    1. `_____________` 엔터티 헤더 필드는 엔터티가 어떤 언어 사용자를 대상으로 하고 잇는지 서술한다.
    2. `_____________`  는 클라이언트가 서버에게 자신이 이해할 수 있는 콘텐츠를 요청하기 위해 사용한다.

    <details>
       <summary> 정답</summary>
       <div markdown="1">

            Content-Language

            Accept-Language
       
</details>

<br>


5. 다음 문자들을 예약된 문자, 예약되지 않은 문자, 이스케이프 문자로 구분하시오. 

    1. `k`
    2. `;`
    3. `=`
    4. `$`
    5. `_`
    6. `.`
    7. `(`
    8. `%`

    <details>
       <summary> 정답</summary>
       <div markdown="1">
       
           1. 예약되지 않음
           2. 예약됨
           3. 예약됨
           4. 예약됨
           5. 예약되지 않음
           6. 예약되지 않음
           7. 예약되지 않음
           8. 이스케이프

</details>
       
<br>

    

6.  다음은 이스케이핑에 대한 설명이다.

    이스케이프는 `____________` 하나와 뒤이은 `___________` 둘로 이루어진 세 글자 문자열이다.

<br>

7. 다음 보기는 국제화된 HTTP 애플리케이션을 작성할 때 명심해야할 점에 대한 설명이다.

   1. HTTP 헤더는 반드시 UTF-8 문자집합의 글자들로만 이루어져야 한다. ( ⭕ ❌)
   2. 웹브라우저는 국제화 도메인 이름를 지원하기 위해 유니코드를 사용한다. ( ⭕ ❌)

    <details>
       <summary> 정답</summary>
       <div markdown="1">

            1. ❌
                HTIP 헤더는 반드시 US-ASCII 문자집합의 글자들로만 이루어져야 한다.
            2. ❌
                오늘날 대부분의 웹브라우저가 퓨니코드(punycode)를 이용해 이를 지원한다. 퓨니코드란 유니코드 문자열을 호스트 명에서 사용 가능한 문자만으로 이루어진 문자열로 변환하는 방법이다.

    

</details>
