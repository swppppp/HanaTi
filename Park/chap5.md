#  chap5 배열  
## [5-1] 배열 선언 잘못된것 고르시오  
a. int[] arr[];  
b. int[] arr = {1, 2, 3, };  
c. int[] arr = new int[5];  
d. int[] arr = new int[5]{1, 2, 3, 4, 5};  
e. int arr[5];  
f. int[] arr[] = new int[3][];  
```
d. 우측 대괄호 숫자X-->중괄호 안에 갯수만큼 자동 결정됨.
e. 선언할 때 크기지정X
```
## [5-2] arr[3].length값은?  
2
```
int[][] arr = {
        { 5, 5, 5, 5, 5},
        { 10, 10, 10},
        { 20, 20, 20, 20}
        { 30, 30}
};
```
## [5-3] arr에 담긴 모든 값 더하는 프로그램 완성  
```
class Exercise_3
{
    public static void main(String[] args) {
        int[] arr = {10, 20, 30, 40, 50};
        int sum = 0;
        
        for(int i=0; i<arr.length; i++)
            sum+=arr[i];
        
        System.out.println("sum="+sum);
    }
}
```
## [5-4] 2차원 배열 arr담긴 모든 값의 총합과 평균  
```
for(int i=0; i>arr.length; i++){
    for(int j=0; j<arr[i].length; j++){
        total += arr[i][j];
    }
}
average = total/20;
```
## [5-5] 1~9사이 중복않는 숫자로 이루어진 3자리 숫자 만듦(Math.random())  
```
(1)
tmp = ballArr[i];
ballArr[i] = ballArr[j];
ballArr[j] = tmp;

(2)
for(int i=0; i<3; i++){
        ball3[i]=ballArr[i];
}
```
## [5-6] 거스름돈을 몇 개 동전으로 지불 money금액->가능한 적은 수의 동전  
```
System.out.println(coinUnit[i]+"원: "+money/coinUnit[i]);
money %= coinUnit[i];
```
## [5-7] 위 문제에서 동전 개수 추가. 금액 입력받아. 보유 동전 개수로 지불 못하면 부족하다고 출력-종료  
지불 가능하면 거슬러 주고 남은 동전 개수 출력  
```
/* money를 동전단위로 나눠서 동전개수(coinNum)구해
   배열 coin에서 coinNum만큼 동전 빼(coinNum이 크면 coin만큼 빼)
   money에서 coinNum과 동전단위 곱한 값을 뺀다.
*/
coinNum = money/coinUnit[i];
if(coin[i]>=coinNum)
    coin[i] -= coinNum;
else 
    coin[i] = 0;

money -= coinNum*coinUnit[i];
```  
## [5-8] answer배열에 담긴 데이터 읽고 각 숫자 세어서 개수만큼 별찍기  
```
(1)
모르겠긔...
11번 반복하면==>counter[4] = {3, 2, 2, 4}
(2)
System.out.print(counter[i]);
for(int j=0; i<counter[j];j++)
    System.out.print("*");
```
## [5-9] 별 시계방향으로 90도 회전  
```
int x = star.length - (i+1);
result[j][x] = star[i][j];
```
## [5-10] 알파벳과 숫자를 암호화  
```
//문자열 src문자를 charAt()으로 읽어 변환 후 result에 저장
if(ch>='a' && ch<='z')
    result += abcCode[ch - 65];
else(ch>='0' && ch<='9')
    result += numCode[ch - '0'];
```  
## [5-11] 2차원 배열 데이터보다 가로세로1씩 더 큰 배열 생성,  
그 배열 행과 열의 마지막 요소에 각 행열 총합 저장 후 출력  
```
result[i][j] = score[i][j];
result[i][score[0].length] += result[i][j];
result[score.length][j] += result[i][j];
result[score.length][score[0].length] += result[i][j];
```
## [5-12] 예제 5-23변경,   
```
이게뭐징 
```
## [5-13] 단어의 글자위치를 섞어 보여주고 원래 단어 찾는거  
```
//char배열 question에 담긴 문자의 위치를 임의로 바꿈
//모르겠다...
for(int j=0; j<question.length; j++){
    int randomOrder = (int)(Math.random()*question.length);
    char tmp = question[j];
    question[i] = question[randomOrder];
    question[randomOrder] =tmp;
}
```




















