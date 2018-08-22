# Chapter 04 조건문과 반복문
### 1. 다음의 문장들을 조건식으로 표현하라.

1. int형 변수 x가 10보다 크고 20보다 작을 때 true인 조건식  
(x > 10) && (x < 20)
2. char형 변수 ch가 공백이나 탭이 아닐 때 true인 조건식  
(ch != ' ') && (ch != '\t')
3. char형 변수 ch가 ‘x' 또는 ’X'일 때 true인 조건식  
(ch == 'x') || (ch == 'X')
4. char형 변수 ch가 숫자(‘0’~‘9’)일 때 true인 조건식  
(ch >= 48) && (ch <= 57)
5. char형 변수 ch가 영문자(대문자 또는 소문자)일 때 true인 조건식  
(ch >= 65) && (ch <= 122)
6. int형 변수 year가 400으로 나눠떨어지거나 또는 4로 나눠떨어지고 100으로 나눠떨어지지 않을 때 true인 조건식  
(year % 400 == 0) || ( year % 4 == 0 ) && (year % 100 != 0)
7. boolean형 변수 powerOn가 false일 때 true인 조건식  
!powerOn
8. 문자열 참조변수 str이 “yes”일 때 true인 조건식  
str.equals("yes");  

### 2. 1부터 20까지의 정수 중에서 2 또는 3의 배수가 아닌 수의 총합을 구하시오.
출력 : 73  

   	public static void main (String[] args) {
		int sum = 0;
		for(int i = 1; i <= 20; i++) {
			if( (i % 2 != 0) && (i % 3 != 0))
				sum += i;
		}
		System.out.println(sum);
	}
 
### 3. 1+(1+2)+(1+2+3)+(1+2+3+4)+...+(1+2+3+...+10)의 결과를 계산하시오.
출력 : 220

	public static void main (String[] args) {
		int sum = 0;
		for( int i = 1; i <= 10; i++) {
			for(int j = 1; j <= i; j++) {
				sum += j;
			}
		}
		System.out.println(sum);
	}
  
### 4. 1+(-2)+3+(-4)+... 과 같은 식으로 계속 더해나갔을 때, 몇까지 더해야 총합이 100이상이 되는지 구하시오.
출력 : 199  

	public static void main (String[] args) 	{
		int sum = 0;
		int i = 1;
		while(true) {
			if (i % 2 == 1) sum += i;
			else sum -= i;
			if (sum >= 100) break;
			i++;
		}
		System.out.println(i);
	}
for문을 이용해 간단히 표현하면  

    for(int i=1; sum < 100; i++, s=-s) {
      num = i * s;
      sum += num;
    }

### 5. 다음의 for문을 while문으로 변경하시오.
주어진 코드  

    public class Exercise4_5 {
      public static void main(String[] args) {
        for(int i=0; i<=10; i++) {
          for(int j=0; j<=i; j++)
            System.out.print("*");
          System.out.println();
        }
      } // end of main
    } // end of class

while문으로 변경한 코드

    public class Exercise4_5 {
      public static void main(String[] args) {
        int i = 0;
        while(i <= 10) {
          int j = 0;
          while(j <= i) {
            System.out.print("*");
            j++;
          }
          System.out.println();
          i++;
        }
      } // end of main
    } // end of class
    
### 6. 두 개의 주사위를 던졌을 때, 눈의 합이 6이 되는 모든 경우의 수를 출력하는 프로그램을 작성하시오.
출력  

주사위 값 : 1, 5  
주사위 값 : 2, 4  
주사위 값 : 3, 3  
주사위 값 : 4, 2  
주사위 값 : 5, 1     

코드    

    public static void main (String[] args) 	{
      for(int i = 1; i <= 6; i++) {
        for(int j = 1; j <= 6; j++) {
          if((i + j) == 6) System.out.println("주사위 값 : " + i + ", " + j);
        }
      } 
    }
    
### 7. Math.random()을 이용해서 1부터 6사이의 임의의 정수를 변수 value에 저장하는 코드를 완성하라. (1)에 알맞은 코드를 넣으시오.

    class Exercise4_7 {
      public static void main(String[] args) {
        int value = (int) (Math.random() * 6) + 1;  
        System.out.println("value:"+value);
      }
    }
    
Math.random() 메소드는 0.0 이상에서 1.0 미만의 double형 실수 값을 반환한다. 

### 8. 방정식 2x+4y=10의 모든 해를 구하시오. 단, x와 y는 정수이고 각각의 범위는 0<=x<=10, 0<=y<=10 이다.

    public static void main (String[] args) {
      for(int x = 0; x <= 10; x++) {
        for(int y = 0; y <= 10; y++) {
          if(2*x + 4*y == 10) System.out.println("x = " + x + ", y = " + y);
        }
      }
    }
    
    
### 9. 숫자로 이루어진 문자열 str이 있을 때, 각 자리의 합을 더한 결과를 출력하는 코드를 완성하라. 만일 문자열이 "12345"라면, ‘1+2+3+4+5’의 결과인 15를 출력이 출력되어야 한다. (1)에 알맞은 코드를 넣으시오.

    class Exercise4_9 {
      public static void main(String[] args) {
        String str = "12345";
        int sum = 0;
        for(int i=0; i < str.length(); i++) {
          sum += (int)str.charAt(i) - 48;
        }
        System.out.println("sum="+sum);
      }
    }
    
### 10. int타입의 변수 num 이 있을 때, 각 자리의 합을 더한 결과를 출력하는 코드를 완성하라. 만일 변수 num의 값이 12345라면, ‘1+2+3+4+5’의 결과인 15를 출력하라. (1) 에 알맞은 코드를 넣으시오. [주의] 문자열로 변환하지 말고 숫자로만 처리해야 한다.

    class Exercise4_10 {
      public static void main(String[] args) {
        int num = 12345;
        int sum = 0;
        //추가된부분
        String numString = num + "";
        for(int i = 0; i < numString.length(); i++) {
        	sum += (int)numString.charAt(i) - 48;
        }
        //
        System.out.println("sum="+sum);
      }
    }
    
### 11. 피보나치(Fibonnaci) 수열(數列)은 앞을 두 수를 더해서 다음 수를 만들어 나가는 수열이다. 예를 들어 앞의 두 수가 1과 1이라면 그 다음 수는 2가 되고 그 다음 수는 1과 2를 더해서 3이 되어서 1,1,2,3,5,8,13,21,... 과 같은 식으로 진행된다. 1과 1부터 시작하는 피보나치수열의 10번째 수는 무엇인지 계산하는 프로그램을 완성하시오.

    public class Exercise4_11 {
      public static void main(String[] args) {
        // Fibonnaci 수열의 시작의 첫 두 숫자를 1, 1로 한다.
        int num1 = 1;
        int num2 = 1;
        int num3 = 0; // 세번째 값
        System.out.print(num1+","+num2);
        for (int i = 0 ; i < 8 ; i++ ) {
          //추가된 코드
          num3 = num1 + num2;
          System.out.print("," + num3);
          num1 = num2;
          num2 = num3;
          //
        }
      } // end of main
    } // end of class

### 12. 구구단의 일부분을 다음과 같이 출력하시오.
[실행결과]  
2\*1=2 3\*1=3 4\*1=4  
2\*2=4 3\*2=6 4\*2=8  
2\*3=6 3\*3=9 4\*3=12  

5\*1=5 6\*1=6 7\*1=7   
5\*2=10 6\*2=12 7\*2=14  
5\*3=15 6\*3=18 7\*3=21      

8\*1=8 9\*1=9  
8\*2=16 9\*2=18  
8\*3=24 9\*3=27  

    public class Exercise4_11 {
      public static void main(String[] args) {
        // Fibonnaci 수열의 시작의 첫 두 숫자를 1, 1로 한다.
        int num1 = 1;
        int num2 = 1;
        int num3 = 0; // 세번째 값
        System.out.print(num1+","+num2);
        for (int i = 0 ; i < 8 ; i++ ) {
          //추가된 코드
          num3 = num1 + num2;
          System.out.print("," + num3);
          num1 = num2;
          num2 = num3;
          //
        }
      } // end of main
    } // end of class

Math.random() 메소드는 0.0 이상에서 1.0 미만의 double형 실수 값을 반환한다. 
