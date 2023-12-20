# Spring Practice
- Spring Boot를 사용하여 서비스를 만들어봅니다. 이 과정에서 다양한 기술과 원리를 배우고 적용해 볼 것입니다. <br/>
  아래는 우리가 다룰 주요 내용들입니다.

## content
1. Gradle: 빌드 자동화 시스템 / 작성한 java코드를 설정에 맞게 자동으로 빌드하는 것
- 빌드란, 우리가 작성한 소스 코드를 실행 가능한 결과물로 만드는 일련의 과정을 의미합니다.
- 예) 빌드 시 *.jar 파일 생성

2. 웹서버의 동작원리
- 사용자는 크롬 브라우저를 통해 HTTP 요청을 서버에 합니다 (Webcast).
- 서버는 이 요청을 승인하고, HTTP 응답을 통해 웹사이트(브라우저)에 정보를 전달합니다.
- 요청 시 주로 사용되는 메소드는 GET입니다.
- 이후, 서버는 관련 정보를 바탕으로 웹 브라우저에 정보를 보냅니다.

3. RESTful API
- 서버의 API가 HTTP를 준수하면서 설계되었을 때를 말합니다.
- 소프트웨어 아키텍처의 일종으로, 통신을 관리하기 위한 지침을 제공합니다.
- 주요 HTTP 메소드:
    - GET: 데이터 조회. 서버에 저장된 정보를 요청하고 검색하는 데 사용됩니다. 데이터를 변경하지 않으므로 안전하고 멱등(idempotent)합니다.
    - POST: 데이터 생성. 새로운 데이터를 서버에 생성하거나 추가할 때 사용됩니다. 예를 들어, 새로운 게시물을 작성하거나 정보를 제출할 때 사용합니다.
    - PUT: 데이터 수정/갱신. 기존의 데이터를 새로운 데이터로 완전히 대체할 때 사용됩니다. 예를 들어, 사용자 프로필 정보를 갱신할 때 사용할 수 있습니다.
    - DELETE: 데이터 삭제. 서버에 저장된 특정 데이터를 삭제할 때 사용됩니다.
    - PATCH: 부분적 데이터 수정. PUT과 유사하지만, 전체 데이터를 대체하는 것이 아니라 일부분만 수정할 때 사용됩니다.
 
** 이러한 메소드들은 RESTful API 설계에서 중요한 역할을 하며, 각각의 메소드는 서버의 리소스에 대한 다른 종류의 요청을 나타냅니다. 이를 통해 클라이언트와 서버 간의 통신이 효율적이고 명확하게 이루어질 수 있습니다.
      
4. Apache Tomcat
- Apache Tomcat은 Java 어플리케이션을 위한 오픈 소스 웹 애플리케이션 서버(WAS)입니다.
- 주로 Java Servlet, JavaServer Pages (JSP), Java Expression Language 등을 실행하기 위해 사용됩니다.
*- *WAS (Web Application Server)**의 역할을 수행하여, 웹 애플리케이션의 실행 환경을 제공합니다. 이는 클라이언트의 요청에 따라 비즈니스 로직을 처리하고 그 결과를 반환하는 역할을 합니다.
- Tomcat은 웹 서버와 서블릿 컨테이너의 기능을 모두 제공합니다:
    - 웹 서버 기능: 정적 컨텐츠(HTML, 이미지 파일 등)를 처리하고 클라이언트(브라우저)에게 전달합니다.
    - 서블릿 컨테이너 기능: Java Servlet을 관리하며, 동적 컨텐츠를 생성하여 클라이언트에게 제공합니다.
- Tomcat은 가벼운 구조로 인해 개발 및 테스트 환경에서 널리 사용되며, 소규모에서 중규모 어플리케이션 서버로도 적합합니다.
- 설정과 관리가 비교적 간단하며, 커뮤니티 기반의 지원이 활발하여 문제 해결에 유용한 리소스를 쉽게 찾을 수 있습니다.

5. Spring과 Spring boot의 차이점
- Spring은 강력한 프레임워크로, 다양한 기능과 설정을 제공합니다.
- Spring Boot는 Spring 기반의 애플리케이션을 쉽게 만들 수 있도록 도와주는 도구입니다. 기본 설정이 많이 포함되어 있어 빠르게 개발을 시작할 수 있습니다.

5-1. Spring
- Spring은 강력하고 유연한 Java 기반의 프레임워크입니다.
- 엔터프라이즈 급 애플리케이션을 개발하기 위한 광범위한 기능과 지원을 제공합니다.
- 의존성 주입(Dependency Injection), 관점 지향 프로그래밍(Aspect-Oriented Programming), 데이터 접근을 위한 다양한 방법 등을 포함합니다.
- 개발자가 애플리케이션의 모든 설정을 세밀하게 제어할 수 있으며, 이는 높은 수준의 맞춤화와 유연성을 가능하게 합니다.
- 다양한 서드파티 라이브러리와의 통합이 가능하며, 복잡한 엔터프라이즈 애플리케이션을 구축하는 데 적합합니다.

5-2. Spring Boot
- Spring Boot는 Spring 기반의 애플리케이션을 더 빠르고 쉽게 개발할 수 있도록 설계된 도구입니다.
- '컨벤션 오버 컨피규레이션(Convention over Configuration)'의 원칙을 따르며, 기본적인 설정을 자동화하여 개발자가 빠르게 개발을 시작할 수 있도록 합니다.
- 내장된 Tomcat, Jetty 또는 Undertow 서버를 사용하여 별도의 웹 서버 설정 없이 바로 실행할 수 있습니다.
- 스타터(Starter) 종속성을 제공하여 필요한 라이브러리를 쉽게 추가할 수 있으며, 이를 통해 의존성 관리가 간소화됩니다.
- 자동 구성(Auto-configuration) 기능을 통해 Spring 애플리케이션의 초기 설정을 간편하게 할 수 있으며, 이는 개발 시간을 단축시키는 데 도움이 됩니다.
