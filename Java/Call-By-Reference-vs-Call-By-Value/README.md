[ Call By Value ]

- 함수의 인자로 값의 복사본을 넘긴다.
- 함수 내에서 넘겨받은 인자를 수정할 경우 원본 값은 변하지 않는다.(read only)

[ Call By Reference ]

- 함수의 인자로 값 자체(주소)를 넘긴다.
- 함수 내에서 넘겨받은 인자를 수정할 경우 원본 값도 같이 변한다.(read & write)

[ Java의 경우 ] 

- 기본적으로 Java는 Call By Value이다.
- 함수의 매개변수가 원시 자료형일 경우 리터럴 값을 넘겨준다. (int, short, long, float, double, char, boolean, byte)
- 함수의 매개변수가 참조 자료형일 경우 주소값을 사용한다. (Array, Class Instance, Object를 상속받은 클래스)