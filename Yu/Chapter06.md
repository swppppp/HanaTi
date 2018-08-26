# Chpter 06 객체지향 프로그래밍 1
#### 1. 다음과 같은 멤버변수를 갖는 SutdaCard 클래스를 정의하시오.

| 타입    | 변수명  | 설명                          |
| ------- | ------- | ----------------------------- |
| int     | num     | 카드의 숫자(1~10사이의 정수)  |
| boolean | isKwang | 광(光)이면 true, 아니면 false |

```java
public class SutdaCard {
    private int num;
    private boolean isKwang;
}
```



#### 2. 문제 6-1에서 정의한 SutdaCard클래스에 두 개의 생성자와 info()를 추가해서 실행 결과와 같은 결과를 얻도록 하시오.
```java
class Exercise6_2 {
    public static void main(String args[]) {
        SutdaCard card1 = new SutdaCard(3, false);
        SutdaCard card2 = new SutdaCard();
        System.out.println(card1.info());
        System.out.println(card2.info());
    }
}
public class SutdaCard {
    private int num;
    private boolean isKwang;
    
    public SutdaCard() {
        this(1, false);
    }
    public SutdaCard(int num, boolean isKwang) {
        this.num = num;
        this.isKwang = isKwang;
    }
    public info() {
        return num;
    }
    
}
```

실행결과

```
3
1K
```



#### 8. 다음의 코드에 정의된 변수들을 종류별로 구분해서 적으시오. 
```java
class PlayingCard {
    int kind;
    int num;
    static int width;
    static int height;
    PlayingCard(int k, int n) {
        kind = k;
        num = n;
    }
    public static void main(String args[]) {
    	PlayingCard card = new PlayingCard(1,1);
    }
}
```

- 클래스변수 : width, height
- 인스턴스변수 : kind, num
- 지역변수 : k, n, card, ***<u>args</u>***



#### 9. 다음은 컴퓨터 게임의 병사(marine)를 클래스로 정의한 것이다. 이 클래스의 멤버중에 static을 붙여야 하는 것은 어떤 것들이고 그 이유는 무엇인가? (단, 모든 병사의 공격력과 방어력은 같아야 한다.)
```java
class Marine {
    int x=0, y=0; // Marine의 위치좌표(x,y)
    int hp = 60; // 현재 체력
    int weapon = 6; // 공격력
    int armor = 0; // 방어력
    
    void weaponUp() {
    	weapon++;
    }
    void armorUp() {
   	 armor++;
    }
    void move(int x, int y) {
        this.x = x;
        this.y = y;
    }
}
```

weapon, armor : 모든 병사들의 공격력과 방어력이 같아야 하기 때문.

***<u>weaponUp(), armorUp() : static변수에 대한 작업을 하는 메서드</u>***



#### 11. 다음 중 this에 대한 설명으로 맞지 않은 것은? (모두 고르시오)

- a. 객체 자신을 가리키는 참조변수이다.
- b. 클래스 내에서라면 어디서든 사용할 수 있다.
- c. 지역변수와 인스턴스변수를 구별할 때 사용한다.
- d. 클래스 메서드 내에서는 사용할 수 없다.

b. 클래스 멤버(static이 붙은 변수나 메서드)에는 사용할 수 없다.



#### 12. 다음 중 오버로딩이 성립하기 위한 조건이 아닌 것은? (모두 고르시오)

- a. 메서드의 이름이 같아야 한다.
- b. 매개변수의 개수나 타입이 달라야 한다.
- c. 리턴타입이 달라야 한다.
- d. 매개변수의 이름이 달라야 한다.

c, d



#### 13. 다음 중 다음 중 아래의 add메서드를 올바르게 오버로딩 한 것은? (모두 고르시오)

```
long add(int a, int b) { return a+b;}
```

- a. long add(int x, int y) { return x+y;}
- b. long add(long a, long b) { return a+b;}
- c. int add(byte a, byte b) { return a+b;}
- d. int add(long a, int b) { return (int)(a+b);}

b, c, d

**<< 오버로딩의 조건 >>**

1. 메서드 이름이 같아야 한다.
2. 매개변수의 개수 또는 타입이 달라야 한다.
3. 매개변수는 같고 리턴타입이 다른 경우는 오버로딩이 성립되지 않는다.
    (리턴타입은 오버로딩을 구현하는데 아무런 영향을 주지 못한다.)



#### 14. 다음 중 초기화에 대한 설명으로 옳지 않은 것은? (모두 고르시오)

- a.멤버변수는 자동 초기화되므로 초기화하지 않고도 값을 참조할 수 있다.
- b.지역변수는 사용하기 전에 반드시 초기화해야 한다.
- c.초기화 블럭보다 생성자가 먼저 수행된다.
- d.명시적 초기화를 제일 우선적으로 고려해야 한다.
- e.클래스변수보다 인스턴스변수가 먼저 초기화된다.

c, e



#### 15. 다음 중 인스턴스변수의 초기화 순서가 올바른 것은?

- a. 기본값-명시적초기화-초기화블럭-생성자
- b. 기본값-명시적초기화-생성자-초기화블럭
- c. 기본값-초기화블럭-명시적초기화-생성자
- d. 기본값-초기화블럭-생성자-명시적초기화

***<u>a</u>***

**<<변수의 초기화 순서>>**
```
클래스변수의 초기화시점 : 클래스가 처음 로딩될 때 단 한번 초기화 된다.
인스턴스변수의 초기화시점 : 인스턴스가 생성될 때마다 각 인스턴스별로 초기화가 이루어진다.
클래스변수의 초기화순서 : 기본값 → 명시적초기화 → 클래스 초기화 블럭
인스턴스변수의 초기화순서 : 기본값 → 명시적초기화 → 인스턴스 초기화 블럭 → 생성자
```



#### 16. 다음 중 지역변수에 대한 설명으로 옳지 않은 것은? (모두 고르시오)

- a. 자동 초기화되므로 별도의 초기화가 필요없다.
- b. 지역변수가 선언된 메서드가 종료되면 지역변수도 함께 소멸된다.
- c. 매서드의 매개변수로 선언된 변수도 지역변수이다.
- d. 클래스변수나 인스턴스변수보다 메모리 부담이 적다.
- e. 힙(heap)영역에 생성되며 가비지 컬렉터에 의해 소멸된다.

***<u>a, e</u>***

a : 지역변수는 자동을 초기화되지 않는다.

e : heap영역은 인스턴스(인스턴스변수)가 생성되는 영역이며 지역변수는 호출스택(call stack)에 생성된다.



#### 17. 호출스택이 다음과 같은 상황일 때 옳지 않은 설명은? (모두 고르시오)

|         |
| ------- |
| println |
| method1 |
| method2 |
| main    |

- a.제일 먼저 호출스택에 저장된 것은 main메서드이다.
- b. println메서드를 제외한 나머지 메서드들은 모두 종료된 상태이다.
- c. method2메서드를 호출한 것은 main메서드이다.
- d. println메서드가 종료되면 method1메서드가 수행을 재개한다.
- e. main-method2-method1-println의 순서로 호출되었다.
- f. 현재 실행중인 메서드는 println 뿐이다.

b. 종료되면 스택에서 사라짐



#### 18. 다음의 코드를 컴파일하면 에러가 발생한다. 컴파일 에러가 발생하는 라인과 그 이유를 설명하시오.

``` java
class MemberCall {
    int iv = 10;
    static int cv = 20;
    int iv2 = cv;
    static int cv2 = iv; // 라인 A 
    
    static void staticMethod1() {
        System.out.println(cv);
        System.out.println(iv); // 라인 B 
    }
    void instanceMethod1() {
        System.out.println(cv);
        System.out.println(iv); // 라인 
    }
    static void staticMethod2() {
        staticMethod1();
        instanceMethod1(); // 라인 D 
    }
    void instanceMethod2() {
        staticMethod1(); // 라인 E
        instanceMethod1();
    }
}
```

- A : static 변수에 인스턴스 변수를 할당할 수 없다.
- B : static 메소드에서는 인스턴스 변수를 생성할 수 없다.
- D : static 메소드에서 인스턴스 메소드 실행 불가.



#### 19. 다음 코드의 실행 결과를 예측하여 적으시오.

``` java
class Exercise6_19
    {
    public static void change(String str) {
        str += "456";
    }
    public static void main(String[] args) {
        String str = "ABC123";
        System.out.println(str);
        change(str);
        System.out.println("After change:"+str);
    }
}
```

~~ABC123456~~ ===> **<u>*ABC123*</u>**

문자열은 내용을 변경할 수 없기 때문에 덧셈연산을 하면 새로운 문자열이 생성되고 새로운 문자열의 주소가 change 내부의 변수 str에 저장된다.



