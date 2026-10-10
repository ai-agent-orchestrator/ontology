# Ontology Feedback

## Core Positioning

```text
Domain-driven AI Technical PM
for healthcare, legal, cybersecurity, and AI governance
```

I combine healthcare and legal domain experience with hands-on AI backend practice.
My focus is building safe, observable, and compliant AI systems for high-stakes domains.

```diff
Medical background
+ Legal dispute structuring experience
+ Ontology-driven thinking
+ AI-native PM / backend orchestration
= Legal/Medical AI Technical PM
```

## Repository Role

`ontology-feedback` is not just an idea archive.
It is a PM feedback repository for turning messy market observations into structured ontology hypotheses, testing them through API experiments, and improving portfolio output through feedback loops.

```text
market observation
-> ontology hypothesis
-> Postman experiment
-> feedback
-> structure revision
-> portfolio improvement
```

In this legal intake case, the repository records how a broad market observation became a concrete AI product structure.

```text
phone-first legal intake problem
-> selective Legal Intake Form
-> mini legal ontology
-> security-aware AI intake architecture
-> Postman evidence
-> portfolio refinement
```

Korean version:

```text
ontology-feedback
= 문제 관찰과 구조화 가설을 실험 결과로 다듬는 PM feedback repo
```

## Multi-Layer PM Analysis

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

## PM 관점 다층 분석

이 프로젝트는 단순히 법률 챗봇을 구현하는 것이 아니라,
법률 intake 문제를 시장, 의뢰인, 변호사, 기술, 보안, 운영 관점에서 나누어 분석한 뒤 설계했습니다.

### 1. 시장 관점

소규모 법률 사무소의 초기 응대는 전화 중심, 주관식 설명 중심, 담당자 역량 의존적인 경우가 많습니다.
고객 문의가 사건 정보로 구조화되지 못하면 상담 전환 손실이 발생할 수 있습니다.

### 2. 의뢰인 관점

법률 문제를 처음 겪는 고객은 자신의 사건이 민사인지, 형사인지, 가사인지조차 알기 어렵습니다.
따라서 처음부터 긴 주관식 설명을 요구하기보다, 선택형 입력과 준비자료 안내가 필요합니다.

### 3. 변호사 관점

정리되지 않은 상담은 변호사의 시간을 사실관계 청취와 기본 확인에 소모시킵니다.
의뢰인이 최소한의 자료와 사건 흐름을 준비하지 못한 상태에서 상담이 시작되면,
고객과 변호사 모두 상담 품질에 만족하기 어려운 구조가 됩니다.

상담 전 사건 유형, 보유 자료, 원하는 도움을 구조화하면
변호사는 상담 시간을 자료 분류가 아니라 쟁점 파악과 전략 검토에 사용할 수 있습니다.

### 4. 기술 관점

자유 대화형 챗봇보다 `Legal Intake Form` 기반 정보 제공형 챗봇이 MVP에 적합하다고 판단했습니다.
선택형 입력과 체크리스트를 사용하면 입력 구조화, DTO Validation, reasonCode, metric 설계가 쉬워집니다.

### 5. 보안 관점

AI 서비스는 LLM 호출 전에 위험 요청, 반복 공격, 비용 폭주, 개인정보 재출력을 통제해야 합니다.
이를 위해 보안 계층을 다음과 같이 분리했습니다.

- Fixed Guard: 단일 위험 요청 차단
- Dynamic Guard: 반복 위험 행동 감지
- Cost Control: 토큰 비용 폭주 방지
- Privacy Output Guard: 개인정보 출력 마스킹

### 6. 운영 관점

AI 서비스는 운영 중 관찰 가능해야 합니다.
초기 문의가 어디서 끊기는지, 어떤 요청이 차단되는지, 비용 차단이 얼마나 발생하는지
Prometheus/Grafana metric으로 볼 수 있어야 합니다.

따라서 차단 이유와 전환 손실을 reasonCode, metric, dashboard로 확인할 수 있도록 설계했습니다.

## Legal Intake Case

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
