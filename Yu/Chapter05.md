# Chpter 05 배열
#### 1. 다음은 배열을 선언하거나 초기화한 것이다. 잘못된 것을 고르고 그 이유를 설명하시오.
a. int[] arr[];  
b. int[] arr = {1,2,3,};  
c. int[] arr = new int[5];  
d. int[] arr = new int[5]{1,2,3,4,5};  
e. int arr[5];  
f. int[] arr[] = new int[3][];  

~~b. {1, 2, 3}; 으로 고치기~~ ----> 뒤에 있는 표는 상관 없음  
d. [5] 제거  
e. 선언시 크기 지정x  
~~f. 크기~~ ---->1차 배열의 크기만 지정해도 된다.  



#### 2. 다음과 같은 배열이 있을 때, arr[3].length의 값은 얼마인가?

```java
int[][] arr = {
  { 5, 5, 5, 5, 5},
  { 10, 10, 10},
  { 20, 20, 20, 20},
  { 30, 30}
};
```

2



#### 3. 배열 arr에 담긴 모든 값을 더하는 프로그램을 완성하시오.
```java
class Exercise5_3
{
  public static void main(String[] args)
    {
    int[] arr = {10, 20, 30, 40, 50};
    int sum = 0;
    //****************추가한코드*********************
    for(int i=0;i<arr.length;i++) {
      sum += arr[i];
    }
    //*********************************************
    System.out.println("sum="+sum);
  }
}
```



#### 4. 2차원 배열 arr에 담긴 모든 값의 총합과 평균을 구하는 프로그램을 완성하시오.

```java
class Exercise5_4
{
  public static void main(String[] args)
  {
    int[][] arr = {
      { 5, 5, 5, 5, 5},
      {10,10,10,10,10},
      {20,20,20,20,20},
      {30,30,30,30,30}
    };
    int total = 0;
    float average = 0;
    //****************추가한코드*********************
    int length = 0;
    	for (int i = 0; i < arr.length; i++) {
		    for(int j = 0; j < arr[i].length; j++) {
			    length++;
			    total += arr[i][j];
		    }
      }
	    average = (float)total / (float)length;
    //**********************************************
    System.out.println("total="+total);
    System.out.println("average="+average);
  } // end of main
} // end of class
```



#### 5. 다음은 1과 9사이의 중복되지 않은 숫자로 이루어진 3자리 숫자를 만들어내는 프로그램이다. (1)~(2)에 알맞은 코드를 넣어서 프로그램을 완성하시오. [참고] Math.random()을 사용했기 때문에 실행결과와 다를 수 있다.

```java
class Exercise5_5 {
  public static void main(String[] args) {
    int[] ballArr = {1,2,3,4,5,6,7,8,9};
    int[] ball3 = new int[3];
    // 배열 ballArr의 임의의 요소를 골라서 위치를 바꾼다.
    for(int i=0; i< ballArr.length;i++) {
      int j = (int)(Math.random() * ballArr.length);
      int tmp = 0;
      /*
      (1) 알맞은 코드를 넣어 완성하시오.
    */ }
    // 배열 ballArr의 앞에서 3개의 수를 배열 ball3로 복사한다.
    /* (2) */
    for(int i=0;i<ball3.length;i++) {
      System.out.print(ball3[i]);
    }
  } // end of main
} // end of class
```


??? 문제가 이해가 잘..... ballArr 배열은 왜필요한거??  



#### 6. 다음은 거스름돈을 몇 개의 동전으로 지불할 수 있는지를 계산하는 문제이다. 변수 money의 금액을 동전으로 바꾸었을 때 각각 몇 개의 동전이 필요한지 계산해서 출력하라. 단, 가능한 한 적은 수의 동전으로 거슬러 주어야한다. (1)에 알맞은 코드를 넣어서 프로그램을 완성하시오. [Hint] 나눗셈 연산자와 나머지 연산자를 사용해야 한다.

```java
class Exercise5_6 {
  public static void main(String args[]) {

	// 큰 금액의 동전을 우선적으로 거슬러 줘야한다.
    int[] coinUnit = { 500, 100, 50, 10 };
    int money = 2680;
    System.out.println("money=" + money);
    for (int i = 0; i < coinUnit.length; i++) {
        //*****************추가된코드********************
      	System.out.println(coinUnit[i] + "원 : " + money / coinUnit[i]);
      	money = money % coinUnit[i];
      	//**********************************************
    }
  } // main
}
```



#### 7. 문제 5-6에 동전의 개수를 추가한 프로그램이다. 커맨드라인으로부터 거슬러 줄 금액을 입력받아 계산한다. 보유한 동전의 개수로 거스름돈을 지불할 수 없으면, ‘거스름돈이 부족합니다.’라고 출력하고 종료한다. 지불할 돈이 충분히 있으면, 거스름돈을 지불한 만큼 가진 돈에서 빼고 남은 동전의 개수를 화면에 출력한다. (1)에 알맞은 코드를 넣어서 프로그램을 완성하시오.

```java
 /**
 * 커맨드라인으로부터 거슬러 줄 금액을 입력받아 계산한다. 
 * 보유한 동전의 개수로 거스름돈을 지불할 수 없으면, 
 * ‘거스름 돈이 부족합니다.’라고 * 출력하고 종료한다.
 *  지불할 돈이 충분히 있으면, 
 *  거스름돈을 지불한 만큼 가진 돈에서 빼고 남은 동전의 개수를 화면에 출력한다. 
 * 
 * @author uyk
 *
 */
class Exercise5_7 {
	public static void main(String args[]) {
		if (args.length != 1) {
			System.out.println("USAGE: java Exercise5_7 3120");
			System.exit(0);
		}
// 문자열을 숫자로 변환한다. 입력한 값이 숫자가 아닐 경우 예외가 발생한다.
		int money = Integer.parseInt(args[0]);
		System.out.println("money=" + money);
		int[] coinUnit = { 500, 100, 50, 10 }; // 동전의 단위
		int[] coin = { 5, 5, 5, 5 }; // 단위별 동전의 개수
		for (int i = 0; i < coinUnit.length; i++) {
			int coinNum = 0;
			/*
			 * (1) 아래의 로직에 맞게 코드를 작성하시오. 
			 * 1. 금액(money)을 동전단위로 나눠서 
			 * 필요한 동전의 개수(coinNum)를 구한다.
			 * 2. 배열 coin에서 coinNum만큼의 동전을 뺀다. 
			 * (만일 충분한 동전이 없다면 배열 coin에 있는 만큼만 뺀다.) 
			 * 3. 금액에서 동전의 개수(coinNum)와 동전단위를 곱한 값을 뺀다.
			 */
			//필요한 동전의 개수
			coinNum = money / coinUnit[i];	
			//사용한 동전의 개수만큼 배열에서 제거
			if(coin[i] >= coinNum) coin[i] -= coinNum;		
			else {
				//coin 부족하면 있는 개수만큼을 coinNum에 대입
				coinNum = coin[i];	
				coin[i] = 0;	
			}
			money -= coinNum * coinUnit[i];
			System.out.println(coinUnit[i] + "원: " + coinNum);
		}
		if (money > 0) {
			System.out.println("거스름돈이 부족합니다.");
			System.exit(0); // 프로그램을 종료한다.
		}
		System.out.println("=남은 동전의 개수 =");
		for (int i = 0; i < coinUnit.length; i++) {
			System.out.println(coinUnit[i] + "원:" + coin[i]);
		}
	} // main
}
```



#### 9. 주어진 배열을 시계방향으로 90도 회전시켜서 출력하는 프로그램을 완성하시오.

```java
/**
 * 주어진 배열을 시계방향으로 90도 회전시켜서 출력하는 프로그램을 완성하시오.
 * 
 * @author uyk
 *
 */
public class Exercise5_9 {
    public static void main(String[] args) {
        char[][] star = {
                { '*', '*', ' ', ' ', ' ' }, 
                { '*', '*', ' ', ' ', ' ' }, 
                { '*', '*', '*', '*', '*' },
                { '*', '*', '*', '*', '*' } };
        char[][] result = new char[star[0].length][star.length];

        // star 출력
        for (int i = 0; i < star.length; i++) {
            for (int j = 0; j < star[i].length; j++) {
                System.out.print(star[i][j]);
            }
            System.out.println();
        }
        System.out.println();

        // 연산하여 result에 저장
        for (int i = 0; i < star.length; i++) {
            for (int j = 0; j < star[i].length; j++) {
                //******************추가된코드********************
                result[j][Math.abs(i-3)] = star[i][j];
                //**********************************************
            }
        }

        // result 출력
        for (int i = 0; i < result.length; i++) {
            for (int j = 0; j < result[i].length; j++) {
                System.out.print(result[i][j]);
            }
            System.out.println();
        }
    } // end of main
}
```



#### 11. 주어진 2차원 배열의 데이터보다 가로와 세로로 1이 더 큰 배열을 생성해서 배열의 행과 열의 마지막 요소에 각 열과 행의 총합을 저장하고 출력하는 프로그램이다. (1)에 알맞은 코드를 넣어서 완성하시오.

```java
/**
 * 주어진 2차원 배열의 데이터보다 가로와 세로로 1이 더 큰 배열을 생성해서
 * 배열의 행과 열의 마지막 요소에 각 열과 행의 총합을 저장하고 출력하는 프로그램이다. 
 *
 * @author uyk
 */
public class Exercise5_11 {
    public static void main(String[] args) {
        int[][] score = { 
                { 100, 100, 100 }, 
                { 20, 20, 20 }, 
                { 30, 30, 30 },
                { 40, 40, 40 }, 
                { 50, 50, 50 } };
        // 행과 열이 각 1씩 큰 배열 result 생성
        int[][] result = new int[score.length + 1][score[0].length + 1];

        for (int i = 0; i < score.length; i++) {
            for (int j = 0; j < score[i].length; j++) {
                //******************추가된코드********************
                // result에 score의 값 복사 
                result[i][j] = score[i][j];
                // 마지막 행에 합 추가
                result[score.length][j] += score[i][j];
                // 마지막 열에 합 추가
                result[i][score[i].length] += score[i][j];
                // 행과 열의 총 합
                result[score.length][score[i].length] += score[i][j];
                //**********************************************
            }
        }
        for (int i = 0; i < result.length; i++) {
            for (int j = 0; j < result[i].length; j++) {
                System.out.printf("%4d", result[i][j]);
            }
            System.out.println();
        }
    } // main
}
```


#### 13. 단어의 글자위치를 섞어서 보여주고 원래의 단어를 맞추는 예제이다. 실행결과와 같이 동작하도록 예제의 빈 곳을 채우시오.

```java
import java.util.Scanner;

/**
 * 단어의 글자위치를 섞어서 보여주고 원래의 단어를 맞추는 예제이다. 
 * @author uyk
 *
 */
public class Exercise5_13 {
    public static void main(String args[]) {
        String[] words = { "television", "computer", "mouse", "phone" };

        Scanner scanner = new Scanner(System.in);

        for (int i = 0; i < words.length; i++) {
            char[] question = words[i].toCharArray(); // String을 char[]로 변환

            //******************추가된코드********************
            // 바뀐 문자열을 저장할 배열
            char[] newWord = new char[words[i].length()];
            for(int j = 0; j < question.length; j++) {
                // 임의의 숫자를 저장할 변수 index
                int index;
                // index의 위치에 다른 문자가 들어있으면 계속 난수 발생
                do {
                    // 0 ~ (마지막 char의 인덱스) 사이의 난수를 index에 저장
                    index = (int)(Math.random() * question.length);
                } while(newWord[index] != '\u0000');
                // 난수 인덱스 위치에 문자 저장
                newWord[index] = question[j];
            }
            // 바꾼 문자열을 기존의 문자열에 대입
            question = newWord;
            //**********************************************

            // 문자열을 입력받아 answer에 저장
            System.out.printf("Q%d. %s의 정답을 입력하세요.>", i + 1, new String(question));
            String answer = scanner.nextLine();

            // trim()으로 answer의 좌우 공백을 제거한 후, equals로 word[i]와 비교
            if (words[i].equals(answer.trim()))
                System.out.printf("맞았습니다.%n%n");
            else
                System.out.printf("틀렸습니다.%n%n");
        }
    } // main의 끝
}
```
