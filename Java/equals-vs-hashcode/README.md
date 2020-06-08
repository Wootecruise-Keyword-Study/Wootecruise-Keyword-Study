### HashCode vs equals

- **equals** 는 두 객체의 내용이 같은지, 동등성(equality) 를 비교하는 연산자
- **hashCode** 는 두 객체가 같은 객체인지, 동일성(identity) 를 비교하는 연산자
- **HashMap**이나 **HashSet, HashTable**과 같은 객체들을 사용하는 경우, 객체의 의미상의 동등성 비교를 위해**hashCode()** 를 호출한다.
- **equals() 와 관련된 규약**
    1. 반사성(Reflexive) : `a.equals(a) == true`
    2. 대칭성(Symmetric) : `a.equals(b) == true` ↔ `b.equals(a) == true`  
    3. 추이성(Transitive) : `a.equals(b) == true && b.equals(c) == true` → `a.equals(c) == true`
    4. 일관성(Consistent) : `a.equals(b)` 는 항상 같은 결과를 반환해야한다.
    5. 널은 항상 false(Null comparison) : `a.equals(null) == false` NPE가 발생하면 안된다.
- **hashCode() 와 관련된 규약**
    1. **equals()** 로 비교시 두개의 오브젝트가 같다면, **hashCode()** 값도 같아야 한다.
    2. **equals()** 로 비교시 **false** 라면, **hashCode()** 값은 다를수도, 같을수도 있다.
    그러나 성능을 위해서는 **hashCode()** 값이 다른것이 낫다. 그래야 해싱 알고리즘으로 **Set** 에 해당 오브젝트가 존재하는지 아닌지 빠르게 검색할 수 있다(perfect hash functions).
    3. **hashCode()** 값이 같다고 해서, **eqauls()** 가 **true** 를 리턴하는 것은 아니다. 해싱 알고리즘 자체의 문제로, 같은 해시값이 나올 수 있다.