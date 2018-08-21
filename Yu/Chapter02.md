# Chapter 02 변수
### 1. 다음 표의 빈 칸에 8개의 기본형(primitive type)을 알맞은 자리에 넣으시오.
| 종류\크기  | 1 byte  | 2 byte | 4 byte | 8 byte |
| :------------: | :---------------: | :-----: | :-----: | :-----: |
| 문자형 | boolean |  |  |  |
| 논리형 |  | char |  |  |
| 정수형 | byte | short | int | long |
| 실수형 |  |  | float | double |

### 2. 주민등록번호를 숫자로 저장하고자 한다. 이 값을 저장하기 위해서는 어떤 자료형 (data type)을 선택해야 할까? regNo라는 이름의 변수를 선언하고 자신의 주민등록번호로 초기화 하는 한 줄의 코드를 적으시오.

    long regNo = 9409070000000L; 
주민등록번호는 13자리로 int형 데이터가 표현할 수 있는 범위를 초과하므로 long 데이터로 선언한다.  

### 3. 다음의 문장에서 리터럴, 변수, 상수, 키워드를 적으시오.
    int i = 100;
    long l =100L;
    final float PI = 3.14f;

* 리터럴 : 100, 100L, 3.14f
* 변수 : i, l
* 키워드 : int, long, final, float
* 상수 : PI

### 4. 다음 중 기본형(primitive type)이 아닌 것은?
* a. int
* b. Byte
* c. double
* d. boolean

자바는 대문자와 소문자를 구분한다. 따라서 byte와 Byte는 다르다. 자바의 기본형은 boolean, byte, char, short, int, long, float, double 의 8개만 있으므로 b. Byte는 기본형이 아니다.

### 5. 다음 문장들의 출력결과를 적으세요. 오류가 있는 문장의 경우, 괄호 안에 ‘오류’라고 적으시오.
    System.out.println("1" + "2");
	System.out.println(true + "");
	System.out.println('A' + 'B');
	System.out.println('1' + 2);
	System.out.println('1' + '2');
	System.out.println('J' + “ava”);
	System.out.println(true + null);
1.  12
정수처럼 보이지만 문자열이므로 문자열의 +연산을 수행하여 12를 출력한다.
2. true
 문자열 ""가 있기 때문에 true를 문자열로 변환하여 true와 ""를 더해 true를 출력한다.
3. 131
작은따옴표로 표시한 'A'와 'B'는 문자열이 아닌 문자 데이터이다. 따라서 '+'연산자는 'A'와 'B'의 아스키코드 값인 65와 66을 더한다. 즉, 131이 출력된다.
4. 51
문자 1의 아스키코드 값 49와 리터럴 2의 값을 더해 51을 출력한다.
5. 99
문자 1의 아스키코드 값 49와 문자 2의 아스키코드 값 50을 더해 99를 출력한다.
6. Java
문자열이 있으므로 문자J를 문자열로 변환하여 문자열의 +연산을 수행한다. 따라서 Java가 출력된다.
7. 오류
null은 + 연산을 수행할 수 없다.

### 6. 다음 중 키워드가 아닌 것은?(모두 고르시오)
* a. if
* b. True
* c. NULL
* d. Class
* e. System

b, c, d, e는 키워드가 아니다. 자바는 대문자와 소문자를 구분한다. 자바의 모든 키워드는 소문자로 시작한다.

### 7. 다음 중 변수의 이름으로 사용할 수 있는 것은? (모두 고르시오)
* a. $ystem
* b. channel#5
* c. 7eleven
* d. If
* e. 자바
* f. new 
* g. $MAX_NUM
* h. hello@com

a, d, e, g
변수의 이름은 숫자로 시작할 수 없으며 특수문자는 '_'와 '$'만 허용한다. 예약어는 변수의 이름으로 사용할 수 없다.  

### 8. 참조형 변수(reference type)와 같은 크기의 기본형(primitive type)은? (모두 고르시오)
* a. int
* b. long
* c. short
* d. float
* e. double

a, d
참조형 변수는 4byte이다. a는 4byte, b는 8byte, c는 2byte, d는 4byte, e는 8byte이다.

### 9. 다음 중 형변환을 생략할 수 있는 것은? (모두 고르시오)
 	byte b = 10;
	 char ch = 'A';
	 int i = 100;
	 long l = 1000L;

* a. b = (byte)i;
* b. ch = (char)b;
* c. short s = (short)ch;
* d. float f = (float)l;
* e. i = (int)ch;

d,e
 a의 경우 4바이트를 1바이트 변수로 할당하기 때문에 형변환이 필요하다. 
 b의 경우 byte 변수인 b는 -2^7~2^7-1 범위를 표현하고 char변수인 ch는 0~2^16-1의 범위를 표현하기 때문에 byte로 표현가능한 범위를 char로 표현할 수 없어 형변환을 생략할 수 없다.
 c의 경우 s의 표현범위는 -2^15 ~ 2^15-1 이고 ch의 표현 범위는 0~2^16-1이기 때문에 형변환을 생략할 수 없다.

### 10. char타입의 변수에 저장될 수 있는 정수 값의 범위는? (10진수로 적으시오)

char은 2byte를 저장하는 데이터 타입으로 0부터 2^16-1의 범위를 표현한다. 따라서 범위는 0~65535 이다.

### 11. 다음중 변수를 잘못 초기화 한 것은? (모두 고르시오)
* a. byte b = 256;
* b. char c = '';
* c. char answer = 'no';
* d. float f = 3.14
* e. double d = 1.4e3f;

a,b,c,d
a : b의 범위를 초과함
b : 반드시 한 개의 문자를 할당해야함
c : 반드시 한 개의 문자를 할당해야함
d : 접미사f를 붙이지 않으면 double형
e : float보다 double이 범위가 크므로 형변환 없이 선언 가능

### 12. 다음 중 main메서드의 선언부로 알맞은 것은? (모두 고르시오)
* a. public static void main(String[] args)
* b. public static void main(String args[])
* c. public static void main(String[] arv)
* d. public void static main(String[] args)
* e. static public void main(String[] args)

a, b, c, e

### 13. 다음 중 타입과 기본값이 잘못 연결된 것은? (모두 고르시오)
* a. boolean - false
* b. char - '\u0000'
* c. float - 0.0
* d. int - 0
* e. long - 0
* f. String - ""

c, e, f

c : 0.0f
e : 0L or 0l
f : null (레퍼런스 변수)
