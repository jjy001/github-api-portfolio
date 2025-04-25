## 🔍 OAuth 과정

## 인증 방식
- Personal Access Token(PAT) 기반 인증 사용
- Authorization 헤더에 Bearer 토큰으로 요청

## 토큰 발급
1. GitHub > Settings > Developer settings > Tokens
2. Scope 설정: `repo`, `user` 포함
3. Token 복사 → Postman에 삽입

## 인증 실패 시나리오
- 토큰 만료 → 401 Unauthorized
- 스코프 부족 → 403 Forbidden
  
