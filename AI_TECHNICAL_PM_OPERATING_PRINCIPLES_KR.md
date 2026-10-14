# AI Technical PM Operating Principles

## 1. Technical PM Positioning

이번 프로젝트는 개발자 관점의 기능 구현만을 목표로 하지 않는다.

기술 중심 PM으로서 시장 문제, 기술 구조, 보안, 비용, 운영, 검증, 산출물을 함께 설계하는 것을 목표로 한다.

구체적으로는 다음 역량을 보여주는 것을 목표로 한다.

1. 숨겨진 시장 needs와 기회 포착

   법률 intake 과정에서 고객이 겪는 정보 비용, 탐색 비용, 상담 전환 손실 문제를 발견하고, 이를 AI 서비스 기회로 정의한다.

2. Spring Boot 기반 AI 서비스 구현

   Spring Boot 서버, JPA DB, React 화면, LLM API 연결을 통해 Legal Intake Form 기반 AI 챗봇과 Search Routing 흐름을 구현한다.

3. AI 보안 체계와 비용 통제 설계/구축

   향후 AI 시장에서 중요한 화두가 될 보안과 비용 통제를 중심으로, 6가지 layer의 AI 보안 체계와 6가지 layer의 비용 통제 구조를 구현한다.

4. 운영 metric과 dashboard 설계

   운영 metric과 dashboard를 통해 운영자 편의성, 서비스 관측성, 마케팅 의사결정 가능성을 높인다.

5. Postman 검증과 리팩토링

   Postman 실험과 feedback을 바탕으로 정상 흐름, 실패 흐름, 차단 흐름을 검증하고 리팩토링한다.

6. AI 시대에 맞는 산출물 구축

   서버 구조와 운영 흐름을 설명 가능한 산출물로 만들고, 기술 PM 관점의 설계 역량을 드러낸다.

즉, 기술 PM은 아이디어만 내는 사람이 아니라 사용자 행동, 도메인 이벤트, 정책, 데이터, 코드, 운영 지표를 하나의 구조로 연결할 수 있어야 한다.

## 2. Market-Driven Positioning

이번 프로젝트는 단순히 기능을 구현하는 개발 과제가 아니라, 실제 시장성과 상업성을 고려한 AI 서비스 설계를 목표로 한다.

법률 intake라는 직접 부딪힌 시장의 정보 비용 불합리성을 개선해, 고객의 법률 탐색 비용을 줄이고 변호사 사무소의 초기 상담 전환 흐름을 높이는 현실생활 솔루션을 적합한 AI 기술에 녹여내는 것을 목표로 한다.

## 3. AI 시대형 개발 방법론

AI가 개발 속도를 높이는 시대에는 사람이 모든 코드를 직접 작성하는 것보다 시장성 있는 것을 정의하고, 보안과 비용 절감을 초기부터 설계하며, 오류 대응과 사용자 경험 개선을 리팩토링 과정에 포함하고, 운영 편의성까지 고려한 feedback loop를 만드는 것이 중요하다.

이번 프로젝트는 수업 시간에 배운 TDD 개념을 AI 시대에 맞게 응용한 실전형 개발 방식으로 진행한다.

```text
AI 모듈화 draft
-> Postman 검증
-> 실패 케이스 확인
-> feedback 기록
-> 리팩토링
-> 문서화
-> 시연
```

이 방식은 개발을 줄이는 것이 아니라, AI가 개발 속도를 높이는 시대에 사람이 더 집중해야 할 시장성, 보안, 비용 통제, 운영 관측, 검증, 리팩토링에 가중치를 두는 방식이다.

## 4. Flexible Early, Strict Late

이번 프로젝트는 처음부터 모든 구조를 완벽하게 확정한 뒤 개발하지 않는다.

AI 서비스는 Spring Boot, JPA, LLM API, 보안 정책, 비용 통제, metric, 화면 흐름이 함께 연결되기 때문에 초기에는 구현하면서 시스템의 실제 흐름을 이해하고, 중반에는 Postman 실험과 Event Storming을 통해 구조를 다시 정리하며, 후반에는 확정된 범위를 set해 안정화와 산출물 정리, 검증, 리팩토링, 문서화, 시연 안정화에 집중한다.

운영 원칙은 다음과 같다.

```text
초반에는 구현하면서 이해한다.
중반에는 실험하면서 구조화한다.
후반에는 확정하고 흔들지 않는다.
```

## 5. Development Weight Balance

이번 프로젝트에서는 개발 자체와 실제 운용, 비용 관리, 검증, 리팩토링에 같은 수준의 가중치를 둔다.

기능이 동작하는 것만으로는 충분하지 않다.

```text
정상 요청이 처리되는가?
위험 요청이 차단되는가?
비용 초과 요청이 LLM 호출 전에 막히는가?
개인정보가 출력에서 마스킹되는가?
외부 API 실패 시 fallback 되는가?
reasonCode와 metric으로 설명 가능한가?
오류가 났을 때 서버 어디를 봐야 하는가?
대안 설계로 축소하거나 우회할 수 있는가?
```

이번 프로젝트에서 기능 완료의 기준은 코드 작성이 아니라 정상 흐름, 실패 흐름, 차단 이유, 운영 관측까지 확인되는 것이다.

## 6. Top / Middle / Bottom Understanding Rule

이번 프로젝트는 기능을 Top / Middle / Bottom 구조로 분리해 이해하고 실험하여, 서버 운용 감각과 전체 흐름을 파악하는 것을 목표로 한다.

### Top Layer

Mermaid Flow Chart로 전체 서버와 AI 흐름을 이해한다.

```text
Client
-> Spring Security
-> Controller
-> DTO Validation
-> Service
-> JPA DB
-> Fixed Guard
-> Cost Control
-> Dynamic Guard
-> LLM Search Routing
-> Output Guardrail
-> Privacy Output Guard
-> Metric / Dashboard
-> Response
```

### Middle Layer

DDD/Event Storming을 통해 사용자 행동이 어떤 Command와 Domain Event로 바뀌는지 정리한다.

```text
Actor
-> Command
-> Domain Event
-> Policy
-> Aggregate
-> Read Model
-> Bounded Context
```

### Bottom Layer

Policy / Read Model / Code / Postman을 연결한다.

```text
Policy
-> 필요한 데이터
-> 코드 위치
-> Postman 검증
-> reasonCode / metric 확인
```

이 구조를 통해 전체 흐름, 도메인 이벤트, 정책, 데이터, 코드, 검증을 하나로 연결한다.

## 7. Event-to-Code Mapping Rule

이번 프로젝트에서는 Event Storming 결과를 문서로만 두지 않는다.

각 Event를 Policy, Read Model, Code, Postman 검증과 연결해 실제 서버에서 어떻게 동작하는지 확인한다.

이 표는 공부 자료이자 운영 디버깅 자료이며, 기술 PM으로서 사용자 행동과 기술 구조를 mapping하는 핵심 산출물이다.

최종적으로는 다음 흐름을 설명할 수 있어야 한다.

```text
전체 흐름
-> 도메인 이벤트
-> 정책
-> 필요한 데이터
-> 코드 위치
-> Postman 검증
-> 리팩토링
```

즉, 기술 PM으로서 사용자 행동에서 발생하는 이벤트를 기술 구조로 mapping하고, 그 구조가 실제 서버에서 어떻게 작동하는지 검증할 수 있는 능력을 기르는 것이 핵심 목표다.

## 8. Module Completion Rule

기능 하나를 만들 때는 단순히 코드 구현에서 끝내지 않는다.

각 기능은 다음 단계를 하나의 묶음으로 완료한다.

```text
모듈별 설계
-> 모듈별 구현
-> Postman 정상 요청
-> Postman 실패/차단 요청
-> reasonCode 확인
-> 로그/metric 확인
-> feedback 기록
-> 산출물 반영
```

이 과정을 통과한 기능만 "구현 완료"로 본다.

## 9. Error Stop Flow Rule

이번 프로젝트에서 중요한 것은 정상 동작뿐만 아니라 실패했을 때 후속 처리가 멈추는지 확인하는 것이다.

대표 흐름은 다음과 같다.

```text
JWT 없음
-> Controller 진입 전 401

DTO Validation 실패
-> Service 진입 전 400

Fixed Guard 차단
-> LLM 호출 없음

Cost Control 차단
-> LLM 호출 없음
-> actual token 증가 없음

Dynamic Guard 차단
-> 후속 요청 차단

OpenAI API 실패
-> fallback 응답
-> 서버 장애로 번지지 않음

Privacy Output Guard
-> 원문 개인정보 노출 없음
```

이 과정을 통해 오류가 발생했을 때 서버의 어느 계층에서 문제가 발생했는지 파악하고, 필요하면 대안 설계를 적용할 수 있는 운영 능력을 기른다.

## 10. Final Project Build-Up Rule

이번 프로젝트는 단독으로 끝나는 프로젝트가 아니라, 추후 2개월짜리 final project인 AI orchestration 프로젝트로 이어지는 빌드업이다.

따라서 이번 프로젝트에서는 무리하게 RAG, Python action, 고급 multi-agent를 넣기보다 다음 기초 체력을 단단히 만든다.

```text
Spring Boot 기반 AI 서버 흐름
JPA DB 설계
LLM API 연결
AI 보안 정책
Cost Control
Privacy Output Guard
Prometheus/Grafana 관측
Postman 검증
DDD/Event Storming
Policy / Read Model / Code mapping
```

이 기반 위에 12월 final project에서 Python, RAG, Vector DB, LangChain/LangGraph, NeMo action, 의료/법률 AI 보안을 확장한다.
