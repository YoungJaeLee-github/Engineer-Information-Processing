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

###
