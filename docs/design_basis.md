# Design Basis

> **Status (Phase 2 – Design-Basis Baseline in Progress):**  
> This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator of the 30 kW-class, water-cooled PMSM drive/converter platform.  
> Its current scope covers design-basis role definition, design-input framing, an initial operating-boundary draft, controlled-assumption structure, and deferred-topic framing.  
> Detailed quantitative assumptions, control-architecture and interface-boundary definition, selected hardware-platform evidence, and build-ownership traceability are introduced progressively through subsequent Phase 2 work.

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

At the current design-basis draft state, this document does not establish hardware-platform evidence, operational validation, full dual-side hardware closure, or product-level claims.

---

## 2. Design Inputs

The design basis is organised around a **machine-side converter demonstrator** that serves as the physical core of the project.

This demonstrator is positioned within a **broader back-to-back system context**, which is retained to define system role, interface boundary, and the interpretation of later validation artefacts.

Within the present validation arrangement, the upstream side is represented at the **DC bus interface** by an **external DC source** rather than by a physically implemented source-side / grid-side stage.

The Phase 2 design-input framing is summarised below.

| Design input | Phase 2 design-basis reading | Engineering role |
| --- | --- | --- |
| Platform class | 30 kW-class water-cooled PMSM drive/converter platform | Defines the demonstrator scale and design-basis context |
| Physical mainline | Machine-side converter demonstrator | Provides the repository’s physical core and later evidence anchor |
| Broader system context | Broader back-to-back system context retained | Defines system role, interface boundary, and validation interpretation |
| Source-side / grid-side function | System-context role retained to explain the upstream side of the DC bus interface | Keeps the upstream system role visible without turning it into a physical implementation branch |
| Upstream representation | External DC source at the DC bus interface | Represents the upstream side in the present validation arrangement |
| DC-side interface | DC input / DC bus interface between the upstream representation and the machine-side converter, with DC-link energy buffering | Provides the reference point for later DC input voltage range, DC-link capacitance and voltage-rating rationale, DC-link voltage sensing, controlled energisation, and protection strategy |
| Current-level framing | Current-level basis framed around the demonstrator power class, DC-link / machine-side voltage context, and representative PMSM interface context | Prepares later device, sensor, connector, protection, and thermal reasoning |
| Cooling approach | Water-cooled platform approach at demonstrator level | Supports the 30 kW-class hardware-platform reading and later thermal-integration evidence |
| Machine-side object | Representative PMSM | Defines the machine-side conversion and later validation object |
| Shaft-side context | Downstream operating context retained for the representative PMSM | Supports later interpretation of machine-side current, speed, and load-related behaviour |
| Machine-side validation focus | Representative machine-side validation context centred on the machine-side converter demonstrator and representative PMSM | Provides the interpretation frame for later bring-up, measured behaviour, observability, and analysis evidence |

These inputs establish the repository-facing design-basis frame for the machine-side converter demonstrator. At design-input level, they do not define final numerical operating limits, detailed component ratings, or validation results.

They also support the Phase 2 evidence route: design-basis reasoning is developed first, while selected static hardware-platform evidence and build-ownership traceability are introduced later only when they can be traced back to this design-basis frame.

---

## 3. Operating Boundary

At the present repository stage, the operating boundary is defined at **design-basis draft level**. Its role is to consolidate the main engineering boundaries for the machine-side converter demonstrator before detailed controlled assumptions, hardware-platform evidence, and later validation artefacts are introduced.

The boundary areas below are derived from the design-input framing in Section 2 and the Phase 2 design-basis scope, but they are restated here from the perspective of operating scope and claim boundary.

| Boundary area | Phase 2 operating-boundary reading | Not established by this boundary |
| --- | --- | --- |
| Demonstrator scale | The platform is read as a 30 kW-class, water-cooled demonstrator-level PMSM drive/converter platform | Product-certified rating, complete performance envelope, or deployment-ready hardware |
| Physical focus within system context | The operating interpretation remains centred on the machine-side converter demonstrator, while the broader back-to-back system context is retained for system role, interface boundary, and validation interpretation | Full dual-side back-to-back hardware closure or a parallel physical mainline |
| Upstream and DC-side condition | The source-side / grid-side function is retained at system-context level, while the present upstream condition is represented by an external DC source at the DC bus interface. The DC input / DC bus interface connects this upstream representation to the machine-side converter, with the DC-link providing converter-side energy buffering | Source-side / grid-side hardware implementation or validation, dedicated pre-charge circuit, final DC-link component values, or validated DC-link operating behaviour |
| Current and thermal framing | Current-level basis is framed around the demonstrator power class, DC-link / machine-side voltage context, and representative PMSM interface context, while water cooling is treated as a demonstrator-level platform approach | Final current rating, overload envelope, validated operating range, full thermal qualification, or product cooling validation |
| Machine-side object and shaft-side context | The representative PMSM defines the immediate machine-side operating object, while the shaft-side context is retained as the downstream operating context for interpreting later machine-side evidence | Universal PMSM compatibility, final load-machine arrangement, mechanical-load validation package, or load-side test-bench validation |
| Control-interface scope | Controller-to-power-stage command path, sensing / feedback paths, and protection-related interfaces are treated at architecture-boundary level during Phase 2 | Detailed control implementation, released firmware package, controller validation, or commissioning closure |
| Validation interpretation | Later evidence is intended to remain representative and machine-side focused | Validation results, product qualification, full operating-envelope validation, or full dual-side system validation |

This operating-boundary draft is intended to support later Phase 2 controlled assumptions and hardware-platform traceability. It should be read as a demonstrator-level engineering boundary for the machine-side converter platform, not as a product specification, compliance statement, or complete validation envelope.

---

## 4. Controlled Assumptions

Phase 2 will progressively introduce controlled assumptions and supporting rationale so that the demonstrator’s design basis becomes explicit, traceable, and consistent with the project boundary.

These controlled assumptions and supporting rationale will cover:

- power / voltage / current basis
- DC input / DC bus / DC-link relationship
- representative machine-side boundary
- switching and control-frequency rationale
- sensing and feedback strategy
- demonstrator-level protection rationale
- cooling and thermal-integration rationale
- EMI-aware design considerations
- control-architecture and interface-boundary clarification

The role of these assumptions and rationale is to support engineering judgement and subsequent hardware-platform interpretation. They are working assumptions for Phase 2 reasoning, not final design or validation claims.

---

## 5. Deferred Topics

The following topics are intentionally deferred beyond the current Phase 2 design-basis draft state:

- detailed quantitative power / voltage / current assumptions
- DC-side voltage, DC-link energy buffering, controlled energisation, and protection rationale
- representative machine-side operating assumptions
- switching and control-frequency rationale
- sensing, feedback, protection, cooling / thermal-integration, and EMI-aware design rationale
- control-architecture and interface-boundary documentation
- selected hardware-platform evidence and build-ownership traceability
- bring-up and debug evidence
- representative measured waveform evidence
- validation-scope interpretation
- PC-side runtime observability evidence
- MATLAB-based analysis and tuning-support evidence

These topics are introduced progressively as substantive engineering content becomes available during later Phase 2 work and subsequent Phase 3 work.