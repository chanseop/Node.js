**HTTP보다 HTTPs가 더 보안이 더 좋다.**

**HTTP v1:텍스트형식**

**HTTP v2:바이너리 형식**

<h2>HTTP Status Codes:</h2>

**100 정보** 
- 100 continue
- 102processing

**200 성공** 
- 200 ok 
- 201 created 
- 204 no content:데이터는 없다

**300 redirection**
- 301 moved permanently:영구적으로 옮겨갔다 
- 302 found:일시적으로 옮겨갔다 
- 303 see ohter:get요청에만 사용 
- 307 temporary redirect:post요청으로 옮겨갔을때  
- 308 permanent redirect:

**400 에러** 
- 400 bad request:쿼리가 잘못됐을때 
- 401 unauthorized:로그인 권한 없는 사람이 요청 
- 403 forbidden:로그인하지만 권한이 없을때 
- 404 not found:원하는 url이 존재하지 않을때 
- 405 method not allowed:쓰거나 삭제가 허용되지 않을때 
- 409 conflict:이미 존재하거나 에러가 있을떄

**500 서버 에러**
- 500 internal server error:서버 내부에 문제가 발생 
- 502 bad gateway:서버가 어떻게 처리해야될지 모를때 
- 503 service unavailable:서버가 준비가 되지 않을때

해설 주소:https://developer.mozilla.org/ko/docs/Web/HTTP/Status 


**URL Request Methods**
- 읽기만 가능
 - GET :get
 - HEAD:get without body
 - OPTION:all supported methods for URL
 - TRACE:echoes the received request

**변경가능**
- POST:create
- PUT:replace
- DELETE:delete
- PATCH:replace partially

해설 주소:https://developer.mozilla.org/ko/docs/Web/HTTP/Methods 


HTTP 헤더:https://developer.mozilla.org/ko/docs/Web/HTTP/Headers 




<h2>REST:respresentational state transger</h2>
 
 1. 클라이언트-서버 아키텍쳐:클라이언트가 무엇이든지 정보를 전달할수 있는 아키텍쳐가 되어야한다
 2. statelessness:하나의 요청이 다른 요청과 state가 없는 상태로 디자인해야한다
 3. cacheability:캐시가 가능하다면 캐리를 할수 잇는것으로 디자인해야한다
 4. layered system:클리이언트가 서버가 얼마나 있든지 공통된 api하나로 사용할수 있어야한다.
 5. code on demand(option):클리이언트가 원한다면 클라이언트가 수행해야하는 코드를 서버에서 보내줄수 있다.
 6. uniform interface

<h3>uniform interface</h3>
 - resource identification in requests:클라이언트가 어떤 resource를 원하는 식별할수 있어야한다.
 - resource manipulation through representations:클라이언트한테 어떤 요청을 받았을때 어떤식으로 요청해야하는지 알수 있어야한다.
 - self-descriptive messages:서버에서 보내는 응답데이터에는 클라이언트가 어떻게 처리해야하는지 설명이 되어야한다.
 - hypermedia as the engine of application state(HATEOAS):서버에 어떤 URL이 있는지 알아야한다.

--------------------------------------------------------------------------------------------------------------------------------------

**Designig Web APIs**
 - CRUD:create read update delete
 - GET /posts :무언가를 가져온다
 - POST /posts :POST 도메인에 (같은 URL에)posts를 만든다.
 - GET/posts/1 :posts라는 도메인에 아이디가 1이라는 posts를 가져온다.
 - PUT/posts/1 :posts라는 도메인에 아이디가 1이라는 posts를 업데이트한다.
 - DELETE/posts/1: //          //              ///         삭제한다.

**EX>**
- GET/tags/?postld=1 :postid가 1인 tag를 가져오고 싶다.
- GET/tags/?query=cool : query=cool이라는 tag를 가져오고 싶다.





