# Chapter 03 ������
### 1.���� ������ ����� �����ÿ�.
/ch3/Exercise3_1.java

	class Exercise3_1 {
		public static void main(String[] args) {
			int x = 2;
			int y = 5;
			char c = 'A'; // 'A'�� �����ڵ�� 65
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

### 2. �Ʒ��� �ڵ�� ����� ��µ� �ʿ��� �ٱ���(����)�� ���� ���ϴ� �ڵ��̴�. ���� ����� ���� 123���̰� �ϳ��� �ٱ��Ͽ��� 10���� ����� ���� �� �ִٸ�, 13���� �ٱ��ϰ� �ʿ��� ���̴�. (1)�� �˸��� �ڵ带 �����ÿ�.

/ch3/Exercise3_2.java

	class Exercise3_2 {
		public static void main(String[] args) {
			int numOfApples = 123; // ����� ����
			int sizeOfBucket = 10; // �ٱ����� ũ��(�ٱ��Ͽ� ���� �� �ִ� ����� ����)
			int numOfBucket = numOfApples/sizeOfBucket + (numOfApples%sizeOfBucket > 0 ? 1 : 0) ;
			System.out.println("�ʿ��� �ٱ����� �� :"+numOfBucket);
		}
	}

������

	13

### 3. �Ʒ��� ���� num�� ���� ���� �������, ��������, ��0���� ����ϴ� �ڵ��̴�. ���� �����ڸ� �̿��ؼ� (1)�� �˸��� �ڵ带 �����ÿ�. [Hint] ���� �����ڸ� �� �� ����϶�.
/ch3/Exercise3_3.java

	class Exercise3_3 {
		public static void main(String[] args) {
			int num = 10;
			System.out.println( /* (1) */ );
		}
	}

