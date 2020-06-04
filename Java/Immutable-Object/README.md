# 불변객체

## 정의

- 생성 후 그 상태를 바꿀 수 없는 객체

## 장점

- 모든 클래스를 상태를 변경할 수 없는 불변 클래스(immutable class)로 만들면 유지 보수성이 크게 향상된다.

- 불변 객체에는 아래의 ‘식별자 변경(identity mutability)’ 문제가 발생하지 않는다.
- 객체가 완전하고 견고한 상태이거나 아니면 아예 실패하는 실패 원자성(failure atomicity)을 가진다.
- 시간적 결합(temporal coupling)을 없앨 수 있다.

```java
Map<Cash, String> map = new HashMap<>(); 
Cash five = new Cash("$5");
Cash ten = new Cash("$10");
map.put(five, "five");
map.put(ten, "ten");
five.mul(2);
__
                    
map.get(five);
```

- **스레드 안정성**
    - 객체가 여러 스레드에서 동시에(concurrently) 사용될 수 있고, 예측 가능한(predictable) 결과를 보장하는 객체의 품질
- **단순성(simplicity)**
    - 객체가 더 단순해질 수록 응집도는 더 높아지고, 유지보수는 더 쉬워진다.
- 불변 객체의 크기가 작은 이유는 불변 객체의 경우 생성자 안에서만 상태를 초기화할 수 있기 때문이다.

## 단점

- 메모리를 많이 차지한다.
- 가독성이 떨어진다.(Java의 경우, Kotlin은 제외)