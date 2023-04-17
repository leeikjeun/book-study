# 람다 표현식


## 람다란?
 - 메서드로 전달할 수 있는 익명 함수를 단순화한 것(책 내용 ㅋ)
 - 인터페이스로 정의되어있는 내용을 함수로 표현하여 처리하는 것

```
 예) // 람다에 사용할 인터페이스 선언 
    Interface LambdaTest{
        String testMethod(Integer value);
    }

    // 인터페이스를 사용하는 메소드 선언
    void testMethod(LambdaTest lambdaTest, Integer value){
        System.out.println(lambdaTest.testMethod(value));
    }
    
    testMethod(
            a -> { // a -> (이부분은 LambdaTest Integer value가 들어온다면을 표현 (파라미터 리스트) 
                    a += 5; // 사실상 value += 5와 같음
                    return Integer.toBinaryString(a); // LambdaTest testMethod 함수의 리턴값인 String을 표현
              }, 10);
    
    // 단순히 한줄로 끝난다면 이와같이 return 및 {}을 없이 한줄로 끝낼 수 있음          
    testMethod(a -> Integer.toBinaryString(a), 10); 
```

## 함수형 인터페이스란?
 - 딱 한개의 메소드만 정의되어있는 인터페이스
    - 한개만 지정해야하는 이유 : 1개 이상인 경우 람다표현식에 어떤 함수가 맵핑되는지 인지를 못함
 - 위의 예제처럼 람다를 사용하고 싶을 때 마다 인터페이스를 만들면 너무 많은 인터페이스가 생김
    - 자바에서 기본적으로 제공해주는 함수형 인터페이스가 있음 의미에 따라 사용하는 것도 좋다고 생각함

 