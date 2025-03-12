## 목차

### BackEnd

### Cookie

#### Cookie 요청

- Clinet가 요청 생성
- WAS는 Cookie를 생성하소 HTTP Header에 Cookie를 넣어 응답
- Client는 Cookie를 저장, 해당 서버에 요청할 때 요청과 함께 Cookie를 전송
- Cookie는 브라우저가 종료되더라도 계속 저장되기 때문에 동일 사이트 재방문하여 요청 시 필요에 따라 Cookie가 재 전송됨

#### Cookie 특징

- 이름, 값, 만료일, 도메인 경로등으로 구성된다.
- 클라이언트에 최대 300개의 쿠키를 저장할 수 있다
- 하나의 도메인당 20개의 쿠키를 저장할 수 있다.
- 쿠키 하나당 4KB(4096byte) 제한

#### Cookie 주요 메서드

|메서드|설명|
|---|---|
|void setComment(String comment)||
|void setDomain(String domain)||
|void setMaxAge(int expiry)||


### Session

- 사용자가 웹 서버에 접속해 있는 상태를 하나의 단위
- 각 세션은 sessionid를 이용해 구분
- WAS의 메모리에 객체 형태로 저장
- 메모리가 허용하는 용량 까지 제한없이 저장가능
- 쿠키는 클라이언트에 저장되기 때문에 공유 PC의 경우 보안에 취약할 수 있다. 하지만 세션은 서버에 저장되기 때문에 쿠키에 비해 보안이 좋다
- 사용자(로그인)정보 및 장바구니 등에 사용한다.

#### HttpSession 주요 메서드

|메서드|설명|
|---|---|
|void setAttribute(String name, Object value)||
|void setMaxInactiveInterval(int interval)||

