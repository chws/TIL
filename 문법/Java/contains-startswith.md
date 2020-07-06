## String의 `contains()`와 `startsWith()`

- 둘 다 boolean 값을 반환한다

```Java
String s1 = "app";
String s2 = "application";
String s3 = "pappico";

System.out.println(s2.contains(s1)); // (1) application이 app을 포함하는지
System.out.println(s3.contains(s1)); // (2) pappico가 app을 포함하는지

System.out.println(s2.startsWith(s1)); // (3) application이 app으로 시작하는지
System.out.println(s3.startsWith(s1)); // (4) pappico가 app으로 시작하는지

String s4 = "Hello World!";
String s5 = "Wor";
//toffset 파라미터는 시작점을 지정해준다
System.out.println(s4.startsWith(s5, 6)); // (5) Hello World의 6번째부터 Wor로 시작하는지
System.out.println(s4.startsWith(s5, 3)); // (6) Hello World의 3번째부터 Wor로 시작하는지
```

```
결과화면

true
true

true
false

true
false
```