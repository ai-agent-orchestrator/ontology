# Legal Ontology Feedback

This `legal` branch is a market-research and ontology-design note for a future legal AI chatbot.

The focus is the intake layer before legal advice begins.

## AI Legal Firm Chatbot Direction

The target product is:

```text
AI Legal Firm Chatbot
= ontology-driven legal intake system
```

The goal is not a final legal-answer chatbot.
The goal is an intake system that structures the case before formal legal advice begins.

```text
legal intake
-> evidence-to-issue mapping
-> case readiness
-> lawyer routing
-> AI-assisted self-representation support
```

Boundary:

```text
This is not legal advice.
This is a legal intake, evidence mapping, and workflow-structuring concept.
```

## Chatbot System Design

The AI chatbot should combine conversation, ontology, backend history, and guardrails.

```text
Legal intake chatbot
-> structured conversation
-> free-text story capture
-> ontology extraction
-> evidence-to-issue mapping
-> readiness score
-> missing information questions
-> consultation packet
-> lawyer routing
-> guardrail boundary
```

Core application modules:

```text
SSE streaming UI
JWT login
chat history
intake history
readiness score
evidence map
case graph
guardrail boundary
admin / lawyer dashboard
metrics and trace history
```

The chatbot should not jump directly to legal conclusions.

It should first ask:

```text
What happened?
Who are the parties?
What claim or outcome does the user want?
What evidence exists?
Which dates and deadlines matter?
What is the current procedural stage?
What information is missing?
What service scope is the user actually asking for?
```

## Ontology-First Structure

The chatbot should convert conversation into a structured ontology.

Core entities:

```text
Case
Party
Claim
Defense
Fact
Evidence
Issue
Deadline
Damage
ProcedureStage
Risk
Action
Document
ServiceScope
ReadinessDecision
ConsultationPacket
LawyerRouting
```

Core relationships:

```text
Case hasParty Party
Case hasClaim Claim
Claim requiresFact Fact
Fact supportedBy Evidence
Evidence proves Issue
Case hasDeadline Deadline
Case hasProcedureStage ProcedureStage
Case hasRisk Risk
Case needsAction Action
User requestsServiceScope ServiceScope
ReadinessDecision recommends Action
ConsultationPacket summarizes Case
LawyerRouting routes Case to ServiceScope
```

Ontology-driven conversation flow:

```text
User narrative
-> extract facts, parties, dates, amounts, documents
-> classify case type
-> identify claims and possible issues
-> map evidence to facts/issues
-> detect missing information
-> calculate readiness score
-> recommend next step
-> generate consultation packet
```

## Market Positioning

This product is positioned between full legal representation and unsupported self-representation.

```text
full representation
<->
AI-assisted legal intake and case preparation
<->
self-representation without tools
```

The market opportunity:

```text
users are increasingly AI-assisted and evidence-aware
but many law offices still rely on phone-first intake and weak routing
```

The product answer:

```text
intake system chatbot
-> filtering
-> summarization
-> readiness scoring
-> evidence mapping
-> consultation packet
-> lawyer routing
```

## Market Observation

After direct contact with many law offices over about a month, the main bottleneck appeared to be less about legal theory itself and more about the weakly structured intake process before consultation.

Legal clients are no longer information-empty.

Many users now arrive after:

```text
search
YouTube
community reading
AI-assisted case structuring
electronic court experience
draft document preparation
```

But many legal offices still operate with:

```text
phone-first intake
desk-level filtering
unstructured consultation
high upfront retainers
weak written output
Naver-focused marketing
limited digital workflow
```

This creates a gap between user expectation and legal service intake.

## Core Thesis

```text
Legal service transformation will not come only from AI answering legal questions.
It will come from AI restructuring the intake, evidence mapping, document preparation, and lawyer routing workflow before formal representation begins.
```

Korean version:

```text
법률 서비스의 변화는 AI가 법률 질문에 답하는 것만으로 오지 않는다.
정식 수임 이전의 intake, 증거 매핑, 문서 준비, 변호사 연결 워크플로우가 AI로 재구조화되면서 온다.
```

## Four Market Segments

The legal market may become more polarized.

```text
1. high-skill lawyers with strong marketing
2. specialized boutique law firms with clear domain positioning
3. network / brand-based firms handling easier cases at scale
4. mid-tier undifferentiated offices with high retainers but weak structured output
```

The fourth segment faces an existential question:

```text
Will it become a consumer-close boutique with structured intake,
clear service scope, strong communication, and digital workflow?

Or will it remain a high-fee, low-output, phone-first office
and lose users who can now prepare cases with AI?
```

This is not only a marketing problem.
It is a business model and workflow problem.

Even courts are becoming more digital:

```text
electronic court
online filing
digital evidence
document-based procedure
remote information access
```

But many legal offices still depend on:

```text
phone calls
signboards
word of mouth
Naver ads
unstructured desk filtering
```

This gap creates both crisis and opportunity.

## Intake Product Direction

The product direction is an intake system chatbot.

```text
not a final legal-answer chatbot
but a filtering, summarization, readiness, and routing chatbot
```

Possible service flow:

```text
1. user starts AI intake
2. AI asks structured questions
3. user writes free-text story
4. AI extracts facts, dates, parties, evidence, claims
5. system creates readiness score
6. system identifies missing information
7. system generates consultation packet
8. user chooses paid consultation or document review
9. lawyer receives structured packet
10. consultation is more efficient
```

## Hybrid Intake Model

Legal intake cannot be fully checkbox-based because legal cases are narrative-heavy.

But pure free text is also too unstructured.

The better structure is hybrid:

```text
minimum checklist
+ free-text narrative
+ AI summarization
+ missing information detection
+ readiness scoring
+ routing decision
```

Draft intake fields:

```text
case type
claim purpose
desired service scope
evidence exists
deadline exists
opponent known
damage amount known
current procedural stage
urgency
budget range
preferred support type
```

## Evidence-To-Issue Mapping

The core of case preparation is not persuasive language alone.

The stronger structure is:

```text
issue
-> fact to prove
-> evidence
-> explanation
-> procedural submission
```

Legal AI should not only generate long arguments.
It should map evidence to issues.

```text
Legal AI should become an evidence map and case preparation system,
not only a legal answer generator.
```

## Self-Represented But AI-Augmented Users

Some users do not primarily need full representation.

They need:

```text
case structuring
evidence organization
issue mapping
document drafting support
deadline checks
procedural checklists
limited expert review
```

User type:

```text
self-represented but AI-augmented legal user
```

This creates a middle layer between:

```text
full representation
```

and:

```text
doing everything alone without tools
```

## Draft Ontology Direction

The future legal ontology should separate:

```text
Case
Party
Claim
Defense
Fact
Evidence
Issue
Deadline
Damage
ProcedureStage
Risk
Action
Document
ServiceScope
ReadinessDecision
```

Possible relationships:

```text
Case hasParty Party
Case hasClaim Claim
Claim requiresFact Fact
Fact supportedBy Evidence
Evidence proves Issue
Case hasDeadline Deadline
Case hasProcedureStage ProcedureStage
Case hasRisk Risk
Case needsAction Action
User requestsServiceScope ServiceScope
ReadinessDecision recommends Action
```

## Development Roadmap

Short-term prototype:

```text
Legal Intake Readiness API
Legal Intake History
Readiness Score
React Draft Panel
Legal Ontology Draft Document
```

Next project direction:

```text
Legal/admin knowledge graph
Case readiness graph API
Evidence-to-issue map
Missing information checklist
Consultation packet generator
```

AI chatbot direction:

```text
Legal intake chatbot
SSE streaming UI
JWT login
chat history
intake history
readiness score
guardrail boundary
```

Python / Guardrails direction:

```text
NeMo Guardrails input rail
legal advice boundary rail
Colang intake flow
Python ontology action
Spring history and metrics integration
```

LangChain / RAG direction:

```text
legal/admin document retrieval
evidence checklist retrieval
procedure guide retrieval
consultation packet grounding
LangSmith trace and evaluation
```

## Documents

- [Legal Ontology Brainstorming](docs/LEGAL_ONTOLOGY_BRAINSTORMING.md)
- [Legal Intake Readiness Draft](docs/LEGAL_INTAKE_READINESS_DRAFT.md)
- [Legal Procedure Knowledge Graph Draft](docs/LEGAL_PROCEDURE_KNOWLEDGE_GRAPH_DRAFT.md)
- [현실 문제 해결 온톨로지](docs/PROBLEM_SOLVING_ONTOLOGY.md)
- [Problem-Solving Ontology English Version](docs/PROBLEM_SOLVING_ONTOLOGY_EN.md)

## Positioning

This repository is a personal knowledge-structuring lab for turning messy legal-service observations into reusable ontology, product hypotheses, and AI system design patterns.

The long-term direction:

```text
Legal intake
-> evidence mapping
-> readiness scoring
-> safe RAG
-> guardrails
-> lawyer routing
-> observable AI workflow
```
