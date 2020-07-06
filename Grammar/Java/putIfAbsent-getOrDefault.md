## HashMap에서 `putIfAbsent()`와 `getOrDefault()`의 차이점

```Java
        Map<String, Integer> map = new HashMap<>();
        //없으면 넣는다 - putIfAbsent
        System.out.println(map.putIfAbsent("rebecca", 2)); // (1) 없으면 map에 넣고 null 출력
        System.out.println(map.putIfAbsent("rebecca", 4)); // (2) 있으면 map에 안넣고 원래 있던 값 출력
        System.out.println(map.get("rebecca")); // (3) 이미 값이 있어서 새로운 값이 들어가지 않았다


        //없으면 정해진 값을 돌려준다 - getOrDefault
        System.out.println(map.getOrDefault("rebecca", 7)); // (4) 있으면 있던 값 2를 돌려준다
        System.out.println(map.getOrDefault("matt", 7)); // (5) 없으면 설정한 default 값 7을 돌려준다
        System.out.println(map.get("matt")); //(6) getOrDefault 는 put을 하지 않는다
```



**결과화면**

```
null
2
2

2
7
null
```

