<div align="center">

<br>

# SHINE HARVEST

#### SPACE-BASED SOLAR POWER

**Controlled Digital Engineering Program**

<br>

[![Program Phase](https://img.shields.io/badge/Phase_0-Architecture-0F172A?style=for-the-badge&labelColor=1E293B)](#program-phases)
&nbsp;
[![Repositories](https://img.shields.io/badge/10-Repositories-0F172A?style=for-the-badge&labelColor=1E293B)](#program-repositories)
&nbsp;
[![Demo Gate](https://img.shields.io/badge/Demo_Gate-Conditional_Pass-0F172A?style=for-the-badge&labelColor=1E293B)](#milestone-status)
&nbsp;
[![Classification](https://img.shields.io/badge/Private-Proprietary-DC2626?style=for-the-badge&labelColor=991B1B)](#)

<br>

---

<br>

*Persistent clean energy from space,*
*delivered through controlled orbital infrastructure.*

<br>

</div>

---

## Program Overview

Shine Harvest is a space-based solar power (SBSP) system architecture designed to collect solar energy in orbit, transmit it as a directed beam to terrestrial receiving stations, and deliver electricity to energy markets through secure, evidence-governed coordination.

This GitHub organization is the **private digital engineering backbone** of the program. It is not a public showcase. It follows Tier-1 aerospace configuration-control practices: baselined requirements, controlled interfaces, traceable verification evidence, and explicit state semantics across every subsystem boundary.

The architecture distinguishes five layers of physical truth and three cross-cutting governance functions, each managed in a dedicated repository with explicit ownership, interface contracts, and verification linkage.

---

## System Architecture

```
                                                                         GOVERNANCE
    PHYSICAL TRUTH CHAIN                                                 ─────────
    ──────────────────

    ┌─────────────────────────────┐                              ┌──────────────────┐
    │      SOLAR GENERATION       │  Collection state            │                  │
    │                             │  Generation output           │    ARCHITECTURE   │
    │  sh-solar-generation        │  Eclipse / degradation       │                  │
    └──────────────┬──────────────┘                              │  Requirements    │
                   │                                             │  State dictionary │
                   │  SH-ICD-SOL-ORB-001                        │  Interface matrix │
                   │                                             │  ConOps / ICDs   │
    ┌──────────────▼──────────────┐                              │                  │
    │      ORBITAL PLATFORM       │  Platform state              └──────────────────┘
    │                             │  Availability
    │  sh-orbital-platform        │  Constellation               ┌──────────────────┐
    └──────────────┬──────────────┘                              │                  │
                   │                                             │   VERIFICATION    │
                   │  SH-ICD-ORB-BMC-001                        │                  │
                   │                                             │  Trace matrix    │
    ┌──────────────▼──────────────┐                              │  XRV cases       │
    │       BEAM CONTROL          │  Transmission state          │  Evidence index  │
    │                             │  Safety interlocks           │  Milestone gates │
    │  sh-beam-control            │  Mode selection              │                  │
    └──────────────┬──────────────┘                              └──────────────────┘
                   │
                   │  SH-ICD-BMC-GND-001                        ┌──────────────────┐
                   │                                             │                  │
    ┌──────────────▼──────────────┐                              │    SECURITY       │
    │      GROUND SEGMENT         │  Site readiness              │                  │
    │                             │  Telemetry                   │  Threat models   │
    │  sh-ground-segment          │  Grid interface              │  Trust boundaries│
    └──────────────┬──────────────┘                              │  Control integrity│
                   │                                             │                  │
                   │  SH-ICD-GND-MKT-001                        └──────────────────┘
                   │
    ┌──────────────▼──────────────┐
    │       MARKET LAYER          │  Dispatch state              ┌──────────────────┐
    │                             │  Delivery accounting         │                  │
    │  sh-market-layer            │  Settlement                  │    SIMULATIONS    │
    └─────────────────────────────┘                              │                  │
                                                                 │  Scenario models │
    ┌─────────────────────────────┐                              │  Evidence output │
    │        AUTONOMY             │  Coordination                │  Benchmarks      │
    │                             │  Anomaly handling            │                  │
    │  sh-autonomy                │  Scheduling                  └──────────────────┘
    └─────────────────────────────┘
         ▲    ▲    ▲    ▲
         │    │    │    │
        SOL  ORB  BMC  GND    (consumes state from all operational layers)
```

**Design principle:** Each layer publishes its own truth. Downstream layers consume that truth — they do not invent it or silently widen its meaning.

---

## Program Repositories

### Phase A — Governance Backbone

These repositories define meaning, control, evidence, and trust before any operational system is built.

| Repository | Domain | Role | Criticality |
|:-----------|:-------|:-----|:------------|
| [`sh-architecture`](https://github.com/shineharvest/sh-architecture) | Systems Engineering | Mission architecture, ConOps, system requirements, state dictionary, ICDs, trade studies, risk register, roadmap, program handbook | Critical |
| [`sh-simulations`](https://github.com/shineharvest/sh-simulations) | Modeling & Analysis | Orbital mechanics, transmission efficiency, reliability, economics scenario models, controlled evidence output | Critical |
| [`sh-verification`](https://github.com/shineharvest/sh-verification) | V&V | Requirements traceability matrix, cross-repo verification cases (XRV), evidence index, milestone gate assessments, review records | Critical |
| [`sh-security`](https://github.com/shineharvest/sh-security) | Security Assurance | System threat model, trust boundary map, control integrity rules, hardening baseline, access/incident/secrets policies | Critical |

### Phase B — Physical Truth

These repositories own the upstream physical state of the system: what power is generated and what platform context surrounds it.

| Repository | Domain | Role | Criticality |
|:-----------|:-------|:-----|:------------|
| [`sh-solar-generation`](https://github.com/shineharvest/sh-solar-generation) | Power Production | Solar collection architecture, 9-state generation model, 5-category output baseline, sunlight/eclipse behavior, degradation logic | High |
| [`sh-orbital-platform`](https://github.com/shineharvest/sh-orbital-platform) | Spacecraft Operations | Platform state model, subsystem health aggregation, energy availability computation, constellation coordination | High |

### Phase C — Operational Systems

These repositories implement transmission, reception, and coordination — all consuming upstream physical truth.

| Repository | Domain | Role | Criticality |
|:-----------|:-------|:-----|:------------|
| [`sh-beam-control`](https://github.com/shineharvest/sh-beam-control) | Transmission & Safety | Phased-array steering, 8-state control model, safety interlock hierarchy, mode selection, beam authorization logic | Safety-Critical |
| [`sh-ground-segment`](https://github.com/shineharvest/sh-ground-segment) | Reception & Grid | 7-state site readiness model, telemetry baseline, operator workflows, grid integration interface | Critical |
| [`sh-autonomy`](https://github.com/shineharvest/sh-autonomy) | Coordination & Scheduling | 7-state coordination model, anomaly handling policy, scheduling baseline, cross-system state synchronization | High |

### Phase D — Value Realization

| Repository | Domain | Role | Criticality |
|:-----------|:-------|:-----|:------------|
| [`sh-market-layer`](https://github.com/shineharvest/sh-market-layer) | Energy Markets | 8-state dispatch model, delivery accounting, settlement baseline, demand signaling interface | High |

---

## Cross-Repo Interface Matrix

The program maintains 35 controlled interfaces (SH-IF-001 through SH-IF-035) across 5 interface types. The full matrix is governed in `sh-architecture/icd/cross-repo-interface-dependency-matrix-v0.2.md`.

**Interface priority after the solar-generation split:**

| Priority | Interfaces | Path | Rationale |
|:---------|:-----------|:-----|:----------|
| P1 | SH-IF-008, 009, 020, 021 | BMC ↔ GND + SEC | Primary safety and operational delivery path |
| P2 | SH-IF-003, 006, 011, 012 | SOL → ORB → AUT/BMC | Upstream physical-truth chain: generation drives platform, which drives beam and autonomy |
| P3 | SH-IF-014, 015, 016, 019 | SOL/ORB/BMC → SIM → VNV | Architecture trade questions become reviewed evidence |
| P4 | SH-IF-025, 026, 027, 028, 029 | Operations → MKT | Market logic remains downstream of real system truth |

**Non-negotiable rules:**

1. A producer repo defines what it publishes. Consumer repos must not silently widen that meaning.
2. If SOL says output is eclipsed, degraded, or constrained — downstream repos must not treat it as normal.
3. If GND is not ready, BMC and MKT must not behave as though valid delivery exists.
4. AUT recommendations do not override safety, authorization, or trust-boundary baselines.

---

## Milestone Status

| Milestone | Tag | Status | Gate Owner |
|:----------|:----|:-------|:-----------|
| Org Baseline | `ORG-BASELINE-v1` | **PASS** | exec-admin |
| System Requirements Review | `SRR-v1` | In Progress | systems-architecture |
| Architecture Baseline | `ARCH-BASELINE-v1` | In Progress | systems-architecture |
| Simulation Baseline | `SIM-BASELINE-v1` | In Progress | simulation-modeling |
| Verification Baseline | `VNV-BASELINE-v1` | In Progress | verification-vnv |
| Security Baseline | `SEC-BASELINE-v1` | In Progress | security-assurance |
| Operations Baseline | `OPS-BASELINE-v1` | Planned | systems-architecture |
| Demo Readiness | `DEMO-READY-v1` | **Conditional Pass** | verification-vnv |
| Pilot Readiness | `PILOT-READY-v1` | Not Started | exec-admin |

**Demo Readiness — Conditional Pass rationale:** 22 requirements defined, all critical ICDs drafted, XRV-001 through XRV-007 closed with actions, risk register and threat model in place. Open items: SH-SIM-001 results pending, 9 XRV actions unresolved, branch protection awaiting Team plan upgrade.

---

## Program Phases

```
    Phase A              Phase B              Phase C              Phase D
    Foundations          Physical Truth       Operations           Value Realization
    ─────────────────    ─────────────────    ─────────────────    ─────────────────
    ARCH  SIM            SOL  ORB             BMC  GND  AUT       MKT
    VNV   SEC
    ─────────────────    ─────────────────    ─────────────────    ─────────────────
    [ CURRENT ]          [ CURRENT ]          [ NEXT ]             [ PLANNED ]
```

**Phase exit criteria are enforced.** No repo may advance to a later phase until its dependencies in the current phase are baselined. This sequencing is non-negotiable.

---

## State Hierarchy

The system follows a strict top-down state flow. Downstream layers interpret upstream truth — they do not contradict it.

```
    Layer 0    Generation Truth        SOL     Generation state, output confidence, eclipse
               │
    Layer 1    Platform Operations     ORB     Platform health, availability (consuming SOL)
               │
    Layer 2    Transmission Control    BMC     Beam state, safety interlocks, mode
               │
    Layer 3    Reception               GND     Site readiness, telemetry, grid
               │
    Layer 4    Coordination            AUT     Scheduling, anomaly response, dispatch
               │
    Layer 5    Value                   MKT     Allocation, settlement, delivery evidence
               │
    Layer 6    Assurance               SEC + VNV    Trust, evidence, readiness
```

All state terms are defined in `sh-architecture/docs/state-dictionary-v0.1.md`. When Layer 2 says the beam is DEGRADED, that word has a specific, controlled meaning — and it is the same meaning for every layer that reads it.

---

## Verification Posture

| Metric | Value |
|:-------|:------|
| System requirements defined | 22 |
| Cross-repo verification cases (XRV) | 18 (XRV-001 through XRV-015, XRV-SOL-001 through XRV-SOL-003) |
| XRV cases executed | 7 (XRV-001 through XRV-007, all Closed with Actions) |
| XRV cases planned | 11 |
| Controlled interfaces | 35 (SH-IF-001 through SH-IF-035) |
| ICDs drafted | 7 |
| ICDs in backlog | 3 (SH-ICD-SOL-ORB/BMC/AUT-001) |
| Risks registered | 8 |
| Simulation scenarios defined | 5 (SH-SIM-001 through SH-SIM-005) |
| Open XRV actions | 9 |

---

## Engineering Principles

| Principle | Meaning |
|:----------|:--------|
| Private by default | Public by exception. Release-controlled always. |
| Architecture before code | Controlled baselines before implementation sprawl. |
| Evidence before claims | No milestone language without traceable artifacts. |
| Safety before throughput | Controlled delivery before optimization. |
| Security from day one | Not a compliance afterthought. Threat models in Phase A. |
| Generation truth is explicit | No downstream claim exceeds what SOL can justify. |
| Interfaces before internals | Cross-repo contracts before subsystem logic. |

---

## Organization

### Engineering Teams

| Team | Domain | Primary Repo |
|:-----|:-------|:-------------|
| `exec-admin` | Program administration | All (admin) |
| `systems-architecture` | Architecture, requirements, ICDs | sh-architecture |
| `solar-generation` | Collection, generation state, output | sh-solar-generation |
| `orbital-platform` | Spacecraft, constellation, availability | sh-orbital-platform |
| `beam-control` | Transmission, steering, safety | sh-beam-control |
| `ground-segment` | Receiving sites, telemetry, grid | sh-ground-segment |
| `autonomy-ai` | Coordination, anomaly detection, scheduling | sh-autonomy |
| `market-systems` | Dispatch, accounting, settlement | sh-market-layer |
| `simulation-modeling` | Scenarios, models, evidence generation | sh-simulations |
| `verification-vnv` | Traceability, evidence, readiness gates | sh-verification |
| `security-assurance` | Threat models, trust, hardening | sh-security |

### External Access

| Team | Access Model |
|:-----|:-------------|
| `external-auditors` | Read-only on governance repos (ARCH, SIM, VNV, SEC, SOL) |
| `vendors-partners` | Per-repo scoped access, granted per engagement |

---

## Key Documents

| Document | Location | Version |
|:---------|:---------|:--------|
| Program Handbook | `sh-architecture/docs/program-handbook-v0.1.md` | 0.2 |
| State Dictionary | `sh-architecture/docs/state-dictionary-v0.1.md` | 0.2 |
| Interface Dependency Matrix | `sh-architecture/icd/cross-repo-interface-dependency-matrix-v0.2.md` | 0.2 |
| System Requirements | `sh-architecture/requirements/system-requirements-v0.1.md` | 0.1 |
| Concept of Operations | `sh-architecture/conops/conops-v0.1.md` | 0.1 |
| Risk Register | `sh-architecture/risk/risk-register-v0.1.md` | 0.1 |
| Verification Plan | `sh-verification/verification-plans/vnv-plan-v0.1.md` | 0.1 |
| Demo Readiness Gate | `sh-verification/milestone-gates/demo-readiness-gate-v0.3.md` | 0.3 |
| System Threat Model | `sh-security/threat-models/system-threat-model-v0.1.md` | 0.1 |
| Generation State Model | `sh-solar-generation/docs/generation-state-model-v0.1.md` | 0.1 |

---

<div align="center">

<br>

**SHINE HARVEST**

Space-Based Solar Power — Controlled Engineering Program

<br>

[![Private](https://img.shields.io/badge/All_Repos-Private-991B1B?style=flat-square)](#)
&nbsp;&nbsp;
[![Proprietary](https://img.shields.io/badge/License-Proprietary-991B1B?style=flat-square)](#)
&nbsp;&nbsp;
[![2FA](https://img.shields.io/badge/2FA-Required-166534?style=flat-square)](#)
&nbsp;&nbsp;
[![Access](https://img.shields.io/badge/Access-Least_Privilege-312E81?style=flat-square)](#)
&nbsp;&nbsp;
[![Baselines](https://img.shields.io/badge/Change_Control-Active-312E81?style=flat-square)](#)

<br>

</div>
