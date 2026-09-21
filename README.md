# AI-Assisted Detection Engineering and SOC Investigation Platform

**Purple Team · Detection Engineering**

`Prototype / lab platform` `MITRE ATT&CK` `Atomic Red Team` `Elastic` `AQL` `D3FEND`

A lab platform for running ATT&CK-aligned Atomic Red Team tests, collecting the telemetry they generate, producing AQL detection logic from that telemetry, validating it with AI assistance, and pairing it with D3FEND defensive guidance.

## Overview

Detection engineering tends to stall in the gap between a technique existing in ATT&CK and a tested rule that actually fires on it. Closing that gap by hand means standing up a target, running the technique, hunting for the telemetry it produced, guessing at field names, writing a query, and re-running everything to check the result.

This platform turns that loop into one guided workflow. A technique is selected from the ATT&CK matrix, the matching Atomic Red Team test is executed against a lab target, and the telemetry the test actually generated becomes the input to detection logic — rather than an assumed schema. Generated queries are AQL, reviewed with AI assistance, and paired with defensive guidance so the output reads as a defensive recommendation, not just a query string.

The current focus is the Detection Lab path. An AI SOC Agent investigation module is a planned expansion and is documented below as direction, not as shipped functionality.

## Detection Lab Workflow

1. **Select MITRE ATT&CK technique** — matrix UI
2. **Run Atomic Red Team test** — dynamic test discovery
3. **Collect telemetry from Windows target** — live output
4. **Retrieve logs from Elastic/Elasticsearch** — ingestion delay handled
5. **Generate AQL detection logic** — AQL + YAML rule
6. **Validate detection with AI** — assistive review
7. **Review telemetry and defensive guidance** — evidence + D3FEND

Each stage feeds the next, so the resulting AQL is written against fields that were genuinely present in the events the technique produced. AI validation is an assistive review step, not a guarantee of detection quality — a human reviewer is still expected in the loop.

## Current Capabilities

**MITRE ATT&CK matrix interface**
Browse tactics and techniques; the technique selection drives the rest of the workflow.

**Atomic Red Team execution**
Tests are discovered dynamically from the target rather than hardcoded, so the list reflects what is installed.

**Windows target attack validation**
Execution is brokered through a control node to the Windows target VM, with live command output streamed to the UI.

**Elastic telemetry lookup**
Post-execution log retrieval from Elastic indices, accounting for the delay before events become searchable.

**AQL detection generation**
Detection logic generated from observed telemetry, rendered as AQL alongside a structured YAML rule definition.

**AI-assisted query validation**
An LLM-backed adjudication step judges whether detection logic plausibly matches the telemetry that was collected.

**Detection library matching**
Telemetry is evaluated against a rule library to show existing coverage and coverage gaps before new logic is written.

**D3FEND defensive guidance**
Techniques are mapped toward defensive countermeasures. The concept is implemented; mapping breadth is still expanding.

**Log viewer and evidence review**
Table and raw-JSON views of the underlying telemetry, so detection logic traces back to the events that justified it.

## Architecture Overview

| Tier | Tech |
|---|---|
| Frontend UI | Next.js · React · Tailwind |
| Backend API | route handlers · execution / logs / detection |
| Kali control node | SSH · single execution path |
| Windows target VM | remote execution |
| Atomic Red Team execution | technique simulation |
| Winlogbeat / Elastic Agent | log shipping |
| Elastic / Elasticsearch | telemetry store |
| Detection Lab UI | results · evidence · guidance |

### Design notes

**The control node is not optional**
All remote execution is brokered through the control node rather than dispatched directly to the target, keeping a single auditable execution path.

**Telemetry is read from Elastic**
Detection logic is built against what the SIEM actually ingested — the same data a deployed rule would run over.

**Ingestion latency is expected**
Events are not searchable the instant a test finishes; retrieval accounts for that rather than assuming immediate availability.

**The pipeline is modular**
Attack execution, log retrieval, and detection generation are separate routes and libraries, so a stage can change independently.

## AI SOC Agent — Future Module

> **Planned module.** The routing surface for this module exists in the codebase as scaffolding; the investigation logic below is not implemented yet. It is documented to record intended direction, not current behavior.

The Detection Lab answers whether a detection exists and fires. The next module is meant to answer the question that follows an alert: what actually happened, and what should be done about it.

1. Detection fires
2. Alert appears in AI SOC Investigations
3. Analyst runs AI SOC Agent
4. Agent collects evidence
5. Agent queries Elastic/SIEM
6. Agent generates findings
7. Agent assigns verdict
8. Agent recommends remediation

The intent is a reviewable investigation record — evidence, findings, verdict, remediation — with the analyst as the decision-maker rather than the agent acting autonomously. Verdicts are meant to be advisory and traceable back to the evidence that produced them.

## Roadmap

| Item | Status |
|---|---|
| Linux VM attack execution | Planned |
| Expanded ATT&CK tactic/technique coverage | In progress |
| Improved telemetry-to-technique mapping | In progress |
| Deeper D3FEND mapping | In progress |
| Alert creation from validated detections | Planned |
| AI SOC Agent investigation workflow | Planned |
| Evidence locker | Planned |
| Investigation timeline | Planned |
| Alert queue | Planned |
| Remediation recommendations | Planned |
| Cloud log sources | Planned |
| Multi-agent SOC roles | Planned |

## Safety & Legal Disclaimer

**Authorized lab use only.** This project is intended only for authorized lab environments, detection engineering research, purple-team validation, and defensive security testing. Do not run attack simulations against systems you do not own or have explicit permission to test.

Running adversary simulation tooling against systems without authorization is illegal in most jurisdictions. Atomic Red Team tests make real changes to the target host — run them only against disposable lab VMs you can restore, and prefer non-destructive, non-administrative tests. You are responsible for the environment you point this at.

---

Lab / prototype platform under active development. Capability descriptions reflect current focus; items marked planned or in progress are not finished. See the repository README for setup and environment configuration.
