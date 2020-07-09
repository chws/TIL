## Iterator 

- 주로 `map`의 원소들을 방문하는 데 쓰인다.

```java
Iterator<String> keys = map.keySet().iterator();
while( keys.hasNext() ){
    String key = keys.next();
    //do something
}

```
