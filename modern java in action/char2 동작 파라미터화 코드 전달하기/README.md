# 동작 파라미터화 코드 전달하기

## 동작 파라미터화란?
 - 아직 동작이 결정하지 않은 코드 블록을 의미
```
 예) fucntion test(param1::String, param2::동작 파라미터(인터페이스){
        String dateFormat = StringToForMatData(param1, "yyyyMMdd");
        
        param2(dateFormat); // --> 동작 파라미터에 따라 해당 스트링을 받고 동작
                            // --> 단순 출력을 할 수도 있고 api콜도 가능
    }
```
 - 만들어진 이유 : 변화하는 요구사항에 좀더 유연하게 대응을 하고 중간만 변화하고 고정된 코드가 있는 경우에 동일한 코드를 사용하기 위해
