# Elastic stack (ELK) on Docker

## Fork
- https://github.com/deviantony/docker-elk

## 참고 사항
1. 우선 샘플로그로 docker-elk/logs 파일을 파싱해서 넣도록 해둠
  - 관련 파일 삭제 후 분석할 로그 파일 해당 디렉토리에 넣어둠 됨

## 사용 가이드
1. docker 설치
2. 리포 클론 & 실행
```
$ git clone https://github.com/chosh31/docker-elk.git
$ cd docker-elk
$ docker compose up -d
```
3. 키바나 대시보드 접속
- http://localhost:5601 접속 (id: elastic/ pw: changeme)
4. 키바나 인덱스 설정
- 키바나 홈 > 왼쪽상단 3줄메뉴 > stack management > Kibana - Data Views 클릭 > create data view > name으로 logstash-* 지정 후 생성
- 왼쪽상단 3줄메뉴 > Analytics - Discover 클릭
5. 종료 시
```
$ docker compose down
```
