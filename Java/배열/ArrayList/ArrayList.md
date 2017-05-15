### ArrayList

#### 정의 
**ArrayList**는 배열과 비슷하지만 기능적인 면에서 차이가 있습니다. 
배열은 배열의 크기를 지정해주고 만약에 크기를 더늘리고 싶으면 다시만들어줘야 합니다.


한마디로 **배열은 메모리 공간을 일정하게(자신이 지정) 할당하여 일렬로 나열합니다.**
반면에 **ArrayList는 자신이 따로 할당을 하지 않아도 됩니다.**.
성능은 배열과 유사하나 기능적인 면에서 더 뛰어나다고 생각하시면 됩니다.
다음 그림을 봅시다.


![ArrayList에제.png](https://github.com/iNusz/Java-Study/blob/master/Java%20image/ArrayList예제.png)



아래행은 각 배열의 위치고 위의 행은 각 배열의 해당하는 값입니다. 
예를들어 내가 값을 추가시키고 싶으면 4번째 배열에 자동으로 값이 맨뒤(마지막 위치)에 데이터를 저장하게 되고 해당 4번째 배열값을 삭제를 하고싶으면 삭제도 가능합니다.


또 특정 위치에 내가 원하는 데이터를 추가를 할수 있습니다.
3위치에 "94"라는 값을 추가를 시키면 3번자리에 "94"의 값이 들어가고 4번자리에 기존에있던 "8"의 값이 들어가게 됩니다. 


또 특정 위치에 있는 데이터를 제거할 수 있습니다. 
위의 방법과 동일하게 만약에 중간의 데이터가 삭제가 된다면 모든 배열이 한칸씩 땡겨지게 되지요. 

이와 관련되서 제네릭이라는 걸 써야하는데 그 내용은 제네릭 파트에 올리겠습니다.




###### 예제 1




기본적인 배열 생성과 각각의 배열을 초기화하는 방법과 다른 클래스의 메소드를 불러오는 과정 입니다.
```
package com.shinseungho.java.array;

public class ArrayMain {

	public static void main(String[] args) {

		
//		int arr[]; //선언한다. 
		int arr[] = new int[10]; //10은 메모리 공간 갯수 , 초기화 , 초기화되는순간 기본적으로 0 으로 된다(기본형만 적용)
		
		int arr2[] = {1, 2, 3, 4, 5}; //위와 같이 2개의 구분이 있다.
		
		for( int a1 :arr){
			System.out.println(a1);
		}
		for( int a1 : arr2){
			System.out.println(a1);
		}
		
		// 타입의 이름만 바뀐다 . 
		ArraySub subs[] = new ArraySub[10]; //안의 값도 초기화를 해줘야한다.  
		
		// 아래의 식은 초기화를 해주는 과정
		subs[0] = new ArraySub();
		subs[1] = new ArraySub();
		subs[2] = new ArraySub();
		subs[3] = new ArraySub();
		subs[4] = new ArraySub();
		subs[5] = new ArraySub();
		subs[6] = new ArraySub();
		subs[7] = new ArraySub();
		subs[8] = new ArraySub();
		subs[9] = new ArraySub();

				
		for( ArraySub sub: subs){ 
			System.out.println(sub.a);
		}
		
		
		
		ArraySub sub = new ArraySub();
		sub.printNumber();


	}

}

```



###### 예제2




```
package com.shinseungho.java.array;

public class ArraySub {
	

	public int a;

//	 int a;  //int 앞에도 public private default protected 를 사용할수 있다. 
		
	 접근제한자 리턴타입 함수명()
	 이때 접근제한자는 삭제할수 있다. 하지만 리턴타입은 유지시켜야한다.
	 아무것도 안적으면 지역제한자 default가 붙는다. 이때 default는 패키지가 다르면 적용되지 않는다 그래서 접근하려면 public을 써야한다. 
	 default를 쓰겠다는거는 그 카테고리만 쓸수있게끔 제한을 걸어두는 것이다.
	 
	void printNumber(){
		System.out.println(a);
	}
	// private 를 쓰면 다른 클래스에서 쓸수없다.
	private void sum(int a, int b){
		
	}
	
}
```