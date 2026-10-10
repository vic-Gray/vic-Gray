<!--
  VICTORY GRAY · SYSTEMS ARCHITECT
  Keep this README evidence-led: update project status and architecture as implementations evolve.
-->

<div align="center">

# VICTORY GRAY

### ENGINEER THE SYSTEM. UNDERSTAND THE PROBLEM.

**Backend Engineering · Product Infrastructure · Open Source**

Nigeria 🇳🇬 · [Portfolio](https://portfolio-1dq.pages.dev/) · [Email](mailto:victorygray59@gmail.com)

[![GitHub](https://img.shields.io/badge/GitHub-vic--Gray-101820?style=flat-square&logo=github&logoColor=white)](https://github.com/vic-Gray)
[![TypeScript](https://img.shields.io/badge/TypeScript-Engineering-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Open Source](https://img.shields.io/badge/Open%20Source-Building%20in%20public-26C99A?style=flat-square&logo=github&logoColor=101820)](https://github.com/vic-Gray?tab=repositories)

</div>

---

> Software is more than the code we write. It's the decisions, data, boundaries, and infrastructure that make the whole system work.

I'm a software engineer focused on backend development, product infrastructure, and building software around real-world problems.

I care about what happens beneath the interface: how data moves, how systems communicate, how trust is established, and how applications behave when things don't go as planned.

**The goal: build software that's understandable, dependable, and worth maintaining.**

## 01 / Systems in development

### SYS.001 — SafeCrib
**Trust infrastructure for student accommodation.**

A campus accommodation platform designed to help students find homes while reducing exposure to rental scams. Its core idea is that a submitted home should not become publicly discoverable until it has passed verification.

**Engineering problem:** model the listing lifecycle so submission, review, verification, and publication are distinct states.

[Project organization](https://github.com/code-flexing)

### SYS.002 — Harvest Finance
**Financing infrastructure for smallholder farmers.**

A blockchain-powered supply-chain financing project exploring how farmers can access upfront capital against confirmed orders, with Stellar-based payment flows and transparent transaction records.

**Engineering problem:** connect application workflows, financing state, and blockchain settlement without losing track of what has happened.

[Explore the repository →](https://github.com/vic-Gray/Harvest-Finance)

### SYS.003 — Engagement API
**Backend for a Web3-ready content platform.**

An API project exploring content interactions and reward mechanisms, with an emphasis on backend functionality and extensible product logic.

[Explore the repository →](https://github.com/vic-Gray/engagement-api)

### SYS.004 — Event API
**The backend behind event-booking workflows.**

An API project featuring authentication, event-booking functionality, and email integration.

[Explore the repository →](https://github.com/vic-Gray/event-api)

---

## 02 / Architecture notes

These are high-level conceptual flows, not claims that every integration is already deployed.

### SafeCrib — trust and verification

~~~mermaid
flowchart LR
    A[Student] --> UI[Application]
    L[Agent / Landlord] --> UI
    UI --> API[Backend API]
    API --> DB[(Application Database)]
    L -->|Submit home| API
    API --> Q[Verification / Review]
    Q -->|Approved| P[Public listings]
    Q -->|Not approved yet| H[Hidden listing]
    A -->|Browse verified homes| P
~~~

**Design principle:** a submitted listing and a public listing are not the same thing.

### Harvest Finance — financing flow

~~~mermaid
flowchart LR
    F[Farmer] --> APP[Application]
    B[Buyer / Order] --> APP
    APP --> API[Backend API]
    API --> DB[(Transaction and order records)]
    API --> SF[Financing workflow]
    SF --> ST[Stellar / payment layer]
    ST --> TX[Settlement and transaction record]
~~~

**Design principle:** application state, financing decisions, and payment settlement should be traceable as separate steps.

---

## 03 / Engineering toolbox

| Layer | Tools |
|---|---|
| Languages | TypeScript · JavaScript · SQL |
| Backend | Node.js · NestJS · Express.js |
| Data | PostgreSQL · MongoDB · Supabase |
| Integrations | REST APIs · Nodemailer · Cloudinary |
| Workflow | Git · GitHub |

I choose tools based on the problem, not the other way around. What matters is understanding the trade-offs behind a technical decision and building with intention.

## 04 / How I think about systems

~~~text
UNDERSTAND THE PROBLEM
          ↓
MODEL THE SYSTEM
          ↓
DEFINE THE BOUNDARIES
          ↓
BUILD AND TEST
          ↓
LEARN FROM FAILURE
          ↓
IMPROVE THE SYSTEM
~~~

The areas I keep exploring:

- **API design:** predictable contracts, validation, authentication, and useful errors.
- **Data integrity:** deliberate models, clear state transitions, and consistency.
- **Architecture:** maintainable modules and boundaries that can evolve.
- **Reliability:** thinking about failure paths, not only the happy path.
- **Product engineering:** connecting implementation choices to real user needs.
- **Open source:** learning in public and building software others can inspect and use.

## 05 / Beyond the code

I'm interested in using software to solve meaningful problems in African communities and beyond—from safer student accommodation to better access to financing.

I value honest engineering, thoughtful collaboration, and the discipline to understand a problem before reaching for a tool.

## 06 / Connect

- **GitHub:** [@vic-Gray](https://github.com/vic-Gray)
- **Portfolio:** [Explore my work](https://portfolio-1dq.pages.dev/)
- **Email:** [victorygray59@gmail.com](mailto:victorygray59@gmail.com)

---

<div align="center">

**BUILD WITH INTENTION. DESIGN FOR REALITY.**

<sub>VICTORY GRAY / SYSTEMS ARCHITECTURE · OPEN SOURCE · REAL PROBLEMS</sub>

</div>
