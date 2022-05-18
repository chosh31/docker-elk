# Elastic stack (ELK) on Docker

## Fork
- https://github.com/deviantony/docker-elk

## 참고 사항
- 우선 샘플로그로 `docker-elk/logs/*.log` 파일을 파싱해서 적재 진행
  - 관련 파일 삭제 후 분석할 로그 파일 해당 디렉토리에 넣고 실행

## 사용 가이드
- docker 설치

- Repo clone & 실행
```
$ git clone https://github.com/chosh31/docker-elk.git
$ cd docker-elk
$ docker compose up -d
```

- Kibana 대시보드 접속
  - http://localhost:5601 접속 (default :: id: elastic/ pw: changeme)

- Kibana 인덱스 설정
  1. `Kibana` 홈
  2. 왼쪽상단 3줄메뉴
  3. `Stack management`
  4. `Kibana - Data Views` 클릭 
  5. `create data view`
  6. `name`으로 `logstash-*` 지정 후 생성

- Kibana Discover
  1. `Kibana` 홈
  2. 왼쪽상단 3줄메뉴
  3. `Analytics - Discover` 클릭

- 종료 시
```
$ docker compose down
```
