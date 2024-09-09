
spring boot 3.3
jdbc: JPA
java: 1.7
DB: mysql container (docker 다른 PC)



1. todo api에 적용 하고자 했던 것
  - Presentation Layer, Business Layer 모듈과 Data Access Layer 모듈로 분리 하여 개발을 진행 하고자 했습니다.
  - Filter에 LoggerFilter을 적용하여 개발 로그를 보려고 하였습니다.
  - api 요청에 대한 응답으로 상태를 포함한 데이터 전송 하고자 하였습니다.
  - api 응답에 대한 예외 핸들러를 만들어 Front-end에서 빠르게 파악 할 수 있게 하고자 하였습니다. (ex : UserError는 1404, 1000번때는 사용자 Error)
  - dto 객체를 만들어 Data Access Layer로 송수신 데이터를 변환 하여 의존성 영향을 받지 않게 하고자 하였으며, Client로 전송 되는 데이터는 DTO를 통해서만 데이터를 주고 받음
  - formatter를 통해 날자,시간에 대한 form를 공통되게 설정 하였습니다.
  - 주고 받는 데이터의 변수들은 스네이크 케이스로 통일 설정 하였습니다.
  - Layer 별로 Text 코드를 작성 하여 Test 진행 ( Presentation Layer 계층 Test시 method 오료를 발견 추후 수정, 동작에는 문제 없음)
  - jwt 토큰을 통해 인증을 하고자 하였습니다. ( jwt 인증이 정상 작동 하였지만, security 설정 부분이 조금씩 변경되면서 인지 하지 못한 부분이 있어서 주석 처리 하였습니다. 변경된 부분을 공부 하고 사용 하고자 함 )
  - todo테이블을 만들어 crud및 페이징 처리를 하였습니다.

하고자 했던것
 - Spring MVC 패턴을 인지 하고 있는지
 - 개발에 필요한 공통된 설정을 할 수 있는지
 - CURD 및 페이징 처리를 할 수 있는지
 - HTTP 통신의 특성인 stateless에 대한 인증 방식을 알고 있는지

2. Intellj를 통해 개발을 진행 - Intellj에서는 잘 동작 하나 build 후 문제가 발생 모듈을 분리 하면서 인지 하지 못한 부분으로 그런 것으로 파악 (공부의 시간이 필요)

3. api, Swagger 
 - /api/todo/{tno}      GET       단건 조회
 - /api/todo/{tno}      PUT       업데이트
 - /api/todo/{tno}      DELETE    삭제
 - /api/todo/           POST      등록 
 - /api/todo/list       GET       10건 조회
 - /api/todo/api/{tno}  GET       Api 상태 포함 조회

- 느낌점
  spring boot 버전 상향 후 조금씩 수정 된 부분 인지 필요
  모듈을 분리로 인해 발생 되는 문제점 해결 필요
  


