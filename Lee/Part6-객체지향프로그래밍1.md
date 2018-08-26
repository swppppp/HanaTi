# 자바의 정석 Part 6 풀이  

[6-1]  
```
class SutdaCard {
	int num;
	boolean isKwang;
}
```  

[6-2]  
```
public SutdaCard() {
	this(1,true);
}

public SutdaCard( int num, boolean isKwang) {
	this.num = num;
	this.iskwang = isKwang;
}

public void info() {
	if (isKwang == false) {
		System.out.println(num);
	} else {
		System.out.println(num + "K");
	}
}
```

[6-3]  
```
class Studend {
	String name;
	int ban, no, kor, eng, math;
}
```

[6-8]
```
클래스변수 : width, height
인스턴스변수 : kind, num
지역변수: card, k, n, args
```

[6-9]  
```
weapon, armor
=> 모든 병사가 같아야 하는 값(공유해야 하는 값)이므로 static 필요.
```

[6-10]    
b, e  

[6-11]  
b  

[6-12]  
c, d  

[6-13]   
b, c, d  

[6-14]   
a, c, e  

[6-15]   
c  

[6-16]   
a, e  

[6-17]   
b  

[6-18]   
A..? => 값이 할당되려나..  
B => 스태틱 메서드에서 인스턴스 변수 사용 불가  
D => 스태틱 매서드에서 인스턴스 메서드 사용 불가  

[6-19]   
ABC123  
ABC123 => str이 static 변수였으면 바뀌었을 것  

  

