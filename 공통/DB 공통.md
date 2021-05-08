# DB 공통

### 1. 데이터 타입

- 다른 타입도 더 있는데 아래를 더 많이 쓰는 듯

![데이터타입](https://user-images.githubusercontent.com/73643473/117341471-1cda3500-aedd-11eb-8c44-a98b9f2879ef.jpg)



### 2. Char VS. Varchar VS. Text

##### CHAR

- 고정길이 문자열을 저장
- 최대길이 255바이트
- 검색 능력은 varchar보다 빠르지만 빈공간도 데이터 차지해서 용량이 커진다.
- 크기보다 작은 문자열 저장시 나머지는 공백으로 채워진다.
- INSERT 저장하는 문자열 길이가 같으면 CHAR 타입을 쓰는게 좋다.
  - 주민등록번호
- CHAR(50) 이면 -> "12345"를 넣었을때 "12345_______________________________" <- 이렇게 저장된다.



##### VARCHAR

- 가변길이 문자열을 저장
- 최대길이 255바이트(255이상도 가능할걸로 알고 있는데...됩니다.(데이터 들어가는 것도 확인))
- INSERT 저장하는 문자열 길이가 랜덤이라면 VARCHAR 타입을 쓰는게 좋다.
  - 주소, 이름, 학교 등등

```txt
예) abc -> char(50)형 : 50byte vs. varchar(50) 형 : 4byte
```



##### TEXT

- 너무너무 긴 문자열은 TEXT 형식으로 바꿔 저장 가능하다.
  - 논설문, 긴 글 등등



### 3. (n)?

- byte 형식으로 알고 있으면 된다. (머리로만)
- int (11), varchar(50) 등 테이블 생성할때 (n) 숫자를 넣어서 만듬

##### INT(n)

- INT(5),(11)해도 -> 10으로 들어간다...(HeidiSQL 프로그램하면서 알았다.)

- INT 사실 2^31 OR 2^32 값이다. (-2,147,483,648 ~ +2,147,483,647)까지 쓸 일 없을거 같은데..

![INT길이](https://user-images.githubusercontent.com/73643473/117408145-762c7d80-af4a-11eb-9834-dc41d7e93f31.jpg)

##### VARCHAR(n)

- (50)은 50byte까지 넣을수 있다.(영문기준 50자, 한글은 2~3byte이므로 반만 채울수 있다는데) 
- mysql 5.0 이상은 utf8로 되어있다면 한영 상관없이 varchar(250) -> 250자 라고 합니다.
- VARCHAR 간단하게 (n)은 길이라고 생각하면 될 듯하다....

![(n)오류](https://user-images.githubusercontent.com/73643473/117405552-c7d30900-af46-11eb-8a97-992f10cb4ced.png)



### 4. ZEROFILL & UNSIGNED

##### Zerofill

- INT에서  나머지칸을 0으로 채운다
- id   INT(5) UNSIGNED **ZEROFILL**로 선언하면 1을 입력했을때 -> 00001이 저장된다.

##### Unsiged

- INT 기본 설정 값은 Singed -> (-n ~ +n) 이다.

- INT(11) **UNSIGNED**로 설정하면 (0~4,294,967,295)까지 쓸 수 있다. 



