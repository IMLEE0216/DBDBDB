# MYSQL 설치하기

### 1. MYSQL Community Downloads 페이지

- [MySQL :: MySQL Community Downloads](https://dev.mysql.com/downloads/)

![mysql1](https://user-images.githubusercontent.com/73643473/117183669-c6082900-ae12-11eb-80b1-d75e9c48a929.jpg)

---



### 2.  Windows 버전 다운

![mysql2](https://user-images.githubusercontent.com/73643473/117183991-2f883780-ae13-11eb-9eb1-01612c6aa444.jpg)

---



### 3.  Developer Default

- MySQL Installer 열기
- Developer Default로 NEXT

![mysql3](https://user-images.githubusercontent.com/73643473/117184277-8261ef00-ae13-11eb-80b2-1f159c8d181a.jpg)

---

---



### 4. Check Requirements 

- 다른 블로그 보면 4-2 사진 또는 여러개의 선택창 같은게 보일수 있지만 4-1 사진처럼 나와도 당황하지 않고 (파이썬 한개만 나옴..) 무시하고 NEXT 하고 YES

​																			4-1 사진

![mysql4_1](https://user-images.githubusercontent.com/73643473/117184986-5135ee80-ae14-11eb-8288-1921877ac93b.jpg)

​																				4-2 사진

![mysql4](https://user-images.githubusercontent.com/73643473/117184641-e5ec1c80-ae13-11eb-8b7f-1015aa1627a2.jpg)

---



### 5. Installation

- Execute 하면 설치 진행

![mysql5](https://user-images.githubusercontent.com/73643473/117185497-dcaf7f80-ae14-11eb-968d-10a8ea5d4db9.jpg)

---



### 6.  Product Configuration (여러번 나옴)

- (Server, Router, Sample 물어보는 식으로 대략 3번 나옵니다.) 그냥 NEXT

![mysql4-2](https://user-images.githubusercontent.com/73643473/117185856-3dd75300-ae15-11eb-8e13-39a44a4dbcb1.jpg)

---



### 7.  High Availability

- 개인적으로 안떴던 사진.... 다른 블로그에는 떴길래 
- 설정 그대로 NEXT

![mysql5-1](https://user-images.githubusercontent.com/73643473/117186907-4ed49400-ae16-11eb-8958-a9d3988520b2.jpg)

---



### 8.  Type and Newtworking (Port)

- 설정 그대로 NEXT
- 만약 Port에 빨간 세모가 뜨고 사용하고 있다라고 나오면 NEXT가 안된다. (해결방법으로)

![mysql7](https://user-images.githubusercontent.com/73643473/117187432-dde1ac00-ae16-11eb-982d-42f06bd13f16.jpg)



### 8-1. Port 해결방법

- 작업관리자 열기 -> 성능 -> 리소스 모니터 열기 (CPU 빨간 네모) -> 수신 대기 포트 누르기
- 포트번호가 3306 있는데 **PID** 번호를 기억해 뒀다가 (3306포트는 대부분 mysqlid 인거 같다.)
- cmd를 **관리자 권한으로 실행** 
- **taskkill /F /PID  ** PID번호 입력하면 프로세스 PID번호가 종료됨이라고 뜬다.
- mysql installer로 돌아가면 빨간 세모는 없어지고 NEXT는 활성화
- MariaDB가 있다면 Port 번호를 다르게 하는것도 나쁘지 않을거 같다.(구글링으로 찾아보기)

![mysql6](https://user-images.githubusercontent.com/73643473/117188676-467d5880-ae18-11eb-96da-64ce72cced06.jpg)

---



### 9. Authentication Method

- NEXT

![mysql8](https://user-images.githubusercontent.com/73643473/117189607-5b0e2080-ae19-11eb-91ca-325832de44d7.jpg)

---



### 10. Accounts and Roles

- 비밀번호 설정 (잊어버리면 다시 설치)

![mysql14](https://user-images.githubusercontent.com/73643473/117190242-264e9900-ae1a-11eb-933c-019b921f9e38.jpg)

---



### 11.  Window Service (NEXT) 

![mysql9](https://user-images.githubusercontent.com/73643473/117189770-86910b00-ae19-11eb-9f5f-dfde21da3a1c.jpg)

---



### 12.  Apply Configuration (Execute) -> 6번 나옴 (NEXT)

- 다른 블로그에서 **컴퓨터 계정이 한글이 들어가면 문제가 생긴다고 다시 설치해야 할 수도...최악은 포맷도 해야한다고 합니다. 그전에 컴퓨터 계정 이름이 영어인지 확인하기....**

![mysql15](https://user-images.githubusercontent.com/73643473/117191134-32872600-ae1b-11eb-9154-ddddc1390809.jpg)

---



### 13. Router (FINISH)

![mysql10](https://user-images.githubusercontent.com/73643473/117189933-bb9d5d80-ae19-11eb-89d6-65a7babda15a.jpg)

---



### 14. Connect To Server

- 비밀번호 입력후 체크하면 녹색으로 바뀐다.

![mysql11](https://user-images.githubusercontent.com/73643473/117190038-dec80d00-ae19-11eb-8713-abafefa3de20.jpg)

---



### 15.  Apply Configuration (Execute)

![mysql12](https://user-images.githubusercontent.com/73643473/117190474-6ca3f800-ae1a-11eb-9650-29ed93bf0770.jpg)

---



### 16.  Installation Complete

- 끝.

![mysql13](https://user-images.githubusercontent.com/73643473/117191412-7e39cf80-ae1b-11eb-87a8-1846d152cb42.jpg)

---



### 17. 도움 블로그

- [[MySQL\] MySQL 설치하기 (feat. Workbench) (tistory.com)](https://ming-jee.tistory.com/19)



### 18. MariaDB가 있다면...

- MariaDB를 쓰고 있었는데 설치하면서 포트번호 덮어써서 MariaDB 데이터 다 날라갔다...
- MariaDB도 같이 쓰고 있다면 포트를 다르게 해서 설치하는게 좋을듯하다. (구글링으로 찾아보기)