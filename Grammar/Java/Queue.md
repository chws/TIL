# Queue
- Queue는 Collection을 상속하는 interface이다.  
- 그렇기 때문에 Queue는 concrete class로 받아줘야 하는데 보통 `LinkedList`, `PriorityQueue`, `ArrayBlockingQueue` 로 구현한다.  
- 한계점: 이 두가지 클래스는 thread-safe 하지 않다. 

### Methods 
```
add(element) // 가장 뒤에 원소를 삽입한다
offer(element) // add와 기능이 같지만 큐가 다 찼을 때 exception을 던지는 것이 아니라 false를 반환해서 더 많이 쓰인다

peek() // 가장 앞의 원소를 조회하며 if empty, returns null
poll() // 가장 앞의 원소를 제거하며 그 원소를 리턴해준다 if empty, returns null  
remove(element) // 괄호 안의 element와 일치하는 것 중 가장 앞에 있는 게 삭제된다, if empty, throws NoSuchElementException
```
