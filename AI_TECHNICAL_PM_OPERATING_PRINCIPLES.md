# AI Technical PM Operating Principles

## 1. Technical PM Positioning

This project is not designed only as a developer-oriented feature implementation task.

As a technical PM, the goal is to design market problems, technical structure, security, cost control, operation, validation, and project artifacts together.

The project is intended to demonstrate the following capabilities.

1. Discovering hidden market needs and opportunities

   The project identifies information cost, search cost, and consultation conversion loss in the legal intake process, and defines them as an AI service opportunity.

2. Implementing a Spring Boot-based AI service

   The project implements a Legal Intake Form-based AI chatbot and Search Routing flow through a Spring Boot server, JPA database, React screen, and LLM API integration.

3. Designing and building AI security and cost control

   The project focuses on AI security and cost control, which will become increasingly important in the AI market. It aims to implement a 6-layer AI security structure and a 6-layer cost control structure.

4. Designing operational metrics and dashboards

   The project uses operational metrics and dashboards to improve operator convenience, service observability, and marketing decision-making.

5. Verifying and refactoring through Postman

   The project verifies normal flows, failure flows, and blocking flows through Postman experiments, then uses feedback to refactor the system.

6. Building AI-era project artifacts

   The project creates explainable artifacts for the server structure and operational flow, showing technical PM-level design capability.

In short, a technical PM is not only someone who proposes ideas.
A technical PM should be able to connect user behavior, domain events, policies, data, code, and operational metrics into one structure.

## 2. Market-Driven Positioning

This project is not just a feature implementation assignment.
It aims to design an AI service with real market value and commercial positioning.

The project starts from a real legal intake problem: clients face unreasonable information cost, search cost, and early consultation conversion loss.

The goal is to reduce the client's legal search burden and improve the early consultation conversion flow of law offices by applying appropriate AI technology to a real-life market problem.

## 3. AI-Era Development Method

In an era where AI accelerates development speed, the human role should not be limited to writing every line of code manually.

It is more important to define a market-relevant problem, design security and cost reduction from the beginning, include error handling and user experience improvement in the refactoring process, and build a feedback loop that considers operational convenience.

This project applies a practical development method based on the TDD concept learned in class, adapted to the AI era.

```text
AI modular draft
-> Postman verification
-> failure case check
-> feedback record
-> refactoring
-> documentation
-> demo
```

This method is not a way to reduce development effort.
It is a way to put more weight on the areas where humans should focus in the AI era: market value, security, cost control, operational observability, validation, and refactoring.

## 4. Flexible Early, Strict Late

This project does not try to fix every structure perfectly before development begins.

An AI service connects Spring Boot, JPA, LLM API, security policy, cost control, metrics, and screen flow. Because these elements interact with each other, the project starts by implementing while understanding the real system flow, then restructures the design through Postman experiments and Event Storming, and finally freezes the confirmed scope for stabilization, artifact organization, validation, refactoring, documentation, and demo preparation.

The operating principle is:

```text
Early stage:
Implement while understanding.

Middle stage:
Experiment and structure.

Late stage:
Freeze the scope and do not shake it.
```

## 5. Development Weight Balance

This project gives similar weight to implementation, real operation, cost management, validation, and refactoring.

It is not enough for a feature to simply work.

```text
Can a normal request be processed?
Can a risky request be blocked?
Can an over-budget request be blocked before the LLM call?
Is personal information masked in the output?
Does the system fallback when an external API fails?
Can the decision be explained through reasonCode and metrics?
Where should the server be checked when an error happens?
Can the design be reduced or rerouted when needed?
```

In this project, a feature is considered complete only when the normal flow, failure flow, blocking reason, and operational visibility are verified.

## 6. Top / Middle / Bottom Understanding Rule

This project is understood and tested through Top / Middle / Bottom layers so that the server operation sense and full system flow can be clearly grasped.

### Top Layer

The Top Layer uses Mermaid flow charts to understand the full server and AI flow.

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

The Middle Layer uses DDD and Event Storming to organize how user behavior becomes commands and domain events.

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

The Bottom Layer connects Policy / Read Model / Code / Postman.

```text
Policy
-> required data
-> code location
-> Postman verification
-> reasonCode / metric check
```

Through this structure, the full flow, domain events, policies, data, code, and verification are connected into one system.

## 7. Event-to-Code Mapping Rule

In this project, Event Storming results are not left only as documents.

Each event is connected to policy, read model, code, and Postman verification so that the actual server behavior can be checked.

This mapping table is a study artifact, an operational debugging artifact, and a core artifact for mapping user behavior to technical structure as a technical PM.

The final goal is to explain the following flow.

```text
overall flow
-> domain event
-> policy
-> required data
-> code location
-> Postman verification
-> refactoring
```

In other words, the core goal is to build the ability to map user behavior into technical structure and verify how that structure works in the real server.

## 8. Module Completion Rule

A feature is not complete just because the code has been written.

Each module should be completed as one bundle.

```text
module design
-> module implementation
-> Postman normal request
-> Postman failure / blocked request
-> reasonCode check
-> log / metric check
-> feedback record
-> artifact update
```

Only a module that passes this process is considered implemented.

## 9. Error Stop Flow Rule

In this project, it is important to verify not only normal behavior, but also whether the system stops the next step correctly when a failure occurs.

Representative stop flows are:

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

OpenAI API failure
-> fallback response
-> no server-wide failure

Privacy Output Guard
-> no raw personal information exposure
```

Through this process, the project builds the operational ability to identify which server layer caused an error and apply an alternative design when needed.

## 10. Final Project Build-Up Rule

This project is not an isolated project.
It is a build-up toward the later two-month final AI orchestration project.

Therefore, this project does not force advanced RAG, Python actions, or complex multi-agent architecture too early. Instead, it builds the following foundations.

```text
Spring Boot-based AI server flow
JPA DB design
LLM API integration
AI security policy
Cost Control
Privacy Output Guard
Prometheus / Grafana observability
Postman verification
DDD / Event Storming
Policy / Read Model / Code mapping
```

Based on this foundation, the final project can later expand into Python, RAG, Vector DB, LangChain / LangGraph, NeMo actions, and medical / legal AI security.
