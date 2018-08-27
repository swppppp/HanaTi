# oop1

[6-1]

```
public class SutdaCard{
    public int num;
    public boolean isKwang;
}
```

[6-2]

```
public SutdaCard(){
    this.num = 1;
    this.isKwang = true;
}
public SutdaCard(int num, boolean kwang){
    this.num = num;
    this.isKwang = kwang;
}

public void info(){
    if(this.isKwang){
        System.out.println(this.num + "K");
    } else{
        sysout.out.println(this.num);
    }
}

```

[6-3]

```
public class Student{
    private String nmae;
    private int ban;
    private int no;
    private int kor;
    private int eng;
    private int math;
}
```

[6-4]

```
public int getTotal(){
    return this.kor + this.eng + this.math;
}

public float getAverage(){
    return Math.round(((getTotal()/3) * 10)) / 10.0;
}
```

[6-5]

```
public void info(){
	System.out.println(this.name+","+this.ban+","+this.no+","+","+this.kor+","+this.eng+","+this.math+","+this.getTotal()+","+this.getAverage());
}
```

[6-6]

```
return Math.sqrt(Math.pow((x-x1),2) + Math.pow((y-y1),2));
```

[6-7]

```
public double getDistance(int x, int y){
    return Math.sqrt(Math.pow((this.x-x1),2) + Math.pow((this.y-y),2));
}
```

[6-8]

> 클래스변수:  width, height
>
> 인스턴스변수: kind, num
>
> 지역변수(매개변수): card

[6-9]

> static int weapon
>
> static int armor
>
> 모든 병사의 공격력과 방어력은 같아야 하므로 객체 데이터가 공유되어야 하기 때문이다.

[6-10]

> b.(생성자는 객체를 생성할 때 사용되기는 하지만 객체를 초기화할 목적으로 사용되는 것)
>
> e(매개변수를 달리해서 오버로딩 가능)

[6-11]

> b (클래스 메서드 내에서는 사용할 수 없음) -> 클래스 메서드에서는 인스턴스 변수를 참조할 수 없다.
>
> c 틀린이유-> 매개변수라 생각했지만 매개변수도 지역변수이다.
>
>

[6-12]

> c, d 
>
> 오버로딩 조건
>
> > 메서드 이름이 같아야 한다.
> >
> > 매개변수 개수나 타입이 달라야 한다.

[6-13]

> b,c,d
>
> 완전 실수

[6-14] * 헷갈림

> c,e
>
> 초기화 블럭은 
>
> {
>
> 	//code
>
> }
>
> static{
>
> 	//code
>
> }
>
> 이렇게 생긴 놈, 생성자보다 먼저 수행됨

[6-15] * 

> d
>
> 기본값-> 초기화블록 -> 생성자-> 명시적초기화 (틀림)
>
> 기본값->명시적초기화-> 초기화블록-> 생성자
>
> 왠지 명시적 초기화 이거일듯
>
> class AAA(){
>
> 	int x = 0;
>
> }
>
>

[6-16]

> a, c, e
>
> e(지역변수는 stack영역에 생성)

[6-17] *

> b 

[6-18]

> 라인 b -> 클래스메서드 내에서는 클래스 변수만 접근이 가능하다. (인스턴스 변수 접근 불가)

[6-19]

> ABC123
>
> After change: ABC123456(틀림)
>
> after change: ABC123
>
> 왜 안바뀌냐면 String 클래스 특성에서 한번 생성된 인스턴스는 변경될 수 없다라는 조건에서
>
> 바뀌지 않는다.  덧셈연산을 하게 되면 새로운 문자열이 생성되고 새로운 문자열의 주소가 ABC123456을 참조하게 된다.

[6-20]

```
for(int i = 0; i < arr.length; i++){
    int j = (int)(Math.random()*arr.length);
    
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
}
```

[6-21]

```
1. 
if(isPowerOn) isPowerOn = false;
else isPowerOn = true;

2.
if(volume < MAX_VOLUME) volume++;

3.
if(volume > MIN_VOLUME) volume--;

4.
channel++;
if(channel == MAX_CHANNEL) channel = MIN_CHANNEL;

5.
channel--;
if(channel == MIN_CHANNEL) channel = MAX_CHANNEL;

```

[6-22]

```
public static boolean(String str){
	try{
        Integer.parseInt(str);
        return true;
	} catch(Exception e){
        return false;
	}
}
```

>원하는 답

```
	public static boolean anotherInt(String str){
		for(int i = 0; i < str.length(); i++){
			System.out.println((int)str.charAt(i));
			if(str.charAt(i) < 48 || str.charAt(i) > 57) return false;
		}
		return true;
	}
```



[6-23]

```

public static int max(int[] arr){
	if(arr == null || arr.length == 0) return -999999;
	int max = Integer.MIN_VALUE;
	
	for(int i = 0; i < arr.length; i++){
        if(max < arr[i]) max = arr[i];
	}
	return max;
}
```

[6-24]

```
public static int abs(int value){
    if(value < 0) return value*-1;
    else return value;
}
```



