<div align="center">

# Shine Harvest

### Space-Based Solar Power · Digital Engineering Program

[![Program Status](https://img.shields.io/badge/Status-Phase%200%20·%20Architecture-blue?style=for-the-badge)](#)
[![Repos](https://img.shields.io/badge/Repos-10%20Active-6366F1?style=for-the-badge)](#program-repositories)
[![Demo Readiness](https://img.shields.io/badge/Demo%20Gate-Conditional%20Pass-FBBF24?style=for-the-badge)](#milestone-status)
[![Classification](https://img.shields.io/badge/All%20Repos-PRIVATE%20·%20PROPRIETARY-red?style=for-the-badge)](#)

---

**Persistent clean energy from space, delivered through controlled orbital infrastructure.**

</div>

---

## About

Shine Harvest is developing a space-based solar power (SBSP) architecture capable of generating solar energy in orbit, managing transmission through controlled beaming, receiving energy through designated ground infrastructure, and delivering it through secure, economically optimized coordination.

This GitHub organization is the **private digital engineering backbone** of the program — not a public showcase. It follows Tier-1 aerospace configuration-control practices.

## Program Architecture

```
                    ┌─────────────────────┐
                    │   SOLAR GENERATION   │  Collection, generation state, output
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │   ORBITAL PLATFORM   │  Platform state, availability
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │    BEAM CONTROL      │  Phased-array steering & safety
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │   GROUND SEGMENT     │  Receiving, telemetry, grid interface
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │    MARKET LAYER      │  Dispatch, accounting, settlement
                    └─────────────────────┘

    ┌─────────────┐  ┌──────────────┐  ┌────────────────┐
    │  AUTONOMY   │  │   SECURITY   │  │  VERIFICATION  │
    │ Coordination│  │ Trust & Ctrl │  │ Evidence & Gates│
    └─────────────┘  └──────────────┘  └────────────────┘
```

## Program Repositories

### Governance Backbone

| Repo | Purpose | Criticality |
|------|---------|-------------|
| [`sh-architecture`](https://github.com/shineharvest/sh-architecture) | Mission architecture, ConOps, requirements, ICDs, trade studies, risk, roadmap | Critical |
| [`sh-simulations`](https://github.com/shineharvest/sh-simulations) | Orbital, transmission, reliability, and economics simulations | Critical |
| [`sh-verification`](https://github.com/shineharvest/sh-verification) | Requirements traceability, evidence control, milestone gates | Critical |
| [`sh-security`](https://github.com/shineharvest/sh-security) | Threat models, trust boundaries, hardening, control integrity | Critical |

### Physical Operations

| Repo | Purpose | Criticality |
|------|---------|-------------|
| [`sh-solar-generation`](https://github.com/shineharvest/sh-solar-generation) | Solar collection architecture, generation-state modeling, sunlight/eclipse logic, generated-power output | High |
| [`sh-orbital-platform`](https://github.com/shineharvest/sh-orbital-platform) | Platform state modeling, energy availability semantics, constellation coordination | High |

### Core Operations

| Repo | Purpose | Criticality |
|------|---------|-------------|
| [`sh-beam-control`](https://github.com/shineharvest/sh-beam-control) | Phased-array steering, safety interlocks, transmission-state logic | Safety-Critical |
| [`sh-ground-segment`](https://github.com/shineharvest/sh-ground-segment) | Site readiness, telemetry interpretation, grid integration | Critical |
| [`sh-autonomy`](https://github.com/shineharvest/sh-autonomy) | Fleet coordination, anomaly detection, scheduling | High |

### Value Layer

| Repo | Purpose | Criticality |
|------|---------|-------------|
| [`sh-market-layer`](https://github.com/shineharvest/sh-market-layer) | Dispatch, delivery accounting, settlement, pricing | High |

## Milestone Status

| Milestone | Tag | Status |
|-----------|-----|--------|
| Org Baseline | `ORG-BASELINE-v1` | PASS |
| System Requirements Review | `SRR-v1` | IN PROGRESS |
| Architecture Baseline | `ARCH-BASELINE-v1` | IN PROGRESS |
| Simulation Baseline | `SIM-BASELINE-v1` | IN PROGRESS |
| Verification Baseline | `VNV-BASELINE-v1` | IN PROGRESS |
| Security Baseline | `SEC-BASELINE-v1` | IN PROGRESS |
| Operations Baseline | `OPS-BASELINE-v1` | PLANNED |
| Demo Readiness | `DEMO-READY-v1` | CONDITIONAL PASS |
| Pilot Readiness | `PILOT-READY-v1` | NOT STARTED |

## Program Phases

```
Phase 0          Phase 1              Phase 2           Phase 3
Architecture ──→ Demonstration ──→ Pilot Deploy ──→ Commercial Scale
  [CURRENT]        [NEXT]
```

## Engineering Principles

- **Private by default** — public by exception, release-controlled always
- **Architecture before code** — controlled baselines before implementation sprawl
- **Evidence before claims** — no milestone language without traceable artifacts
- **Safety before throughput** — controlled delivery before optimization
- **Security from day one** — not a compliance afterthought

## Teams

| Team | Domain |
|------|--------|
| `exec-admin` | Program administration |
| `systems-architecture` | Architecture, requirements, ICDs |
| `orbital-platform` | Spacecraft, constellation, availability |
| `beam-control` | Transmission, steering, safety |
| `autonomy-ai` | Coordination, anomaly detection, scheduling |
| `ground-segment` | Receiving sites, telemetry, grid |
| `market-systems` | Dispatch, accounting, settlement |
| `security-assurance` | Threat models, trust, hardening |
| `simulation-modeling` | Scenarios, models, evidence generation |
| `verification-vnv` | Traceability, evidence, readiness gates |
| `external-auditors` | Read-only review access |
| `vendors-partners` | Per-repo scoped access |

---

<div align="center">

**Shine Harvest** · Space-Based Solar Power

*Controlled engineering program — not a public startup code dump.*

[![Private](https://img.shields.io/badge/All%20Repos-Private-red?style=flat-square)](#)
[![Proprietary](https://img.shields.io/badge/License-Proprietary-red?style=flat-square)](#)
[![2FA Required](https://img.shields.io/badge/2FA-Required-22C55E?style=flat-square)](#)
[![Least Privilege](https://img.shields.io/badge/Access-Least%20Privilege-6366F1?style=flat-square)](#)

</div>
