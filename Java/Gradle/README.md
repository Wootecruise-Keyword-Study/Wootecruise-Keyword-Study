- Groovy를 이용한 빌드 자동화 시스템이다.
    - 빌드 자동화  : 서비스를 운영하면서 코드 수정이 발생할 경우 컴파일, 빌드, 배포 과정을 반복해야 하는데, 이 과정을 자동화 한 것.
- Maven의 장점인 관례(Gradle Plugin)와 Ant의 장점인 자유도(Gradle Task)를 모두 흡수
- gralde 빌드 과정
    - build.gradle 스크립트에 플러그인을 추가하면 프로젝트 빌드를 위한 여러 task들이 추가.
    - 이 task들은 서로 의존관계를 맺으면서 빌드 라이프사이클을 추가.
- [https://www.slipp.net/wiki/pages/viewpage.action?pageId=12189700](https://www.slipp.net/wiki/pages/viewpage.action?pageId=12189700)