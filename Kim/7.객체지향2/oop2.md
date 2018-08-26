[7-1]

```
	public SutdaDeck() {
		for(int i = 0; i < 20; i++){
			if(i < 10){
				if(i+1 == 1 || i+1 == 3 || i+1 ==8){
					cards[i] = new SutdaCard(i+1, true);
				}
				else cards[i] = new SutdaCard(i+1, false);
			} else {
				cards[i] = new SutdaCard(i-9,false);
			}
		}
	}
```

[7-2]

```
public void shuffle(){
    for(int i = 0; i < cards.length; i++){
        int j = (Math.random()*cards.length);
        SutdaCard temp = cards[i];
        cards[i] = card[j];
        cards[j] = temp;
    }
}

SutdaCard pick(int idx){
    return cards[idx];
}

SutdaCard pick(){
    int idx = (int)(Math.random()*cards.length);
    return cards[idx];
}
```

[7-3]

>클래스 상속에서 부모클래스의 정의된 메서드를 자식클래스에서 재정의 해서 사용하는 기법
>
>부모 클래스에서 상속받은 메서드를 자식에서 사용할수 없는 경우가 있기때문에 오버라이딩 필요

[7-4]

> c (접근제어자는 부모클래스보다 넓은 범위로만 변경 가능), d

[7-5]

> Product class의 디폴트 생성자가 없기때문에 에러가 난다.
>
> 왜냐하면 Tv클래스에서 디폴트 생성자가 호출될때 컴파일러 내부적으로
>
> super()를 호출하기 때문에

[7-6]

> 부모 인스턴스 변수의 초기화를 위해서 자식 클래스에서 부모 클래스 생성자를 호출한다.

[7-7]

> 200
>
> child() -> child(int x) -> Parent() -> parent(intx);

[7-8]

> a
>
> private-> 같은 클래스
>
> default-> 같은 패키지
>
> protected-> 같은 패키지, 다른패키지 부모자신간
>
> public -> 제한 없음

[7-9]

> c (오버라이딩)

[7-10]

```
private boolean isPowerOn;
private int channel;
private int voloume;

public void setIsPowerOn(boolean isPowerOn){
    this.isPowerOn = isPowerOn;
}
public boolean getIsPowerOn(){
    return this.isPowerOn;
}

public void setChannel(int channel){
    this.channel = channel;
}
public int getChannel(){
    return this.channel;
}

public void setVolume(int vol){
    this.volume = vol;
}
public int getVolume(){
    return this.volume;
}

```

[7-11]

이 문제 아이디어 너무좋다 알아두면 좋은 코드....

```

private int preChannel;
public void setChannel(int channel){
     preChannel = this.channel;
     this.channel = channel;
}
public void gotoPrevCHannel(){
    setChannel(this.preChannel);
}
```

[7-12]

> c

[7-13]

>  Math클래스들의 모든 메서드가 클래스메서드 이므로 객체를 생성할 필요가 없기 때문에

>  private로 지정

[7-14]

```
final static int num;
final static boolean isKwang;
```

[7-15] * 엄청헷갈리네 (이해 잘해야해)

> e-> 헷갈림(왠지될듯) 안되네..

[7-16] 

> b (interface는 instance가 아니지 않을...) 
>
> Instanceof 는 실제 인스턴스의 모든 조상이나 구현한 인터페이스에 대해 true를 반환한다.
>
> instanceof 는 인스턴스를 생성한 클래스를 따라간다.

