# 자바의정석 Part 4 풀이


[4-1]
1. int x > 10 && x < 20
2. !(ch == '' || cj == '\t')
3. ch == 'x' || ch == 'X' 
4. ch > '0' && ch < '1'
5. ch >= 65 && ch <= 122
6. (year % 400 == 0) || (year % 4 == 0 && year % 100 != 0)
7. powerOn == false
8. str == "yes"


[4-2]
```
int sum = 0;  
// 입력값 x  
if ( x % 2 == 0 || x % 3 == 0){  
	sum += x;  
}  
```

[4-3]
```
int sum = 0;
for( int i = 1; i <= 10; i++) {
	for( int j = 1; j <= i; j ++) {
		sum += j;
	}
}
```

[4-4]
```
int sum = 0, count=0;
for (int i = 1; i <= 100; i++) {
  if(sum >= 100) {
    System.out.println(count);
    break;
  }
  if(sum % 2 == 0) {
    sum += -i;
    count ++;
  } else {
    sum += i;
    count ++;
  }
} 
답 : 99
```

[4-5]
```
while(i <= 10){
	while(j <= i){
		System.out.print("*");
		j++;
	}
	System.out.println();
	i++;
}
```

[4-6]
```
for( int i = 1; i <= 6; i++) {
	for (int j = 1; j <= 6; j++) {
		if(i + j == 6) {
			System.out.println( i + "와" + j + "=" + i + j);
		}
	}
}
```

[4-7]
```
(int)Math.random() * 6 + 1;
```

[4-8]
```
for(int i =0; i<=10 ; i++) {
	for(int j=0; j<=10; j++) {
		if(2*x + 4*y == 10) { 
			System.out.println("x=" + x + "y=" + y);
		}
	}
}
```

[4-9]
```
sum += str.charAt(i);
```

[4-10]
```
sum += num % 10;
num = num / 10;
```

[4-11]
```
num3 = num1 + num2;
num1 = num2;
num2 = num3;
```

[4-12]


[4-13]
```
ch = value.charAt(i);
if(!(ch <= 89 && ch >= 80)) {
  isNumber == false;
}
```


[4-14]
```
(1) Math.random * 100 + 1;
(2) if (answer == input) {
	System.out.println("맞췄습니다.");
	System.out.println("시도횟수는 " + count + "번입니다.");
} else if(answer > input) {
	System.out.println("더 큰 수를 입력하세요.");
} else { 
	System.out.println("더 작은 수를 입력하세요.")
}
```

[4-15]