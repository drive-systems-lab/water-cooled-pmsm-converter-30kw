# Design Basis

> **Status (Phase 2 – Design-Basis Baseline in Progress):**  
> This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator of the 30 kW-class, water-cooled PMSM drive/converter platform.  
> Its scope is limited at the present stage to design-basis role definition, design-input framing, operating-boundary framing, controlled-assumption structure, and deferred-topic framing.  
> Detailed quantitative assumptions, operating-boundary tables, control-architecture and interface-boundary definition, selected hardware-platform evidence, and build-ownership traceability are introduced progressively through subsequent Phase 2 work.

---

## 1. Purpose and Scope

This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator.

Its purpose is to define the engineering basis that later Phase 2 hardware-platform evidence, build-ownership traceability, and subsequent Phase 3 bring-up and representative validation work should build on.

At this stage, the document is intended to:

- define the role of the design-basis layer within the repository
- frame the initial design inputs for the machine-side converter demonstrator
- frame the operating-boundary categories at design-basis level
- set out the controlled-assumption structure to be developed during Phase 2
- prepare the design-basis layer for later hardware-platform evidence and build-ownership traceability
- preserve scope discipline as later engineering content is introduced

At this entry stage, this document does not establish hardware-platform evidence, operational validation, full dual-side hardware closure, or product-level claims.

---

## 2. Design Inputs

The design basis is organised around a **machine-side converter demonstrator** that serves as the physical core of the project.

This demonstrator is positioned within a **broader back-to-back system context**, which is retained to define system role, interface boundary, and the interpretation of later validation artefacts.

Within the present validation arrangement, the upstream side is represented at the **DC bus interface** by an **external DC source** rather than by a physically implemented source-side / grid-side stage.

At Phase 2 entry, the design-basis layer is introduced to support a demonstrator-level engineering reading in which:

- the machine-side converter demonstrator remains the only physical mainline
- broader back-to-back system context is retained at interpretation level
- the external DC source remains an upstream representation within the present validation arrangement
- subsequent design reasoning and hardware-platform evidence can be introduced with traceable continuity from this design-basis layer

---

## 3. Operating Boundary

At the present repository stage, the operating boundary is introduced at **design-basis level** rather than as a complete operating-envelope definition.

The role of this section is to frame the boundary categories that later Phase 2 work will progressively make explicit.

These categories include:

- power-class interpretation
- DC input / DC bus / DC-link relationship
- current-level framing
- cooling approach
- representative PMSM and shaft-side boundary
- machine-side operating and later validation focus
- source-side / grid-side context retained at system-context level only

At this stage, these categories provide controlled engineering framing for the machine-side converter demonstrator, rather than a final product specification or complete validation envelope.

---

## 4. Controlled Assumptions

Phase 2 will progressively introduce controlled assumptions so that the demonstrator’s design basis becomes explicit, traceable, and consistent with the project boundary.

These controlled assumptions will cover:

- power / voltage / current basis
- DC input / DC bus / DC-link relationship
- representative machine-side boundary
- switching and control-frequency rationale
- sensing and feedback strategy
- demonstrator-level protection rationale
- cooling and thermal-integration rationale
- EMI-aware design considerations
- control-architecture and interface-boundary clarification

The role of these assumptions is to support engineering judgement and subsequent hardware-platform interpretation. They are working assumptions for Phase 2 reasoning, not final design or validation claims.

---

## 5. Deferred Topics

The following topics are intentionally deferred beyond the current Phase 2 design-basis entry state:

- detailed operating-boundary tables
- quantitative power / voltage / current assumptions
- representative machine-side boundary development
- control-architecture and interface-boundary documentation
- selected hardware-platform evidence and build-ownership traceability
- bring-up and debug evidence
- representative measured waveform evidence
- validation-scope interpretation
- PC-side runtime observability evidence
- MATLAB-based analysis and tuning-support evidence

These topics are introduced progressively as substantive engineering content becomes available during later Phase 2 work and subsequent Phase 3 work.