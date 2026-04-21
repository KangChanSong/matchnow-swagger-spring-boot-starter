# Version 0.1.0

- Thin-jar 재설계: `maven-shade-plugin` 제거, starter 산출물에서 Spring/Springdoc 클래스를 더 이상 번들하지 않음
- `spring-boot-starter-parent` 상속 제거, `spring-boot-dependencies:2.5.4` BOM import 방식으로 변경
- 모든 Spring/Servlet/Lombok 의존성을 `provided` 스코프로 전환 → 소비 서비스의 Spring Boot 버전이 런타임 버전을 결정
- 빌드 baseline을 Spring Boot 2.5.4 로 낮춰 2.5.x / 2.6.x / 2.7.x 전 범위 호환 단일 artifact 로 통합 (`-2.6`, `-2.7` 분리 artifact 불필요)
- `groupId` 를 `com.matchnow` 로 명시 (기존 배포 artifact와 일치)
- `distributionManagement` 에 Nexus release/snapshot 저장소 명시, source jar 자동 첨부 (`maven-source-plugin`) 추가

# Version 0.0.7

- Jitpack refresh 용 버전업

# Version 0.0.6

- [ADD] 커스텀 ObjectMapper 설정 기능 추가

# Version 0.0.5

- 배포용 버전업

# Version 0.0.4

- include-path-patterns 설정 추가
    - path-pattern 없으면 해당 설정 사용, 잇으면 사용 안함

# Version 0.0.3

- display-servers -> servers 로 변경
- spring-security 관련 코드, 의존성 제거
- redirect-path-replacer 별도 빈 등록하지 않고 yml파일로 설정할 수 있도록 수정
- 서비스명 변경: g-swagger -> matchnow-swagger

# Version 0.0.2

- WebSecurity 자동 설정 기능 추가

# Version 0.0.1

- G-Swagger 초도 배포