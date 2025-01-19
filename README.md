# Backend Onboarding Project ( java )

## 💡 요구사항

- [x] Spring Security를 이용한 Filter에 대한 이해
- [x] JWT와 구체적인 알고리즘의 이해
- [x] PR 날려보기
- [x] 리뷰 바탕으로 개선하기
- [x] EC2에 배포해보기


## 💡 시나리오 설계
<details>
<summary> Spring Security 기본 이해</summary>

 - Spring Security
   - Spring 기반 애플리케이션에서 인증과 권한을 관리하는 보안 프레임워크다. 
   - 필터 체인을 통해 요청별 보안 처리를 제공한다.

- Filter
    - Servlet 에서 클라이언트 요청과 응답을 가로채 처리하는 컴포넌트다.
    - 인증, 로깅, 데이터 변환 등에 사용된다.
    - Interceptor 는 Spring 에서 Handler 전후를 제어하며, AOP 는 메서드 실행 전후 로직을 적용한다. [AOP 에 대해 이해하기](https://hanstory33.tistory.com/204)
</details>

<details>
<summary> JWT 기본 이해</summary>

[JWT 에 대해 알아보기 (링크)](https://hanstory33.tistory.com/191)

JWT 는 클라이언트와 서버 간 인증 및 정보를 안전하게 전달하기 위한 토큰으로 토큰 자체에 데이터를 포함해 서버의 별도 저장소 접근 없이 인증을 처리할 수 있다는 특징이 있다.
</details>

<details>
<summary> Access Token, Refresh Token 발행과 유효성 확인</summary>

### 토큰 검증 테스트 시나리오
  - `/check/token` 유저 권한으로만 접근 가능한 API 엔드포인트 생성
  - 로그인 시 `Access Token`, `RefreshToken` 발급
  - `Access Token` 유효시간 만료 후 `/check/token` API 접근 시 `Refresh Token` 으로 `Access Token` 재발급 후 접근 확인
</details>

<details>
<summary> 유닛 테스트 작성</summary>

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FRHtSd%2FbtsLRkeTaTX%2FtcnQhW8GOx8QVy1mXpD6J0%2Fimg.png" style="width:400px; padding-left:10px;">

[JUnit5 를 활용한 단위 테스트 코드 작성하기](https://hanstory33.tistory.com/201)
</details>

## 💡 API 명세
  <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbGaIX4%2FbtsLSzI4gJq%2F3xVpftQL3lztNWUS4oKcfK%2Fimg.png" style="width:600px; padding-left:10px;">


## 💡 작업 진행
- [x] 회원가입 기능 구현 및 테스트

  <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbSsq60%2FbtsLTGNTSVn%2FKKB4KAnyAE4i0VfqBQjJg0%2Fimg.png" style="width:500px; padding-left:10px;">
  
- [x] 로그인 기능 구현 및 테스트
  
  <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FToNrw%2FbtsLS935fmm%2FZgstJZIs2KXj8h8E9Ov8lk%2Fimg.png" style="width:500px; padding-left:10px;">

- [x] Swagger UI 설정 및 API 검증

  <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbb4Wxl%2FbtsLTHeW5mx%2Fp8uwzRLYDFEoTNiTKiN13K%2Fimg.png" style="width:500px; padding-left:10px;">
  <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcGcr1h%2FbtsLTHlJreb%2FIcKfLZ8vk0dSgokYp1lWxK%2Fimg.png" style="width:500px; padding-left:10px;">

- [x] PR 작성 및 제출

  <img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbMafHo%2FbtsLRmKzBMd%2FPCHXKelgxXp7QKUkOpuRKk%2Fimg.png" style="width:300px; padding-left:10px;">
