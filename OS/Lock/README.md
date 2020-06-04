# Lock

## Critical Section

- 공유 자원(shared data), 즉 동시 접근하려고 하는 그 포커싱된 자원에서 문제가 발생하지 않도록 독점을 보장해줘야하는 영역

## Mutex Lock

- mutex lock은 lock의 가용 여부를 판단하는 available이라는 변수를 가짐
- lock이 가용하다면 acquire()를 호출하여 lock을 획득하고, lock은 사용불가가 됨
- lock을 반환할 때는 release()를 호출함

### spin lock

- 다른 스레드가 lock을 소유하고 있다면 그 Lock이 반환될 때까지 **계속 확인**하며 기다리는 것

### busy waiting

- 원하는 자원을 얻기 위해 기다리는 것이 아니라 **권한을 얻을 때까지 확인**하는 것을 의미
- Busy Waiting은 CPU cycle을 낭비함

## Semaphore

- 세마포어는 공유 자원에 **세마포어의 변수**만큼의 프로세스(또는 쓰레드)가 접근할 수 있습니다.(뮤텍스는 오직 **1개**만의 프로세스(또는 쓰레드)만 접근할 수 있음)