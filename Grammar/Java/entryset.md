## HashMap의 `entrySet()` 

`keySet()`과 다르게, `key`와 `value`를 모두 가져오기 때문에 맵을 한 번만 돌면 되어서 시간 복잡도를 줄일 수 있다.  

```Java
Map<String, Integer> map = new HashMap<>();
map.put("rebecca", 4);
map.put("matt", 2);
map.put("james", -1);
map.put("lisa", 21);

int sum = 0;
for (Map.Entry<String, Integer> entry : map.entrySet()){
    sum += entry.getValue();
}
System.out.println(sum);

```

**결과화면**
```
26
```
