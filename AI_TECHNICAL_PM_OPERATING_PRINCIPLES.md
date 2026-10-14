# AI Technical PM Operating Principles

This document defines my working principles as a domain-driven AI Technical PM.

I do not approach AI projects only as feature implementation tasks.
I structure real-world problems through domain ontology, user behavior, security risk, cost control, observability, feedback loops, and reusable project artifacts.

## 1. Market-Driven Problem Discovery

Start from real market pain.

Find hidden information cost, search cost, operational waste, user confusion, and conversion loss.
Then define whether AI can reduce time, money, and energy cost for the actual users.

## 2. Ontology-Based Problem Structuring

Use ontology as a practical product structure.

The goal is not to create an abstract knowledge graph for its own sake.
The goal is to turn messy user input into selectable categories, meaningful states, and reusable decision paths.

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
Therefore, the human role should focus more on market judgment, system design, security, cost control, validation, refactoring, and operation.

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

AI services must control risk before, during, and after the LLM call.

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

Understand AI systems through three layers.

```text
Top Layer
-> overall architecture and request flow

Middle Layer
-> DDD / Event Storming

Bottom Layer
-> policy, data, code, Postman, reasonCode, metric
```

## 6. Event-to-Code Mapping

Event Storming should not remain only as a planning artifact.

Each user action and domain event should be connected to policy, read model, code, Postman verification, and operational evidence.

```text
overall flow
-> domain event
-> policy
-> required data
-> code location
-> Postman verification
-> refactoring
```

## 7. Postman-Based Feedback Loop

Postman is used to understand the server, verify policy decisions, reproduce failure cases, and collect evidence for refactoring.

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

## 9. Observable Operation

Treat reasonCode, metrics, dashboard, and feedback logs as part of the product.

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

```text
Spring Boot AI server
-> security policy
-> cost control
-> observability
-> ontology-driven input structure
-> Postman feedback loop
-> Python / RAG / Vector DB / LangChain / LangGraph / NeMo actions
-> medical and legal AI security
-> multi-agent orchestration
```

## Core Thesis

AI-era product development should not stop at feature implementation.

It should connect market needs, domain ontology, user experience, server architecture, security, cost control, observability, feedback, and reusable artifacts.
