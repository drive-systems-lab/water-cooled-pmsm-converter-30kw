# Design Basis

> **Status (Phase 2 – Design-Basis Baseline in Progress):**  
> This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator of the 30 kW-class, water-cooled PMSM drive/converter platform.  
> Its current scope covers design-basis role definition, design-input framing, an operating-boundary draft, initial power / voltage / current controlled assumptions, representative machine-side boundary definition, and deferred-topic framing.  
> Further quantitative detail where appropriate, supporting design-basis rationale, control-architecture and interface-boundary definition, selected hardware-platform evidence, and build-ownership traceability are introduced progressively through subsequent Phase 2 work.

---

## 1. Purpose and Scope

This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator.

Its purpose is to define the engineering basis that later Phase 2 hardware-platform evidence, build-ownership traceability, and subsequent Phase 3 bring-up and representative validation work should build on.

At this stage, the document is intended to:

- define the role of the design-basis layer within the repository
- frame the initial design inputs for the machine-side converter demonstrator
- frame the operating-boundary categories at design-basis level
- establish initial controlled assumptions for power / voltage / current and DC-side interpretation at design-basis level
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
| Platform class | 30 kW-class water-cooled PMSM drive/converter platform | Retains the demonstrator scale established by the Phase 1 project-positioning baseline; Phase 2 explains the representative machine-side operating basis behind this platform class |
| Physical mainline | Machine-side converter demonstrator | Provides the repository’s physical core and later evidence anchor |
| Broader system context | Broader back-to-back system context retained | Defines system role, interface boundary, and validation interpretation |
| Source-side / grid-side function | System-context role retained to explain the upstream side of the DC bus interface | Keeps the upstream system role visible without turning it into a physical implementation branch |
| Upstream representation | External DC source at the DC bus interface | Represents the upstream side in the present validation arrangement |
| DC-side interface | DC input / DC bus interface between the upstream representation and the machine-side converter, with DC-link energy buffering | Provides the reference point for later DC input voltage range, DC-link capacitance and voltage-rating rationale, DC-link voltage sensing, controlled energisation, and protection strategy |
| Machine-side object | Representative PMSM | Defines the machine-side conversion and later validation object |
| Machine-side power-boundary input | Representative PMSM-side operating basis expressed as a 30 kW continuous converter-platform power reference, with a 40 kW short-duration overload power reference within an up-to-60 s design window | Defines the continuous and short-duration power boundaries used to interpret the representative PMSM-side operating context and to support later protection, cooling, power-limiting, and hardware-platform reasoning |
| Current-level framing | Current-level basis framed around the machine-side power-boundary input, the DC bus and machine-side voltage relationship, and the representative PMSM interface | Prepares later device, sensor, connector, protection, thermal, and hardware-platform reasoning |
| Cooling approach | Water-cooled platform approach at demonstrator level | Supports the 30 kW-class hardware-platform reading and later thermal-integration evidence |
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
| Demonstrator scale and power boundary | The platform is read as a 30 kW-class, water-cooled demonstrator-level PMSM drive/converter platform. At design-basis level, this platform class is interpreted through a 30 kW continuous converter-platform power reference and a 40 kW short-duration overload power reference within an up-to-60 s design window | Product-certified rating, validated overload capability, complete performance envelope, or deployment-ready hardware |
| Physical focus within system context | The operating interpretation remains centred on the machine-side converter demonstrator, while the broader back-to-back system context is retained for system role, interface boundary, and validation interpretation | Full dual-side back-to-back hardware closure or a parallel physical mainline |
| Upstream and DC-side condition | The source-side / grid-side function is retained at system-context level, while the present upstream condition is represented by an external DC source at the DC bus interface. The DC input / DC bus interface connects this upstream representation to the machine-side converter, with the DC-link providing converter-side energy buffering | Source-side / grid-side hardware implementation or validation, dedicated pre-charge circuit, final DC-link component values, or validated DC-link operating behaviour |
| Current and thermal framing | Current-level basis is framed around the machine-side power-boundary input, the DC bus and machine-side voltage relationship, and the representative PMSM interface, while water cooling is treated as a demonstrator-level platform approach | Final current rating, validated overload capability, validated operating range, full thermal qualification, or product cooling validation |
| Machine-side object and shaft-side context | The representative PMSM defines the immediate machine-side operating object, while the shaft-side context is retained as the downstream operating context for interpreting later machine-side evidence | Universal PMSM compatibility, final load-machine arrangement, mechanical-load validation package, or load-side test-bench validation |
| Control-interface scope | Controller-to-power-stage command path, sensing / feedback paths, and protection-related interfaces are treated at architecture-boundary level during Phase 2 | Detailed control implementation, released firmware package, controller validation, or commissioning closure |
| Validation interpretation | Later evidence is intended to remain representative and machine-side focused | Validation results, product qualification, full operating-envelope validation, or full dual-side system validation |

This operating-boundary draft is intended to support later Phase 2 controlled assumptions and hardware-platform traceability. It should be read as a demonstrator-level engineering boundary for the machine-side converter platform, not as a product specification, compliance statement, or complete validation envelope.

---

## 4. Controlled Assumptions

The operating boundary in Section 3 is converted here into initial design-basis assumptions for Phase 2 reasoning.

These assumptions make the demonstrator’s power, voltage, current, and DC-side interpretation explicit enough to support subsequent Phase 2 design-basis reasoning and later hardware-platform interpretation. They should be read as demonstrator-level engineering assumptions rather than product specifications, certified ratings, or complete validation limits.

### 4.1 Assumption Categories

| Assumption category | Meaning in this document | Boundary |
| --- | --- | --- |
| Fixed project-level basis | The Phase 1 project-level reading is retained: a 30 kW-class, water-cooled machine-side converter demonstrator within a broader back-to-back system context, with the upstream side represented at the DC bus interface by an external DC source | Does not establish product qualification, deployment readiness, or full dual-side hardware closure |
| Representative design-basis reference | A representative value, range, or engineering reference condition used to support Phase 2 design-basis reasoning | Does not establish final component values, product-level specifications, or a fully validated operating range |
| Deferred detailed closure | Detailed component values, final ratings, validation results, or operating-envelope closure intentionally left for later Phase 2 or Phase 3 work | Not established by the current design-basis draft; later closure requires appropriate supporting rationale, hardware-platform evidence, or validation artefacts |

### 4.2 Power / Voltage / Current Basis

| Design-basis item | Controlled assumption | Engineering role | Boundary |
| --- | --- | --- | --- |
| Power boundary | The representative PMSM-side operating basis is translated into a 30 kW continuous converter-platform power reference, with a 40 kW short-duration overload power reference within an up-to-60 s design window | Defines the continuous and short-duration power boundaries used to interpret the machine-side operating context and to support later protection, cooling, power-limiting, and hardware-platform reasoning | Does not establish a product-certified continuous power rating or a validated overload capability |
| DC-side voltage basis | The DC-side voltage basis is framed at the DC input / DC bus interface, with the upstream side represented by an external DC source in the present validation arrangement | Provides the DC-side voltage reference for subsequent Phase 2 design-basis reasoning | Does not establish a physically implemented source-side / grid-side stage or a fully validated DC-side operating range |
| DC-link interpretation | The DC-link is treated as the converter-side energy-buffering layer between the external DC source representation and the machine-side inverter stage | Clarifies how the DC input / DC bus interface is read within the present demonstrator | Does not establish final DC-link component values or validated DC-link operating behaviour |
| Machine-side voltage basis | The machine-side voltage basis is interpreted through a representative PMSM high-speed boundary centred around 4000 rpm and approximately 510 V line-line RMS voltage / back-EMF demand | Supports representative high-speed current estimation and prepares the PMSM-side voltage-headroom basis for later DC-side voltage-reference reasoning | Does not claim a PMSM product voltage rating, universal PMSM compatibility, or complete operating-envelope coverage |
| Current-level basis | Current-level reasoning includes a 50 A-class representative high-speed operating-current estimate under the defined power boundary and the representative machine-side voltage / back-EMF demand at the high-speed operating point | Provides a representative PMSM-side operating-current reference for subsequent current-level reasoning, later hardware-platform interpretation, and representative validation | Does not establish PMSM rated current, converter current-capacity limit, overload capability, validated operating range, or product-level thermal validation |

### 4.3 DC Input / DC Bus / DC-Link Relationship

Within the present validation arrangement, the upstream side is represented by an external DC source at the DC bus interface. The DC input / DC bus interface should therefore be read as the DC-side reference point between the upstream representation and the physically realised machine-side converter demonstrator.

The DC-link is interpreted as the converter-side energy-buffering layer associated with the machine-side inverter stage. This interpretation supports the Phase 2 design-basis reading of the machine-side converter without implying that the source-side / grid-side stage has been physically implemented or validated.

### 4.4 Current-Level Basis

The current-level basis is framed at demonstrator level in this document.

It connects the machine-side power-boundary input, the representative PMSM-side voltage / back-EMF demand at the high-speed operating point, and subsequent converter design-basis reasoning, while preserving the distinction between an engineering reference condition and a final converter rating.

At the representative high-speed boundary, the 30 kW continuous converter-platform power reference and the 40 kW short-duration overload power reference remain within a tens-of-amps current reading when interpreted against the approximately 510 V line-line RMS PMSM-side voltage demand. This supports a 50 A-class representative high-speed operating-current estimate.

At this Phase 2 stage, the current-level basis should therefore be read as a controlled design-basis assumption. It does not establish a final current rating, converter current-capacity limit, validated overload capability, validated operating range, or product-level thermal limit.

### 4.5 Fixed, Representative, and Deferred Items

| Category | Items | Treatment |
| --- | --- | --- |
| Fixed | Machine-side physical mainline; broader back-to-back system context; external DC source representation; 30 kW-class water-cooled demonstrator reading | Retained as project-level and design-basis anchors |
| Representative | Machine-side power boundary; representative PMSM high-speed point; representative machine-side voltage / back-EMF demand; representative high-speed operating-current estimate; DC-side voltage basis; representative PMSM interface; current-level basis | Used as design-basis references for Phase 2 reasoning and later evidence interpretation |
| Deferred | Final component values; detailed machine-side operating assumptions beyond the representative boundary defined in this document; validated overload capability; full thermal validation; selected hardware-platform evidence and build-ownership traceability; bring-up and measured validation evidence | Deferred to later Phase 2 or Phase 3 work, depending on whether the item requires hardware-platform evidence or operational validation |

---

## 5. Representative Machine-Side Boundary

The representative machine-side boundary defines how the machine-side converter demonstrator is interpreted against a PMSM-side operating basis at design-basis level.

This boundary is not a motor product specification or a complete PMSM datasheet. It is used to connect the project-level 30 kW-class platform identity, the machine-side converter demonstrator, the representative PMSM interface, and later design-basis and validation interpretation.

| Representative boundary item | Phase 2 design-basis reading | Engineering role | Boundary |
| --- | --- | --- | --- |
| Continuous power reference | 30 kW continuous converter-platform power reference | Defines the continuous machine-side power context for later converter, cooling, protection, power-limiting, and hardware-platform reasoning | Not a product-certified continuous rating |
| Short-duration power reference | 40 kW short-duration overload power reference within an up-to-60 s design window | Provides a transient power-boundary margin above the 30 kW continuous reference | Not a validated overload capability or product-level maximum power claim |
| Representative high-speed point | Around 4000 rpm | Provides the high-speed PMSM-side reference point for voltage / back-EMF and current interpretation | Not a complete speed range or field-weakening validation target |
| PMSM-side voltage / back-EMF demand | Approximately 510 V line-line RMS at the representative high-speed point | Defines the PMSM-side voltage demand that later DC-side voltage-reference reasoning must accommodate | Not a PMSM rated voltage or universal PMSM compatibility claim |
| Representative high-speed operating-current estimate | 50 A-class | Provides a representative PMSM-side operating-current reference for subsequent current-level reasoning, later hardware-platform interpretation, and representative validation | Not PMSM rated current, converter current-capacity limit, validated overload current, or validated operating range |

The 30 kW continuous power reference and 40 kW short-duration overload reference are retained as machine-side power-boundary references. They are not introduced as motor nameplate ratings, product-certified ratings, or validated operating results.

The approximately 510 V line-line RMS PMSM-side voltage / back-EMF demand is retained as a representative high-speed voltage boundary. It defines the machine-side voltage-headroom requirement that later DC-side voltage-reference reasoning must accommodate.

The 50 A-class representative high-speed operating-current estimate should be read as a class-level operating estimate under this representative high-speed boundary. It supports subsequent current-level reasoning, later hardware-platform interpretation, and representative validation, but it should not be confused with the converter-output current-capacity design input, which is introduced separately in later Phase 2 work.

The shaft-side context remains a downstream operating boundary for interpreting machine-side behaviour. It does not establish a load-side validation package, final mechanical-load arrangement, or complete shaft-side test-bench validation.

---

## 6. Deferred Topics

The following topics are intentionally deferred beyond the current design-basis draft state:

- final component-level ratings and protection thresholds, including device, sensor, and connector-level closure
- final DC-link component values and validated DC-link operating behaviour
- validated current rating, validated overload capability, and complete operating-envelope closure
- detailed machine-side operating assumptions beyond the representative boundary defined in this document
- switching-frequency and control-frequency rationale
- sensing, feedback, protection, cooling / thermal-integration, and EMI-aware design rationale
- control-architecture and interface-boundary definition
- selected hardware-platform evidence and build-ownership traceability
- bring-up and debug evidence
- representative measured waveform evidence
- validation-scope interpretation
- PC-side runtime observability evidence
- MATLAB-based analysis and tuning-support evidence

These topics are introduced progressively as substantive engineering content becomes available during later Phase 2 work and subsequent Phase 3 work.