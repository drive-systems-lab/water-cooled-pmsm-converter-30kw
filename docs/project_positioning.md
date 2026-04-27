# Project Positioning

> **Status (Phase 1 – Positioning Baseline):**  
> This document defines the project-level positioning baseline for the 30 kW-class, water-cooled PMSM drive/converter platform.
> Its scope is limited to project identity, physical core, hardware basis and build ownership, broader system context, present validation arrangement, and demonstrator boundary.  
> Detailed design-basis reasoning, hardware-platform baselining, bring-up/debug evidence, and representative validation artefacts are deferred to subsequent phases.

---

## 1. Purpose and Positioning of This Document

This document establishes the authoritative positioning baseline for the project.

Its purpose is to establish a stable project-level reference for:

- how the project is positioned at engineering level
- what its physical core is
- how hardware basis and build ownership are framed at positioning level
- how broader system context is retained
- how the present validation arrangement should be interpreted
- what project boundary should be preserved as subsequent artefacts are introduced

This document does **not** provide detailed design reasoning, hardware evidence, executable validation claims, or release-facing performance conclusions.

---

## 2. Project Identity

The project is positioned as a **30 kW-class, water-cooled PMSM drive/converter platform** developed as an **engineering demonstrator**. Its physical core is a **machine-side converter demonstrator**, while broader back-to-back system context is retained to define system role, interface boundary, and validation meaning.

At repository level, the project is intended to grow as a **phase-driven engineering repository** rather than as a planning-only record, a simulation-only showcase, or a product-facing hardware release.

The present Phase-1 baseline therefore establishes project identity at **platform level**, while detailed subsystem baselines, evidence packages, and validation artefacts are intentionally deferred to later phases.

---

## 3. Physical Core

The physical core of the project is a **machine-side converter demonstrator**.

This demonstrator defines the project’s principal engineering mainline and serves as the primary anchor for later hardware, firmware, bring-up, debug, and validation artefacts.

Accordingly, it is the **only physical mainline** within the project baseline.

---

## 4. Hardware Basis and Build Ownership

The demonstrator presented in this repository is based on the author's own converter hardware platform, developed through an end-to-end design-and-build process.

At positioning level, build ownership is framed across both platform design and hands-on implementation.

On the design side, it covers mechanical and cooling design, power-stage design, control, gate-drive, and supporting interface electronics, together with PCB layout and EMI-aware integration considerations across the platform.

On the implementation side, it covers PCB assembly, soldering, mechanical assembly, wiring, board-level checks and debugging, and machine-side platform integration.

This section establishes the hardware basis and build-ownership framing at positioning level only. Detailed hardware-platform evidence, design-basis rationale, build records, bring-up/debug evidence, and representative validation artefacts are deferred to later phases.

---

## 5. Broader System Context

Although the physical core is a machine-side converter demonstrator, it is positioned within a **broader back-to-back system context**.

This broader context is retained to clarify:

- system role
- interface boundary
- how the present demonstrator should be understood in relation to the broader back-to-back system
- how later validation artefacts should be read in that same system context

Source-side or grid-side context is retained at **system-context level only** and is **not established as a parallel physical implementation line** within the project baseline.

Detailed system-context interpretation is established separately in [`system_context.md`](system_context.md).

---

## 6. Validation Arrangement

The project’s present validation arrangement is based on a **machine-side converter demonstrator** in which the upstream side is represented at the DC bus interface by an **external DC source**.

Within this arrangement, the external DC source should be read as an upstream representation for the present demonstrator rather than as a physically implemented source-side / grid-side stage.

This defines the present upstream condition for the demonstrator without changing the project's present physical mainline.

---

## 7. Demonstrator Boundary

The project should be read as an **engineering demonstrator** whose physical core is a **machine-side converter demonstrator** within a broader back-to-back system context.

Accordingly, it is not presented as:

- a full hardware implementation of the broader back-to-back system
- a product-qualified or deployment-ready hardware platform

Later bring-up, debug, and validation artefacts belong to subsequent project phases and are not established by this document.

---

## 8. Relevance and Engineering Context

At engineering level, the demonstrator is relevant to **PMSM drive development** in which a **machine-side converter demonstrator** provides the primary physical reference for power-conversion, control-integration, and validation-oriented engineering work, while broader back-to-back system context is retained for system interpretation.

This relevance should be read as an **engineering-context boundary** rather than as an application catalogue, sector claim, or qualification statement.

Accordingly, the demonstrator may inform adjacent engineering contexts that involve comparable machine-side converter questions, but it does not imply that application-specific integration, operating-envelope coverage, or product-facing completeness has been established.

---

## 9. Open Points and Deferred Development

The following topics remain intentionally deferred beyond this positioning baseline:

- hardware-platform evidence, build-ownership evidence, and detailed platform composition
- design-basis reasoning and subsystem-level baselines
- bring-up, debug, and representative validation evidence
- PC-side and MATLAB-based support-chain artefacts and evidence

These topics are introduced progressively as substantive engineering content becomes available in later phases.

---

## 10. Summary

This document establishes the project-level positioning baseline for a **30 kW-class, water-cooled PMSM drive/converter platform** developed as an **engineering demonstrator**.

Within this baseline, the project’s physical core is defined as a **machine-side converter demonstrator**, while broader back-to-back system context is retained to clarify system role, interface boundary, and the interpretation of later validation artefacts. The physical platform is also framed as the author’s own converter hardware platform, with detailed hardware-platform and build-ownership evidence deferred to later phases. The project’s present validation arrangement is based on this machine-side demonstrator, with the upstream side represented at the DC bus interface by an **external DC source**, without implying full dual-side hardware closure.

Accordingly, the project is positioned around a **single physical mainline** at machine-side level, rather than as a full hardware implementation of the broader back-to-back system or as a product-qualified or deployment-ready hardware platform. Detailed system-context interpretation is established in [`system_context.md`](system_context.md). More detailed hardware-platform evidence, design-basis rationale, and bring-up/debug/representative validation artefacts are intentionally deferred to subsequent phases as substantive engineering content becomes available.