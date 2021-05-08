# MySQL 실행하기(Client)

### 1. Client 로 실해하기

- 설치 잘 했으면 시작프로그램에 MySQL 이라치면 Client 나온다 cmd 창 같은거 눌러서 실행
- 비밀번호 입력 하면 아래처럼 나온다.

![실행1](https://user-images.githubusercontent.com/73643473/117294012-19c75080-aead-11eb-8ec3-a2909b6a1b1b.jpg)

##### 1-1) 현재 유저 확인하기

- **SELECT user();**

![1_2_유저확인](https://user-images.githubusercontent.com/73643473/117313188-a0d1f400-aec0-11eb-852d-e23c8b7050c3.jpg)





### 2. Database

##### 2-1) Database 만들기

- **CREATE DATABASE ** + Database Name;

![2_database만들기](https://user-images.githubusercontent.com/73643473/117296856-7d9f4880-aeb0-11eb-931c-7dc6d86699a9.jpg)



##### 2-2) Database 조회하기

- **SHOW DATABASES;** -> 생성되어 있는 database를 조회한다.  (-s 꼭 붙이기)

  ![2_2_database조회하기](https://user-images.githubusercontent.com/73643473/117299276-4f6f3800-aeb3-11eb-93aa-4f3900cd2fd9.jpg)

- 다른 Database 들은 MySQL 설치하면서 자동으로 생성되는 Database



##### 2-3) Database 삭제하기

- **DROP DATABASE** + Database Name;
- Database를 삭제하면 내장되어 있던 Table, 데이터 등등 전부 삭제가 된다.

![2_3_database삭제하기](https://user-images.githubusercontent.com/73643473/117300617-b4775d80-aeb4-11eb-99a6-2d75631486dd.jpg)



##### 2-4) Database 사용하기

- **USE** + Database Name;

- 사용하고자하는 데이터 베이스를 선택한다.
- MariaDB는 mysql>  ->  test> 이렇게 변경되는데....MySQL은 mysql> -> mysql> 변경 없음

![2_4_database사용하기](https://user-images.githubusercontent.com/73643473/117302450-9a3e7f00-aeb6-11eb-9ed9-7fe382d8de59.jpg)



##### 2-5) 현재 사용중인 Database 확인하기 

- **SELECT DATABASE();**

![2_5_database확인하기](https://user-images.githubusercontent.com/73643473/117313251-afb8a680-aec0-11eb-9864-0c4447ba9f8e.jpg)



### 3. Table

##### 3-1) Table 생성하기

```sql
CREATE table Table-name (
	field type,
    field type
);
```

예시)

```sql
CREATE table member (
	no int(11) NOT NULL,
    name varchar(20) DEFAULT NULL,
    tel varchar(20) DEFAULT NULL,
    address varchar(80) DEFAULT NULL,
    type varchar(20) DEFAULT NULL,
    PRIMARY KEY(no)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

```sql
'member' 라는 table을 만들거다.
'member' table 안에 field 'no', 'name', 'tel', 등을 추가할거다.
'no'의 type은 int이며 범위(길이)는 (11)이다 추가적 조건으로 NOT NULL을 추가하였다.
'name'의 tpye은 varchar이며 범위(길이)는 (20) DEFAULT NULL을 추가하였다.
 ('no')를 PRIMARY KEY로 하였다. 
 (11), (20) -> DB 공통.md에 작성
```

###### 얕은지식) ENGINE=InnoDB DEFAULT CHARSET=utf8;

- engine = InnoDB ->  저장형식으로 참조키나 프로시저 등의 고급기능 사용가능.
- default charset = utf8 -> 기본 문자열 저장형식을 UTF8로 설정



##### 3-2) Table 보기

- **SHOW TABLES;**  
- 사용중인 Database가 가지고 있는 table들을 보여준다.









###### 저장 경로 확인하기

**show variables like 'datadir';** 