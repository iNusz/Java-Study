# 목차
[TOC "float:left"]
<br/>

### for을 이용해 계산하기

###### start 부터 end 까지 더한 결과값을 출력해보세요

- [ ] 방법 1 (기본 알고리즘으로써 실행시키기 까지 시간이 오래 걸린다.)

```
public class BasicMain2 {public static void main(String[] args) {

	long start = 0;
	long end = 9999999999L;
    
	//long의 값의 범위가 넘어가서 음수로 나온다. 따라서 double로 바꾸면 제데로 출력이된다.

	double c = 999999999L;
	double d = 999999999L/2;
			
	System.out.print("결과값="+(c+1)*d); //4.99999999E17
	
}
```

_ _ _

- [ ] 방법 2 (for문을 이용함으로써 시간을 단축시킬 수 있다.)

```
public class BasicMain2 {public static void main(String[] args) {


	long start = 0;
	long end = 9999999999L;
	
	double result = 0;
	for (long i=start; i<=end; i=i+1){
		result = result +i;
	}
	System.out.println("결과값="+result);  //4.99999999E17
	
	
}
```



* * *
###### 1부터 100까지 짝수값을 더한 결과값을 출력해보세요.
```
public class BasicMain2 {public static void main(String[] args) {

	//1. 결과값을저장할 변수를 선언하고
	int result = 0;
    
	//2. 로직을 수정하다. 만약 홀수값으 더한 결과값을 출력하려면 
    // if문에서 연산자를 !=을 써도 되고 ==1 써도 되고 %1 을 써도 된다.
    
	for(int i=0 ; i<=100 ; i=i+1){ 
		if (i%2 ==0 ) { 
			result = result + i;
		}
		 
	}

	//3. 결과값을 출력한다.
		System.out.println("결과값="+result);
}
```






