### Docker 이미지 이름별 차이점

#### Alpine
* 가장 가벼움 (5MB 미만)
* musl libc 사용 (glibc와 호환성 주의)
* 보안 최소주의 → 최소 패키지만 포함
* 성능 좋지만 호환성 문제 있을 수 있음

#### Bookworm
* Debian 12 버전
* 최신 안정판 Debian
* 2023년 6월 출시

#### Bullseye
* Debian 11 버전
* 현재 널리 사용되는 안정판
* 2021년 8월 출시

#### Trixie
* Debian 테스트 버전
* 차기 Debian 버전 (아직 안정판 아님)
* 개발/테스트용

#### Iron (Ubuntu)
* Ubuntu 24.04 코드명
* 2024년 4월 출시
* 최신 Ubuntu LTS

####  slim 특징:
* 기본 이미지보다 작음
* 필수 패키지만 포함
* 빌드 도구, 개발 도구 제외
* 프로덕션 실행용 최적화

* python:3.9-alpine    → 50MB 미만  (가장 작음)
* python:3.9-slim      → 100MB 정도 (가벼움)  
* python:3.9-bullseye  → 300MB 정도 (표준)

### 선택 가이드:
##### Alpine 선택:
* 최소 크기가 최우선
* 호환성 문제 없음을 확인 후 사용해야 함
* 마이크로서비스/경량 앱

##### Slim 선택 when:
* 안정성 중요
* Alpine 호환성 문제 없음
* 적절한 크기 절충

##### Bullseye/Bookworm 선택 when:
* 풀 패키지 필요
* 개발/빌드 환경
* 호환성 최대화

* Alpine < Slim < Standard 순으로 가볍다.