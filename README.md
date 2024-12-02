# 스프링 부트 애플리케이션, 도커 이미지 빌드, 컨테이너 실행 실습

스프링 부트 애플리케이션으로 도커 이미지를 빌드하고, 컨테이너를 생성해서 스프링 부트 애플리케이션 배포 연습하기 프로젝트입니다.

## 스프링 부트 애플리케이션으로 도커 이미지 빌드 및 컨테이너 실행하기

```bash
# 1. 스프링 부트 애플리케이션 패키징 하기
mvnw clean package

# 2. 도커 이미지 빌드하기
docker build -t demo-app:0.1 .

# 3. 도커 이미지 확인하기
docker image ls

# 4. 도커 컨테이너 실행하기
docker run -d -p 8080:8080 --name demo demo-app:0.1

# 5. 웹 브라우저에서 http://localhost:8080/hello를 입력해서 응답결과 확인하기
# "Hello, Spring boot"이 출력된다.
```
