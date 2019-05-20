1. ``` bool prev_permutation (&first, &last, (func)comp)```
    내림차순의 순열을 만들어주는 STL
2. ``` bool next_permutation (&first, &last, (func)comp)```
    오름차순의 순열을 만들어주는 STL



```
#include <algorithm>

int main(){
	
	int array[5] = {1,2,3,4,5};

	do{
		for(int i=0; i<5; i++){
			cout << array[i] << ',';
		}
		cout << '\n';
	}while(next_permutation(array, array+5));
}
```

<출력>
    ```1,2,3,4,5,```
    ```1,2,3,5,4,```
    ```1,2,4,3,5,```
    ```...```

bool 값을 리턴하기 때문에 다음 증가하는 순열(next_permutation의 경우)이 있다면 true를 반환한다.
그래서 do~while 문을 사용해야 ```1,2,3,4,5``` 부터 결과값이 출력됨.
