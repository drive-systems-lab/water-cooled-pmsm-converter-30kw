# Design Basis

> **Status (Phase 2 – Design-Basis Baseline in Progress):**  
> This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator of the 30 kW-class, water-cooled PMSM drive/converter platform.  
> Its current scope covers design-basis role definition, design-input framing, an operating-boundary draft, initial power / voltage / current controlled assumptions, representative machine-side boundary definition, DC-side voltage-reference reasoning, current-level clarification, converter output current-capacity framing, switching / control-frequency rationale, sensing / protection / cooling / EMI-aware rationale, and deferred-topic framing.  
> Additional quantitative detail where appropriate, control-architecture and interface-boundary definition, selected hardware-platform evidence, and build-ownership traceability are introduced progressively through subsequent Phase 2 work.

---

## 1. Purpose and Scope

This document establishes the Phase 2 design-basis baseline for the machine-side converter demonstrator.

Its purpose is to define the engineering basis that later Phase 2 hardware-platform evidence, build-ownership traceability, and subsequent Phase 3 bring-up and representative validation work should build on.

At this stage, the document is intended to:

- define the role of the design-basis layer within the repository
- frame the initial design inputs for the machine-side converter demonstrator
- frame the operating-boundary categories at design-basis level
- establish initial controlled assumptions and supporting rationale at design-basis level across power / voltage / current, DC-side interpretation, switching / control timing, and sensing / protection / cooling / EMI-aware design
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
| Representative machine-side boundary | Representative PMSM-side operating boundary covering a 30 kW continuous power reference, a 40 kW short-duration overload power reference within an up-to-60 s design window, and a representative high-speed point around 4000 rpm at which the PMSM-side voltage / back-EMF demand is approximately 510 V line-line RMS | Provides the representative PMSM-side operating context for subsequent DC-side voltage-reference and current-level reasoning |
| Converter output current capacity | 100 A-class current-capacity target for the machine-side converter output, specified as a platform-level design input | Sets the implementation-facing current-capacity basis for later current-path, sensing, protection, cooling, wiring, terminal interface, and hardware-platform reasoning |
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
| Upstream and DC-side condition | The source-side / grid-side function is retained at system-context level, while the present upstream condition is represented by an external DC source at the DC bus interface. The DC input / DC bus interface connects this upstream representation to the machine-side converter, with the DC-link providing converter-side energy buffering | Source-side / grid-side hardware implementation or validation, dedicated pre-charge circuit, final DC-link component values, full DC-side operating range, or validated DC-link operating behaviour |
| Current and thermal framing | Current-related design-basis reasoning is framed by the representative machine-side boundary and the 100 A-class converter output current-capacity target, while water cooling is treated as a demonstrator-level platform approach | Final current rating, PMSM rated current, DC-side input current, validated current or overload capability, complete operating-envelope validation, full thermal qualification, product cooling validation, or a simultaneous 900 V / 100 A operating point |
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
| Platform-level design target | A platform-level target specified within the design basis to guide implementation-facing design reasoning | Does not establish final component values, product-level specifications, validated performance capability, or hardware-platform evidence closure |
| Deferred detailed closure | Detailed component values, final ratings, validation results, or operating-envelope closure intentionally left for later Phase 2 or Phase 3 work | Not established by the current design-basis draft; later closure requires appropriate supporting rationale, hardware-platform evidence, or validation artefacts |

### 4.2 Power / Voltage / Current Basis

| Design-basis item | Controlled assumption | Engineering role | Boundary |
| --- | --- | --- | --- |
| Power boundary | The representative PMSM-side operating basis is translated into a 30 kW continuous converter-platform power reference, with a 40 kW short-duration overload power reference within an up-to-60 s design window | Defines the continuous and short-duration power boundaries used to interpret the machine-side operating context and to support later protection, cooling, power-limiting, and hardware-platform reasoning | Does not establish a product-certified continuous power rating or a validated overload capability |
| DC-side voltage basis | The voltage basis at the DC input / DC bus interface is defined around a 900 V nominal design-basis reference for the DC bus, with the upstream side represented by an external DC source in the present validation arrangement | Provides the nominal voltage reference for the DC input / DC bus interface, supporting subsequent DC-link and power-stage voltage class reasoning, DC bus voltage sensing and voltage protection rationale, insulation / spacing awareness, voltage-related EMI / dv/dt-aware design considerations, and later hardware-platform interpretation | Does not establish a product operating envelope, certified voltage rating, test-validated DC-side performance claim, physically implemented source-side / grid-side stage, or fully validated DC-side operating range |
| DC-link interpretation | The DC-link is treated as the converter-side energy-buffering layer between the external DC source representation and the machine-side inverter stage | Clarifies how the DC input / DC bus interface is read within the present demonstrator | Does not establish final DC-link component values or validated DC-link operating behaviour |
| Machine-side voltage basis | The machine-side voltage basis is interpreted through a representative PMSM high-speed boundary centred around 4000 rpm and approximately 510 V line-line RMS voltage / back-EMF demand | Supports representative high-speed current estimation and prepares the PMSM-side voltage-headroom basis for later DC-side voltage-reference reasoning | Does not claim a PMSM product voltage rating, universal PMSM compatibility, or complete operating-envelope coverage |
| Current-level basis | Current-level reasoning is organised around two distinct current references: a 50 A-class representative high-speed PMSM-side operating-current estimate under the representative machine-side boundary, and a 100 A-class converter output current-capacity target specified as a platform-level design input | Provides the current-level basis for representative PMSM-side operating-current interpretation and implementation-facing converter output reasoning, including later current-path, sensing, protection, cooling, wiring, terminal-interface, hardware-platform, and validation interpretation | Does not establish PMSM rated current, DC-side input current, validated current capability, product-certified current rating, complete operating-envelope validation, or a simultaneous 900 V / 100 A operating point |

### 4.3 DC Input / DC Bus / DC-Link Relationship and DC-Side Voltage Reference

Within the present validation arrangement, the upstream side is represented by an external DC source at the DC bus interface. The DC input / DC bus interface should therefore be read as the DC-side reference point between the upstream representation and the physically realised machine-side converter demonstrator.

The DC-link is interpreted as the converter-side energy-buffering layer associated with the machine-side inverter stage. This interpretation supports the Phase 2 design-basis reading of the machine-side converter without implying that the source-side / grid-side stage has been physically implemented or validated.

The representative machine-side voltage / back-EMF demand introduced above is approximately 510 V line-line RMS at the representative high-speed point. At design-basis level, the DC-side voltage reference is selected so that this demand uses about 80% of the available line-line RMS fundamental voltage under the linear SVPWM voltage limit, rather than being placed at the modulation boundary.

This gives an available voltage target of approximately 510 / 0.80 ≈ 638 V line-line RMS. For a two-level machine-side inverter stage under linear SVPWM, the available maximum fundamental voltage is approximately Vdc / √2 line-line RMS. This corresponds to a DC-side reference of approximately √2 × 638 ≈ 900 V.

Accordingly, the DC-side voltage basis is defined around a 900 V nominal design-basis reference for the DC bus. For the present machine-side demonstrator, this value is treated as the intended nominal DC bus interface condition represented by the external DC source, rather than as a closed upstream voltage-generation result.

This reference is retained for DC-link interpretation, later DC bus voltage sensing and voltage protection rationale, voltage class and insulation / spacing awareness, voltage-related EMI / dv/dt-aware design considerations, and later hardware-platform interpretation.

This value is not presented as a product operating envelope, a certified voltage rating, a test-validated DC-side performance claim, a universal upstream compatibility claim, or a fully validated DC-side operating range.

### 4.4 Current-Level Basis

The current-level basis is framed at demonstrator level in this document.

It covers two distinct current references:

- a 50 A-class representative high-speed PMSM-side operating-current estimate under the representative machine-side boundary
- a 100 A-class converter output current-capacity target specified as a platform-level design input

The representative high-speed operating-current estimate is treated as a class-level current-scaling check, not as a defined rated operating point of the representative PMSM.

At the representative high-speed boundary, the PMSM-side voltage / back-EMF demand is approximately 510 V line-line RMS. If the 30 kW continuous and 40 kW short-duration power references are interpreted against this voltage level as a class-level current-scaling check, the three-phase relationship $I \approx P / (\sqrt{3} V_{LL})$ gives approximately 34 A and 45 A, respectively, before power-factor effects and implementation-related factors are considered. This supports a 50 A-class representative high-speed operating-current estimate.

This estimate should therefore be read as a representative PMSM-side high-speed current scale. It does not establish that the representative PMSM is rated for 30 kW or 40 kW at 4000 rpm, and it does not define the converter output current-capacity target.

The converter output current-capacity target is defined separately at platform level. The machine-side converter output is therefore specified with a 100 A-class current-capacity target as a platform-level design input.

This target prevents the converter output current-capacity basis from being tied only to one representative high-speed PMSM operating point, and supports later implementation-facing reasoning around the converter output current path, sensing, protection, cooling, wiring, terminal interface, and hardware-platform evidence.

At this Phase 2 stage, these values should be read as design-basis references rather than validated operating results. The 50 A-class estimate does not establish a PMSM rated current or converter current-capacity limit, and the 100 A-class target does not establish a DC-side input current, validated current capability, product-certified current rating, or a single simultaneous 900 V / 100 A operating point.

### 4.5 Switching and Control-Frequency Basis

The switching and control-frequency basis is introduced at design-basis level to define the representative timing layer for the machine-side converter demonstrator.

A 6–8 kHz switching-frequency range is retained as an experience-informed design-basis reference for the machine-side converter demonstrator, considering the already defined 30 kW / 40 kW power boundary, 900 V nominal DC-side reference, and 100 A-class converter-output current-capacity target. These references define the design envelope for switching-rationale purposes rather than a single simultaneous operating point. Within this range, 8 kHz is used as the representative switching and current-control baseline for Phase 2 reasoning.

This range is selected to balance current-control quality, current ripple, switching loss, EMI / dv/dt pressure, power-device stress, thermal design, and controller timing. It should be read as a design-basis reference rather than as a final quantitative switching-frequency closure. Such closure would require motor inductance and current-ripple targets, power-device switching-energy data, gate-drive behaviour, DC-link characteristics and layout parasitics, thermal-path evidence, controller execution margin, and EMI / dv/dt observations.

The 8 kHz representative baseline gives a 125 µs PWM period. At design-basis level, this provides a practical timing basis for current-control update and PWM-synchronised current-feedback sampling.

The switching and control-frequency basis also supports later sensing, protection, cooling, EMI-aware design, control-interface, and hardware-platform reasoning. For example, the switching baseline affects current-feedback timing, gate-drive behaviour, layout awareness, EMI / dv/dt interpretation, power-device switching-loss considerations, and thermal-design interpretation.

At this stage, these timing references do not establish final dead-time, final ADC trigger placement, final current-loop bandwidth, final switching-loss calculation, EMI validation, thermal validation, or firmware scheduling closure. Final switching-frequency closure remains tied to later power-device, gate-drive, DC-link, layout, thermal, controller timing, and hardware-platform evidence.

### 4.6 Sensing, Protection, Cooling, and EMI-Aware Rationale

The sensing, protection, cooling, and EMI-aware design rationale is introduced here at design-basis level.

This section translates the previously defined power, voltage, current, and switching references into implementation-facing design considerations for the machine-side converter demonstrator. It forms the design-to-implementation bridge between the design-basis references defined in this document and the selected hardware-platform evidence to be introduced later in Phase 2. It does not establish final component qualification, final protection thresholds, full thermal validation, certified EMC performance, selected hardware-platform evidence, or build-ownership traceability.

| Rationale area | Design-basis reading | Basis used | Deferred closure |
| --- | --- | --- | --- |
| Phase-current sensing | Machine-side phase-current sensing is treated as the primary current-feedback basis for converter output current supervision and later representative machine-side validation | 100 A-class converter output current-capacity target; 50 A-class representative high-speed PMSM-side operating-current estimate; 8 kHz representative current-control baseline | Final sensor qualification, calibration evidence, bandwidth verification, accuracy closure, and complete ADC-channel mapping |
| DC-bus voltage sensing | DC-bus voltage sensing is treated as a local converter-side DC-link measurement basis used for voltage monitoring, startup supervision, and software-level overvoltage / undervoltage protection | 900 V nominal DC-side design-basis reference; DC input / DC bus / DC-link relationship; local converter-side DC-link measurement basis | Final voltage-scaling disclosure, exact thresholds, hardware overvoltage-trip claim, or upstream source-side validation |
| Protection — operating-envelope supervision | Software-supervised protection is organised around measured phase-current supervision, local DC-link voltage supervision, temperature-related supervision, enable / interlock checks, and plausibility checks | Phase-current sensing basis; local DC-link voltage-sensing basis; thermal-supervision basis; 100 A-class current-capacity target; 900 V nominal DC-side reference; 30 kW / 40 kW power boundary | Final warning / inhibit / trip thresholds, protection-response timing, validated software-commanded shutdown implementation, or product-level protection validation |
| Protection — driver-level hard-fault handling | Severe gate-driver fault indications are treated as a driver-level hard-fault path that can force inverter PWM outputs into a defined safe state | Driver-level FAULT / DESAT path; PWM trip-safe-state principle; gate-drive / power-stage interface boundary | Exact trip configuration, measured shutdown timing, fault-source mapping, short-circuit qualification, or certified functional-safety closure |
| Thermal monitoring and cooling | Thermal supervision and water cooling are treated as part of the demonstrator-level thermal design basis for the 30 kW-class platform and short-duration overload context | 30 kW continuous power reference; 40 kW short-duration overload reference; 100 A-class current-capacity target; IGBT-module internal NTC feedback; motor-side temperature-interface basis; water-cooled platform approach | Final coolant flow, thermal-resistance calculation, thermal-rise validation, direct junction-temperature measurement claim, or product cooling qualification |
| EMI-aware integration | EMI-aware design is treated as layout, wiring, grounding, shielding, isolation, gate-drive, and interface-awareness reasoning for a high-voltage, high-current switching converter | 900 V nominal DC-side reference; 100 A-class current-capacity target; 6–8 kHz switching-frequency range; local DC-link support; gate-drive proximity; isolated sensing / communication paths; shield-ground and chassis-awareness basis | Certified EMC result, final EMI filter design, measured loop inductance, formal grounding / shielding verification, or compliance-level testing |

#### 4.6.1 Phase-Current Sensing Strategy

The current-sensing basis is centred on the machine-side converter output phase currents.

At design-basis level, the current-feedback basis is defined around three machine-side phase-current sensing channels. These channels are interpreted as converter output phase-current measurements, while DC-link current measurement remains outside the current sensing basis defined in this document.

The phase-current sensing capacity is interpreted against the 100 A-class converter output current-capacity target, rather than only against the 50 A-class representative high-speed PMSM-side operating-current estimate. This preserves the distinction between a representative operating-current estimate and the implementation-facing current-capacity envelope.

The sensing chain is treated as a bidirectional analogue Hall-effect phase-current measurement path suitable for machine-side current feedback, current supervision, controller observability, and later representative validation interpretation. ADC range, zero-current offset, filtering, calibration consistency, and current-to-voltage gain confirmation remain part of later control-interface, hardware-platform, and bring-up work.

This sensing rationale defines the current-feedback basis for the demonstrator, without establishing product-level metrology qualification, certified isolation performance, final sensor calibration, or validated 100 A operation.

#### 4.6.2 DC-Bus Voltage Sensing Strategy

The DC-bus voltage sensing basis is centred on the local converter-side DC-link voltage.

At design-basis level, the voltage-supervision basis is defined around local converter-side DC-link measurement and is interpreted relative to the 900 V nominal DC-side design-basis reference. This measurement basis supports startup supervision, DC-bus voltage monitoring, overvoltage / undervoltage supervision, PWM-enable condition checking, and later DC-link evidence interpretation.

The voltage-sensing path is treated as a distributed high-voltage resistor-divider followed by local serial ADC conversion and digitally isolated signal transfer to the DSP-side control domain. Within the present demonstrator boundary, this path provides converter-side voltage monitoring and software-supervised voltage protection context, while the complete upstream source-side / grid-side stage remains outside the present physical validation scope.

Exact divider values, software scaling coefficients, ADC count mapping, overvoltage / undervoltage thresholds, and PCB-level implementation details remain outside the public design-basis scope unless they are later deliberately introduced with supporting evidence.

This voltage-sensing rationale defines the DC-link voltage-supervision basis for the demonstrator, without establishing a hardware overvoltage trip path, product-level voltage protection qualification, certified isolation performance, or full DC-side operating-range validation.

#### 4.6.3 Demonstrator-Level Protection Strategy

The protection basis is centred on demonstrator-level fault handling, operating-envelope supervision, and PWM-enable conditions for the machine-side converter.

At design-basis level, it defines how severe driver faults, measured-current / voltage / temperature supervision, and enable-condition checks support controlled operation and safe-state reasoning. It is not presented as certified product-level functional safety.

The protection basis is organised around three layers.

First, driver-level hard-fault handling supports rapid shutdown under severe switching-device fault conditions. Driver DESAT / FAULT-type indications are treated as severe gate-driver-level hard-fault signals that can trigger a PWM trip path and force inverter PWM outputs into a defined safe state.

Second, software-supervised operating-envelope protection monitors phase current, DC-bus voltage, and temperature-related conditions. This layer supports current limiting, overcurrent handling, DC-bus overvoltage / undervoltage supervision, startup / precharge readiness checks, and overtemperature supervision.

Third, enable interlocks and plausibility checks are used to prevent PWM enable when essential measurement, feedback, communication, or external-enable conditions are not valid.

Severe protective faults should be treated as latched events requiring manual acknowledgement and controlled reinitialisation before re-enable. Conditions such as startup-not-ready, precharge-incomplete, sensor-offset-pending, or warning-level states may inhibit PWM enable or raise a warning without being classified as severe latched faults. Their final latch, reset, and recovery behaviour remains part of later control-interface and bring-up definition.

Exact trip thresholds, response timing, trip configuration, reset sequence, and measured shutdown performance remain deferred. This section does not claim certified functional safety, complete short-circuit qualification, or product-level protection-chain validation.

#### 4.6.4 Thermal Monitoring and Cooling Rationale

The thermal and cooling basis is centred on power-module temperature supervision and the power-stage heat-removal path for the water-cooled machine-side converter demonstrator.

At design-basis level, converter-side thermal supervision is organised around IGBT-module internal NTC feedback. This feedback is treated as power-module temperature feedback routed into the converter-side thermal-supervision path, rather than as direct semiconductor junction-temperature measurement. Motor-side temperature input is retained as a machine-side thermal-monitoring interface provision, while its use in later PMSM bring-up remains dependent on the selected machine setup and available interface evidence.

Temperature handling should be organised at design-basis level into warning, inhibit, and trip concepts. Warning-level conditions support observability and early thermal awareness. Inhibit-level conditions prevent startup when thermal conditions are outside the allowed range. Trip-level conditions disable PWM during operation and should be latched if the fault is severe.

The cooling rationale is centred on the power-stage heat-removal path. The power-stage thermal path is defined around IGBT module baseplates thermally coupled to an integrated water-cooled cold-plate / enclosure-base structure. The intended heat-flow path is from the module baseplates, through the thermal interface and cold-plate body, into the coolant loop.

This supports the 30 kW-class / short-duration overload design-basis rationale and explains why water cooling is part of the demonstrator-level platform basis.

The boundary remains demonstrator-level. This section does not claim that all converter components are directly water-cooled, nor does it establish coolant flow rate, coolant temperature, thermal resistance, thermal-rise validation, direct junction-temperature measurement, or product-level thermal qualification.

#### 4.6.5 EMI-Aware Layout and Integration Considerations

The EMI-aware layout and integration basis is introduced at design-basis level because the demonstrator combines a 900 V nominal DC-side reference, a 100 A-class converter output current-capacity target, and a 6–8 kHz switching-frequency design-basis range.

At this stage, EMI-aware reasoning is based on layout and integration awareness rather than formal EMC testing or compliance evidence. The relevant considerations include separation between high-voltage power interfaces and low-voltage signal interfaces, compact DC-link and power-stage current-path organisation, local gate-drive placement close to the power stage, isolated sensing and communication paths, shield-ground provisions for selected feedback and communication interfaces, and chassis / enclosure-level grounding awareness.

The design-to-implementation route should therefore be organised around a structured control-drive-power arrangement rather than an unpartitioned mixed layout. Later hardware-platform evidence should be prepared to show power/control separation, DC-link support, gate-drive proximity, signal-interface isolation, shield-aware interface provision, grounding awareness, and wiring organisation where these features can be clearly evidenced.

This rationale remains at design-basis level. It does not establish measured EMI performance, certified EMC compliance, fully verified grounding design, final filter design, measured loop inductance, exact shield-termination strategy, or formal product-level isolation verification.

### 4.7 Fixed, Representative, Platform-Level, and Deferred Items

| Category | Items | Treatment |
| --- | --- | --- |
| Fixed | Machine-side physical mainline; broader back-to-back system context; external DC source representation; 30 kW-class water-cooled demonstrator reading | Retained as project-level and design-basis anchors |
| Representative | Representative machine-side boundary, including the 30 kW / 40 kW power references, representative high-speed point, and PMSM-side voltage / back-EMF demand; 50 A-class representative high-speed PMSM-side operating-current estimate; 900 V nominal DC-side voltage basis; 6–8 kHz switching-frequency design-basis range; 8 kHz representative switching / current-control baseline, with its derived 125 µs PWM period and PWM-synchronised current-feedback sampling assumption; representative PMSM interface | Used as representative engineering references for Phase 2 design-basis reasoning and later evidence interpretation |
| Platform-level | 100 A-class converter output current-capacity target | Used as an implementation-facing platform-level target for later current-path, sensing, protection, cooling, wiring, terminal interface, and hardware-platform reasoning; not treated as a PMSM rated current, DC-side input current, product-certified current rating, validated current capability, or simultaneous 900 V / 100 A operating point |
| Deferred | Final component values and implementation parameters; detailed machine-side operating assumptions beyond the representative boundary defined in this document; final current rating, validated current / overload capability, and complete operating-envelope closure; final sensor calibration / qualification and voltage-sensing scaling disclosure; exact protection thresholds, PWM trip configuration, reset / recovery behaviour, and measured shutdown timing; final cooling, thermal, EMI / EMC, grounding / shielding, and switching-frequency closure; control-architecture and interface-boundary definition; selected hardware-platform evidence, build-ownership traceability, bring-up, and measured validation evidence | Deferred to later Phase 2 or subsequent project work, depending on whether the item requires control-interface definition, hardware-platform evidence, or operational validation artefacts |

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
| Representative high-speed operating-current estimate | 50 A-class | Provides a representative PMSM-side operating-current reference for current-level reasoning and later validation interpretation | Not a PMSM rated current, converter output current-capacity target, validated overload current, or validated operating range |

The 30 kW continuous power reference and 40 kW short-duration overload reference are retained as machine-side power-boundary references. They are not introduced as motor nameplate ratings, product-certified ratings, or validated operating results.

The approximately 510 V line-line RMS PMSM-side voltage / back-EMF demand is retained as a representative high-speed voltage boundary. It defines the machine-side voltage-headroom requirement that later DC-side voltage-reference reasoning must accommodate.

The 50 A-class representative high-speed operating-current estimate should be read as a class-level PMSM-side operating estimate under this representative high-speed boundary. It supports current-level reasoning and later validation interpretation, but it should not be read as a converter output current-capacity target or a validated current limit.

The shaft-side context remains a downstream operating boundary for interpreting machine-side behaviour. It does not establish a load-side validation package, final mechanical-load arrangement, or complete shaft-side test-bench validation.

---

## 6. Deferred Topics

The following topics remain intentionally deferred beyond the current design-basis-level rationale presented in this document:

- final component-level ratings, detailed component values, and implementation parameters, including device, sensor, connector, and protection-path closure
- final DC-link component values, full DC-side operating range, and validated DC-link operating behaviour
- final current rating, validated current or overload capability, and complete operating-envelope closure
- detailed machine-side operating assumptions beyond the representative boundary defined in this document
- final switching-frequency closure, final dead-time, final ADC trigger placement, final current-loop bandwidth, final switching-loss calculation, and firmware scheduling closure
- final sensing-chain closure, including current-sensor range, calibration, bandwidth / accuracy verification, voltage-sensing scaling disclosure, exact voltage thresholds, and complete ADC / interface mapping
- exact protection thresholds, PWM trip configuration, reset / recovery behaviour, and measured shutdown timing
- final cooling / thermal closure, including coolant flow, coolant temperature, thermal resistance, thermal-rise behaviour, junction-temperature estimation methodology, and full thermal validation
- final EMI / EMC and grounding / shielding closure, including final filter design, measured loop inductance, exact shield-termination strategy, formal grounding / shielding verification, and compliance-level testing
- control-architecture and interface-boundary definition
- selected hardware-platform evidence and build-ownership traceability
- bring-up and debug evidence
- representative measured waveform evidence
- validation-scope interpretation
- PC-side runtime observability evidence
- MATLAB-based analysis and tuning-support evidence

These topics are introduced, refined, or kept explicitly deferred as relevant control-interface definitions, hardware-platform evidence, implementation-level details, or operational validation artefacts become available during later Phase 2 work and subsequent project phases.