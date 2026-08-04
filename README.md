# agentic-ai-network-investigation-team

# Agentic AI Network Investigation Team

> A vendor-agnostic multi-agent AI framework for autonomous network investigation and root cause analysis.

---

# Vision

Modern networks already generate enormous amounts of operational data.

Every second, organizations collect:

- Streaming telemetry
- SNMP metrics
- NetFlow/IPFIX records
- Syslog messages
- Configuration snapshots
- Routing information
- Synthetic test results
- Packet captures
- Digital twins
- Topology information

Collecting telemetry is becoming a commodity.

The difficult problem is transforming thousands of disconnected observations into a coherent explanation of:

- **What happened?**
- **Why did it happen?**
- **What evidence supports that conclusion?**
- **How should the problem be fixed?**

This repository focuses on that reasoning layer.

Rather than building another monitoring platform, this project builds an **Agentic AI Network Investigation Team** that investigates incidents much like an experienced Network Operations Center (NOC) engineer.

---

# Motivation

Today's network investigations are largely manual.

A typical engineer:

- reviews alarms
- checks dashboards
- runs CLI commands
- examines topology
- compares configuration changes
- analyzes routing
- performs traceroutes
- validates hypotheses
- gradually narrows the possible root causes

This process depends heavily on individual experience and is often difficult to reproduce.

Our goal is to create an AI-native investigation framework that performs this reasoning in a structured, explainable, and reproducible way.

---

# Project Goals

The Agentic AI Team should autonomously:

- understand an incident
- frame the investigation
- generate competing hypotheses
- plan evidence collection
- execute deterministic investigations
- analyze supporting and contradicting evidence
- challenge its own conclusions
- identify the most probable root cause
- recommend remediation

Version 1 intentionally stops at:

> **REMEDIATION_RECOMMENDED**

The system does **not** automatically modify production networks.

---

# Core Design Principles

## Vendor Agnostic

Evidence should come from any platform.

Examples include:

- Cisco
- Juniper
- Arista
- Nokia
- ThousandEyes
- Kentik
- Prometheus
- OpenTelemetry
- NIKA
- RIPE Atlas
- Topology Zoo

No reasoning agent should depend on vendor-specific APIs.

---

## Evidence First

Every conclusion must be grounded in observable evidence.

The framework distinguishes between:

- facts
- assumptions
- hypotheses
- observations
- evidence
- diagnoses

This separation enables explainable investigations.

---

## Agents Reason

Large Language Models perform reasoning.

Agents are responsible for:

- framing incidents
- generating hypotheses
- interpreting evidence
- challenging conclusions
- recommending remediation

---

## Executors Execute

Executors perform deterministic work.

Examples include:

- loading telemetry
- parsing configurations
- running graph algorithms
- querying routing information
- computing blast radius
- comparing network paths

Agents never directly query data sources.

---

## Network Twin

The investigation is grounded in a network twin represented as an Evidence Graph.

This graph enables reasoning across:

- topology
- dependencies
- routing
- services
- telemetry
- configuration
- events
- changes

rather than isolated datasets.

---

# Version 1 Architecture

```
NetworkInvestigationConfig
        │
        ▼
Incident Framing Agent
        │
        ▼
Investigation Manager Agent
        │
        ▼
Hypothesis Generator Agent
        │
        ▼
Evidence Planning Agent
        │
        ▼
Deterministic Executors
        │
        ▼
Evidence Analyst Agent
        │
        ▼
Hypothesis Challenger Agent
        │
        ▼
Root Cause & Remediation Agent
        │
        ▼
REMEDIATION_RECOMMENDED
```

---

# Initial Public Data Sources

Version 1 focuses on public datasets and network twins.

## Primary

- NIKA (Network Incident Benchmark for AI Agents)

## Planned

- RIPE Atlas
- Topology Zoo
- CAIDA
- MAWI
- UPC Network Digital Twin datasets

Commercial platforms will later be supported through vendor-specific adapters.

---

# Repository Structure

```
agentic-ai-network-investigation-team/
│
├── notebooks/
│
├── src/
│   ├── agents/
│   ├── executors/
│   ├── adapters/
│   ├── graph/
│   ├── schemas/
│   └── config/
│
├── data/
│
├── docs/
│
└── tests/
```

---

# Current Status

🚧 Early architecture and framework development.

Current work includes:

- investigation domain model
- configuration objects
- evidence graph
- NIKA integration
- deterministic executors
- multi-agent investigation workflow

---

# Long-Term Vision

This project aims to define an **AI-native operating model for Network Operations Centers (NOCs).**

Instead of manually correlating dashboards, logs, telemetry, topology, routing, and configuration data, engineers collaborate with an Agentic AI Team capable of constructing evidence-based explanations, identifying root causes, and recommending remediation using transparent and reproducible reasoning.

---

# License

MIT
