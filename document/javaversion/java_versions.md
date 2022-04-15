이번 장에서는 자바 버전에 따른 변경사항과 트렌드에 대해서 알아본다.
대부분 기계인간 John Grib과 Oracle 공식문서를 참고하여 작성하였으며 Java 7 이후 버전에 대한 정리만 진행한다.
주요 변경사항이라고 표시한 부분은 어디까지나 스프링 기반 백엔드 개발자인 필자의 개인적인 의견일 뿐이며 관점에 따라서 달라질 수 있다.

---

### 개요

필자가 재직 중인 회사에 새로운 프로젝트를 진행하게 되면서 자바의 버전을 선택해야하는 시간을 가지게 되었다.
지금까지 사용해왔고 편한 8, 11을 사용할 수는 있겠지만 요즘 자바와 코틀린이 빠르게 성장하며 자바의 버전도 빠르게 업데이트 되고 있기 때문에 버전별로 업데이트 된 사항들을 정리하는 시간을 가져보도록 한다.
이전과는 다르게 현시대의 자바 개발자들은 자바 버전에 관심을 가지고 개발을 해야한다. 아래의 이미지는 Wikipedia에 나와있는 자바 버전 이력이다.

![](image/java-version-history.png)

주의깊게 봐야하는 부분은 **JDK Beta에서 Java SE 7까지 총 9개의 버전을 출시하는데 16년이라는 시간**이 걸렸다.
하지만 **Java SE 8(LTS)부터 Java SE 17(LTS)까지 총 10개의 버전을 출시하는데 이전의 절반도 안되는 7년이라는 시간**이 걸렸다.
밑에서 다루겠지만 Java 17이후 부터는 LTS 출시 간격을 3년에서 2년으로 줄인다는 발표까지 진행되었다.
(Oracle이 Sun을 2009년 쯤에 인수하고 처음으로 Java 7을 출시하였으니 이때를 시작으로 빠른 버전업이 진행되었다고 보는 것이 맞을 듯 하다.)
이렇게 빠르게 자바의 버전이 변경되며 새로운 문법과 새로운 GC 등등 새로운 기능들이 판을 치는 자바 생태계에 버전에 따른 변경사항을 공부하는 것은 어떻게 보면 당연하다.

여담이지만 이렇게 글을 정리하는 가장 큰 이유는 자바의 버전별 변경사항이 인터뷰 질문에 자주 등장하기 때문이다.
작성일 기준 1년 전쯤 "자바8에서 변경된 사항이 무엇인가요?" 라는 인터뷰 질문에 필자는 "Stream과 Optional이 추가되었습니다."라는 답변을 하였다.
답변을 들은 면접관은 "자바8에서 변경사항이 많이 있을텐데 다른 건 없나요???"라고 질문하였고 필자는 입을 다물 수 밖에 없었다.

이 글을 읽는 사람들은 필자와 같은 실수를 하지 않았으면 하는 바램으로 변경사항을 정리하며 인터뷰 질문에 대한 답변도 정리하는 시간을 가져보려 한다.
모든 변경사항을 다루지는 않으며 인터뷰 질문을 대비한 "주요 변경사항"과 JVM 관련 변경사항 및 기타 변경사항에 대해서 알아본다.

보안(Security)관련 업데이트는 내용이 너무 길어져서 추후 따로 정리하도록 한다. 

---

### [Java 8(LTS)](https://www.oracle.com/java/technologies/javase/8-whats-new.html)

#### 주요 변경사항

- [**Lambda Expressions**](https://docs.oracle.com/javase/specs/jls/se8/html/jls-15.html#jls-15.27): 
  메소드를 하나의 식으로 표현한 람다 표현식이 등장하였다. 익명 함수라고도 불리며 코드를 사용 이전보다 깔끔하게 만들어준다는 장점이 있다.
  특히 구현해야하는 메서드가 하나 뿐인 인터페이스를 구현하는 경우에 이전보다 훨씬 간략하게 코드를 작성할 수 있다.
- [**Functional Interface**](https://docs.oracle.com/javase/specs/jls/se8/html/jls-9.html#jls-9.8):
  구현해야하는 추상 메서드를 단 하나만 가지고 있는 인터페이스를 의미한다. 이러한 인터페이스를 람다 표현식과 함께 간편하게 사용할 수 있다.
- [**Interface Default Method**](https://docs.oracle.com/javase/specs/jls/se8/html/jls-13.html#d5e19889):
  추상 클래스와 같이 인터페이스에도 default 메서드가 추가되어 구현된 메서드를 가질 수 있다.
- [**Stream**](https://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html):
  순차 및 병렬 집계 작업을 도와주는 Collections의 Stream 추가, 병렬 작업으로 다중 코어에서의 성능 향상
- [**Optional**](https://docs.oracle.com/javase/8/docs/api/java/util/Optional.html):
  NPE방지를 위한 새로운 타입의 Optional 클래스 추가
- [**DateTime Package**](https://www.javatpoint.com/java-date):
  java.time 경로에 Data-Time 패키지 추가

#### JVM 관련 변경사항

- AES(Advanced Encryption Standard) 내장 기능 추가
- PermGen 제거

#### 기타 변경사항

- [@Repeatable Annotation](https://www.javatpoint.com/java-8-type-annotations-and-repeating-annotations):
  중복되는 애노테이션 사용으로 인한 중복 코드를 제거하기 위해 @Repeatable 애노테이션 추가
- [Improved type inference](https://www.javatpoint.com/java-8-type-inference): 
  타입 추론 성능 향상 
- [Method parameter reflection](https://www.javatpoint.com/java-8-method-parameter-reflection): 
  메소드 또는 생성자의 매개변수 이름을 가져올 수 있는 기능 추가
- HashMap 성능 향상: 중복 키에 대한 성능 향상
- java.util.concurrent 개선: 새로운 인터페이스와 클래스 추가 및 람다 표현식 지원
- CompletableFuture-Future: 인터페이스에서 제공하는 기능 개선
- IO/NIO 개선: java.lang.String(byte[], *), java.lang.String.getBytes() 메서드 퍼포먼스 향상
- java.util 패키지에 Parallel Array Sorting 추가

#### 정리

Java8의 핵심 변경사항은 람다 표현식, Stream, Optional 정도가 될 듯하다.

JVM 메모리 구조에 대한 인터뷰 질문도 많이 나오는데 Java8에서 PermGen이 제거되었다는 것을 기억하고 PermGen에 대한 언급은 하지 않거나 언급하게 된다면 Java8에서 삭제되었다고 얘기해야한다.

Concurrent, Parallel, Stream, CompletableFuture 모두 다중 스레드를 염두한 동시처리 및 병렬처리와 관련이 있다. 
하드웨어 성능 향상으로 다중 코어 및 다중 스레드에 초점을 맞추어 Java도 발전하고 있는 것을 볼 수 있다.

---

### [Java 9](https://docs.oracle.com/javase/9/whatsnew/toc.htm#JSNEW-GUID-C23AFD78-C777-460B-8ACE-58BE5EA681F6)

#### 주요 변경사항

- [**Modular Java Application Packaging**](http://openjdk.java.net/jeps/275):
  Project Jigsaw 기능을 통합하여 패키징 모듈화
- [**jlink**](https://docs.oracle.com/javase/9/tools/jlink.htm#JSWOR-GUID-CECAC52B-CFEE-46CB-8166-F17A8E9280E9):
  패키징 모듈화에 따른 jlink 추가
- [**Release Cadence**](https://blogs.oracle.com/java/post/update-and-faq-on-the-java-se-release-cadence):
  새로운 버전 발표 주기 변경
- [**Deprecated CMS**](http://openjdk.java.net/jeps/291): CMS GC Deprecated 처리
- [**New Default GC**](http://openjdk.java.net/jeps/248): G1GC를 기본 GC로 선정
- [**Private Interface Method**](http://openjdk.java.net/jeps/213): 인터페이스에 Private 메서드 사용가능
- [**Reactive Streams**](https://community.oracle.com/tech/developers/discussion/4418040/reactive-programming-with-jdk-9-flow-api):
  비동기 처리를 위한 반응형 프로그래밍 추가

#### JVM 관련 변경사항

- [Unified JVM Logging](http://openjdk.java.net/jeps/158): 통합 JVM 로깅, -Xloggc
- [Remove Deprecated GC Combinations](http://openjdk.java.net/jeps/214): Deprecated 되었던 GC 조합 제거

#### 기타 변경사항

- [jshell](http://openjdk.java.net/jeps/222): REPL(Read-Eval-Print Loop) 기능을 추가
- [HTML5 Javadoc](http://openjdk.java.net/jeps/224): JavaDoc -> HTML5 빌드기능 추가
- [try-with-resource 개선](https://bugs.openjdk.java.net/browse/JDK-7196163)
- [익명 메서드 <>연산자 추가](https://bugs.openjdk.java.net/browse/JDK-8062373)
- [Process API](http://openjdk.java.net/jeps/102): 프로세스 ID, 인수, 정보, 명령과 같은 정보를 반환하는 기능 추가.
- [CompletableFuture 개선](http://openjdk.java.net/jeps/266): 타임아웃과 지연 기능 추가

#### 정리

새로운 버전의 발표주기가 6개월로 변경되었다는 표현이 기존보다 짧은 주기로 업데이트가 이뤄진다는 의미처럼 보이지만 그렇지는 않다.
예를 들어 java8은 2014년 3월에 출시되었고 기능 릴리즈인 8u20은 2014년 8월에 출시되었다. 다음 릴리즈는 8u40으로 6개월 후에 출시되었다.
결국 기존에 6 ~ 8개월마다 기능 릴리즈가 있던 것을 6개월로 고정한다는 의미로 보면 될 듯하다.

CMS GC는 Deprecated되었고 기본 GC가 Parallel GC에서 G1GC로 변경되었다.
결국 자바는 메모리 단편화 문제를 해결하지 못한 CMS GC를 실패작으로 판단하고 G1GC를 표준으로 밀고 나가려는 것으로 보인다.
만약 인터뷰를 진행하려는 회사가 자바9 이상 버전을 쓰고 있다면 JVM 메모리 구조나 GC 과정에 대한 답변을 G1GC의 메커니즘에 맞춰야 한다.

이번에도 CompletableFuture가 개선되었으며 비동기 반응형 API인 Reactive Streams가 추가되었다.
본격적으로 자바도 비동기 프로그래밍의 시대를 열 것으로 예상된다.

공식문서에 따르면 Java9에서의 가장 큰 변화는 Java 프로그래밍 구성 요소인 모듈 추가라고 한다.
사실 이 부분에 대해서는 이해도 어렵고 분석하는데 시간이 많이 소요될 듯 하여 링크만 남겨두고 분석은 미루도록 한다.
[Java Platform Module System(JSR 376)](http://openjdk.java.net/projects/jigsaw/spec/)
[Module System(JEP 261)](http://openjdk.java.net/jeps/261)
[The Modular JDK(JEP 200)](https://openjdk.java.net/jeps/200)
[Modular Run-Time Images(JEP 220)](https://openjdk.java.net/jeps/220)
[Encapsulate Most Internal APIs(JEP 260)](https://openjdk.java.net/jeps/260)

---

### [Java 10](https://www.oracle.com/java/technologies/javase/10-relnote-issues.html)

#### 주요 변경사항

- **Java9의 안정화 버전**
- [**Improvements for Docker**](https://bugs.openjdk.java.net/browse/JDK-8146115): 
  도커 컨테이너에서의 성능 향상, 추가된 flag들은 링크를 통해서 확인


#### JVM 관련 변경사항

- [Full GC 병렬처리](https://bugs.openjdk.java.net/browse/JDK-8172890): 
  G1의 Full GC를 병렬화하여 애플리케이션 지연 시간 단축
- [Unified Logging](https://bugs.openjdk.java.net/browse/JDK-8184286): 
  TraceYoungGenTime, TraceOldGenTime flag를 gc+heap+exit flag 하나로 통합

#### 기타 변경사항

- [Optional.orElseThrow() Method 추가](https://bugs.openjdk.java.net/browse/JDK-8140281)
- [Unmodifiable Collections 추가](https://bugs.openjdk.java.net/browse/JDK-8177290)
- [Class File Versioning 방식 변경](http://openjdk.java.net/jeps/322)

#### 정리

Java9의 안정화 버전이라서 그런지 이렇다할 변경사항은 보이지 않지만 도커 컨테이너에서의 성능 향상을 위한 플래그 추가는 만족스럽다.

기본 GC인 G1GC의 병렬 처리로 변경하였다. GC가 애플리케이션 스레드를 멈추지 않고 병렬로 처리되면 당연히 리소스 사용량이 높아질 수 밖에 없다.
혹시 [GC 작동 방식](https://imprint.tistory.com/35) 이 궁금하다면 링크로 이동하여 확인해본다.
필자가 이전에 작성한 [GC별 벤치마크 자료](https://imprint.tistory.com/51) 를 확인해보면 확실히 G1GC의 리소스 사용량이 높은 것을 확인할 수 있다.
하드웨어의 성능이 높아지는 추세이다보니 자바에서도 적은 리소스를 사용하는 것보다 할당된 리소스를 충분히 사용하여 빠르게 GC를 수행하는 방향으로 업데이트가 진행되는 것으로 보인다.

Collections final 키워드를 사용해도 내용물이 바뀌는 것을 막을 수 없어서 불편하였는데 Unmodifiable 타입이 추가되어 컬렉션의 내용을 변경하지 못하는 것은 충분히 매력적인 기능이다. 

---

**참고자료**

- [람다의 개념 및 사용법](https://khj93.tistory.com/entry/JAVA-%EB%9E%8C%EB%8B%A4%EC%8B%9DRambda%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B4%EA%B3%A0-%EC%82%AC%EC%9A%A9%EB%B2%95)
- [Java8 함수형 인터페이스](https://bcp0109.tistory.com/313)
- [Java8 함수형 인터페이스 이해하기](https://codechacha.com/ko/java8-functional-interface/)
