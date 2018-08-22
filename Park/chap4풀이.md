# chap4. 조건문과 반복문  
## 연습문제  
### [4-1] 조건식으로 표현  
1. x>10 && x<20  
2. !(ch == '' || ch =='\t')  
3. ch == 'x' || ch == 'X'  
4. ch >= '0' && ch <='9'  
5. (ch >= 'a' && ch <= 'z')||(ch >= 'A' && ch <= 'Z')  
6. year%400==0 || year%4==0 && year%100!=0  
7. !powerOn  
8. str.equals("yes")    
### [4-2] 1~20정수 중 2 또는 3 배수 아닌 수 총합  
<pre><code>
  class Example4_2 {
    public static void main(String[] args){
      int sum = 0;
      for(int i=1; i<=20; i++){
        if(i%2!=0 && i%3!=0)
          sum+=i;
      }
      System.out.println(sum);
    }
   }  
   </code></pre>
### [4-3] 1+(1+2)+...(1+2+...+10)결과  
<pre><code>
class Example4_3 {
  public static void main(String[] args){
    int sum=0;
    int res=0;
    for(int i=1; i<=10; i++){
      sum+=i;
      res+=sum;
    }
    System.out.println(res);
   }
 }
</code></pre>  
### [4-4] 1+(-2)+3+(-4)+... 몇까지 해야 총합이 100이상일까  
_못품못품못품!!!!!!!!!!!!!!!!!!!!!_
<pre>못풀었어ㅠㅠ<code>
class Example4_4 {
  public static void main(String[] args){
    int sum=0;
    int num=0;
    for(int i=1; ){
      
    }
  }
}
</code></pre>
### [4-5] for문->while문으로 바꿔요  
<pre>변경 전
<code>
public class Exercise4_5 {
  public static void main(String[] args){
    for(int i=0; i<=10; i++){
      for(int j=0; j<=i; j++)
        System.out.print("*");
      System.out.println();
    }
  }
}
</code></pre>  
<pre>변경 후<code>
public class Exercise4_5 {
  public static void main(String[] args){
    int i=0;
    while(i<=10){
      int j=0;
      while(j<=i){
        System.out.print("*");
        j++;
      }
      System.out.println();
      i++;
    }
  }
}</code>
</pre>
### [4-6] 주사위 2개, 눈의 합 6되는 경우의 수 출력  
<pre><code>
public class Exercise4_6 {
  public static void main(String[] args){
    for(int i=1; i<=6; i++){
      for(int j=1; j<=6; j++){
        if(i+j == 6)
          System.out.println(i+"+"+j+"="+(i+j));
      }
    }
  }
}
</code></pre>  
### [4-7] Math.random()이용, 1~6사이의 임의의 정수를 value에 저장하는 코드 완성  
<pre>빈 칸에 들어갈 코드  이거 잘 모르겠음<code>

</code></pre>  
### [4-8] 2x + 4y = 10 구하시오(0<=x<=10, y도 같음, 둘다정수)  
<pre><code>
for(int x=0; x<=10; x++){
  for(int y=0; y<=10; y++){
    if(2*x+4*y==10)
      System.out.println("x="+x+", "+"y="+y);
  }
}
</code></pre>  
### [4-9] str은 숫자로 이루어진 문자열. 각 자리 합 더한 결과 출력  
<pre>빈 곳에 들어갈 코드<code>
sum+=str.charAt(i) - '0';
</code></pre>  
### [4-10] int num의 각 자리 합 더하는 결과 출력(숫자로만 처리)  
<pre>빈 곳에 들어갈 코드<code>
while(num!=0){
  sum += num%10;
  num/=10;
  }
</code></pre>  
### [4-11]피보나치. 1과 1부터 시작하는 수 10번째 피보나치 구하는 프로그램 완성해192.  
<pre>빈 곳에 들어갈 코드<code>
num3 = num1 + num2;
System.out.print(", "+num3);
num1 = num2;
num2 = num3;
</code></pre>  
### [4-12] 구구단 출력  
<pre>잘 모르겠다..ㅠㅠ<code>
//몰라몰라몰라!!!!!!!!
for(int i=1; i<=9; i++){
  for(int j=1; j<=3; j++){
    int x = j+1
  }
  System.out.println();
}
</code></pre>  
### [4-13] 주어진 문자열(value)이 숫자인지 판단. 빈곳 코드  
<pre>빈 곳에 들어갈 코드<code>
ch = value.charAt(i);
if(!(ch>='0'&&ch<='9')){
  isNumber = false;
  break;
}
</code></pre>  
### [4-14] 199 숫자맞추기 게임. 1~100 반복 입력 맞으면 게임끝. 몇번만에 맞췄나 출력  
<pre>빈 곳에 들어갈 코드<code>
(int)(Math.random()*100)+1  

if(answer == input){
  System.out.println("맞췄습니다.");
  System.out.println("시도횟수는 "+count+"번입니다.");
  break;
}else if(answer > intput){
  System.out.print("더 큰 수를 입력하세요 :");
}else if(answer < input){
  System.out.print("더 작은 수를 입력하세요 :");
}
</code></pre>  
### [4-15] 회문수(palindrome)..거꾸로 앞으로 읽어도 같은 수(대칭) hint. 나머지 연산자  
<pre>빈 곳에 들어갈 코드  헷갈려ㅠㅠ<code>
result = tmp%10 + result*10;
tmp/=10;
</code></pre>  





