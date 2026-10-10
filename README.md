# SpringBoot_Discord_WebHook

Spring Boot에서 이벤트 발생 시 Discord 웹훅으로 알림을 보내는 연동 예제입니다.

- 이벤트 진입점: `POST /api/event`
- 알림 전송: [WebHookService.java](src/main/java/discord/webhook_test/Service/WebHookService.java)의 `RestTemplate` 호출
- 요청 처리: [ApiController.java](src/main/java/discord/webhook_test/controller/ApiController.java)
- 구성: Java 11, Spring Boot 2.7.4, JSON.simple

## 실행

JDK 11을 준비하고 `WebHookService`의 빈 `url`에 본인의 Discord 웹훅 설정을 구성한 뒤 실행합니다. 웹훅 주소는 저장소에 커밋하지 않습니다.

```bash
./gradlew bootRun
```

Windows에서는 `gradlew.bat bootRun`을 사용합니다. 이 저장소는 연동 코드를 살펴보는 예제로, 이벤트 처리와 응답은 현재 소스 범위에 맞춰 확인합니다.
