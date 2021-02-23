# HTTP 스터디 19장

# 19. 배포시스템

> HTTP에 기반을 둔 웹 콘텐츠 배포 기술을 알아보자.
<br>

## 19.1 배포 지원을 위한 FrontPage 서버 확장

- FrontPage : MS 사의 웹개발 및 배포 도구 집합, 웹 사이트 관리와 제작

1. 다음은 FrontPage 서버확장(FPSE)에 대한 설명이다. 다음 보기 중 틀린 것을 모두 고르시오.
    1. 서버 측 컴포넌트는 웹 서버와 통합되어 웹 사이트와 FP 클라이언트 사이에서 필요한 변환 작업을 수행한다.
    2. FP 배포 프로토콜은 POST 요청 위에 NPC 계층을 구현했다.
    3. 클라이언트와 서버 사이에 방화벽이나 프락시 서버가 없어야 FP는 서버와 통신을 계속할 수 있다. 
    4. FPSE의 보안은 웹 서버에 의존한다.
<details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	2 : NPC가 아니라 RPC
	3 : 클라이언트와 서버 사이에 방화벽과 프락시 서버가  있더라도 POST 메서드 통신만 할 수 있으면 FP는 서버와 통신을 계속할 수 있다. p.492
	    
</details>
<br><br>


2. FP 클라이언트와 FPSE는 자체 프로토콜을 사용해 통신한다. 다음 단어를 넣어 이 프토토콜을 설명하시오.

→  `POST요청` `본문` `RPC매서드`
<details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	    RPC 프로토콜은 RPC 메서드와 그와 관련한 변수를 HTTP POST 요청의 본문에 기술하여 HTTP POST를 감싼다. p.493
	    
</details>
<br><br>


## 19.2 WebDAV와 공동 저작

- WebDAV : 웹 분산 저작과 버저닝

1. 다음 빈칸을 채우시오.

	HTTP는 요청과 응답에 관한 정보를 메시지 헤더에 담아 전달한다.
	하지만 헤더에만 정보를 담아 전송하는 것은 하나의 요청에 있는 여러 개의 리소스나 계층 관계에 있는 리소스들에 대한 정보를
	선택적으로 기술하기 어려운 점 등의 한계를 지닌다. 따라서 WebDAV는 이 문제를 해결하려고 __________을 지원한다.

- 힌트 : WebDAV는 _______를 데이터를 어떻게 처리할지 설명하기 위해, 서버의 복잡한 응답을 표현하기 위해 등의 용도로 사용한다.
<details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	    XML
	    
</details>
<br><br>

2. 다음 상황을 개선하기 위해 WebDAV는 ____개념을 지원한다.
![캡처](https://user-images.githubusercontent.com/76691680/108810394-601b4c00-75ee-11eb-8ccb-fea3a6c6795f.JPG)
<details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	    LOCK 잠금 : 공동 작업 시 버전을 통합하지 않고 이전 작업 버전을 잃어버리는 것을 막기 위해 배타적 쓰기 잠금과 공유된 쓰기 잠금을 지원
	    
</details>
<br><br>


3. WebDAV에서 UNLOCK이 성공하기 위한 두 가지 조건은 기본인증과 Lock-Token 헤더에 보내는 잠금 토큰의 일치 검사이다. (O/X)
<details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	    O : p.505
	    
</details>
<br><br>

4. 저작자의 이름, 수정 날짜 등과 같은 속성의 발견과 수정을 지원하기 위해 WebDAV는 ____(1)______와 _____(2)______라는 두 가지 새로운 메서드를 포함한다.
    - 힌트 :
        - (1)은 속성(property)과 값을 요청하고 찾는데 사용
        - (2)는 특정 리소스의 속성(property)를 설정하거나 제거하는 메커니즘 제공

<details>
	    <summary> 정답</summary>
	    <div markdown="1">
	    
	    (1) PROPFIND / (2) PROPPATCH
	    
</details>
<br><br>
    
