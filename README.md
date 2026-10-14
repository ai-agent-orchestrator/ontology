# Who Am I

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

Through hands-on experience and this development project, I designed an ontology structure that satisfies multi-dimensional market needs: client usability, lawyer workflow efficiency, AI security, observability, and cost control.

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

## AI Technical PM Operating Principles

This repository is not only a collection of ontology notes.
It defines how I structure real-world problems into AI service architecture.

My operating principle is simple:

```text
Market problem
-> domain ontology
-> user behavior
-> server flow
-> security policy
-> cost control
-> observability
-> feedback loop
-> reusable portfolio artifact
```

AI-era technical PM work is not just about proposing ideas.
It is about connecting user behavior, domain events, policies, data, code, and operational metrics into one explainable structure.

## 1. Market-Driven Problem Discovery

I start from hidden market needs, not from technology buzzwords.

The goal is to identify real information cost, search cost, operational waste, user confusion, and conversion loss.
Then I define whether an AI system can reduce time, money, and energy cost for the actual users.

## 2. Ontology-Based Problem Structuring

Ontology is not treated as an abstract concept.

I use ontology as a practical product structure that turns messy user input into selectable categories, meaningful states, and reusable decision paths.

```text
unstructured real-world problem
-> selectable structure
-> domain category
-> required information
-> next action
-> safer AI processing
```

## 3. AI-Native Development Method

AI accelerates code generation.
That means the human role should move higher: market judgment, system design, security, cost control, validation, refactoring, and operation.

My development flow follows a practical AI-era variation of TDD.

```text
AI modular draft
-> Postman verification
-> failure case check
-> feedback record
-> refactoring
-> documentation
-> demo
```

## 4. Security and Cost Control by Design

AI services must be designed with security and cost control from the beginning.

The key question is not only whether the LLM can answer.
The key question is whether the system can control risk before, during, and after the LLM call.

```text
risky request
-> block before LLM

repeated attack
-> detect by session behavior

long or expensive request
-> block by cost policy

personal information
-> allow necessary input, mask unsafe output

security decision
-> explain through reasonCode, metric, and audit trail
```

## 5. Top / Middle / Bottom Understanding

I understand AI systems through three layers.

### Top Layer

Overall architecture and request flow.

```text
Client
-> Security
-> Controller
-> Validation
-> Service
-> Policy
-> LLM
-> Output Guard
-> Metric
-> Response
```

### Middle Layer

DDD and Event Storming.

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

Implementation and verification.

```text
Policy
-> required data
-> code location
-> Postman verification
-> reasonCode / metric check
```

## 6. Event-to-Code Mapping

Event Storming should not remain only as a whiteboard artifact.

Each user action and domain event should be connected to policy, read model, code, Postman test, and operational evidence.

```text
overall flow
-> domain event
-> policy
-> required data
-> code location
-> Postman verification
-> refactoring
```

This is both a study method and an operational debugging method.

## 7. Postman-Based Feedback Loop

Postman is not used only to check whether an API works.

It is used to understand the server, verify policy decisions, reproduce failure cases, and collect evidence for refactoring.

```text
normal request
-> blocked request
-> cost limit request
-> repeated risky request
-> external API failure
-> output masking check
```

## 8. Error Stop Flow Verification

A reliable AI service must stop correctly when something goes wrong.

```text
No JWT
-> 401 before Controller

DTO Validation failure
-> 400 before Service

Fixed Guard block
-> no LLM call

Cost Control block
-> no LLM call
-> no actual token increase

Dynamic Guard block
-> subsequent requests blocked

External AI API failure
-> fallback response
-> no server-wide failure

Privacy Output Guard
-> no raw personal information exposure
```

This builds the ability to identify which server layer caused an error and how to redesign or reduce scope when needed.

## 9. Observable Operation

AI services must be observable in operation.

I treat `reasonCode`, metrics, dashboard, and feedback logs as part of the product, not as extra decoration.

```text
blocked reason
-> reasonCode

service behavior
-> Prometheus metric

operator understanding
-> Grafana dashboard

project learning
-> feedback loop and refactoring record
```

## 10. Build-Up Toward AI Orchestration

Each project should build reusable foundations for the next project.

The current focus is Spring Boot-based AI server architecture, security policy, cost control, observability, ontology-driven input structure, and Postman feedback loops.

The next expansion path is:

```text
Python
-> RAG
-> Vector DB
-> LangChain / LangGraph
-> NeMo actions
-> medical / legal AI security
-> multi-agent orchestration
```

## Core Thesis

AI-era product development should not stop at feature implementation.

It should connect market needs, domain ontology, user experience, server architecture, security, cost control, observability, feedback, and reusable artifacts.

That is the direction of my work as a domain-driven AI Technical PM.

## Documents

- [AI Technical PM Operating Principles](AI_TECHNICAL_PM_OPERATING_PRINCIPLES.md)
- [Problem-Solving Ontology English Version](docs/PROBLEM_SOLVING_ONTOLOGY_EN.md)
- [현실 문제 해결 온톨로지](docs/PROBLEM_SOLVING_ONTOLOGY.md)
- [선택형 Legal Intake와 미니 법률 온톨로지](docs/SELECTIVE_LEGAL_INTAKE_MINI_ONTOLOGY.md)
