# Legal Intake Case Draft

This draft keeps the detailed Legal Intake case separate from the main ontology README.

The main README should explain the general operating principles of a domain-driven AI Technical PM.
This document keeps the concrete Legal Intake case for later reuse, editing, and portfolio expansion.

## Core Sentence

```text
The client selects, and the chatbot organizes.
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

1. Inquiry Purpose
   - Procedure guidance
   - Required document check
   - Drafted document review
   - Lawyer engagement or contract review
   - Electronic litigation filing guidance

2. Case Type
   - Civil
   - Criminal
   - Family
   - Electronic litigation
   - Not sure

3. Party Position
   - Victim
   - Accused person
   - Plaintiff
   - Defendant
   - Applicant
   - Counterparty
   - Not sure

4. Core Facts
   - Incident date
   - Counterparty
   - Disputed amount or damage scale
   - Current stage
   - One-sentence summary of the core issue

5. Available Documents
   - Contract
   - Bank transfer records
   - KakaoTalk/text messages
   - Photos/videos
   - Complaint/petition/notice
   - None

6. Desired Next Step
   - Consultation
   - Document review
   - Litigation preparation
   - Electronic litigation filing
   - Lawyer engagement

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

This case is not just a chatbot idea.
It is an AI Technical PM design case that connects domain ontology, customer experience, security architecture, and operational metrics.
