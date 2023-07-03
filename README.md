# Dockerfile 
FROM [이미지]:[태그] // 기반 이미지 

COPY [현재위치파일위치] [docker내위치] // 파일복사

# docker hub 에서 이미지 태그 확인
* https://hub.docker.com/

# 이미지 생성
* 특정한 태그 이름으로 이미지 빌드
    * -t : --tag
        * [REPOSITORY]:[TAG]
```
$ docker build -t nginx:test-nginx .
// $ docker build -t [생성할이미지명]:[태그] [Dockerfile위치]
```

# 컨테이너 실행
* 컨테이너 이름
    * --name
* 데몬 실행(백그라운드 실행)
    * -d
* 포트 설정
    * -p [호스트 서버 포트] [도커 컨테이너 내서버 포트]
```
$ docker run --name mynginx -d -p 8080:80 nginx:test-nginx
// $ docker run --name [컨테이너이름] -d -p [호스트포트]:[컨테이너포트] [이미지명]:[태그]
```
