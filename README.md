# Engineer Information Processing(정보처리기사)
## 1. 소프트웨어 설계
### 1. 요구사항 확인
#### 소프트웨어 생명 주기
* 소프트웨어 생명주기란 소프트웨어 개발 방법론의 바탕이 되는 것으로 소프트웨어 수명 주기라고도 한다. 
* 즉, SW 개발 단계를 나누고, 그에 대한 골격을 제공하는 것이다.
* 대표적인 예로는 폭포수 모형, 프로토타입 모형, 나선형 모형, 애자일 모형이 있다.

##### 폭포수 모형
* 사용자의 요구사항이 명확할 때 사용하는 모형이다.
* 가장 전통적이고 폭넓게 사용하는 모형이다.
* 이전 단계가 끝나야 다음 단계로 넘어갈 수 있다. 즉, 전 단계로 돌아가서 수정하기가 어렵다. 그렇기 때문에 새로운 요구사항을 받아들이기가 어렵다.
* 타당성 검토 -> 계획 -> 요구분석 -> 설계 -> 개발 -> 테스트 -> 유지보수 단계로 진행한다.

##### 프로토타입 모형
* 사용자의 요구사항이 명확하지 않을 때 모형(프로토타입)을 제시해 미래 최종 결과물을 예측하는 모형, 프로토타입을 제시하고 점점 개선해 나가면서 완성하는 방법이다.
* 오류를 초기에 발견할 수 있으며 변경이 용이하다.
* 하지만 모형을 만드는데 드는 비용과 시간이 많이 든다.
* 요구 분석 -> 프로토타입 설계 -> 프로토타입 개발 -> 고객평가 -> 프로토타입 조정 -> 구현 단계로 진행한다.

##### 나선형 모형
* 폭포수 모형과 프로토타입 모형의 특징에서 개발하는데 발생할 수 있는 위험을 분석하는 단계를 추가한 것으로 대규모 프로젝트에 적합하고, 반복적이고 점진적인 모형이다.
* 생명 주기를 반복하면서 점진적으로 완성해 나가므로 별도의 유지보수가 필요없고 정밀하다.
* 계획 수립 -> 위험 분석 -> 개발 -> 고객 평가 -> 계획 수립 -> … 이처럼 반복적인 형태의 모형이다.

##### 애자일 모형
* 폭포수 모형과는 다르게 고객의 요구사항에 유연하게 대응할 수 있고, 고객과의 소통을 중점적으로 진행하는 모형이다.
* 스프린트(Sprint) 또는 이터레이션(Iteration)이라고 불리는 짧은 개발 주기를 반복하고 만들어질 때마다 고객에게 평가를 받아 고객의 요구를 적극적으로 수용한다.
* 소규모 프로젝트에 적합하며 숙달된 개발자, 급현하는 요구사항에 적합하다.
* 애자일 모형을 기반으로 하는 소프트웨어 개발 모형에는 스크럼, XP, ASD, FDD, DSDM, DAD, Lean, 크리스탈, 칸반 등이 있다.

##### 애자일 개발 4가지 핵심 가치
1. 프로세스와 도구보다는 개인과 상호작용에 더 가치를 둔다.
2. 방대한 문서(매뉴얼)보다는 실행되는 SW에 더 가치를 둔다.
3. 계약 협상보다는 고객과 협업에 더 가치를 둔다.
4. 계획을 따르기 보다는 변화에 반응하는 것에 더 가치를 둔다.

##### 애자일 개발 12가지 실행 지침
1. 유용한 소프트웨어를 빠르고, 지속적으로 제공하여 고객을 만족시킨다.
2. 개발 막바지라도 요구사항 변경을 적극 수용한다.
3. 몇 개월이 아닌 몇 주 단위로 실행되는 소프트웨어를 제공한다.
4. 고객과 개발자가 프로젝트 기간에 함께 일한다.
5. 개발에 대한 참여 의지가 확실한 사람들로 팀을 구성하고,  필요한 개발 환경과 지원을 제공하며, 일을 잘 끝낼 수 있도록 신뢰한다.
6. 같은 사무실에서 얼굴을 맞대고 의견을 나눈다.
7. 개발의 진척도를 확인하는 1차 기준은 작동하는 소프트웨어다.
8. 지속 가능한 개발을 장려하고 일정한 속도로 개발을 진행한다.
9. 기술적 우수성과 좋은 설계에 지속적인 관심을 기울이면 민첩성이 향상된다.
10. 단순하를 추구한다.
11. 최상의 구조, 명확한 요구사항, 최상의 설계는 자기 스스로 일을 주도하는 조직적인 팀으로부터 나온다.
12. 더 효과적인 팀이 될 수 있는 방안을 정기적으로 깊이 고민하고 그에 따라 팀의 행동을 조정한다.

###### 폭포수 모형과 애자일 비교
<img width="479" alt="스크린샷 2020-03-01 오후 11 58 24" src="https://user-images.githubusercontent.com/37511312/75628016-8f37f100-5c18-11ea-8348-528eece39f2b.png">

#### 스크럼(Scrum) 기법
* 팀의 중요성을 나타내는 말로, 애자일 기법의 한 종류
* 구성원은 제품 책임자, 스크럼 마스터, 개발팀으로 구성되어 있음.
* 제품 책임자는 주로 개발의뢰자나 사용자, 제품에 대한 요구사항을 작성하는 주체, 백로그 작성, 우선순위를 지정하는 역할을 함.
* 스크럼 마스터는 팀원을 통제하려는 것이 아닌 스크럼 수행의 가이드 역할을 하며 개발 과정의 장애 요소를 공론화 하여 처리하는 역할을 함.
* 개발 팀은 앞의 제품 책임자와 스크럼 마스터를 제외한 7~8명의 인원이 적합.
* 백로그란, 제품 개발에 필요한 요구사항을 우선순위를 지정해 작성해 놓은 목록.
##### 스크럼 기법 개발 과정
* 제품 백로그 작성 -> 스프린트 계획 회의 -> 스프린트 (2~4주) -> 일일 스크럼 회의(매일) -> 스프린트 검토회의 -> 스프린트 회고

#### XP(eXtreme Programming) 기법
* 소규모 프로젝트에 적합한 기법으로 애자일 모형의 한 종류임.
* 수시로 발생하는 고객의 요구사항에 유연하게 대응하기 위해 고객의 참여와 개발 과정의 반복을 극대화 하여 생산성을 향상시키기 위한 기법임.

##### XP기법의 5가지 핵심 가치
* 의사소통
* 단순성
* 용기
* 존중
* 피드백 

##### XP기법 개발 과정
* 사용자 스토리 -> 릴리즈 계획 수립 -> 스파이크 -> 주기 -> 승인 검사 -> 소규모 릴리즈
* 사용자 스토리 : 고객의 요구사항을 간단한 시나리오로 표현.
* 릴리즈 : 스토리에 대한 부분적인 기능이 완료된 제품을 제공하는 것.
* 스파이크 : 요구사항의 신뢰성을 높이고 기술 문제의 위험성을 감소시키기 위한 간단한 프로그램.
* 주기(Iteration) : 하나의 릴리즈를 더 세분화 한 것(보통 1~3주 반복 수행).
* 승인 검사 : 릴리즈 검사.
*  소규모 릴리즈 : 고객의 요구사항에 유연하게 대응(기능별로 확인이 가능하기 때문).

##### XP의 주요 실천 방법
* 짝 프로그래밍(Pair Programming) : 다른 사람과 함께 개발함으로써 공동으로 책임을 나눌 수 있음.
* 테스트 주도 개발(Test Driven Development) : 테스트 케이스를 실제 코드 구현하기 전에 작성.
* 전체 팀(Whole Team) : 각자 자신의 역할에 대해 책임을 가져야 함.
* Continuous Integration(계속적인 통합) : 나누어서 개발한 코드들을 지속적으로 통합.
* Design Improvement or Refactoring : 시스템 재구성
* 소규모 릴리즈(Small Releases)  : 릴리즈 기간을 짧게 반복함으로써 고객의 요구사항에 대응.

#### 현행시스템파악 
* 새로 개발하는 시스템의 개발 범위를 명확하게 하기 위한 것.

##### 현행 시스템 파악 절차
* 1단계 : 시스템 구성 파악, 시스템 기능 파악, 시스템 인터페이스 파악
* 2단계 : 아키텍처 구성 파악, 소프트웨어 구성 파악
* 3단계 : 시스템 하드웨어 구성 파악, 네트워크 구성 파악

#### 개발 기술 환경 파악
* 개발 하고자 하는 소프트웨어와 관련된 운영체제, DB, 미들웨어 등을 선정할 때 고려해야 할 사항을 기술하고, 오픈 소스 사용 시 주의사항을 파악해야 한다.

##### 운영체제(OS)
* 운영체제는 컴퓨터 시스템의 자원들을 효율적으로 관리하며, 사용자가 컴퓨터를 편리하고 효율적으로 사용할 수 있도록 환경을 제공하는 소프트웨어.
* 상용 운영체제로는 Windows, MacOS, Unix, 오픈소스로는 Linux
* 상용 모바일 운영체제로는 iOS, 오픈소스 모바일 운영체제로는 Android등이 있다.

##### 운영체제 관련 요구사항 식별시 고려사항
* 가용성 : 시스템의 장시간 운영으로 인해 발생할 수 있는 운영체제 고유의 장애 발생 가능성, 메모리 누수로 인한 성능 저하 및 재가동, 보안상 발견된 허점을 보완하기 위한 지속적인 패치로 인한 재가동, 운영체제의 결함 등으로 인한 패치 설치를 위한 재가동
* 성능 : 댁모 동시 사용자 요청에 대한 처리, 대규모 및 대용량 파일 작업에 대한 처리, 지원 가능한 메모리 크기 (처리 가능한 명령어 주소단위)(32bit, 64bit)
* 기술 지원 : 제작 업체의 안정적인 기술지원, 여러 사용자들 간의 정보 공유, 오픈 소스 여부
* 주변 기기 : 설치 가능한 하드웨어, 여러 주변기기 지원 여부
* 구축 비용 : 지원 가능한 하드웨어 비용, 설치할 응용 프로그램의 라이선스 정책 및 비용, 유지 관리 비용, 총 소유 비용(TCO)

##### 데이터베이스 관리 시스템(DBMS)
* 사용자의 요구에 따라 데이터를 생성, 관리해주는 소프트웨어
* 파일 시스템과 어플리케이션 간의 종

#### UI 상세 설계
* UI 설계서를 바탕으로 실제 설계 및 구현을 위해 모든 화면에 대해 자세한 설계를 진행하는 단계로, UI 상세 설계를 할 떄는 반드시 시나리오를 작성해야 함
* UI 시나리오 문서는 사용자 인터페이스의 기능 구조, 대표 화면, 화면 간 인터랙션의 흐름, 다양한 상황에서의 예외 처리 등을 문서로 정리한 것
##### UI 시나리오 문서 작성 원칙
* 개발자가 전체적인 UI의 기능과 작동 방식을 한눈에 이해할 수 있도록 구체적으로 작성
* 모든 기능에 공통적으로 적용될 UI 요소와 인터랙션을 일반 규칙으로 정의
* 대표 화면의 레이아웃과 그 화면에 속할 기능을 정의
* 인터랙션의 순서, 분기, 조건, 루프 등을 명시
* 예외 상황에 대비한 다양한 케이스를 정의
* UI 일반 규칙을 지키면서 기능별 상세 기능 시나리오를 정의
* UI 시나리오 규칙을 지정
##### UI 시나리오 문서 작성을 위한 일반 규칙
* 주요 키의 위치와 기능
* 공통 UI 요소
* 기본 스크린 레이아웃
* 기본 인터랙션 규칙
* 공통 단위 태스크 흐름
* 케이스 문서
##### UI 시나리오 문서의 요건
* 완전성
* 일관성
* 이해성
* 가독성
* 수정 용이성
* 추적 용이성
##### UI 시나리오 문서로 인한 기대 효과
* 요구사항이나 의사소통에 대한 오류가 감소
* 개발 과정에서의 재작업이 감소하고, 혼선이 최소화됨
* 불필요한 기능을 최소화함
* 소프트웨어 개발 비용을 절감
* 개발 속도를 향상시킴
##### UI 시나리오
* UI 설계자 혹은 인터랙션 디자이너가 담당
##### UI 디자인
* 디자이너가 담당
##### UI 구현
* 개발자가 담당

#### HCI / UX / 감성공학
* 대상이 컴퓨터뿐만 아니라 서비스, 디지털 콘텐츠 등으로 사람도 개인뿐만 아니라 사회나 집단으로 확대 되었음
##### UX(User Experience)
* 주관성(Subjectivity)
* 정황성(Contextuality)
* 총체성(Holistic)
##### 감성 공학
* 기반 기술 : 제품 설계에 적용할 인간의 특성을 파악
* 구현 기술 : 인간의 특성에 맞는 인터페이스를 구현
* 응용 기술 : 인간에 맞는지 파악하여 새로운 감성을 만듦

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
##### 모델-뷰=컨트롤러 패턴(MVC)
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
