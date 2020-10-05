# jwp-spring-boot
Spring + Spring Boot 학습을 위한 저장소

#### 캐싱 설정, 테스트 코드
- myblog.WebMvcConfig: Spring Boot에서 캐싱, ETag 설정
- support.handlebars.BlogHandlebarsHelper: 캐싱 무효화를 위한 Handlerbars.java template engine Helper
- Helper가 사용된 곳은 src/main/resources/templates의 include/header.html에서 확인 가능함
- myblog.web.StaticResourcesTest: 테스트 코드를 활용해 ETag 학습

#### 미션 요구사항1
- 모든 정적 자원에 대해 no-cache, private 설정을 하고 테스트 코드를 통해 검증한다.
- 확장자는 css인 경우는 max-age를 1년, js인 경우는 no-cache, private 설정을 한다.
- 모든 정적 자원에 대해 no-cache, no-store 설정을 한다. 가능한가?

#### 미션 요구사항2
- Spring Boot에 CORS filter를 설정한다.
- 설정 조건은 https://edu.nextstep.camp 의 요청 중 GET method의 모든 요청에 대해 접근을 허용한다.
- StaticResourcesTest의 cors 테스트 메소드가 pass해야 한다.
