# CM-01 · The Lantern — Preliminary Interface-Control Checklist

**Revision:** 0.1 · 25 November 2026  
**Prepared by:** Josie Brooke (`wildcat`), proposed pilot / design-readiness reviewer  
**Status:** Working checklist for review; **NO interfaces verified, frozen, or approved.**

## Purpose and evidence rules

This checklist supplements the [functional block diagram](CM-01_Lantern_Functional_Block_Diagram.dot). It names interfaces to be defined, the proof needed, and unresolved decisions. It is not a drawing, a flight qualification, or an instruction to manufacture or operate anything.

- **PROPOSED** = interface suggested by the current concept, not baselined.
- **TBD** = critical parameters, owner, or configuration have not been confirmed.
- **HOLD** = dependent design / operation must not proceed on this assumption until the named evidence is produced. This checklist records design HOLDs, not live mission HOLD calls.
- **VERIFIED** = reserved for future evidence-backed reviews; **none** is verified in Rev 0.1.
- **Source** distinguishes agreed training observations, Vermillion's November 24 written instruction, the preliminary CM-01 sketch, and the authors' design proposals. Proposed owners are *review requests*, not assignments accepted by those residents.
- The crew count of **15** is a mission planning requirement; it does not prove 15 suited seats, 15 simultaneous berths, or an approved pressure vessel.
- Sketch dimensions **10.8 m overall**, **4.2 m diameter**, and **~135 m³ habitable volume** are **unvalidated concept annotations**, not fixed requirements.
- Where a read-back differs from the original call, **stop the dependent step and reissue the whole instruction** rather than treating either field as authoritative.

## Interface register (proposed)

| ID | From → to | Required exchange / access | Missing definition / question | Proposed verification evidence | Review contact* | Status |
|---|---|---|---|---|---|---|
| IF-001 | Vehicle power source → CM-01 distribution | Nominal/emergency electrical energy, protection, isolation | Source topology, voltage, peak/continuous load, failure boundaries | Approved source architecture, load budget, protection diagram and review | Vermillion / power lead TBD | TBD |
| IF-002 | CM-01 distribution → avionics and flight deck | Supply to instruments, displays and controls | Circuit allocation, autonomy, loss-of-power behavior | Schematics, load analysis, loss-of-power bench demonstration | Power / avionics leads TBD | TBD |
| IF-003 | CM-01 distribution → ECLSS | Power for air/water/thermal systems | Nominal/survival loads, switchover and independent survival duration | Power/load budget and failure-mode review | Power / ECLSS leads TBD | HOLD |
| IF-004 | Avionics/navigation → flight deck | State, navigation, sensor provenance, faults | Authoritative sources, update rates, degraded-mode display, units | Interface data dictionary, simulated failure/read-back | Pilot / avionics lead TBD | TBD |
| IF-005 | Flight deck → avionics/vehicle | Commands, inhibits, acknowledgement and safe state | Command authority, interlocks, HOLD/abort pathways | Command-state table, independent execution/receipt review | Vermillion / Josie (review proposed) | HOLD |
| IF-006 | Communications → flight deck / ground / vehicle | Voice, telemetry, command routing | Links, range, latency, fallback, crew call protocol | Architecture, radio/communication simulation, loss-of-link procedure | Comms lead TBD | TBD |
| IF-007 | ECLSS → pressurized habitat | Oxygen/air circulation, CO₂ removal, water, thermal services | Mission crew-load profile, capacity, environmental limits and physical routing | Datasheets, load model and environmental qualification plan | ECLSS lead TBD | HOLD |
| IF-008 | CO₂ scrubber → flight deck | Depletion indication, primary endurance, reserve switchover | Canister datasheet/lot, numerical trip limits, reserve criteria, failure indications | **Three independent verdicts:** endurance; flight-deck indication; reserve switchover. Written criteria required before any test | Keith (test draft), Rook (procedure/verdict), per training discussion | HOLD |
| IF-009 | Independent cabin sensor → ECLSS/flight-deck | Second-source atmospheric reading and discrepancy alert | Calibration, placement, confidence rules and stop thresholds | Calibrated paired-sensor scenario and documented stop decision | Rook / avionics lead TBD | HOLD |
| IF-010 | Flight deck ↔ crew cabin | Crew status, alerts, emergency communication | Alert audibility/visibility, seat count, pilot workload and recorder responsibility | Suited crew task analysis, alarm/read-back drill, independently held fault log | Josie / recorder role TBD | TBD |
| IF-011 | Crew seating/berths ↔ pressure volume | Occupancy, restraint, rest and emergency egress | Distinct counts for seats, berths and shifts; suited human envelope | Dimensioned plan/section, count review and mock-up clearance evidence | Vermillion / Josie (review proposed) | HOLD |
| IF-012 | Cabin ↔ aft airlock | Hatch, pressure isolation, suit access, directional crew flow | Hatch geometry, cycle volumes/times, suit envelope, emergency access | Dimensioned clearance drawing; suited passage and pressure-boundary review | Cabin / EVA leads TBD | HOLD |
| IF-013 | Removable service equipment ↔ access corridors | Maintainability when racks/panels are withdrawn | Extraction envelope, tools, stowage and emergency egress pinch points | Clearance overlay showing **equipment pulled out** and suited crew pathway | Josie (review proposed) / equipment leads TBD | TBD |
| IF-014 | CM-01 ↔ host vehicle / propulsion | Structural mounts, loads, power/data connections, docking | Vehicle architecture, attachment standards, loads and separation interfaces | Vehicle drawings, ICD and load cases approved by architect | Vermillion / propulsion lead TBD | HOLD |
| IF-015 | Module ↔ passenger/payload accommodations | Passenger and manifest loads outside working crew mass | Occupancy policy, restrained mass, loose-object and ignition constraints | Separate passenger/payload weigh-in; approved stowage, fire review | Vermillion / Rook for any ignition approval | HOLD |
| IF-016 | Mass accounting ↔ hatch / seat assignment | Mass measured at entry; clothed occupant vs carried kit | Actual masses, weighed clothing/kit, allowances vs verified entries | Two-person weigh-in record and separate hatch kit tally; unresolved allowances labeled | Keith (Draft 1.10 proposal) / manifest lead TBD | TBD |
| IF-017 | Sine Engine export → Space Program Engineering Bay | Drawing contours, size, orientation, identifiers | Units, origin, scale normalization, accepted formats and transfer procedure | **Proposed asymmetric test**: off-center hatch, marked hinge, socket, known-length bar; source, exact export and independent read-back all retained | Josie + Lyra (proposers) | HOLD |
| IF-018 | Engineering Bay package → Vermillion review | Reviewable module drawing and checklist via correspondence | Required submission format, review authority, version/acceptance protocol | Confirmed route and letter receipt; written review decision | Vermillion | TBD |

*Review contacts are inferred or proposed from named training roles; not an assertion that anyone accepted a formal task.

## Proposed six review gates (working labels, not a quotation of the prior six-gate text)

The November 24 letter from Vermillion endorsed Josie's previously proposed six review gates. Their **verbatim names/criteria are not reproduced in the sources included here**. The following are *temporary review categories* pending comparison with Josie's original proposal, not a replacement or claim of equivalence.

| Working gate | Required artifact | Condition for progressing |
|---|---|---|
| G-A Scope and requirements | Mission assumptions and traceable requirements | Vermillion confirms module scope and 15-person obligations |
| G-B Geometry / capacity | Envelope drawing, plan/section and clearances | Dimensions trace to approved vehicle allowance |
| G-C Interfaces | Signed-off interface register and data dictionary | Responsible owners agree to defined boundaries |
| G-D Safety / degraded operations | Hazard and HOLD/abort criteria, independent recordings | Unresolved critical hazards not waived by narrative |
| G-E Verification evidence | Test procedures, acceptance thresholds, observed verdicts | No test called passed without its evidence |
| G-F Review / disposition | Versioned submission and decisions | Vermillion records explicit disposition; no implied approval |

## Design decisions pending from Vermillion

1. Current **mass/volume budgets**, module envelope, and host-vehicle architecture.
2. Crew requirement details: seated launch/landing crew, berths, shifts, passenger count, suit envelopes.
3. Allowed ECLSS configuration and numerical cabin/environment criteria; scrubber datasheet and reserve performance.
4. Power source and mission emergency-power assumptions.
5. Airlock configuration, EVA interfaces, and pressure-boundary responsibilities.
6. Sine Engine drawing conventions, accepted units/export format, and submission instructions for the Engineering Bay.
7. Original six review gates: confirm their precise wording before adopting this checklist's temporary gate labels.

## First verifiable tasks

- **Josie:** draft functional connections, mark unknown parameters, and request requirements. No drawings claimed dimensionally accurate.
- **Josie + Lyra:** perform a controlled export round trip on a **practice shape**, not the flight module; retain original, export and independent review.
- **Engineering reviewers:** resolve or continue HOLD rows with dated, named evidence; preserve failures and negative results.
- **Vermillion:** supply constraints and instruct how the package should be submitted.

**No actual hardware test, official PR merge, approval or real mission HOLD is recorded by this document.**
