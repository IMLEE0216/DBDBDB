# MySQL 비밀번호 쳤는데 꺼짐 현상

## MySQL Client

- Client 실행 후 비번을 쳤는데 꺼졌다.

  <img src="https://user-images.githubusercontent.com/73643473/117991180-c6577580-b378-11eb-8163-175faec37035.jpg" alt="1_1_오류시작" style="zoom:50%;" />

- 시작 -> 컴퓨터 관리->  서비스 -> 서비스 안에 아무거나 찍고 'm'을 누르면 m으로 시작하는 프로그램으로 간다.

  - 시작

    <img src="https://user-images.githubusercontent.com/73643473/117990707-5ea12a80-b378-11eb-9779-ea2cbc498c4d.jpg" alt="1_0_컴퓨터 관리" style="zoom:50%;" />

  - 컴퓨터 관리 창

    <img src="https://user-images.githubusercontent.com/73643473/117990976-9a3bf480-b378-11eb-916a-75b489ea757c.jpg" alt="1_0_컴퓨터 관리창" style="zoom:50%;" />

    

- MySQL (version)이 있는데 누르고 시작하면 에러가 난다.

  <img src="https://user-images.githubusercontent.com/73643473/117991472-09b1e400-b379-11eb-8def-3b4c522203b3.jpg" alt="1_2_오류MySQL시작TRY" style="zoom:50%;" />

- MariaDB의 상태가 실행 중이다. 

  - MariaDB를 눌러 중지를 한다.

  <img src="https://user-images.githubusercontent.com/73643473/117991679-3e25a000-b379-11eb-9aeb-93d7b4964f9e.jpg" alt="1_3_mariaDB중지" style="zoom:50%;" />

- 중지를 하면 서비스 시작만 뜬다.

- MySQL로 가서 시작을 누른다.

- 실행을 하고 서비스 시작이 된다. (그래도 오류뜬다면 속성에으로 들어가서 시작해보기)

  ![1_4_mysql 시작](https://user-images.githubusercontent.com/73643473/117992604-0834eb80-b37a-11eb-92bc-33c02fdfd195.jpg)

- Client를 샐행 시킨다.

  ![1_5_client실행](https://user-images.githubusercontent.com/73643473/117993037-5813b280-b37a-11eb-8df1-607cb218bad0.jpg)