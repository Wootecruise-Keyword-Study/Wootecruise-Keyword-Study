### HTTP 메시지

- HTTP 메시지는 서버와 클라이언트 간에 데이터가 교환되는 방식(요청, 응답)

### 요청

- 시작 줄
    - HTTP 메서드(GET, POST, PUT, DELETE, OPTIONS)
    - 요청 타겟(URL)
    - HTTP 버전
- 헤더
    - 메타 데이터 포함(Request, General - 별 뜻 없음, Entity - 본문)
- 바디
    - 보통 POST 요청에서 업데이트에 필요한 정보를 포함해서 보냄

### 응답

- 상태 줄
    - 프로토콜 버전, 상태 코드, 상태 텍스트
- 헤더
    - 메타 데이터 포함(Request, General - 별 뜻 없음, Entity - 본문)
- 바디
    - 길이가 알려진 경우 : Content-Type과 Content-Length
    - 알려지지 않은 경우(파일) : Transfer-Encoding이 chuncked로 설정