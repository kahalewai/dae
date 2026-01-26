<div align="center">

# DAE Security Standard for AI Agents

Welcome to the **DAE** (Deterministic Agent Execution) Security Specification Landing

![dae](https://github.com/user-attachments/assets/27987a4f-0e49-480e-9350-4bf258957c03)


</div>

## Intro

As AI agents become increasingly autonomous, current architectures rely heavily on probabilistic reasoning systems to both decide *what* to do and implicitly authorize *doing it*. This methodology has led to fundamental security and governance failures. DAE (Deterministic Agent Execution) is a security standard for AI agents that proposes a more deterministic methodology inspired by capability-based security. 

The AI industry lacks a formal, deterministic execution boundary that clearly defines what an agent is *allowed* to do versus what it *recommends*. Existing approaches depend on prompts, tool allowlists, and best-effort guardrails that cannot be enforced, audited, or revoked at runtime.

DAE addresses this gap.

DAE defines a production-ready, vendor-neutral security standard that separates reasoning from authority and enforces all actions through explicit, single-use, revocable capabilities validated by a deterministic runtime state machine. Under DAE, nothing happens unless it is explicitly authorized in code.

The goal of DAE is simple: enable secure, auditable, deterministic agent execution by introducing a formal authority model that makes autonomous systems predictable, governable, and safe for real-world deployment.

<br>

## DAE Execution Model

DAE provides a deterministic execution and security reference model for AI agents, describing the runtime mechanisms required to safely authorize, execute, and govern agent actions. Rather than layering intelligence, DAE layers *authority and enforcement*, ensuring that every action is intentional, approved, and verifiable.

The DAE model is built around a strict separation of concerns:

* Reasoning systems propose actions
* Policy systems issue authority
* Runtime enforcement guarantees compliance

<br>

| Component | Name                    | Responsibility                           | Security Guarantee Provided                       |
| --------- | ----------------------- | ---------------------------------------- | ------------------------------------------------- |
| 1         | Intent                  | Declares user-desired outcome            | Binds maximum allowable authority                 |
| 2         | Plan                    | Defines ordered execution steps          | Prevents implicit or emergent behavior            |
| 3         | Runtime State Machine   | Governs legal execution transitions      | Blocks skipped steps and illegal execution        |
| 4         | Authority Tokens        | Represent single-use execution authority | Eliminates ambient and implicit permissions       |
| 5         | Enforcement Gate        | Mediates all side-effectful actions      | Guarantees policy-compliant execution             |
| 6         | Provenance Enforcement  | Classifies and constrains data influence | Prevents prompt injection and authority smuggling |
| 7         | Escalation & Revocation | Handles policy violations and approvals  | Enables safe interruption and recovery            |

<br>

This execution model is implementation-agnostic and applies to single agents, multi-agent systems, tool-using LLMs, autonomous workflows, and shared multi-tenant platforms. Security, correctness, and governance are first-class properties enforced at runtime, not aspirational guidelines.

<br>

## View the DAE Security Specification

For a complete specification of the DAE standard, including formal definitions, principles, mechanisms, and conformance requirements, see the full reference document: 

https://github.com/kahalewai/dae/blob/main/dae_standard.md

**Status:** Production-Ready  
**Version:** v1.0.0  
**License:** Apache License 2.0  
**Date:** 2025-12-22

<br>

## Reference Implementation of DAE

For a reference implementation of the DAE Standard, visit the Agent Policy Engine (APE) Repository: [https://github.com/kahalewai/agent-policy-engine](https://github.com/kahalewai/agent-policy-engine), also released Apache 2.0

<br>

## Contribute

DAE is a production-ready open security standard, and like all successful standards, it is designed to evolve through open, collaborative development. This repository serves as the canonical home for the DAE specification, where the community can propose improvements while preserving the standard’s formal guarantees.

We invite AI platform builders, security architects, researchers, and standards authors to participate in the evolution of DAE through transparent, structured collaboration.

Participation includes:

* Contributing clarifications, examples, and formal refinements
* Proposing extensions that preserve deterministic enforcement
* Reviewing changes for security and correctness impact
* Advancing interoperability and certification readiness

**Why contribute?**

* Help define a foundational security standard for autonomous AI
* Establish clear authority boundaries for agent systems
* Enable auditable, certifiable AI deployments
* Influence the future of safe autonomous execution

**How to get started:**

1. Fork the repository.
2. Review the current DAE specification and principles.
3. Open a Pull Request with proposed edits or additions.
4. Participate in technical discussions and reviews.

<br>

By working together, we can ensure DAE becomes a **widely adopted, rigorously defined execution standard** that enables trustworthy autonomy across the AI ecosystem.



