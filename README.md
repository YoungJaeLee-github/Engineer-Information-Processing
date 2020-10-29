# Engineer Information Processing(정보처리기사)


### 3. 애플리케이션 설계
#### 소프트웨어 아키텍처
* 소프트웨어의 골격이 되는 기본 구조이자 소프트웨어를 구성하는 요소들 간의 관계를 표현하는 시스템의 구조 또는 구조체
* 소프트웨어 개발 시 적용되는 원칙과 지침
##### 모듈화(Modularity)
* 소프트웨어의 성능을 향상시키거나 시스템의 수정 및 재사용, 유지관리 등 이 용이하도록 시스템의 기능들을 모듈 단위로 나누는 것
* 크기를 너무 작게 나누면 개수가 많아져 모듈 간의 통합 비용이 많이 들고 너무 크게 나누면 개수가 적어 통합 비용은 적게 들지만 모듈 하나의 개발 비용이 많이 듬
##### 추상화(Abstraction)
* 전체적이고 포괄적인 개념을 설계한 후 차례로 세분화하여 구체화 시켜 나가는 것
* 추상화의 유형 : 과정 추상화, 데이터 추상화, 제어 추상화
##### 단계적 분해
##### 정보 은닉
##### 소프트웨어 아키텍처의 품질 속성
###### 시스템 측면
* 성능
* 보안
* 가용성
* 기능성
* 사용성 
* 변경 용이성
* 확장성
* 테스트 용이성, 배치성, 안정성 등
###### 비즈니스 측면
* 시장 적시성
* 비용과 혜택
* 예상 시스템 수명
###### 아키텍처 측면
* 개념적 무결성
* 정확성, 완결성
* 구축 가능성
##### 소프트웨어 아키텍처의 설계 과정
* 1. 설계 목표 설정 : 전체 시스템의 설계 목표를 설정함
* 2. 시스템 타입 결정 : 시스템과 서브시스템의 타입을 결정하고, 설계 목표와 함께 고려하여 아키텍처 패턴을 선택
* 3. 아키텍처 패턴 적용
* 4. 서브시스템 구체화
* 5. 검토

#### 아키텍처 패턴
* 소프트웨어 시스템의 구조를 구성하기 위한 기본적인 윤곽을 제시
* 아키텍처 패턴을 아키텍처 스타일 또는 표준 아키텍처라고 함
##### 아키텍처 패턴의 장점
* 시행착오를 줄여 개발 시간을 단축시키고, 고품질의 소프트웨어를 생산할 수 있음.
* 검증된 구조로 개발하기 때문에 안정적인 개발이 가능함
* 이해관계자들이 공통된 아케틱처를 공유할 수 있어 의사소통이 간편해짐
* 시스템의 구조를 이해하는 것이 쉬움
* 시스템의 특성을 개발 전에 예측하는 것이 가능해짐
##### 레이어 패턴
* 레이어 패턴은 시스템을 계층으로 구분하여 구성하는 고전적인 방법 중의 하나
* 서로 마주보는 두 개의 계층 사이에서만 상호작용이 이루어지며, 변경사항을 적용할 때도 서로 마주보는 두 개의 계층에만 영향을 미치므로 변경 작업이 용이
* 레이어패턴은 특정 계층만을 교체해 시스템을 개선하는 것이 가능함
* 대표적으로 OSI 참조 모델이 있음
##### 클라이언트-서버 패턴
* 하나의 서버 컴포넌트와 다수의 클라이언트 컴포넌트로 구성되는 패턴
* 서버는 클라이언트의 요청에 대비해 항상 대기 상태를 유지
* 클라이언트나 서버는 요청과 응답을 받기 위해 동기화되는 경우를 제외하고는 서로 독립적
##### 파이프-필터 패턴
* 파이프 필터 패턴은 데이터 스트림 절차의 각 단계를 필터 컴포넌트로 캡슐화 하여 파이프를 통해 데이터를 전송하는 패턴
* 파이프 필터 패턴은 데이터 변환, 버퍼링, 동기화 등에 주로 사용
* 대표적으로 UNIX의 쉘
##### 모델-뷰-컨트롤러 패턴(MVC)
* 모델 : 서브시스템의 핵심 기능과 데이터를 보관
* 뷰 : 사용자에게 정보를 표시
* 컨트롤러 : 사용자로부터 받은 입력을 처리
* 한 개의 모델에 대해 여러개의 뷰를 필요로 하는 대화형 애플리케이션에 적합함
##### 기타 패턴
* 마스터 슬레이브 패턴 : 장애 허용, 병렬 컴퓨팅에 많이 쓰임
* 브로커 패턴 : 분산 환경 시스템에 주로 활용
* 피어 투 피어 패턴 : 멀티스레딩 방식을 사용
* 이벤트 버스 패턴 
* 블랙보드 패턴
* 인터프리터 패턴

#### 객체지향(Object-Oriented)
* 현실 세계의 개체(Entity)를 기계의 부품처럼 하나의 객체로 만들어, 기계적인 부품들을 조립하여 제품을 만들 듯이 소프트웨어를 개발할 때에도 객체들을 조립해서 작성할 수 있는 기법
* 구조적 기법의 문제점으로 인한 소프트웨어 위기의 해결책으로 채택되어 사용되고 있음
* 재사용 및 확장이 용이하여 고품질의 소프트웨어를 빠르게 개발할 수 있고 유지보수가 쉽다
* 객체, 클래스, 캡슐화, 상속, 다형성이 있다.
##### 객체
* 데이터와 데이터를 처리하는 함수를 묶어 놓은(캡슐화한) 하나의 소프트웨어 모듈
* 데이터 : 속성, 상태, 변수, 상수, 자료구조 라고도 함
* 함수 : 객체가 수행하는 기능으로 객체가 갖는 데이터를 처리하는 알고리즘
###### 객체의 특성
* 객체는 독립적으로 식별 가능한 이름을 가지고 있음
* 조건을 상태(State)라고 하는데, 일반적으로 상태는 시간에 따라 변함
* 객체와 객체는 상호 연관성에 의한 관계가 형성됨
* 객체가 반응할 수 있는 메시지의 집합을 행위라고 하며, 객체는 행위의 특징을 나타냄
* 객체는 일정한 기억장소를 가지고 있음
* 객체의 메소드는 다른 객체로부터 메시지를 받았을 때 정해진 기능을 수행함
##### 클래스
* 공통된 속성과 연산을 갖는 객체의 집합
* 각각의 객체들이 갖는 속성과 연산을 정의하고 있는 틀
* 클래스에 속한 각각의 객체를 인스턴스라 하며, 클래스로부터 새로운 객체를 생성하는 것을 인스턴스화 라고 함
* 최상위 클래스는 상위 클래스를 갖지 않는 클래스를 의미
* 슈퍼 클래스는 특정 클래스의 상위 클래스이고, 서브 클래스는 특정 클래스의 하위 클래스를 의미
##### 캡슐화(Encapsulation)
* 캡슐화는 데이터와 데이터를 처리하는 함수를 하나로 묶는 것을 의미
* 캡슐화된 객체는 인터페이스를 제외한 세부 내용이 은폐(정보 은닉)되어 외부에서의 접근이 제한적이기 때문에 외부 모듈의 변경으로 인한 파급 효과가 적음
* 재사용이 용이함
* 인터페이스가 단순해지고, 객체 간의 결합도가 낮아짐
##### 상속(Inheritance)
* 상속을 이용하면 하위 클래스는 상위 클래스의 모든 속성과 연산을 자신의 클래스내에서 다시 정의하지 않고서도 즉시 자신의 속성으로 사용할 수 있음
* 하위클래스는 상위클래스로부터 상속받은 속성과 연산 외에 새로운 속성과 연산을 첨가하여 사용할 수 있음
* 다중 상속 : 한 개의 클래스가 두 개 이상의 상위 클래스로부터 속성과 연산을 상속받는 것
##### 다형성(Polymorphism)
* 메시지에 의해 객체가 연산을 수행하게 될 때 하나의 메시지에 대해 각각의 객체가 가지고 있는 고유한 방법으로 응답할 수 있는 능력을 의미함
* 동일한 메소드명을 사용하며 같은 의미의 응답을 함
#### 모듈
* 모듈화를 통해 분리된 시스템의 각 기능들로, 서브루틴, 서브시스템, 소프트웨어 내의 프로그램, 작업 단위 등과 같은 의미로 사용됨
* 모듈은 단독으로 컴파일이 가능하며, 재사용 할 수 있음
* 기능적 독립성은 소프트웨어를 구성하는 각 모듈의 기능이 서로 독립됨을 의미하는 것, 모듈이 하나의 기능만을 수행하고 다른 모듈과의 과도한 상호작용을 배제함으로써 이루어짐
* 모듈의 독립성은 결합도와 응집도에 의해 측정됨
* 모듈의 결합도는 약하게, 응집도는 강하게 해야 함
##### 결합도(Coupling)
* 모듈 간에 상호 의존하는 정도 또는 두 모듈 사이의 연관 관계를 의미함
* 결합도가 약할수록 품질이 높고, 강할수록 품질이 낮음
* 자료 결합도
* 스탬프 결합도
* 제어 결합도
* 외부 결합도
* 공통 결합도
* 내용 결합도
##### 응집도(Cohesion)
* 응집도는 정보 은닉 개념을 확장한 것으로 명령어나 호출문 등 모듈의 내부 요소들의 서로 관련되어 있는 정도
* 응집도가 강할수록 품질이 높고, 약할수록 품질이 낮음
* 기능적 응집도
* 순차적 응집도
* 교환적 응집도
* 절차적 응집도
* 시간적 응집도
* 논리적 응집도
* 우연적 응집도
##### 팬인 팬 아웃
* 팬인은 어떤 모듈을 제어하는 모듈의 수 : 들어오는 수
* 팬 아웃은 어떤 모듈에 의해 제어되는 모듈의 수 : 나가는 수
* 시스템의 복잡도를 최적화하려면 팬인은 높게, 팬아웃은 낮게 설계 해야 함
#### 코드
* 컴퓨터를 이용해 자료를 처리하는 과정에서 분류 조합 및 집계를 용이하게 하고, 특정 자료의 추출을 쉽게 하기 위해서 사용하는 기호
* 정보를 신속 정확 명료하게 전달할 수 있음
* 일정한 규칙에 따라 작성되며, 정보 처리의 효율과 처리된 정보의 가치에 많은 영향을 미침
* 주민등록번호, 학번, 전화번호 등이 있음
* 식별 기능, 분류 기능, 배열 기능
##### 코드의 종류
* 순차 코드
* 블록 코드
* 10진 코드
* 그룹 분류 코드
* 연상 코드
* 표의 숫자 코드
* 합성 코드
##### 코드 부여 체계
* 이름만으로 개체의 용도와 적용 범위를 알 수 있도록 코드를 부여하는 방식
* 코드 부여 체계를 담당하는 자는 코드의 자릿수와 구분자, 구조 등을 상세하게 명시해야 함

#### 디자인 패턴
* 모듈들 간의 인터페이스와 같은 코드를 작성하는 수준의 세부적인 구현방안을 설계할 때 참조할 수 있는 전형적인 해결 방식 또는 예제를 의미
* GoF라고 불리는 에릭 감마, 리차드 헬름, 랄프 존슨, 존 블리시디스가 처음으로 구체화 및 체계화함
* 생성 패턴 5개, 구조 패턴7개, 행위 패턴 11개 총 23개의 패턴으로 구성 됨
##### 아키텍처 패턴 vs 디자인 패턴
* 아키텍처 패턴이 더 상위 수준의 설계에 사용됨
* 아키텍처 패턴이 전체 시스템의 구조를 설계하기 위한 참조 모델이라면 디자인 패턴은 서브 시스템에 속하는 컴포넌트들과 그 관계를 설계하기 위한 참조 모델
##### 생성 패턴(Creational Pattern)
* 객체의 생성과 관련된 패턴으로 총 5개의 패턴이 있음
* 객체의 생성과 참조 과정을 캡슐화 하여 객체가 생성되거나 변경되어도 프로그램의 구조에 영향을 크게 받지 않도록 하여 프로그램에 유연성을 더해줌
* 추상 팩토리 : 연관된 서브 클래스를 묶어 한 번에 교체하는 것이 가능함
* 빌더 : 작게 분리된 인스턴스를 건축 하듯이 조합하여 객체를 생성함
* 팩토리 메소드 : 객체 생성을 서브 클래스에서 처리하도록 분리하여 캡슐화한 패턴
* 프로토타입 : 원본 객체를 복제하는 방법으로 객체를 생성하는 패턴
* 싱글톤 : 클래스 내에서 인스턴스가 하나뿐임을 보장하며, 불필요한 메모리 낭비를 최소화 할 수 있음
##### 구조 패턴(Structural Pattern)
* 클래스나 객체들을 조합하여 더 큰 구조로 만들 수 있게 해주는 패턴으로 총 7개의 패턴
* 구조가 복잡한 시스템을 개발하기 쉽게 도와줌
* 어댑터 : 호환성이 없는 클래스들의 인터페이스를 다른 클래스가 이용할 수 있도록 변환해주는 패턴
* 브리지 : 기능과 구현을 두 개의 별도 클래스로 구현
* 컴포지트 : 객체들을 트리 구조로 구성하여 디렉터리 안에 디렉터리가 있듯이 복합 객체 안에 복합 객체가 포함되는 구조를 구현할 수 있음
* 데코레이터 : 객체 간의 결합을 통해 능동적으로 기능들을 확장할 수 있는 패턴
* 퍼싸드 : 복잡한 서브 클래스 들을 피해 더 상위에 인터페이스를 구성함으로써 서브 클래스들의 기능을 간편하게 사용할 수 있도록 하는 패턴
* 플라이웨이트 : 인스턴스가 필요할 때마다 매번 생성하는 것이 아니고 가능한 한 공유해서 사용함으로써 메모리를 절약하는 패턴
* 프록시 : 네트워크 연결, 메모리의 대용량 객체로의 접근 등에 주로 이용
##### 행위 패턴(Behavioral Pattern)
* 클래스나 객체들이 서로 상호작용하는 방법이나 책임 분배 방법을 정의하는 패턴으로 총 11개의 패턴이 있음
* 책임 연쇄 : 요청을 처리할 수 있는 객체가 둘 이상 존재하여 한 객체가 처리하지 못하면 다음 객체로 넘어가는 형태의 패턴
* 커맨드 : 각종 명령어 들을 추상 클래스와 구체 클래스로 분리하여 단순화 함
* 인터프리터 : 언어에 문법 표현을 정의 하는 패턴
* 반복자 : 자료 구조와 같이 접근이 잦은 객체에 대해 동일한 인터페이스를 사용하도록 하는 패턴
* 중재자 : 수많은 객체들 간의 복잡한 상호작용을 캡슐화하여 객체로 정의하는 패턴
* 메멘토 : 특정 시점에서의 객체 내부 상태를 객체화 함으로써 이후 요청에 따라 객체를 해당 시점의 상태로 되돌릴 수 있는 기능을 제공하는 패턴
* 옵서버 : 한 객체의 상태가 변화하면 객체에 상속되어 있는 다른 객체들에게 변화된 상태를 전달하는 패턴
* 상태 : 객체의 상태에 따라 동일한 동작을 다르게 처리해야 할 때 사용하는 패턴
* 전략 : 동일한 계열의 알고리즘들을 개별적으로 캡슐화하여 상호 교환할 수 있게 정의하는 패턴
* 템플릿 메소드 : 상위 클래스에서 골격을 정의하고, 하위 클래스에서 세부 처리를 구체화하는 구조의 패턴
* 방문자 : 분리된 처리 기능은 각 클래스를 방문하여 수행함

### 4. 인터페이스 설계
#### 시스템 인터페이스 요구사항 분석
* 독립적으로 떨어져 있는 시스템들끼리 서로 연동하여 상호작용하기 위한 접속 방법이나 규칙을 의미함
* 인터페이스 이름, 연계 대상 시스템, 연계 범위및 내용, 연계 방식, 송신 데이터, 인터페이스 주기, 기타 고려사항 등이 포함되어야 함
* 요구사항 분석은  요구사항 명세서에서 요구사항을 기능적 요구사항과 비기능적 요구사항으로 분류하고 조직화하여 요구사항 명세를 구체화하고 이를 이해관계자에게 전달하는 일련의 과정
##### 시스템 인터페이스 요구사항 분석 절차
* 1. 소프트웨어 요구사항 목록에서 시스템 인터페이스 관련 요구사항을 선별하여 별도로 시스템 인터페이스 요구사항 목록을 만듦
* 2. 시스템 인터페이스 요구사항과 관련된 자료를 준비함
* 3. 기능적인 요구사항과 비기능적인 요구사항으로 분류함
* 4. 요구사항을 분석하고 내용을 추가하거나 수정함
* 5. 요구사항 명세서와 시스템 인터페이스 요구사항 목록을 관련 이해관계자에게 전달함
#### 인터페이스 요구사항 검증
* 인터페이스의 설계 및 구현 전에 사용자들의 요구사항이 요구사항명세서에 정확하고 완전하게 기술되었는지 검토하고 개발 범위의 기준인 베이스라인을 설정하는 것
* 검토 계획 수립 -> 검토 및 오류 수정 -> 베이스라인 설정 순으로 수행
##### 인터페이스 요구사항 검토 계획 수립
* 검토 기준 및 방법 : 프로젝트의 규모와 참여 인력, 검토 기간 등을 고려하여 검토 기준 및 방법을 정함
* 참여자 : 프로젝트 관리자, 품질관리자, 인터페이스분석가, 소프트웨어 아키텍트, 시스템 사용자, 테스트 관리자  등 요구사항 검토 참여자를 선정함
* 체크리스트 : 요구사항 검토 체크리스트를 작성함
* 관련 자료 : 요구사항 검토에 필요한 자료들을 준비함
* 일정 : 인터페이스 요구사항 검토 일정을 정함
##### 인터페이스 요구사항 검토 및 오류 수정
* 요구사항 검토는 검토 체크리스트의 항목에 따라 인터페이스 요구사항 명세서를 검토하는 것
* 오류가 발견되면 오류를 수정할 수 있도록 오류 목록과 시정 조치서를 작성함
* 오류 수정과 요구사항 승인 절차를 진행할 수 있도록 요구사항 검토 결과를 검토 관련자들에게 전달함
* 시정 조치서를 작성한 경우 시정 조치가 완료되었는지 확인해 시정 조치가 완료되면 인터페이스 요구사항 검토 작업을 완료함
##### 인터페이스 요구사항 베이스라인 설정
* 프로젝트 관리자와 주요 의사 결정자에게 공식적으로 승인 받음
* 소프트웨어 설계 및 구현을 위해 요구사항 명세서의 베이스라인을 설정함
##### 요구사항 검증 방법
* 요구사항 검토 : 동료 검토, 워크스루, 인스펙션
* 프로토타이핑 : 소프트웨어에 대한 견본품을 만들어 최종 결과물을 예측함
* 테스트 설계 : 요구사항은 테스트할 수 있도록 작성되어야 함
* CASE 도구 활용 
##### 인터페이스 요구사항 검증의 주요 항목
* 완전성, 일관성, 명확성, 기능성, 검증 가능성, 추적 가능성, 변경 용이성

#### 인터페이스 방법 명세화
* 내 외부 시스템이 연계하여 작동할 때 인터페이스별 송수신 방법, 송수신 데이터, 오류 식별 및 처리 방안에 대한 내용을 문서로 명확하게 정리하는 것
##### 시스템 연계 기술
* 개발할 시스템과 내외부 시스템을 연계할 때 사용되는 기술을 의미
* DB Link
* API/Open API
* 연계 솔루션 : EAI 서버
* Socket
* Web Service : WSDL, UDDI, SOAP
##### 인터페이스 통신 유형
* 개발할 시스템과 내 외부 시스템 간 데이터를 송 수신하는 형태를 의미
* 단방향 : 시스템에서 거래를 요청만 하고 응답이 없는 방식
* 동기 : 시스템에서 거래를 요청하고 응답이 올 때까지 대기 하는 방식
* 비동기 : 시스템에서 거래를 요청하고 다른 작업을 수행하다 응답이 오면 처리하는 방식
##### 인터페이스 처리 유형
* 송수신 데이터를 어떤 형태로 처리할 것인지에 대한 방식을 의미함
* 실시간 방식 : 사용자가 요청한 내용을 바로 처리
* 지연 처리 방식 : 데이터를 매건 단위로 처리, 비용이 많이 발생할 때 처리
* 배치 방식 : 대량의 데이터를 처리
##### 인터페이스 발생 주기
* 개발할 시스템과 내 외부 시스템 간 송 수신 데이터가 전송되어 인터페이스가 사용되는 주기를 의미
 #### 미들웨어 솔루션 명세
##### 미들웨어의 개념 및 종류
* 운영체제가 제공하는 서비스 이외에 추가적인 서비스를 제공하는 소프트웨어
* 표준화된 인터페이스를 제공함으로써 시스템 간의 데이터 교환에 일관성을 보장함
* 통신 제공 방법이나 기능에 따라 DB, RPC, MOM, TP-Monitor, ORB, WAS 등으로 구분됨
##### DB(DataBase)
* 데이터베이스 벤더에서 제공하는 클라이언트에서 원격의 데이터베이스와 연결하기 위한 미들웨어
* 2-Tier 아키텍처라고 함, ODBC, IDAPI, Glue 등이 있음
##### RPC(Remote Procedure Call)
* 응용프로그램의 프로시저를 사용해 원격 프로시저를 마치 로컬 프로시저처럼 호출하는 방식의 미들웨어
##### MOM(Message Oriented Middleware)
* 메시지 기반의 비동기형 메시지를 전달하는 방식의 미들웨어
* MQ, Message Q, JMS 등이 있음
##### TP-Monitor(Transaction Processing Monitor)
* 온라인 트랜잭션 업무에서 트랜잭션을 처리 및 감시하는 미들웨어
* tuxedo, tmax등이 있음
##### ORB(Object Request Broker)
* 객체 지향 미들웨어로 코바 표준 스펙을 구현한 미들 웨어
* Orbix, CORBA등이 있음
##### WAS(Web Application Server)
* 웹 서버와 달리 사용자의 요구에 따라 변하는 동적인 콘텐츠를 처리하기 위해 사용되는 미들 웨어
* WebLogic, WebSphere 등이 있음
##### 미들웨어 솔루션 식별
* 개발 및 운영 환경에 사용될 미들웨어 솔루션을 확인하고 목록을 작성하는 것
* 솔루션의 시스템, 구분, 솔루션명, 버전, 제조사 등의 정보를 정리한 미들웨어 솔루션 목록을 작성함
* 이해관계자 등에게 전달해 오류 및 누락을 확인하고 수정함
##### 미들웨어 솔루션 명세서 작성
* 미들웨어 솔루션별로 관련정보들을 상세하게 기술하는 것
## 2. 소프트웨어 개발
### 1. 데이터 입출력 구현
#### 자료 구조
* 자료 구조는 프로그램에서 사용하기 위한 자료를 기억장치의 공간 내에 저장하는 방법과 저장된 그룹 내에 존재하는 자료 간의 관계, 처리 방법 등을 연구 분석하는 것을 말함
* 자료구조는 자료의 표현과 그것과 관련된 연산
* 일련의 자료들을 조직하고 구조화하는 것
* 자료구조에서도 필요한 모든 연산들을 처리할 수 있음
* 자료구조에 따라 프로그램 실행시간이 달라짐
##### 자료 구조의 분류
* 선형 구조 : 배열, 선형 리스트(연속 리스트, 연결 리스트), 스택, 큐, 데크
* 비선형 구조 : 트리, 그래프
##### 배열(Array)
* 동일한 자료형의 데이터들이 같은 크기로 나열되어 순서를 갖고 있는 집합임
* 정적인 자료 구조로 기억 장소의 추가가 어렵고, 데이터 삭제 시 데어터가 저장되어 있던 기억장소는 빈 공간으로 남아있어 메모리의 낭비가 발생함
* 배열의 첨자를 이용해 데이터에 접근
* 반복적인 데이터 처리 작업에 적합한 구조
* 데이터마다 동일한 이름의 변수를 사용해 처리가 간편
* 사용한 첨자의 개수에 따라 n 차원 배열이라고 부름
##### 선형 리스트(Linear List)
* 일정한 순서에 의해 낭려된 자료 구조
* 연속 리스트와 포인터를 이용하는 연결 리스트로 구분 됨
* 연속 리스트(Contiguous List) : 배열과 같이 연속되는 기억장소에 저장되는 자료 구조
* 이용효율은 밀도가 1로서 가장 좋음
* 연속리스트는 중간에 데이터를 삽입하기 위해서 연속된 빈 공간이 있어야 하며, 삽입 삭제 시 자료의 이동이 필요함
* 연결 리스트(Linked List) : 노드의 포인터 부분을 이용해 서로 연결시킨 자료 구조
* 연결리스트는 노드의 삽입 삭제 작업이 용이함
* 기억 공간이 연속적으로 놓여 있지 않아도 저장할 수 있음
* 순차리스트에 비해 기억 공간의 이용 효율이 좋지 않음
* 접근속도가 느림
* 중간 노드 연결이 끊어지면 그 다음 노드를 찾기 힘듬
##### Stack
* 리스트의 한 쪽 끝으로만 자료 삽입, 삭제 작업이 이루어지는 자료 구조
* LIFO방식으로 자료를 처리
* 꽉 채워져 있는 상태에서 데이터가 삽입되면 오버플로우가 발생하며, 더 이상 삭제할 데이터가 없는 상태에서 데이터를 삭제하면 언더플로우가 발생함
* TOP : 스택으로 할당된 기억 공간에 가장 마지막으로 삽입된 자료가 기억된 위치를 가리킴
* Bottom : 스택의 가장 밑 바닥
##### Queue
* 리스트의 한쪽에서는 삽입 작업이 이루어지고 한쪽에서는 삭제 작업이 이루어짐
* FIFO 방식으로 처리함
* 시작과 끝을 표시하는 두 개의 포인터가 있음
* 프런트 포인터 : 가장 먼저 삽입된 자료의 공간을 가리키는 포인터로 삭제할 때 사용
* 리어 포인터 : 가장 마지막에 삽입된 자료가 위차한 기억 공간을 가리키는 포인터, 삽입 작업할 때 사용
* 큐는 운영체제 작업 스케줄링에 사용
##### Tree
* 정점과 선분을 가지고 사이클이 이루어 지지 않도록 구성한 그래프의 특수한 형태
* 트리는 하나의 기억 공간을 노드라고 하며 노드와 노드를 연결하는 선을 링크라고 함

#### 데이터저장소/ 데이터베이스/ DBMS
##### 데이터저장소
* 소프트웨어 개발 과정에서 다루어야 할 데이터들을 논리적인 구조로 조직화하거나, 물리적인 공간에 구축한 것을 의미함
* 논리 데이터저장소와 물리 데이터 저장소로 구분됨
* 논리 데이터저장소는 데이터 및 데이터 간의 연관성, 제약조건을 식별하여 논리적인 구조로 조직화 한 것을 의미
* 물리 데이터저장소는 논리 데이터저장소에 저장된 데이터와 구조들을 소프트웨어가 운용될 환경의 물리적 특성을 고려해 하드웨어적인 저장장치에 저장한 것을 의미
* 논리 데이터저장소를 거쳐 물리 데이터저장소를 구축하는 과정은 데이터베이스를 구축하는 과정과 동일
##### 데이터베이스
* 특정 조직의 업무를 수행하는 데 필요한 상호 관련된 데이터들의 모임
* 통합된 데이터(Integrated Data) 
* 저장된 데이터(Stored Data)
* 운영 데이터(Operational Data)
* 공용 데이터(Shared Data)
##### DBMS(DataBase Management System)
* 사용자와 데이터베이스 사이에서 사용자의 요구에 따라 정보를 생성해주고, 데이터베이스를 관리해 주는 소프트웨어
* 정의(Definition), 조작(Manipulation), 제어(Control) 기능이 있음
* 정의 기능 : 데이터의 Type과 구조에 대한 정의, 이용 방식, 제약 조건등을 명시하는 기능
* 조작 기능 : 데이터 검색, 갱신, 삽입, 삭제
* 제어 기능 : 허가된 데이터만 접근할 수 있도록 보안을 유지하고 권한을 검사할 수 있어야 함
##### DBMS의 장단점
* 장점 : 데이터의 일관성, 무결성 등등을 유지할 수 있음
* 단점 : 전산화 비용이 증가, 파일의 백업과 회복이 어려움
#### 데이터 입출력
* 소프트웨어 기능 구현을 위해 데이터베이스에 데이터를 입력하거나 데이터베이스의 데이터를 출력하는 작업을 의미
##### SQL(Structured Query Language)
* 관계형 데이터베이스를 지원하는 언어로 채택하고 있음
* 관계 대수와 관계 해석을 기초로한 혼합 데이터 언어
* DDL(데이터 정의어)
* DML(데이터 조작어)
* DCL(데이터 제어어)
##### 데이터 접속(Data Mapping)
* 소프트웨어의 기능 구현을 위해 프로그래밍 코드와 데이터베이스의 데이터를 연결하는 것을 말함
* SQL Mapping : 프로그래밍 코드 내에 SQL을 직접 입력해 DBMS의 데이터에 접속하는 기술 JDBC, ODBC, MyBatis등이 있음
* ORM(Object Relational Mapping) : 객체지향 프로그래밍의 객체와 관계형 데이터베이스의 데이터를 연결하는 기술, JPA, Hibernate, Django
##### 트랜잭션(Transaction)
* 데이터베이스의 상태를 변환시키는 하나의 논리적 기능을 수행하기 위한 작업의 단위 또는 한꺼번에 모두 수행되어야 할 일련의 연산들을 의미
* COMMIT : 트랜잭션 처리가 정상적으로 종료되어 트랜잭션이 수행한 변경 내용을 데이터베이스에 반영하는 명령어
* ROLLBACK : 모든 변경 작업을 취소하고 이전 상태로 되돌리는 연산
* SAVEPOINT(=CHECKPOINT) : 트랜잭션 내에 ROLLBACK 할 위치인 저장점을 지정함
#### 절차형 SQL
* 연속적인 실행이나 분기, 반복 등의 제어가 가능한 SQL을 의미
* 일반적인 프로그래밍 언어에 비해 효율은 떨어지지만 단일 SQL 문장으로 처리하기 어려운 연속적인 작업들을 처리하는데 적합함
* BEGIN ~ END 형식으로 작성되는 블록 구조로 되어 있기 때문에 기능별 모듈화가 가능함
* 프로시저 : 특정 기능을 수행하는 일종의 트랜잭션 언어로 호출을 통해 실행되어 미리 저장해 놓은 SQL 작업을 수행함
* 트리거 : 데이터베이스 시스템에서 데이터의 입력, 갱신, 삭제 등의 이벤트가 발생할 때마다 관련 작어비 자동으로 수행됨
* 사용자 정의 함수 : 프로시저와 유사하게 SQL을 사용하여 일련의 작업을 연속적으로 처리하며, 종료 시 예약어 Return을 통해 처리결과를 단일값으로 반환 함
##### 절차형 SQL의 테스트와 디버깅
* 디버깅을 통해 기능의적합성 여부를 검증하고, 실행을 통해 결과를 확인하는 테스트 과정을 수행함
* 테스트 전에 생성을 통해 구문 오류나 참조 오류의 존재 여부를 확인함
* 많은 코드로 구성된 절차형 SQL의 특성상 오류 및 경고 메시지가 상세히 출력되지 않으므로 SHOW 명령어를 통해 내용을 확인하고 문제를 수정함
* 정상적으로 생성도니 절차형 SQL은 디버깅을 통해 로직을 검증하고, 결과를 통해 최종적으로 확인함
##### 쿼리 성능 최적화
* 데이터 입출력 애플리케이션의 성능 향상을 위해 SQL 코드를 최적화 하는 것
* 성능을 최적화 하기 전에 성능 측정 도구인 APM을 사용해 최적화 할 쿼리를 선정 해야 함
* 옵티마이저가 수립한 실행 계획을 검토하고 SQL 코드와 인덱스를 재구성함
### 2. 통합 구현
#### 단위 모듈 테스트
* 프로그램 단위 기능을 구현하는 모듈이 정해진 기능을 정확히 수행하는지 검증하는 것
* 단위 테스트라고도 하며 화이트박스 테스트와 블랙박스 테스트 기법을 사용함
* 모듈의 통합 이후에는 오랜시간 추적해야 발견할 수 있는 에러들로 단위 모듈 테스트를 수행하면 쉽게 발견하고 수정할 수 있음
##### 테스트 케이스
* 구현된 소프트웨어가 사용자의 요구사항을 정확하게 준수 했는지를 확인하기 위해 설계된 입력 값, 실행 조건, 기대 결과 등으로 구성된 테스트 항목에 대한 명세서로, 명세 기반 테스트의 설계 산출물에 해당됨
* 테스트에 필요한 입력 데이터, 테스트 조건, 예상 결과 등을 모아 테스트 케이스를 만듬
* ISO/IEC/IEEE 29119-3 표준에 따른 텥스트 케이스의 구성요소
* 식별자, 테스트 항목, 입력 명세, 출력 명세, 환경 설정, 특수 절차 요구, 의존성 기술
##### 테스트 프로세스
1. 계획 및 제어 단계 : 목표를 달성하기 위한 계획을 수립하고, 계획대로 진행 되도록 제어하는 단계
2. 분석 및 설계 단계 : 목표를 구체화하여 테스트 시나리오와 테스트 케이스를 작성하는 단계
3. 구현 및 실현 단계 : 효율적인 테스트 수행을 위해 테스트 케이스들을 조합, 테스트 프로시저에 명세하는 단계, 모듈의 환경에 적합한 단위 테스트 도구를 이용해 테스트를 수행하는 단계
4. 평가 단계 : 테스트가 계획과 목표에 맞게 수행되었는지 평가하고 기록하는 단계
5. 완료 단계 : 이후의 테스트를 위한 참고 자료 및 테스트 수행에 대한 증거 자료로 활용하기 위해 수행 과정과 산출물을 기록 및 저장하는 단계
#### 개발 지원 도구
##### 통합 개발 환경(IDE)
* 개발에 필요한 환경, 즉 편집기, 컴파일러 등의 다양한 툴을 하나의 인터페이스로 통합하여 제공하는 것을 의미
* 이클립스, 비주얼 스튜디오, 엑스코드, 안드로이드 스튜디오, IDEA
##### 빌드 도구
* 소스 코드를 소프트웨어로 변환하는 과정에 필요한 전처리, 컴파일 등의 작업들을 수행하는 소프트웨어를 말함
* Ant, Maven, Gralde 등이 있음
##### 기타 협업 도구
* 개발에 참여하는 사람들이 서로 다른 작업 환경에서 원활히 프로젝트를 수행할 수 있도록 도와주는 도구로 협업 소프트웨어, 그룹웨어 등으로 불림
* 프로젝트 및 일정 관리 : 구글 캘린더, 지라, 플로우 등
* 정보 공유 및 커뮤니케이션 : 슬랙, 잔디, 태스크월드 등
* 디자인 : 스케치, 제플린 등
* 기타 : 에버노트, 스웨거, 깃허브 등

### 3. 제품 소프트웨어 패키징
#### 소프트웨어 패키징
* 개발자가 아니라 사용자를 중심으로 진행
* 모듈화하여 패키징
* 손쉽게 사용할 수 있도록 일반적인 배포 형태로 패키징
* 사용자를 중심으로 진행되는 작업이므로 사용자의 편의성 및 실행 환경을 우선적으로 고려해야 함
##### 패키징 시 고려사항
* 운영체제, CPU, 메모리 등에 필요한 초쇠환경을 정의함
* UI는 사용자가 눈으로 직접 확인할 수 있도록 시각적인 자료와 함께 제공하고 매뉴얼과 일치시켜 패키징 함
* Managed Service 형태로 제공하는 것이 좋음
* 고객의 편의성을 고려한 안정적인 배포가 중요
* 패키징의 변경 및 개선에 대한 관리를 항상 고려함
##### 패키징 작업 순서
기능 식별(작성된 코드의 기능 확인) -> 모듈화(코드들을 분류) -> 빌드 진행 -> 사용자 환경 분석 -> 패키징 및 적용 시험 -> 패키징 변경 개선 -> 배포
#### 릴리즈 노트 작성
* 개발과정에서 정리된 릴리즈 정보를 소프트웨어의 최종 사용자인 고객과 공유하기 위한 문서
* 소프트웨어 사양에 대한 개발팀의 정확한 준수 여부를 확인할 수 있음
* 소프트웨어에 포함된 전체 기능, 서비스의 내용, 개선 사항 등을 사용자와 공유할 수 있음
* 소프트웨어의 초기 배포 시 또는 출시 후 개선 사항을 적용한 추가 배포시에 제공함
##### 릴리즈 노트 초기 버전 작성 시 고려사항
* 릴리즈 노트는 정확하고 완전한 정보를 기반으로 개발팀에서 직접 현재 시제로 작성해야 함
* 신규 소스, 빌드 등의 이력이 정확하게 관리되어 변경 또는 개선된 항목에 대한 이력 정보들도 작성되어야 함
* Header(머릿말), 개요, 목적, 문제 요약, 재현 항목, 수정/개선 내용, 사용자 영향도, SW 지원 영향도, 노트, 면책 조항, 연락처
##### 릴리즈 노트 추가 버전 작성 시 고려사항
* 소프트웨어의 테스트 과정에서 베타 버전이 출시되거나 긴급한 버그 수정, 업그레이드와 같은 자체 기능 향상, 사용자 요청 등의 특수한 상황이 발생하는 경우 릴리즈 노트를 추가로 작성 함
##### 릴리즈 노트 작성 순서
* 모듈 식별 -> 릴리즈 정보 확인 -> 릴리즈 노트 개요 작성 -> 영향도 체크 -> 정식 릴리즈 노트 작성 -> 추가 개선 항목 식별
#### 디지털 저작권 관리(DRM)
* 컴퓨터 프로그램 저작물 등에 대해 창작자가 가지는 배타적 독점적 권리로 타인의 침해를 받지 않을 고유한 권한
* 불법 복제 및 배포등을 막기 위한 기술적인 방법을 통칭해 저작권 보호 기술이라고 함
#### Digital Right Management의 개요
* 저작권자가 의도한 용도로만 사용되도록 디지털 콘텐츠의 생성, 유통, 이용까지의 전 과정에 걸쳐 사용되는 디지털 콘텐츠 관리 및 보호 기술임
* 아날로그인 경우에는 디지털로 변환 후 패키저에 의해 DRM 패키징을 수행함
* 콘텐츠의 크기에 따라 음원이나 문서와 같이 크기가 작은 경우에는 사용자가 콘텐츠를 요청하는 시점에서 실시간으로 패키징을 수행하고, 크기가 큰 경우에는 미리 패키징을 수행한 후 배포함
* 저작권자의 전자 서명이 포함되고 저작권자가 설정한 라이선스 정보가 클리어링 하우스에 등록됨
##### 디지털 저작권 관리의 흐름도
* 클리어링 하우스(Clearing House) : 저작권자에 대한 사용 권한, 라이선스 발급, 사용량에 따른 결제 관리 등을 수행하는 곳
* 콘텐츠 제공자(Contents Provider) : 콘텐츠를 제공하는 저작권자
* 패키저(Packager) : 콘텐츠를 메타 데이터와 함께 배포 가능한 형태로 묶어 암호화하는 프로그램
* 콘텐츠 분배자(Contents Distributor) : 암호화된 콘텐츠를 유통하는 곳이나 사람
* 콘텐츠 소비자(Customer) : 콘텐츠를 구매해서 사용하는 주체
* DRM 컨트롤러(DRM Controller) : 배포된 콘텐츠의 이용 권한을 통제하는 프로그램
* 보안 컨테이너(Security Container) : 콘텐츠 원본을 안전하게 유통하기 위한 전자적 보안 장치
#### 소프트웨어 버전 등록
##### 소프트웨어 패키징의 형상 관리
* 형상 관리(SCM)는 소프트웨어의 개발 과정에서 소프트웨어의 변경 사항을 관리하기 위해 개발된 일련의 활동임
* 변경의 원인을 알아내고 제어하며, 적절히 변경되고 있는지 확인하여 해당 담당자에게 통보함
* 형상 관리는 소프트웨어 개발의 전 단계에 적용되는 활동이며, 유지보수 단계에서도 수행 됨
* 형상 관리는 소프트웨어 개발의 전체 비용을 줄이고, 개발 과정의 여러 방해 요인이 최소화되도록 보증하는 것을 목적으로 함
##### 형상 관리의 중요성
* 지속적인 소프트웨어의 변경 사항을 체계적으로 추적하고 통제할 수 있음
* 제품 소프트웨어에 대한 무절제한 변경을 방지할 수 있음
* 발견된 버그나 수정 사항을 추적할 수 있음
* 진행 정도를 확인하기 위한 기준으로 사용될 수 있음
##### 형상 관리 기능
* 형상 식별 : 이름과 관리 번호를 부여하고, 계층 구조로 구분하여 수정 및 추적이 용이하도록 하는 작업
* 버전 제어 : 소프트웨어 업그레이드나 유지 보수 과정에서 생성된 다른 버전의 형상 항목을 관리하고, 이를 위해 특정 절차와 도구를 결합시키는 작업
* 형상 통제(변경 관리) : 현재의 BaseLine이 잘 반영될 수 있도록 조정하는 작업
* 형상 감사 : 기준선의 무결성을 평가하기 위해 확인, 검증, 검열 과정을 통해 공식적으로 승인하는 작업
* 형상 기록(상태 보고) : 형상의 식별, 통제, 감사 작업의 결과를 기록 관리하고 보고서를 작성하는 작업
##### 소프트웨어의 버전 등록 관련 주요 용어 및 버전 등록 과정
* 저장소, 가져오기, 체크아웃, 체크인, 커밋, 동기화
* 가져오기(Import) -> 인출(Check-Out) -> 예치(Commit) -> 동기화(Update) -> 차이(Diff)
#### 소프트웨어 버전 관리 도구
##### 공유 폴더 방식
* 버전 관리 자료가 로컬 컴퓨터의 공유 폴더에 저장되어 관리되는 방식
* 개발이 완료된 파일을 약속된 공유 폴더에 매일 복사함
* 공유 폴더의 파일을 자기 PC로 복사한 후 컴파일 하여 이상 유무를 확인 함
* 오류가 확인되면 해당 파일을 등록한 개발자에게 수정을 으뢰
* 파일에 이상이 없다면 다음날 각 개발자들이 동작 여부를 다시 확인
* 데이터베이스에 기록하여 관리
* SCCS, RCS, PVCS, QVCS 등이 있음
##### 클라이언트/서버 방식
* 버전 관리 자료가 중앙 시스템(서버)에 저장되어 관리되는 방식
* 서버의 자료를 개발자별로 자신의 PC로 복사해 작업한 후 변경된 내용을 서버에 반영
* 모든 버전관리는 서버에서 수행
* 하나의 파일을 서로 다른 개발자가 작업할 경우 경고 메시지를 출력
* 서버에 문제가 생기면 서버가 복구되기 전까지 다른 개발자와의 협업 및 버전 관리 작업은 중단됨
* 대표적으로 SVN 등이 있음

##### 분산 저장소 방식
* 버전 관리 자료가 하나의 원격 저장소와 분산된 개발자 PC의 로컬 저장소에 함께 저장되어 관리되는 방식
* 대표적으로 Git이 있음
##### Subversion(SVN)
* 클라이언트/서버 구조로, 서버(저장소, Repository)에는 최신 버전의 파일들과 변경 내역이 관리됨
* 서버의 자료를 클라이언트로 복사해와 작업한 후 변경 내용을 서버에 Commit함
* 모든 개발 작업은 trunk 디렉터리에서 수행되며, 추가 작업은 branches 디렉터리 안에 별도의 디레터리를 만들어 작업을 완료한 후 trunk 디레터리와 병합함
* Commit할 때마다 리비전이 1씩 증가함
* 클라이언트는 대부분의 운영체제에서 사용되지만, 서버는 주로 유닉스를 사용함
* 소스가 오픈되어 있어 무료로 사용할 수 있음
* 서버에서 check-out해와 작업 완료 후 서버에 commit 하는 방식
##### Git
* 분산 버전 관리 시스템으로 2ㅐ의 저장소, 로컬 저장소와 원격 저장솨 존재함
* 지역 저장소는 개발자들이 실제 개발을 진행하는 장소로 버전 관리가 수행됨
* 원격 저장소는 여러 사람들이 협업을 위해 버전을 공동 관리하는 곳
* 버전관리가 지역 저장소에서 진행되므로 버전 관리가 신속하게 처리되고, 원격 저장소나 네트워크에 문제가 있어도 작업이 가능함
* 브랜치를 이용하면 기본 버전 관리 틀에 영향을 주지 않으면서 다양한 형태의 기능 테스팅이 가능함
* fetch, push, clone 등 사용
#### 빌드 자동화 도구
* 소스 코드 파일들을 컴파일한 후 여러 개의 모듈을 묶어 실행 파일로 만드는 과정
* 애자일 환경에서는 하나의 작업이 마무리될 때마다 모듈 단위로 나눠서 개발된 코드들이 지속적으로 통합되는데, 이러한 지속적인 통합 개발 환경에서 빌드 자동화 도구는 유용하게 활용됨
* Ant, Make, Maven, Gradle, Jenkins 등이 있음
##### Jenkins
* Java 기반 오픈소스 형태
* 서블릿 컨테이너에서 실행되는 서버 기반 도구
* SVN, Git 등 대부분의 형상 관리 도구와 연동 가능
* 친숙한 Web GUI 제공으로 사용이 쉬움
* 분산 빌드나 테스트가 가능함
##### Gradle
* Groovy를 기반으로 한 오픈 소스 형태의 자동화 도구
* 안드로이드 앱 개발 환경에서 사용
* Java, C/C++, Python 등의 언어도 빌드 가능
* DSL을 스크립트 언어로 사용
* 실행할 처리 명령들을 모아 태스크로 만든 후 태스크 단위로 실행함
* 빌드 캐시 기능을 지원하므로 빌드의 속도를 향상 시킬 수 있음

### 4. 애플리케이션 테스트 관리
#### 애플리케이션 테스트
* 애플리케이션에 잠재되어 있는 결함을 찾아내는 일련의 행위
* 고객의 요구사항을 만족시키는지 확인(Validation)하고 소프트웨어가 기능을 정확히 수행하는지 검증(Verification)함
##### 애플리케이션 테스트의 필요성
* 프로그램 실행 전에 오류를 발견해 예방할 수 있음
* 제품의 신뢰도를 향상시킴
* 개발 초기부터 애플리케이션 테스트를 계획하고 시작하면 단순한 오류 발견뿐만 아니라 새로운 오류의 유입도 예방할 수 있음
* 최소한의 시간과 노력으로 많은 결함을 찾을 수 있음
##### 애플리케이션 테스트의 기본 원리
* 완벽한 소프트웨어 테스팅은 불가능함
* 특정 모듈에 집중 되어 있음, 파레토 법칙을 적용하기도 함
* 살충제 패러독스(Pesticide Paradox)  현상이 발생함
* 테스트 케이스를 지속적으로 보완 및 개선해야 함
* 정황에 따라 테스트를 다르게 수행해야 함
* 결함을 모두 제거해도 사용자의 요구사항을 만족시키지 못하면 해당 소프트웨어는 품질이 높다고 말할 수 없음. -부재의 궤변(Absence of Errors Fallacy)
* 테스트와 위험은 반비례함
* 작은 부분에서 시작해 점점 확대하며 진행함
* 개발자와 관계없는 별도의 팀에서 수행해야 함
#### 애플리케이션 테스트의 분류
##### 프로그램 실행 여부에 따른 테스트
* 정적 테스트 : 프로그램을 실행하지 않고 명세서나 소스 코드를 대상으로 분석 - 워크스루, 인스펙션, 코드 검사 등
* 동적 테스트 : 프로그램을 실행하여 오류를 찾는 테스트로, 소프트웨어 개발의 모든 단계에서 테스트를 수행할 수 있음 - 블랙박스 테스트, 화이트박스 테스트
##### 테스트 기반에 따른 테스트
* 명세 기반 테스트 : 사용자의 요구사항에 대한 명세를 빠짐없이 테스트 케이스로 만들어 구현하고 있는지 확인하는 테스트 - 동등 분할, 경계 값 분석
* 구조 기반 테스트 : 내부의 논리 흐름에 따라 테스트 케이스를 작성하고 확인하는 테스트 - 구문 기반, 결정 기반, 조건 기반, 결정 기반 등
* 경험 기반 테스트 : 유사 소프트웨어나 기술 등에 대한 테스터의 경험을 기반으로 수행하는 테스트 - 에러 추정, 체크리스트, 탐색적 테스팅
##### 시각에 따른 테스트
* 누구를 기준으로 하느냐에 따라 검증(Verification) 테스트와 확인(Validation)으로 나뉨
* 검증(Verification) 테스트 : 개발자의 시각
* 확인(Validation) 테스트 : 사용자의 시각
##### 목적에 따른 테스트
* 회복 테스트
* 안전 테스트
* 강도 테스트
* 성능 테스트
* 구조 테스트
* 회귀 테스트
* 병행 테스트
#### 테스트 기법에 따른 애플리케이션 테스트
##### 화이트박스 테스트
* 논리적인 모든 경로를 테스트하여 테스트 케이스를 설계하는 방법
* 설계된 절차에 초점을 둔 구조적 테스트로 테스트 과정의 초기에 적용됨
* 모듈 안의 작동을 직접 관찰함
* 원시 코드의 모든 문장을 한 번이상 실행함으로써 수행됨
* 프로그램의 제어 구조에 따라 선택, 반복 등의 분기점 부분들을 수행함으로써 논리적 경로를 제어함
* 기초 경로 검사 : 대표적인 화이트박스 테스트 기법
* 제어 구조 검사 : 조건검사, 루프 검사, 데이터 흐름 검사
##### 화이트박스 테스트의 검증 기준
* 문장 검증 기준 : 소스 코드의 모든 구문이 한 번 이상 수행되도록 테스트 케이스 설계
* 분기 검증 기준 : 소스 코드의 모든 조건문이 한 번 이상 수행되도록 테스트 케이스 설계
* 조건 검증 기준 : 소스 코드의 모든 조건문에 대해 조건이 True인 경우와 False인 경우가 한 번 이상 수행되도록 테스트 케이스 설계
* 분기/조건 기준 : 소스코드의 모든 조건문과 각 조건문에 포함된 개별 조건식의 결과가 True인 경우와 False인 경우가 한 번 이상 수행되도록 테스트 케이스 설계
##### 검증 기준(Coverage)의 종류
* 기능 기반 커버리지 : 실제 테스트가 수행된 기능의 수/ 전체 기능의 수
* 라인 커버리지 : 테스트 시나리오가 수행한 소스 코드의 라인 수 / 전체 소스 코드의 라인 수
* 코드 커버리지 : 소스 코드의 구문, 분기, 조건 등의 구조 코드 자체가 얼마나 테스트 되었는지를 측정하는 방법
##### 블랙박스 테스트
* 각 기능이 완전히 작동되는 것을 입증하는 테스트로, 기능 테스트 라고도 함
* 주로 구현된 기능을 테스트 함
* 인터페이스에서 실시되는 테스트
* 테스트 과정의 후반부에 적용됨
##### 블랙박스 테스트의 종류
* 동치 분할 검사 : 입력 조건에 타당한 입력 자료와 타당하지 않은 입력 자료의 개수를 균등하게 하여 테스트 케이스를 정하고, 해당 입력 자료에 맞는 결과가 출력되는지 확인하는 기법
* 경계값 분석 : 동치분할 기법을 보완하기 위한 기법
* 원인 효과 그래프 검사 : 입력 데이터 간의 관계와 출력에 영향을 미치는 상황을 체계적으로 분석한 다음 효용성이 높은 테스트 케이스를 선정하여 검사하는 기법
* 오류 예측 검사 : 과거의 경험이나 확인자의 감각으로 테스트하는 기법
* 비교 검사 : 여러 버전의 프로그램에 동일한 테스트 자료를 제공해 동일한 결과가 출력되는지 테스트 하는 기법
#### 개발 단계에 따른 애플리케이션 테스트
* 소프트웨어의 개발 단계에 따라 단위 테스트, 통합 테스트, 시스템 테스트, 인수 테스트로 분류됨
* 요구사항 -> 분석 -> 설계 -> 구현 -> 단위 테스트 -> 통합 테스트 -> 시스템 테스트 -> 인수 테스트
##### 단위 테스트(Unit Test)
* 단위 테스트는 코딩 직후 소프트웨어 설계의 최소 단위인 모듈이나 컴포넌트에 초점을 맞춰 테스트 하는 것
* 구조 기반 테스트 : 화이트 박스 테스트 시행, 제어흐름, 조건 결정
* 명세 기반 테스트 : 목적 및 실행 코드 기반의 블랙박스 테스트 시행, 동등 분할, 경계 값 분석
##### 통합 테스트(Integration Test)
* 단위 테스트가 완료된 모듈들을 결합해 하나의 시스템으로 완성시키는 과정에서의 테스트를 의미
##### 시스템 테스트(System Test)
* 개발된 소프트웨어가 해당 컴퓨터 시스템에서 완벽하게 수행되는가를 점검하는 테스트
* 기능적 요구사항 : 블랙박스 테스트 시행
* 비기능적 요구사항  : 화이트박스 테스트 시행
##### 인수 테스트(Acceptance Test)
* 개발한 소프트웨어가 사용자의 요구사항을 충족하는지에 중점을 두고 테스트하는 방법
* 사용자 인수 테스트 : 사용자가 시스템 사용의 적절성 여부를 확인
* 운영상의 인수 테스트 : 시스템 관리자가 시스템 인수 시 수행하는 테스트 기법
* 계약 인수 테스트
* 규정 인수 테스트
* 알파 테스트
* 베타 테스트
#### 통합 테스트
* 단위 테스트가 끝난 모듈을 통합하는 과정에서 발생하는 오류 및 결함을 찾는 테스트 기법
* 비점진적 통합 방식 : 단계적으로 통합하는 절차 없이 모든 모듈이 미리 결합되어 있는 프로그램 전체를 테스트하는 방법
* 점진적 통합 방식 : 모듈 단위로 단계적으로 통합하면서 테스트하는 방법으로 하향식 상향식 혼합식 통합 방식이 있음, 오류 수정이 용이함
##### 하향식 통합 테스트(Top Down Integration Test)
* 상위 모듈에서 하위 모듈 방향으로 통합하면서 테스트하는 기법
* 주요 제어 모듈은 작성된 프로그램을 사용하고, 주요 제어 모듈의 종속 모듈들은 스텁으로 대체함
* 깊이 우선 또는 넓이 우선 등의 통합 방식에 따라 하위 모듈인 스텁들이 한 번에 하나씩 실제 모듈로 교체됨
* 모듈이 통합될 때마다 테스트를 실시함
* 새로운 오류가 발생하지 않음을 보증하기 위해 회귀 테스트를 실시함
##### 상향식 통합 테스트(Bottom up Integration Test)
* 하위 모듈에서 상위 모듈 방향으로 통합하면서 테스트하는 기법
* 하나의 주요 제어 모듈과 관련된 종속 모듈의 그룹인 클러스터가 필요함
* 하위 모듈들을 클러스터로 결합함
* 상위 모듈에서 데이터의 입출력을 확인하기 위해 더미 모듈인 드라이버를 작성함
* 통합된 클러스터 단위로 테스트함
* 테스트가 완료되면 클러스터는 프로그램 구조의 상위로 이동해 결합하고 드라이버는 실제 모듈로 대체됨
##### 혼합식 통합 테스트
* 하위 수준에서는 상향식 통합, 상위 수준에서는 하향식 통합, 샌드위치식 통합테스트 방법이라고도 함
##### 회귀 테스팅(Regression Testing)
* 회귀 테스트는 이미 테스트된 프로그램의 테스팅을 반복하는 것, 새로운 오류가 있는지 확인하는 테스트
* 기존 테스트 케이스 중 변경된 부분을 테스트할 수 있는 테스트 케이스만을 선정해 수행함
* 모든 애플리케이션 기능을 수행할 수 있는 대표적인 테스트케이스를 선정함
* 파급 효과를 분석해 파급 효과가 높은 부분이 포함된 테스트 케이스를 선정함
* 실제 수정이 발생한 모듈 또는 컴포넌트에서 시행하는 테스트 케이스를 선정함
#### 애플리케이션 테스트 프로세스
* 테스트 계획 -> 테스트 분석 및 디자인 -> 테스트 케이스 및 시나리오 작성 -> 테스트 수행 -> 테스트 결과 평가 및 리포팅 -> 결함 추적 및 관리
##### 테스트 계획 
* 프로젝트 계획서, 요구 명세서 등을 기반으로 테스트 목표를 정의하고 테스트 대상 및 범위를 결정함
##### 테스트 분석 및 디자인
* 테스트의 목적과 원칙을 검토하고 사용자의 요구사항을 분석함
##### 테스트 케이스 및 시나리오 작성
* 테스트 케이스의 설계 기법에 따라 테스트 케이스를 작성하고 검토 및 확인한 후 테스트 시나리오를 작성함
##### 테스트 수행
* 테스트 수행 단게에서는 테스트 환경을 구축한 후 테스트를 수행함
##### 테스트 결과 평가 및 리포팅 
* 테스트 결과를 비교 분석 해 테스트 결과서를 작성함
##### 결함 추적 및 관리 
* 에러 발견
* 에러 등록
* 에러 분석
* 결함 확정
* 결함 할당
* 결함 조치
* 결함 조치 검토 및 승인
#### 테스트 케이스/ 테스트 시나리오/ 테스트 오라클
##### 테스트 케이스
* 구현된 소프트웨어가 사용자의 요구사항을 정확하게 준수했는지 확인하기 위해 설계된 입력 값, 실행 조건, 기대 결과 등으로 구성된 테스트 항목에 대한 명세서로, 명세 기반 테스트의 설계 산출물에 해당됨
* 테스트 케이스를 미리 설계하면 테스트 오류를 방지할 수 있고 테스트 수행에 필요한 인력, 시간 등의 낭비를 줄일 수 있음
* 가장 이상적인 테스트 케이스를 설계하려면 시스템 설계 시 작성해야 함
##### 테스트 케이스 작성 순서
1. 테스트 계획 검토 및 자료 확보
2. 위험 평가 및 우선순위 결정
3. 테스트 요구사항 정의
4. 테스트 구조 설계 및 테스트 방법 결정
5. 테스트 케이스 정의
6. 테스트 케이스 타당성 확인 및 유지 보수
##### 테스트 시나리오
* 테스트 케이스를 적용하는 순서에 따라 여러 개의 테스트 케이스 들을 묶은 집합으로 테스트 케이스들을 적용하는 구체적인 절차를 명세한 문서
##### 테스트 시나리오 작성 시 유의 사항
* 시스템별, 모듈별, 항목별 등과 같이 여러 개의 시나리오로 분리하여 작성해야 함
* 사용자의 요구사항과 설계 문서 등을 토대로 작성해야함
* 식별자 번호, 순서 번호, 테스트 데이터, 테스트 케이스, 예상 결과, 확인 등을 포함해서 작성해야 함
* 유스케이스 간 업무 흐름이 정상적인지를 테스트할 수 있도록 작성해야함
* 개발된 모듈 또는 프로그램 간의 연계가 정상적으로 동작하는지 테스트할 수 있도록 작성해야 함
##### 테스트 오라클
* 테스트 결과가 올바른지 판단하기 위해 사전에 정의된 참 값을 대입하여 비교하는 기법 및 활동을 말함
* 예상 결과를 계산하거나 확인함
* 제한된 검증 : 모든 테스트 케이스에 적용할 수 없음
* 수학적 기법 : 오라클의 값을 수학적 기법을 이용해 구할 수 있음
* 자동화 가능 : 프로그램의 실행, 결과 비교, 커버리지 측정 등을 자동화 할 수 있다
##### 테스트 오라클의 종류
* 참 오라클
* 샘플링 오라클
* 추정 오라클
* 일관성 검사 오라클
#### 테스트 자동화 도구
* 사람이 반복적으로 수행하던 테스트 절차를 스크립트 형태로 구현하는 자동화 도구를 적용함으로써 쉽고 효율적으로 테스트를 수행할 수 있도록 한 것임
* 휴먼 에러를 줄이고 테스트의 정확성을 유지하면서 테스트의 품질을 향상시킬 수 있음
##### 테스트 자동화 도구의 장점/단점
* 장점 : 인력 및 시간을 줄일 수 있음
* 단점 : 고가의 추가 비용이 필요함
##### 테스트 자동화 수행 시 고려사항
* 재사용 및 측정이 불가능한 테스트 프로그램은 제외함
* 용도에 맞는 적절한 도구를 선택해서 사용함
* 자동화 도구의 환경 설정 및 습득 기간을 고려해서 프로젝트 일정을 계획해야 함
* 투입 시기가 늦어지면 프로젝트의 이해 부족으로 인해 불완전한 테스트를 초래할 수 있으므로 반드시 프로젝트 초기에 테스트 엔지니어의 투입 시기를 계획해야 함
##### 테스트 자동화 도구의 유형
* 정적 분석 도구
* 테스트 실행 도구
* 성능 테스트 도구
* 테스트 통제 도구
* 테스트 하네스 도구 : 애플리케이션의 컴포넌트 및 모듈을 테스트하는 환경의 일부분으로, 테스트를 지원하기 위해 생성된 코드와 데이터를 의미
##### 테스트 하네스의 구성 요소
* 테스트 드라이버
* 테스트 스텁
* 테스트 슈트
* 테스트 케이스
* 테스트 스크립트
* 목 오브젝트
#### 결함 관리
* 오류 발생, 작동 실패 등과 같이 소프트웨어가 개발자가 설계한 것과 다르게 동작하거나 다른 결과가 발생되는 것을 의미
* 예상한 결과와 실행 결과 간의 차이나 업무 내용과의 불일치 등으로 인해 변경이 필요한 부분도 모두 결함에 해당됨
##### 결함 관리 프로세스
1. 결함 관리 계획
2. 결함 기록
3. 결함 검토
4. 결함 수정
5. 결함 재확인
6. 결함 상태 추적 및 모니터링 활동
7. 최종 결함 분석 및 보고서 작성
##### 결함 상태 추적
* 발견된 결함은 지속적으로 상태 변화를 추적하고 관리해야 함
* 결함 분포 : 모듈 또는 컴포넌트 특정 속성에 해당하는 결함 수 측정
* 결함 추세 : 테스트 진행 시간에 따른 결함 수의 추이 분석
* 결함 에이징 : 특정 결함 상태로 지속되는 시간 측정
##### 결함 추적 순서
1. 결함 등록
2. 결함 검토
3. 결함 할당
4. 결함 수정
5. 결함 조치 보류
6. 결함 종료
7. 결함 해제
##### 결함 분류
* 시스템 결합
* 기능 결합
* GUI 결함
##### 테스트 단계별 유입 결함
* 기획시 유입되는 결함
* 설계시 유입되는 결함
* 코딩시 유입되는 결함
* 테스트 부족으로 유입되는 결함
##### 결함 우선순위
* 심각도가 높다고 반드시 우선순위가 높은 것은 아님
* 우선순위는 결정적(Critical), 높음(High), 보통(Medium), 낮음(Low), 또는 즉시 해결, 주의 요망, 대기, 개선 권고 등으로 분류됨
##### 결함 관리 도구
* Mantis
* Trac
* Redmine
* Bugzilla

### 5. 인터페이스 구현
#### 모듈 연계를 위한 인터페이스 기능 식별
* 내부 모듈과 외부 모듈 또는 내부 모듈 간 데이터의 교환 을 위해 관계를 설정하는 것으로 대표적으로 EAI, ESB가 있으며 ESB는 EAI에 속한 것임
##### EAI(Enterprise Application Integration)
* 기업 내 각종 애플리케이션 및 플랫폼 간의 정보 전달, 연계, 통합 등 상호 연동이 가능하게 해주는 솔루션
* EAI는 비즈니스 간 통합 및 연게성을 증대시켜 효율성 및 각 시스템 간의 확정성을 높여줌
* Point to Point
* Hub & Spoke : 중앙 집중형 방식, 확장 및 유지보수가 용이, 허브 장애 발생시 시스템 전체에 영향을 미침
* Message Bus(ESB) : 미들웨어를 두어 처리하는 방식, 확장성이 뛰어나며 대용량 처리가 가능 
* Hybrid : Hub & Spoke와 Message Bus의 혼합 방식
##### ESB(Enterprise Service Bus)
* 애플리케이션 간 연계, 데이터 변환, 웹 서비스 지원 등 표준 기반의 인터페이스를 제공하는 솔루션
* 특정 서비스에 국한되지 않고 범용적으로 사용하기 위해 애플리케이션과의 결합도를 약하게 유지함
* 관리 및 보안 유지가 쉽고, 높은 수준의 품질 지원이 가능함
##### 모듈 간 연계 기능 식별
* 모듈 간 공통 기능 및 데이터 인터페이스를 기반으로 모듈과 연계된 기능을 시나리오 형태로 구체화하여 식별함
##### 모듈 간 인터페이스 기능 식별
* 인터페이스 동작에 필요한 기능을 식별함
* 외부 모듈의 결과 또는 요청에 의해 수행되므로 외부 및 인터페이스 모듈 간 동작하는 기능을 통해 인터페이스 기능을 식별함
#### 인터페이스 기능 구현 정의
* 인터페이스를 실제로 구현하기 위해 인터페이스 기능에 대한 구현 방법을 기능별로 기술한 것
##### 모듈 세부 설계서
* 모듈의 구성 요소와 세부적인 동작 등을 정의한 설계서
* 컴포넌트 명세서와 인터페이스 명세서가 있음
* 컴포넌트 명세서 : 컴포넌트의 개요 및 내부 클래스의 동작, 인터페이스를 통해 외부와 통신하는 명세 등을 정의한 것
* 인터페이스 명세서 : 컴포넌트 명세서의 항목 중 인터페이스 클래스의 세부 조건 및 기능 등을 정의한 것
##### 모듈 세부 설계서 확인
* 컴포넌트 명세서와 인터페이스 명세서를 기반으로 인터페이스에 필요한 기능을 확인함
* 컴포넌트의 개요, 내부 클래스의 클래스명과 설명 등을 통해 컴포넌트가 가지고 있는 주요 기능을 확인함
* 컴포넌트 명세서의 인터페이스 클래스를 통해 인터페이스에 필요한 주요 기능을 확인함
* 인터페이스 명세서를 통해 컴포넌트 명세서의 인터페이스 클래스에 명시된 인터페이스의 세부 조건 및 기능을 확인함
##### 인터페이스 기능 구현 정의
* 인터페이스의 기능, 인터페이스 데이터 표준, 모듈 세부 설계서를 기반으로 일관성 있고 정형화된 인터페이스 기능 구현에 대해 정의함
* 일관성 있는 인터페이스 기능 구현 정의
* 정의된 인터페이스 기능 구현 정형화
#### 인터페이스 예외 처리
* 인터페이스 예외 처리는 구현된 인터페이스가 동작하는 과정에서 기능상 예외 상황이 발생 했을 때 이를 처리하는 절차를 말함
* 인터페이스 예외 처리는 인터페이스를 구현하는 방법에 따라 데이터 통신을 이용한 방법과 인터페이스 엔티티를 이용한 방법이 있음
##### 데이터 통신을 이용한 인터페이스 예외 처리
* JSON, XML 등 인터페이스 개체를 이용해 구현한 인터페이스 동작이 실패할 경우를 대비한 것으로 인터페이스 객체의 송수신 시 발생할 수 있는 예외 케이스를 정의하고 각 예외 케이스마다 예외처리 방법을 기술함
* 시스템 환경, 송수신데이터, 프로그램 자체 원인 등 다양한 원인으로 인해 예외 상황이 발생함
#### 인터페이스 보안
* 인터페이스는 시스템 모듈 간 통신 및 정보 교환을 위한 통로로 사용되므로 충분한 보안 기능을 갖추지 않으면 시스템 모듈 전체에 악영향을 주는 보안 취약점이 될 수도 있음
##### 인터페이스 보안 취약점 분석
* 수행되는 각 구간들의 구현 현황을 확인하고 각 구간에 어떤 보안 취약점이 있는지를 분석함
* 기능이 수행되는 각 구간의 구현 현황은 송수신 영역의 구현 기술 및 특징 등을 구체적으로 확인함
* 확인된 인터페이스 기능을 기반으로 송신 데이터 선택, 송신 객체 생성, 인터페이스 송수신, 데이터 처리 결과 전송 등 영역별로 발생할 수 있는 보안 취약점을 시나리오 형태로 작성함
##### 인터페이스 보안 기능 적용
* 분석한 인터페이스 기능과 보안 취약점을 기반으로 인터페이스 보안 기능을 적용함
* 일반적으로 네트워크, 애플리케이션, 데이터베이스 영역에 적용함
* 네트워크 영역 : 인터페이스 송수신간 스니핑 등을 이용한 데이터 탈취 및 변조 위협을 방지하기 위해 네트워크 트래픽에 대한 암호화를 설정함, 암호화는 인터페이스 아키텍처에 따라 IPSec, SSL, S-HTTP등의 다양한 방식으로 적용함
##### IPsec(IP Security)
* 네트워크 계층에서 IP 패킷 단위의 데이터 변조 방지 및 은닉 기능을 제공하는 프로토콜
##### SSL(Secure Sockets Layer)
* TCP/IP 계층과 애플리케이션 계층 사이에서 인증, 암호화, 무결성을 보장하는 프로토콜
##### S-HTTP
* 클라이언트와 서버 간에 전송되는 모든 메시지를 암호화 하는 포로토콜
##### 스니핑(Sniffing) / 소프트웨어 개발보안
* 스니핑 : 도청하는 해킹 유형의 하나로 수동적 공격에 해당됨
* 소프트웨어 개발 보안 : 시큐어 코딩이라고도 불림
#### 연계 테스트
* 구축된 연계 시스템과 연계 시스템의 구성 요소가 정상적으로 동작하는지 확인하는 활동
* 연계테스트 케이스 작성, 연계 테스트 환경 구축, 연계 테스트 수행, 연계 테스트 수행 결과 검증 순으로 진행됨
##### 연계 테스트 케이스 작성
* 연계 시스템 간의 데이터 및 프로세스의 흐름을 분석하여 필요한 테스트 항목을 도출하는 과정
* 기능상 결함을 확인하는 단위 테스트 케이스 형태로 작성함
##### 연계 테스트 환경 구축
* 테스트의 일정, 방법, 절차, 소요 시간 등을 송 수신 기관과의 협의를 통해 결정하는 것
##### 연계 테스트 수행
* 송수신용 연계 응용 프로그램의 단위 테스트를 먼저 수행함
* 데이터 추출, 데이터 송수신, 데이터 반영 과정 등의 연계 테스트를 수행함
##### 연계 테스트 수행 결과 검증
* 연계 테스트 케이스의 시험 항목 및 처리 절차를 수행한 결과가 예상 결과와 동일한지를 확인하는 것
* 운영 DB 테이블의 건수를 확인하는 방법
* 테이블 또는 파일을 열어 데이터를 확인하는 방법
* 파일 생성 위치에서 파일 생성 여부 및 파일 크리글 확인하는 방법
* 연계 서버에서 제공하는 모니터링 현황을 확인하는 방법
* 시스템에서 기록하는 로그를 확인하는 방법
#### 인터페이스 구현 검증
* 인터페이스가 정상적으로 문제없이 작동하는 확인하는 것
* 인터페이스 구현 검증 도구와 감시도구를 이용해 인터페이스의 동작 상태를 확인함
##### 인터페이스 구현 검증 도구
* 인터페이스 단위 기능과 시나리오 등을 기반으로 하는 통합 테스트가 필요함
* 자동화 도구를 이요하면 효율적으로 수행할 수 있음
* xUnit - Java(Junit), C++(Cppunit), .Net(Nunit) 등등
* STAF
* FitNEsse
* NTAF
* Selenium
* watir - Ruby를 사용하는 애플리케이션 테스트 프레임워크
##### 인터페이스 구현 감시 도구
* 인터페이스 동작 상태는 APM을 사용하여 감시 할 수 있음
* 애플리케이션 성능 관리 도구를 통해 데이터베이스와 웹 애플리케이션의 트랜잭션, 변수값, 호출 함수, 로그 및 시스템 부하 등 종합적인 정보를 조회하고 분석할 수 있음
* 대표적으로 스카우터(Scouter), 제니퍼(Jennifer)등이 있음
##### 인터페이스 구현 검증 도구 및 감시 도구 선택
* 인터페이스 기능 구현 정의를 통해 구현된 인터페이스 명세서의 세부 기능을 참조하여 인터페이스의 정상적인 동작 여부를 확인하기 위한 검증 도구와 감시도구의 요건을 분석함
##### 인터페이스 구현 검증 확인
* 인터페이스 구현 검증 도구를 이용해 외부 시스템과 연계 모듈의 동작 상태를 확인함
##### 인터페이스 구현 감시 확인
* 인터페이스 구현 감시 도구를 이용해 외부 시스템과 연결 모듈이 서비스를 제공하는 동안 정삭적으로 동작하는지 확인함

## 3. 데이터베이스 구축
### 1. 논리 데이터베이스 설계
#### 데이터베이스 설계
* 사용자의 욕구를 분서해 ㅡ것들을 컴퓨터에 저장할 수 있는 데이터베이스의 구조에 마제 변형한 후 특정 DBMS로 데이터베이스를 구현하여 일반 사용자들이 사용하게 하는 것
##### 데이터베이스 설계 시 고려사항
* 무결성 : 삽입, 삭제, 갱신 등의 연산 후에도 데이터베이스에 저장된 데이터가 정해진 제약 조건을 항상 만족해야 함
* 일관성 : 특정 질의에 대한 응답이 처음부터 끝까지 변함없이 일정해야 함
* 회복 : 시스템에 장애각 발생했을 때 장애 발생 직전의 상태로 복구할 수 있어야 함
* 보안 : 불법적인 데이터의 노출 또는 변경이나 손실로부터 보호할 수 있어야 함
* 효율성 : 응답시간의 단축, 시스템의 생산성, 저장 공간의 최적화 등이 가능해야 함
* 데이터베이스 확장 : 데이터베이스 운영에 영향을 주지 않으면서 지속적으로 데이터를 추가할 수 있어야 함
##### 데이터베이스 설계 순서
* 요구 조건 분석 -> 개념적 설계 -> 논리적 설계 -> 물리적 설계 -> 구현
##### 요구 조건 분석
* 수집된 정보를 바탕으로 요구 조건 명세를 작성함
##### 개념적 설계(정보 모델링, 개념화)
* 개념 스키마 모델링과 트랜잭션 모델링을 병행 수행함
* DBMS에 독립적인 ER다이어그램을 작성함
* DBMS에 독립적인 개념 스키마를 설계함
##### 논리적 설계(데이터 모델링)
* DBMS에 따라 서로 다른 논리적 스키마를 설계하는 단계임
* 관계형 데이터베이스라면 테이블을 설계하는 단계임
##### 물리적 설계(데이터 구조화)
* 저장할 수 있는 물리적 구조의 데이터로 변환하는 과정
* 파일의 저장 구조 및 액세스 경로를 결정
* 레코드의 형식, 순서, 접근 경로와 같은 정보를 사용하여 데이터가 컴퓨터에 저장되는 방법을 묘사함
##### 파일로 데이터를 관리할 경우
1. 동시성 문제
2. 중복성 문제
3. 일관성 문제
4. 복구 기능 문제
5. 보안성 문제
##### 데이터베이스 구현
* 논리적 설계 단계와 물리적 설계 단계에서 도출된 데이터 베이스 스키마를 파일로 생성하는 과정
* DBMS의 DDL(데이터 정의어)을 이용해 데이터베이스 스키마를 기술한 후 컴파일하여 빈 데이터베이스 파일을 생성함
* 응용프로그램을 위한 트랜잭션을 작성함
* 데이터베이스 접근을 위한 응용 프로그램을 작성함
#### 데이터 모델의 개념
* 현실 세계의 정보들을 컴퓨터에 표현하기 위해 단순화, 추상화하여 체계적으로 표현한 개념적 모형
* 데이터 모델 구성요소 : 개체, 속성, 관계
* 데이터 모델 종류 : 깨념적 데이터 모델, 논리적 데이터 모델, 물리적 데이터 모델
* 데이터 모델에 표시할 요소 : 구조, 연산, 제약 조건
##### 데이터 모델의 구성요소
* 개체(Entity)
* 속성(Attribute)
* 관계(Relationship)
##### 개념적 데이터 모델
* 현실 세계에 대한 인간의 이해를 돕기 위해 현실 세계에 대한 인식을 추상적 개념으로 표현하는 과정
* 현실 세계에 존재하는 개체를 인간이 이해할 수 있는 정보구조로 표현하기 때문에 정보 모델이라고도 함
* 대표적인 개념적 데이터 모델로 ER모델이 있음
##### 논리적 데이터 모델
* 특정 DBMS는 특정 논리적 데이터 모델 하나만 선정하여 사용함
* 관계모델, 계층 모델, 네트워크 모델로 구분함
##### 논리적 데이터 모델의 품질 검증
* 개체 품질 검증 항목 : 단수 명사 여부, 개체의 주 식별자, 개체 간 상호 배타성
* 속성 품질 검증 항목 : 단수 명사 여부, 속성의 각ㅂㅅ 존재 여부 및 개수, 도메인의 정이(범위)
* 관계 품질 검증 항목 : 관계의 명칭, 2개 이상의 노드와 관계 존재 여부, 노드의 기수성과 선택성
* 식별자 품질 검증 항목 : 식별자의 명칭, 정의, 구성, 정합성, 크기, 순서 등
* 전반적인 품질 검증 항목 : 주제 영역 구성의 적절성, 데이터 모델 상에 정규화 여부
##### 데이터 모델에 표시할 요소
* 구조(Structure) : 개체 타입들 간의 관계로서 데이터 구조 및 정적 성질을 표현
* 연산(Operation) : 실제 데이터를 처리하는 작업에 대한 명세
* 제약 조건(Constraint) : 데이터베이스에 저장될 수 있는 실제 데이터의 논리적인 제약 조건
