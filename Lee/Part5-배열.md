# 자바의 정석 Part 5 풀이  


[5-1]    
a.  
b.  
d.  

[5-3]
```
for( int i=0; i < arr.length; i++ ) {
	sum += arr[i];
}
```  

[5-5]
```
(1) 
if(j != ballArr[i]) {
	temp = ballArr[i];
	ballArr[i] = j;
	ballArr[j] = temp;
}

(2)
for(int j = 0; j < 3; j++) {
	ball3[j] = ballArr[j];
}
```  

[5-7]
```
(1)
if(money > coinUnit[i]) {
	1. coinNum = money / coinUnit[i];
	if(coin[i] >= coinNum) {
		2. coin[i] -= coinNum;
		3. money -= coinNum * coin[i];
	} else {
		3. money -= coinUnit[i] * coin[i];
		2. coin[i] = 0;
	}
}  
```

[5-9]
```
result[i][j] = star[j][i];
```  

[5-11]  

[5-13]  


 



