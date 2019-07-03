## Vector
***
* 벡터 선언하고 입력 값 받을 때 주의해야할 점:
<pre><code>
vector"<int>" arr;
arr.push_back(input);
arr[0] = input;
</pre></code>

이렇게 해야한다.

내가 한 실수:
<pre><code>
vector\<int\> arr(n); // 이건 크기 n의 벡터를 만든 후 0으로 초기화한다는 의미.
arr.push_back(input); // 여기에 push_back을 하면 그 뒤에 입력이 들어가게 된다.
</pre></code>
