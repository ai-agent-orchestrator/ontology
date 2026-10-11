# Who Am I

```text
Domain-driven AI Technical PM
for healthcare, legal, cybersecurity, and AI governance
```

I combine healthcare and legal domain experience with hands-on AI backend practice.
My focus is building safe, observable, and compliant AI systems for high-stakes domains.

Repository focus:

```text
Domain-driven AI Technical PM portfolio for healthcare, legal, cybersecurity, and AI governance.
```

```diff
Medical background
+ Legal dispute structuring experience
+ Ontology-driven thinking
+ AI-native PM / backend orchestration
= Legal/Medical AI Technical PM
```

## Ontology Applied Architecture Saves Cost And Time

The client selects inside an ontology structure.
The chatbot organizes the selected values into a clear case summary.
The lawyer receives structured intake information before consultation.
The LLM handles shorter, cleaner, and safer inputs.

```text
Selective Legal Intake Form
-> mini legal ontology
-> structured case summary
-> safer and cheaper AI processing
```

This is the core value of the architecture.
The ontology is not presented as an abstract concept.
It is applied as a product structure that reduces cost for the client, the lawyer, and the LLM system.

```text
Client
-> less confusion and lower input burden

Lawyer
-> less repeated basic questioning and faster case understanding

LLM system
-> shorter input, clearer context, lower token cost, safer guardrail processing
```

Through hands-on experience and this development project, I designed an ontology structure that satisfies multi-dimensional market needs:
client usability, lawyer workflow efficiency, AI security, observability, and cost control.

## 온톨로지 적용 아키텍처는 비용과 시간을 줄인다

고객은 온톨로지 구조 안에서 선택합니다.
챗봇은 선택값을 사건 요약으로 정리합니다.
변호사는 상담 전에 구조화된 사건 정보를 확인합니다.
LLM은 더 짧고, 더 정리되고, 더 안전한 입력을 처리합니다.

```text
선택형 Legal Intake Form
-> 미니 법률 온톨로지
-> 구조화된 사건 요약
-> 더 안전하고 저렴한 AI 처리
```

이것이 이 아키텍처의 핵심 가치입니다.
온톨로지를 추상적인 개념으로 설명하는 것이 아니라,
고객, 변호사, LLM 시스템 모두의 비용을 줄이는 제품 구조로 적용합니다.

```text
고객
-> 덜 헤매고, 입력 부담이 줄어든다.

변호사
-> 반복적인 기본 질문이 줄고, 사건 파악이 빨라진다.

LLM 시스템
-> 입력이 짧아지고, 맥락이 명확해지고, 토큰 비용이 줄고, guardrail 처리가 쉬워진다.
```

직접 겪고 분석한 문제의식과 이번 개발 과정을 통해,
고객 사용성, 변호사 업무 효율, AI 보안, 관측 가능성, 비용 통제를 함께 만족시키는
다면적 시장 요구 기반 온톨로지 구조를 설계했습니다.

## Detailed Multi-Layer PM Analysis

This project is not just an implementation of a legal chatbot.
It analyzes the legal intake problem from six perspectives: market, client, lawyer, technology, security, and operation.

### 1. Market Perspective

Small law offices often rely on phone-first, free-text, staff-dependent intake.
When client inquiries are not converted into structured case information, consultation conversion loss can occur.

### 2. Client Perspective

Clients who face legal problems for the first time often do not know whether their case is civil, criminal, family-related, or electronic-litigation-related.
Instead of forcing clients to explain everything in long free text, the system should provide selective input and preparation guidance.

### 3. Lawyer Perspective

Unstructured consultation consumes the lawyer's time on basic fact-finding.
If the client enters consultation without minimum preparation, both the client and the lawyer can be dissatisfied with the consultation quality.

By structuring case type, available documents, party position, and desired next step before consultation,
the lawyer can spend more time on issue analysis and strategy rather than document sorting and basic questioning.

### 4. Technical Perspective

For an MVP, a `Legal Intake Form` based informational chatbot is more suitable than a fully free-form conversational chatbot.
Selective input and checklists make input structuring, DTO validation, reasonCode design, and metric design easier.

### 5. Security Perspective

AI services must control risky requests, repeated attacks, cost explosions, and privacy re-exposure before or after LLM calls.
The security layers are separated as follows.

- Fixed Guard: blocks single risky requests
- Dynamic Guard: detects repeated risky behavior
- Cost Control: prevents token cost explosion
- Privacy Output Guard: masks personal information in output

### 6. Operation Perspective

AI services must be observable in operation.
Operators should be able to see where intake drops off, which requests are blocked, and how often cost blocks occur through Prometheus/Grafana metrics.

The system is designed so that block reasons and conversion loss can be checked through reasonCode, metrics, and dashboards.

## Legal Intake Case

The core of this legal intake case is not to replace legal consultation with a chatbot.
It is to design a `Selective Legal Intake` flow that turns the client's unstructured explanation into a structured case format before consultation.

Core sentence:

```text
The client selects, and the chatbot organizes.
```

## Problem

Clients who face legal problems for the first time often do not know whether their case is civil, criminal, family-related, or electronic-litigation-related.
However, many law offices still require clients to explain their problem from the beginning in long free-form speech over the phone.

This creates the following problems.

```text
The client does not know legal terminology.
Phone conversations disappear the moment they end.
Dates, amounts, counterparties, and available documents are easily missed.
Case information is not structured at the intake desk stage.
The lawyer must spend consultation time checking basic facts again.
The client may feel that even a paid consultation only covered basic questions.
```

As a result, early inquiries may fail to convert into actual consultations.

## Solution

This problem is structured through a `Selective Legal Intake Form` and a `mini legal ontology`.

Instead of writing a long free-form explanation, the client selects information like using a kiosk.

```text
Inquiry purpose
Case type
Party position
Core facts
Available documents
Desired next step
```

The chatbot organizes the selected values into a natural-language guide.

```text
This inquiry appears to be close to a civil case.

There may be a money return or loan dispute.
Before consultation, please organize bank transfer records,
KakaoTalk/text messages, and records showing that you requested repayment
in chronological order.

If you have a contract or written agreement, please prepare it as well.
Personal information entered by the user is not displayed as-is and is masked in the response.
```

## Minimal Legal Intake Form

### 1. Inquiry Purpose

- Procedure guidance
- Required document check
- Drafted document review
- Lawyer engagement or contract review
- Electronic litigation filing guidance

### 2. Case Type

- Civil
- Criminal
- Family
- Electronic litigation
- Not sure

### 3. Party Position

- Victim
- Accused person
- Plaintiff
- Defendant
- Applicant
- Counterparty
- Not sure

### 4. Core Facts

- Incident date
- Counterparty
- Disputed amount or damage scale
- Current stage
- One-sentence summary of the core issue

### 5. Available Documents

- Contract
- Bank transfer records
- KakaoTalk/text messages
- Photos/videos
- Complaint/petition/notice
- None

### 6. Desired Next Step

- Consultation
- Document review
- Litigation preparation
- Electronic litigation filing
- Lawyer engagement

## Mini Legal Ontology

In this case, ontology is not a complex legal knowledge graph.
It is a minimal classification structure that connects the client's selected values and keywords to case type, dispute area, required documents, and next organization direction.

```text
Client input
-> selected values
-> case type
-> dispute area
-> required documents
-> next organization direction
```

Examples:

```text
Civil
-> loan / contract / lease / damages

Criminal
-> fraud / assault / complaint / accused person

Family
-> divorce / child support / inheritance / parental rights

Electronic litigation
-> complaint / answer / correction order / service of documents
```

## Product Value

### Customer Value

Clients can organize their problem through selective input even if they do not know legal terminology.

- They can understand whether their issue is closer to civil, criminal, family, or electronic litigation.
- They can know what documents to prepare before consultation.
- They feel less anxious before calling or visiting a law office.
- They feel that the office has a structured intake process.
- They can better understand why a paid consultation may be necessary.

### Lawyer Value

Lawyers can review client inquiries in a structured format before consultation.

- They can understand the likely case direction faster.
- The client's document preparation quality improves.
- Repeated basic questions are reduced.
- Consultation conversion can improve.
- Initial inquiry flow can be managed even when the lawyer is not always in the office.
- It can work as a low-cost, high-efficiency marketing tool that turns ad-driven inquiries into consultation-ready cases.

### System Value

The system can reduce long free-form input and unnecessary LLM calls.

- Selective input reduces free-text length.
- Case-type templates can be used for responses.
- DTO validation and reasonCode design become easier.
- Cost Control becomes easier to apply.
- Privacy masking, security guardrails, and metric collection can be attached more reliably.

## Cost Reduction Thesis

Selective intake and mini legal ontology reduce cost for the client, the lawyer, and the system.

```text
The client wanders less.
The lawyer asks fewer repeated basic questions.
The system calls the LLM less.
```

In summary:

```text
Selective intake improves customer experience.
Mini legal ontology turns selected values into case structure.
Together, they reduce time, money, and energy cost for the client, the lawyer, and the system.
```

## Security-Aware Extension

This Legal Intake structure can be combined with an AI security architecture.

```text
Fixed Guard
-> blocks risky requests

Dynamic Guard
-> blocks repeated risky behavior

Cost Control
-> blocks long input and token cost explosion

Privacy Output Guard
-> allows personal information input but masks personal information in output

Prometheus / Grafana
-> observes inquiry flow, security blocks, and cost blocks
```

In other words, this case is not just a chatbot idea.
It is an AI Technical PM design case that connects domain ontology, customer experience, security architecture, and operational metrics.

## Legal Intake Case Korean Version

이번 legal intake case의 핵심은 법률 상담을 대체하는 챗봇이 아닙니다.
법률 상담 전 단계에서 고객의 비정형 설명을 사건 구조로 바꾸는 `선택형 Legal Intake` 설계입니다.

핵심 문장:

```text
고객은 선택하고, 챗봇은 정리한다.
```

## Problem

법률 문제를 처음 겪는 고객은 자신의 사건이 민사인지, 형사인지, 가사인지조차 알기 어렵습니다.
그런데 많은 법률 사무소의 초기 응대는 여전히 고객에게 전화로 자신의 문제를 처음부터 주관식으로 설명하도록 요구합니다.

이 방식은 다음 문제를 만듭니다.

```text
고객은 법률 용어를 모른다.
전화는 순간적으로 말하고 사라진다.
날짜, 금액, 상대방, 보유 자료가 빠지기 쉽다.
데스크 단계에서 사건 정보가 구조화되지 못한다.
변호사는 상담 시간에 기본 사실관계부터 다시 확인해야 한다.
고객은 상담료를 내도 기본 질문만 받고 끝났다고 느낄 수 있다.
```

결과적으로 초기 문의가 상담으로 이어지지 못하는 전환 손실이 발생합니다.

## Solution

이 문제를 `선택형 Legal Intake Form`과 `미니 법률 온톨로지`로 구조화합니다.

고객은 긴 주관식 설명을 쓰는 대신, 키오스크처럼 선택합니다.

```text
문의 목적
사건 유형
당사자 위치
핵심 사실
보유 자료
원하는 다음 단계
```

챗봇은 선택값을 자연어 안내문으로 정리합니다.

```text
현재 문의는 민사 사건에 가까워 보입니다.

금전 반환 또는 대여금 분쟁 가능성이 있습니다.
상담 전에는 입금 내역, 카카오톡/문자 대화,
상대방에게 반환을 요청한 기록을 날짜순으로 정리해 주세요.

계약서나 약정서가 있다면 함께 준비하는 것이 좋습니다.
입력하신 개인정보는 답변에 그대로 표시하지 않고 마스킹 처리됩니다.
```

## Minimal Legal Intake Form

### 1. 문의 목적

- 절차 안내
- 필요한 자료 확인
- 작성한 문서 검토
- 변호사 선임/계약 검토
- 전자소송 제출 안내

### 2. 사건 유형

- 민사
- 형사
- 가사
- 전자소송
- 잘 모르겠음

### 3. 당사자 위치

- 피해자
- 피고소인
- 원고
- 피고
- 신청인
- 상대방
- 잘 모르겠음

### 4. 핵심 사실

- 사건 발생일
- 상대방
- 문제가 된 금액 또는 피해 규모
- 현재 진행 단계
- 핵심 내용 한 문장

### 5. 보유 자료

- 계약서
- 입금 내역
- 카카오톡/문자
- 사진/영상
- 소장/고소장/통지서
- 없음

### 6. 원하는 다음 단계

- 상담
- 서면 검토
- 소송 준비
- 전자소송 제출
- 변호사 선임

## Mini Legal Ontology

이 case에서 온톨로지는 복잡한 법률 지식 그래프가 아닙니다.
고객의 선택값과 키워드를 사건 유형, 분쟁 영역, 준비 자료로 연결하는 최소 분류 체계입니다.

```text
고객 입력
-> 선택값
-> 사건 유형
-> 분쟁 영역
-> 준비 자료
-> 다음 정리 방향
```

예시:

```text
민사
-> 대여금 / 계약 / 임대차 / 손해배상

형사
-> 사기 / 폭행 / 고소 / 피고소

가사
-> 이혼 / 양육비 / 상속 / 친권

전자소송
-> 소장 / 답변서 / 보정명령 / 송달
```

## Product Value

### Customer Value

고객은 법률 용어를 몰라도 선택형 입력을 통해 자신의 문제를 정리할 수 있습니다.

- 내 문제가 민사, 형사, 가사, 전자소송 중 어디에 가까운지 감을 잡을 수 있습니다.
- 상담 전에 어떤 자료를 준비해야 하는지 알 수 있습니다.
- 전화하기 전에 불안이 줄어듭니다.
- 사무소가 체계적으로 응대하고 있다는 인상을 받습니다.
- 상담료를 내더라도 왜 필요한지 이해하기 쉬워집니다.

### Lawyer Value

변호사는 상담 전에 고객 문의를 구조화된 형태로 확인할 수 있습니다.

- 상담 전 사건 방향을 빠르게 파악할 수 있습니다.
- 고객의 자료 정리 상태가 개선됩니다.
- 기본 질문을 반복하는 시간이 줄어듭니다.
- 고객 전환율을 개선할 수 있습니다.
- 변호사가 사무실에 계속 상주하지 않아도 초기 문의 흐름을 관리할 수 있습니다.
- 광고 유입 고객을 놓치지 않고 상담 가능 상태로 구조화하는 저비용 고효율 마케팅 도구로 활용할 수 있습니다.

### System Value

시스템은 긴 자유입력과 불필요한 LLM 호출을 줄일 수 있습니다.

- 선택형 입력으로 자유입력 길이를 줄입니다.
- 사건 유형별 템플릿 응답을 활용할 수 있습니다.
- DTO Validation과 reasonCode 설계가 쉬워집니다.
- Cost Control을 적용하기 쉬워집니다.
- 개인정보 출력 마스킹, 보안 guardrail, metric 수집을 안정적으로 붙일 수 있습니다.

## Cost Reduction Thesis

선택형 intake와 미니 법률 온톨로지는 고객, 변호사, 시스템 모두의 비용을 줄이는 구조입니다.

```text
고객은 덜 헤맨다.
변호사는 덜 묻는다.
시스템은 덜 호출한다.
```

정리하면:

```text
선택형 intake는 고객 경험을 개선하고,
미니 법률 온톨로지는 그 선택값을 사건 구조로 바꿔
고객, 변호사, 시스템 모두의 시간·돈·에너지 비용을 줄인다.
```

## Security-Aware Extension

이 Legal Intake 구조는 AI 보안 구조와 결합될 수 있습니다.

```text
Fixed Guard
-> 위험 요청 차단

Dynamic Guard
-> 반복 위험 행동 차단

Cost Control
-> 긴 입력과 토큰 비용 폭주 차단

Privacy Output Guard
-> 개인정보 입력은 허용하되 출력은 마스킹

Prometheus / Grafana
-> 문의 흐름, 보안 차단, 비용 차단을 관찰
```

즉, 이 case는 단순한 챗봇 아이디어가 아니라,
도메인 온톨로지, 고객 경험, 보안 구조, 운영 지표를 연결하는 AI Technical PM 설계 사례입니다.

## Documents

- [선택형 Legal Intake와 미니 법률 온톨로지](docs/SELECTIVE_LEGAL_INTAKE_MINI_ONTOLOGY.md)
- [현실 문제 해결 온톨로지](docs/PROBLEM_SOLVING_ONTOLOGY.md)
- [Problem-Solving Ontology English Version](docs/PROBLEM_SOLVING_ONTOLOGY_EN.md)
