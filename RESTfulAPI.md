## RESTfulAPI

* REpresentational State Transfer의 약자로 웹을 이용할 때 제약 조건들을 정의하는 소프트웨어 아키텍쳐 스타일이다
* HTTP URL을 통해 자원(Resource)를 명시하고 HTTP Method(GET, POST, PUT, DELETE)를 통해서 해당 URL에 대한 CRUD를 적용하는 것을 의미한다
* HTTP의 장점을 살리고자 하는 통신 규약이며, 이러한 규약을 바탕으로 자원(Resource) 중심으로 설계하고 기능에 맞게 HTTP Method를 사용하여 설계된 API입니다

    * GET : 지정된 URL에서 리소스의 표현을 조회
    * POST : 지정된 URL에 신규 리소스를 생성
    * PUT : 지정된 URL에 리소스를 생성하거나 업데이트
    * PATCH : 리소스의 부분 업데이트
    * DELETE : 지정된 URL의 리소스를 제거

## REST 특징

> REST 아키텍쳐에 적용되는 6가지 제한 조건

* 인터페이스 일관성 : 일관적인 인터베이스로 분리되어야 한다
* 무상태 : 각 요청 간 클라이언트의 context, 세션과 같은 상태 정보를 서버에 저장하지 않는다
* 캐시 처리 기능 : 클라이언트는 응답을 캐싱할 수 있어야 한다. 캐시를 통해 대량의 요청을 효율적으로 처리할 수 있다
* 계층화 : 클라이언트는 대상 서버에 직접 연결되어 있는지, Proxy를 통해서 연결되어 있는지를 알 수 없다
* Code on demand : 자바 애플릿이나 자바스크립트의 제공을 통해 서버가 클라이언트를 실행시킬 수 있는 로직을 전송시켜 기능을 확장시킬 수 있디
* 클라이언트/서버 구조 : 아키텍쳐를 단순화시키고 작은 단위로 분리함으로써 클라이언트-서버의 각 파트가 독립적으로 구분하고 서로 간의 의존성을 줄인다

## REST 구성 요소 

- 1. 자원(Resource) : HTTP URL
- 2. 자원에 대한 행위 : HTTP Method
- 3. 자원에 대한 표현 : (Representations)

## RESTAPI 설계 및 Rules 및 예시

* 소문자를 사용한다

* 언더바(_) 대신에 하이픈(-)을 사용한다
    > 하이픈 사용도 최소화

* 마지막에 슬래시를 포함하지 않는다

* 행위를 포함하지 않는다

* 파일 확장자는 URL에 표시하지 않는다

* 자원에는 형용사, 동사가 아닌 명사를 사용하며, 컨트롤 지원을 의미하는 경우 예외적으로 동사를 사용한다

## HTTP Status Code란 

* 클라이언트가 웹 서버에 HTTP 요청을 했을 때 웹 서버는 응답으로 HTTP 상태 코드를 알려준다

* 이러한 코드는 HTTP 요청의 성공/실패 여부를 알려주는 코드이며, 5가지 그룹으로 나뉘게 된다

## HTTP Status Code 분류

* 1xx(조건부 응답)
    - 100(계속) : Continue
    - 101(프로토콜 전환)

* 2xx(성공)
    - 200(성공)
    - 204(성공했으나 컨텐츠 없음)
    - 206(일부 컨텐츠)

* 3xx(리다이렉션 완료)
    - 301(영구 이동)
    - 304(수정되지 않음)

* 4xx(요청 오류)
    - 400(잘못된 요청)
    - 401(권한 없음)
    - 403(금지됨)
    - 404(찾을 수 없음)
    - 408(요청 시간 초과)
    - 410(사라짐)

* 5xx(서버 오류)
    - 500(내부 서버 에러)
    - 502(불량 게이트웨이)
    - 503(서비스를 사용할 수 없음)
    - 504(게이트웨이 시간 초과)