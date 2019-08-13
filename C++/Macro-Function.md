### 매크로
* \# : Stringizing Operation - 매크로 인자를 문자열로 인식하게 해준다.
      
      ```c++
      #define stringer(x) printf(#x "\n")
      stringer(Hello\n);
      ```
      
      
      <출력>
      Hello
     
      
* \## : Token-pasting Operation - 분리되어 있는 2개의 토큰을 하나로 뭉쳐준다.

      ```c++
      #define X(n)        x##n                              
      #define PRINT(n)    printf("x%d = %d\n", n, x##n)          
      for(int i=0; i<2; i++){
        X(i);
        PRINT(i);
      }
      ```
      
      ```
      <출력>
      x0 = 0
      x1 = 1
      ```
      
      
