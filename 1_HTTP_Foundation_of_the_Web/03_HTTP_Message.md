## 03장. HTTP 메시지 `Serin-Yoon`

### 3.1 메시지의 흐름
1. HTTP 메시지는 HTTP _____ 간에 주고받은 데이터의 블록들이다.
2. 데이터 블록들은 메시지의 내용과 의미를 설명하는 텍스트 _____로 시작하고 그 다음에 선택적으로 데이터가 올 수 있다.
3. 인바운드, 아웃바운드, 업스트림, 다운스트림은 메시지의 방향을 의미하는 용어다. (O/X)
4. 메시지가 원 서버로 향하는 것은 아웃바운드로 이동하는 것이고, 모든 처리가 끝난 뒤 메시지가 사용자 에이전트로 돌아오는 것은 인바운드로 이동하는 것이다. (O/X)
5. HTTP 메시지는 요청 메시지인지 응답 메시지인지와 관계없이 모두 업스트림으로 흐른다. (O/X)

<br />
💡 답안 및 해설 보기
<br /><br />

### 3.2 메시지의 각 부분

#### 3.2.1 메시지 문법
1. HTTP 메시지는 시작줄, 헤더 블록, 본문으로 이루어져 있는데, 이중 본문은 아예 없을 수도 있다. (O/X)
2. 요청 메시지의 형식은 다음과 같다.
```
<메서드> <_____> <버전>
<헤더>

<엔터티 본문
```
3. 응답 메시지의 형식은 다음과 같다.
```
<_____> <상태 코드> <사유 구절>
<헤더>

<엔터티 본문>
```
4. HTTP 헤더는 항상 빈줄(CRLF)로 끝나야 한다. (O/X)

#### 3.2.2 시작줄
1. 클라이언트가 뭔가 잘못된 요청을 했음을 의미하는 상태 코드의 정의된 범위는 ___ ~ ___ 이다.
2. 버전 번호의 각 숫자는 하나의 실수로 다루어진다. (O/X)

#### 3.2.3 헤더
1. `Content-type: image/gif`는 엔터티 본문이 GIF 이미지라는 것을 의미한다. (O/X)


#### 3.2.4 엔터티 본문
1. HTTP 메시지는 이미지, 비디오, HTML 문서, 소프트웨어 애플리케이션, 신용카드 트랜잭션, 전자우편 등 여러 종류의 디지털 데이터를 실어나른다. (O/X)

#### 3.2.5 버전 0.9 메시지
1. HTTP/0.9 응답 메시지에 포함되어 있는 것은 무엇인가?
a) 상태 코드
b) 엔터티
c) 사유구절
d) 헤더
e) 버전 정보

<br />
💡 답안 및 해설 보기
<br /><br />

### 3.3 메서드
#### 3.3.1 안전한 메서드(Safe Method)
1. 안전한 메서드가 사용된 HTTP 요청은 서버에 영향을 미친다. (O/X)

#### 3.3.2 GET
1. GET 메서드는 서버가 처리해야 할 데이터를 보내도록 요청하는 메서드이다. (O/X)

#### 3.3.3 HEAD
1. HEAD 메서드의 기능이 아닌 것은 무엇인가?
a) 리소스의 엔터티 본문을 확인한다.
b) 리소스가 변경되었는지 검사한다.
c) 응답 메시지의 상태 코드를 통해 개체가 존재하는지 확인한다.
d) 리소스의 타입, 길이 등을 알아낸다.

#### 3.3.4 PUT
1. PUT 메서드는 리소스를 생성하거나 리소스 내용을 변경하도록 하기 때문에 사용자에게 로그인하도록 요구하는 것이 좋다. (O/X)

#### 3.3.5 POST
1. POST 메서드는 서버에 _____를 전송하는 메서드이다.

#### 3.3.6 TRACE
1. TRACE 요청은 목적지 서버에 _____ 진단을 시작한다.
2. TRACE 메서드를 사용하면 서버는 자신이 받은 요청 메시지를 본문에 넣어 응답 메시지를 보낸다. (O/X)
3. TRACE 메서드를 사용할 때엔 엔터티 본문을 보낼 수 없다. (O/X)

#### 3.3.7 OPTIONS
1. OPTIONS 메서드는 리소스에 접근하여 서버가 지원하는 메서드의 목록을 확인하도록 하는 메서드이다. (O/X)

#### 3.3.8 DELETE
1. DELETE 메서드를 사용해도 리소스가 삭제되었다고 확신할 수는 없다. (O/X)

#### 3.3.9 확장 메서드
1. 확장 메서드는 HTTP/1.2 명세에 정의되지 않은 메서드다. (O/X)
2. 확장 메서드를 다룰 때는 "관대하게 보내고 엄격하게 받아들여라"라는 규칙에 따르는 것이 바람직하다. (O/X)

<br />
💡 답안 및 해설 보기
<br /><br />

### 3.4 상태 코드
#### 3.4.1 100-199: 정보성 상태 코드
1. 서버로부터 100 Continue 응답을 받은 클라이언트는 엔터티를 보내면 된다. (O/X)
2. 서버가 100 Continue 응답을 보내기도 전에 클라이언트로부터 엔터티 일부 또는 전체를 전송받은 경우에도 클라이언트에게 100 Continue 응답을 보내주어야 한다. (O/X)
3. 서버가 엔터티까지 모두 전송받은 후에는 최종 응답을 보내야 한다. (O/X)

#### 3.4.2 200-299: 성공 상태 코드
1. 상태 코드 ___ (사유 구절 No Content)는 '응답 메시지는 헤더와 상태줄을 포함하지만 엔터티 본문은 포함하지 않음'을 의미한다.
2. 상태 코드 ___ (사유 구절 Accepted)는 는 '요청은 받아들여졌으나 서버는 아직 요청에 대한 어떤 동작도 수행하지 않았음'을 의미한다.

#### 3.4.3 300-399: 리다이렉션 상태 코드
1. 몇몇 리다이렉션 상태 코드는 리소스에 대한 로컬 복사본이 유효한지, 즉 최신인지 수정되었는지 확인하기 위해 사용된다. (O/X)
2. 클라이언트는 문서가 특정 날짜 이후에 수정된 경우에만 문서를 가져오라고 요청하기 위해 __________ 헤더를 전송하고, 해당 날짜 이후에 변한 것이 없다면 서버는 문서 대신 304 상태 코드로 답한다.

#### 3.4.4 400-499: 클라이언트 에러 상태 코드
1. 413 상태 코드(사유 구절: Request Entity Too Large)는 서버가 처리할 수 있는 혹은 처리하고자 하는 한계를 넘은 길이의 요청 URL이 포함된 요청을 클라이언트가 보냈을 때 사용한다. (O/X)

#### 3.4.5 500-599: 서버 에러 상태 코드
1. 505 상태 코드(사유 구절: HTTP Version Not Supported)는 서버가 지원할 수 없거나 지원하지 않으려고 하는 버전의 프로토콜로 된 요청을 받았을 때 사용한다. (O/X)

<br />
💡 답안 및 해설 보기
<br /><br />

### 3.5 헤더
#### 3.5.1 일반 헤더
1. 일반 헤더는 요청 메시지, 응답 메시지에 모두 사용된다. (O/X)

#### 3.5.2 요청 헤더
1. Accept 관련 헤더는 서버에게 클라이언트의 선호와 능력을 알려줄 수 있다. 이때 `Accept: */*` 가 의미하는 것은 무엇인가?
2. [보기] 중 알맞은 단어를 선택해 넣자.
[보기] 조건부 요청 / 요청 보안
	-  _____ 헤더는 서버에 제약을 넣을 때 사용한다.

#### 3.5.3 응답 헤더
1. 응답 보안 헤더 중 WWW-Authenticate 헤더는 프락시에서 클라이언트로 보낸 인증요구의 목록을 나타낸다. (O/X)

#### 3.5.4 엔터티 헤더
1. 다음 중 콘텐츠 헤더인 것을 모두 골라보자.
a) Content-Encoding
b) Content-Range
c) Content-Length
d) Content-Language
e) Content-Type

<br />
💡 답안 및 해설 보기
<br /><br />