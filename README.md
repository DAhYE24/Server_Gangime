[Server] Gangime
=================
Gangime is a errand agent application(O2O Service) based on subway lines.
## Image
#### 서버 구성
![server_diagram](https://i.imgur.com/Er9vXGR.jpg)
<br></br>
## Project Info
#### 수행기관
SK테크엑스 T아카데미
#### 프로젝트 명
심부름 대행 o2o서비스 “ 간김에 ”
#### 프로젝트 소개
간김에는 지하철역 기반으로 진행되는 심부름 대행 서비스로 사용자는 동시에 심부름을 요청하는 "요청자"와 수행하여 수익을 얻는 "대행자" 역할이 될 수 있습니다.
#### 작업 Commit 내역
*작업 초기 git config 미등록으로 Contributor에 포함되지 않아 저장소를 따로 분리했습니다.<br>
당시 Commit 작업 내역을 확인하고 싶다면 [간김에_서버작업](https://github.com/hinco114/GANGIME)를 방문해주세요*
<br></br>
## Development Info
#### 개발 기간 / 개발 인원
2017.05.24 - 2017.06.21 / 5명(본인 포함 서버 2인 외 안드로이드, 기획자, 디자이너 각각 1인)
#### 개발 환경 / 개발 언어
WebStorm(IntelliJ) / Javascript(中), Node.js(中), HTML(中), Jquery(下)
#### 주요 역할
* 서버 개발 
* DB 설계 및 구현(RDB)
* 심부름 진행 프로세스 설계
#### 특징
* Javascript ES6  작업 진행
  * Promise의 콜백 지옥을 해결하기 위해서 Javascript ES6의 Async/Await 방식을 사용하여 비동기 방식의 문제점 해결
* AWS의 EC2, S3, RDS를 활용하여 서버 연동 작업 진행
* JWT로 토큰을 암호화, 복호화 작업 진행
* FCM을 통해서 심부름 상태를 사용자에게 전달
* Sequelize를 통해서 복잡한 SQL 쿼리를 단순화하여 CRUD 작업을  진행
* Scheduler npm을 통해 1분마다 심부름 프로세스 상태를 체크하는 작업을 설정
  * 스케줄러를 자체 서버로 따로 분리할 예정이었으나 시간문제로 중단한 상태
* Express, npm 사용
* Jquery의 ajax를 통해서 데이터를 전달하는 방식(url, message)을 커스텀 하여 서버에 연결하여 심부름 프로세스를 변경
* Maria DB에 적용할 수 있는 ST_DISTANCE 함수를 사용하여 거리 계산
