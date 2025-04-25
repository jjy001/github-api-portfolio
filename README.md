# github-api-portfolio
GitHub REST API 기반 인증 및 이슈 기능 테스트
GitHub의 REST API 중 이슈(issue) 기능과 사용자 인증 과정을 중심으로
QA 관점에서 테스트 시나리오를 설계하고 검증한 결과를 정리하였습니다.

개인적으로 API 테스트 역량을 강화하고 싶다는 생각에서 시작하게 되었으며
실제로 OAuth 기반 인증 처리, 권한별 접근 제어, 정상/예외 케이스 분리 등 단순 기능 확인을 넘어서 테스트 케이스를 세분화하는 과정에 집중하였고 테스트 도구로는 **Postman**을 사용하였습니다.

## 🔍 주요 테스트 항목
- 사용자 정보 조회 API (GET /user)
- 레포지토리 목록 조회 API (GET /user/repos)
- 이슈 생성 / 수정 / 삭제 (POST, PATCH, DELETE)
- OAuth 토큰 없이 호출 시 응답 처리 확인
- 스코프(scope)에 따른 API 접근 제어 검증


## 🛠 사용 도구 및 환경
- GitHub Personal Access Token (PAT) 활용
- Postman + Bearer Token 인증 방식
- API 문서: [GitHub REST API](https://docs.github.com/en/rest)


## 🗂 디렉토리 구성

| 경로 | 설명 |
|------|------|
| `/testcases/` | 기능별 테스트 시나리오 정리 |
| `/results/` | 실제 요청/응답 캡처 및 테스트 결과 |
| `/docs/` | OAuth 인증 흐름, 테스트 설계 기준 등 |
| `README.md` | 프로젝트 개요 및 요약 문서 |


## 🧩 회고
이번 포트폴리오를 통해 API 테스트 시 예상 응답이 명확하지 않거나
문서화되지 않은 예외가 있을 때 QA가 어떤 기준을 가지고 테스트해야 하는지를 체감했습니다.  
특히 인증 스코프에 따른 접근 차단 테스트는 문서만 보면 놓치기 쉬운 항목이라  
직접 요청을 구성하고 다양한 조합으로 시도해보며 경험적으로 정리할 수 있었습니다.
