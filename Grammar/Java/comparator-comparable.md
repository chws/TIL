# Sorting - Comparator vs Comparable


## 클래스 `Comparator`의 객체를 생성하여 정렬 
```Java
List<String> strings = new ArrayList<>();
...
```
이 리스트에 `add()`를 이용해서 배열을 만든다

1. 익명 클래스
```Java
Collections.sort(strings, new Comparator<String>() {
    @Override
    public int compare(String o1, String o2) {
        return o1.length() - o2.length();
    }
});
```
**결과화면**
```
lkj23
lkjsdlf
asldkjfasdk
1234566789999
```



2. 람다식  
원리는 똑같다. 순서가 중요하다.  
```Java
Collections.sort(strings, (s1, s2) -> s2.length() - s1.length());
```
**결과화면**
```
1234566789999
asldkjfasdk
lkjsdlf
lkj23
```

---




## 인터페이스 `Comparable` 을 이용하여 정렬
`Comparable`은 `compareTo()` 함수만 있는 interface이다.  
```Java
public interface Comparable<T> {
    public int compareTo(T o);
}
```
`Comparable`을 사용하기 위해서는 `Comparable`을 implement하는 클래스 안에 `compareTo()` 메소드를 오버라이딩 해주면 된다. 방식은 `Comparator`과 같다. `int`를 리턴하는 방식  

*주의할 점*은 `Comparable`을 implement하는 클래스 A 안에서 정의가 되므로,  
정렬되는 대상의 배열은, A로 만들어진 배열이어야 한다. 

```Java
List<Text> texts = new ArrayList<>();
...

Collections.sort(texts);
```

아래의 클래스 안에서 `compareTo()`를 오버라이딩하여 메인에서 사용한다.
```Java
public class Text implements Comparable<Text> {
    private String text;

    public Text(String text) {
        this.text = text;
    }

    public int getLength() {
        return text.length();
    }

    public String getText() {
        return text;
    }

    @Override
    public int compareTo(Text o) {
//        return this.getText().length() - o.getText().length();
        return this.getLength() - o.getLength();
    }
}
```

### 알고리즘 문제풀이를 할 때엔 Comparator이 더 활용도가 높을 것 같다

[참고한 자료](https://codechacha.com/ko/java-sorting-comparator/)
