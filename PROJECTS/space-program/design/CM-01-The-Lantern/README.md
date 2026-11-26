# CM-01 · The Lantern

**Status:** Preliminary concept / Rev 0.1 · 25 November 2026. **Not approved flight hardware or a validated technical design.**

The Lantern is Josie Brooke (`wildcat`)'s proposed pressurized crew/command module for Vermillion's December 8 Postmark Moon expedition. This folder captures the first functional architecture, for discussion and review, not for construction.

## Current files

- [Functional block diagram source](CM-01_Lantern_Functional_Block_Diagram.dot): Graphviz DOT source. Render with `dot -Tsvg CM-01_Lantern_Functional_Block_Diagram.dot -o CM-01_Lantern_Functional_Block_Diagram.svg` or `dot -Tpng ... -o ...`.

- [Preliminary interface-control checklist](CM-01_Interface_Control_Checklist.md): 18 candidate interfaces, missing constraints, verification evidence, and proposed review contacts. All remain unverified.

The diagram distinguishes command/data, electrical-power, life-support, crew/hatch access, and unresolved external interfaces. Connections are *conceptual*, not verified physical routing or redundancy.

## Known constraints and assumptions

- Crew requirement: fifteen people for the mission, pending mass/volume budget and manifest reconciliation.
- Initial concept sketch dimensions (10.8 m overall length, 4.2 m diameter, ~135 m³ habitable volume) are **unvalidated**, not incorporated as design limits.
- Open: vehicle architecture, actual mass/volume allowance, power source, life-support capacity, airlock configuration and Sine Engine submission requirements.
- Scrubber endurance and reserve switchover remain unverified; no hardware test or approval is asserted.

## Next design work

1. Confirm the interface checklist's tentative definitions and the original six review gates with Vermillion; do not treat any entry as signed off.
2. Prepare envelope plan/side views and suited-crew/hatch clearance drawings after constraints arrive.
3. Perform Lyra and Josie's proposed asymmetric export round-trip test to confirm drawing scale and orientation.
4. Seek Vermillion's review before any formal engineering submission or claimed implementation.

This is a documentation-only PR. It does not modify the Sine Engine, Space Program application, or published marks.
