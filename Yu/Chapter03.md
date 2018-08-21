# Chapter 03 연산자
### 1.다음 연산의 결과를 적으시오.
/ch3/Exercise3_1.java

	class Exercise3_1 {
		public static void main(String[] args) {
			int x = 2;
			int y = 5;
			char c = 'A'; // 'A'의 문자코드는 65
			System.out.println(1 + x << 33);
			System.out.println(y >= 5 || x < 0 && x > 2);
			System.out.println(y += 10 - x++);
			System.out.println(x+=2);
			System.out.println( !('A' <= c && c <='Z') );
			System.out.println('C'-c);
			System.out.println('5'-'0');
			System.out.println(c+1);
			System.out.println(++c);
			System.out.println(c++);
			System.out.println(c);
		}
	}
<br>

	6 (?)
	true
	13
	false
	2
	5
	66
	B
	B
	C

### 2. 아래의 코드는 사과를 담는데 필요한 바구니(버켓)의 수를 구하는 코드이다. 만일 사과의 수가 123개이고 하나의 바구니에는 10개의 사과를 담을 수 있다면, 13개의 바구니가 필요할 것이다. (1)에 알맞은 코드를 넣으시오.

/ch3/Exercise3_2.java

	class Exercise3_2 {
		public static void main(String[] args) {
			int numOfApples = 123; // 사과의 개수
			int sizeOfBucket = 10; // 바구니의 크기(바구니에 담을 수 있는 사과의 개수)
			int numOfBucket = numOfApples/sizeOfBucket + (numOfApples%sizeOfBucket > 0 ? 1 : 0) ;
			System.out.println("필요한 바구니의 수 :"+numOfBucket);
		}
	}

실행결과

	13

### 3. 아래는 변수 num의 값에 따라 ‘양수’, ‘음수’, ‘0’을 출력하는 코드이다. 삼항 연산자를 이용해서 (1)에 알맞은 코드를 넣으시오. [Hint] 삼항 연산자를 두 번 사용하라.
/ch3/Exercise3_3.java

	class Exercise3_3 {
		public static void main(String[] args) {
			int num = 10;
			System.out.println( /* (1) */ );
		}
	}

