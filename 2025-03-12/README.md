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
|void setComment(String comment)|쿠키에 대한 설명 설정|
|void setDomain(String domain)|쿠키의 유효한 도메인 설정|
|void setMaxAge(int expiry)|쿠키 유효기간 설정|
|void setPath(String path)|쿠키 유효 디렉토리 설정|
|void setValue(String value)|쿠키 값 설정|
|String getComment()|쿠키 설명 반환|
|String getDomain()|쿠키 유효 도메인 반환|
|int getMaxAge()|쿠키 유효기간 반환|
|String getPath()|쿠키 유효 디렉토리 반환|
|String getValue()|쿠키 값 반환|


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
|void setAttribute(String name, Object value)|session에 지정한 name에 해당하는 객체를 추가|
|void setMaxInactiveInterval(int interval)|사용자가 다음 요청을 보낼 때 까지 세션을 유지하는 최대시간(sec) 설정|
|void invalidate()|현재 세션을 없애고, 속성도 삭제한다|
|String getId()|현재 세션의 고유 id를 반환|
|long getLastAccessTime()|현재 세션에 클라이언트가 마지막으로 요청을 보낸 시간을 반환(long)|
|Object getAttribute(String name)|name에 해당하는 속성값 반환, 반환형이 Object 임에 유의|
|long getCreationTime()|세션이 만들어진 시간 반환|
|void removeAttribute(String name)|세션에서 지정한 이름의 객체를 제거|
|Enumeration getAttributeNames()|세션에서 모든 객체의 이름을 Enumeration형으로 반환|

