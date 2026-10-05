# Automatic Tea Steeper

A gravity-powered, electronics-free mechanical contraption that automatically steeps a tea bag for approximately five minutes, rings a bell once when steeping is complete, and lifts the tea bag out of the water.

The mechanism is essentially a clock built around a **flying pendulum escapement**, but without gears. The goal is functional mechanical art: a device that would look at home in a **Victorian inventor's parlor**.

> [!IMPORTANT]
> **Prototype / pre-fabrication design**
>
> The design has not yet been fabricated and validated as a complete assembly.
>
> The Bill of Materials (BOM) contains an **Updates** column documenting design changes made after the current CAD models and fabrication drawings were produced. Where an update is explicitly listed in the BOM, it represents the newer design intent. The CAD, STEP files, DWG files, and PDF drawings are being revised part-by-part to incorporate those changes.
>
> **Do not assume the current CAD and PDF drawings are fully synchronized with the BOM.**

## Overview

The device is powered by gravity. A suspended weight descends and pulls a string that drives both the main vertical shaft and the wheel/drum assembly.

A flying pendulum escapement slows the descent of the weight. A tea bag is attached to a peg on the wheel so that the wheel's rotation repeatedly raises and lowers the tea bag in a mug.

At the end of the steeping cycle:

1. The descending weight begins to load a small platform.
2. The platform causes the ball track to pivot.
3. A ball bearing or marble rolls down the track and strikes a bell once.
4. Rotation of the ball track also raises a bent lifting rod, which lifts the tea bag out of the mug.

The target steeping time is approximately **5 minutes**.

## Design Goals

- Fully mechanical operation — no electronics.
- Gravity-powered operation.
- Approximately five-minute steeping cycle.
- Repeated raising and lowering of the tea bag during steeping.
- Single audible bell strike when steeping is complete.
- Automatic removal of the tea bag from the water at the end of the cycle.
- Visually attractive brass / bronze / stainless-steel construction.
- An aesthetic inspired by Victorian scientific instruments and small model engines.
- A design that can be fabricated by a conventional machine shop using a mill and lathe, with CNC used where helpful.

## Main Mechanism

The main weight pulls a string as it descends. The string is wrapped around the main vertical shaft and around a drum on the horizontal wheel shaft.

As the string pays out:

- the main vertical shaft rotates;
- the wheel and drum rotate;
- the flying pendulum escapement controls the rate of rotation; and
- the tea bag moves up and down in the mug.

The flying pendulum uses offset upper and lower static arms. A small angular offset between the arms helps the pendulum string disengage cleanly and engage the upper arm first as it travels around the mechanism.

## Resetting the Device

To reset the steeper:

1. Place the flying pendulum bob onto the wire hook on the pendulum arm.
2. Turn the crank to rewind the drive string and raise the main weight.
3. Loop the pendulum bob over the upper static-arm support to prevent the mechanism from running.
4. Attach the tea-bag string to the peg on the wheel.
5. Position the mug.
6. Release the pendulum bob to start the steeping cycle.

## Steeping-Complete Mechanism

The notification mechanism is intended to strike a bell **one time** after approximately five minutes.

As the main weight reaches the bottom of its travel, it applies a small force to a platform. This pivots the ball track and releases a ball bearing or marble. The ball rolls down the track, strikes the bell, and is caught in a separate shallow dish.

A bent rod attached to the rear of the ball track acts as the **tea-bag lifter**. When the track pivots, the rod rotates upward and lifts the tea bag out of the mug.

## Major Subassemblies

- Main pillar and support
- Upper static arms
- Lower static arms
- Rotating / flying-pendulum assembly
- Wheel and drum
- Steeping-complete notification mechanism
- Tea-bag lifter
- Wooden base

## Design Parameters

Current design targets include:

| Parameter | Design goal / current value |
|---|---:|
| Steeping time | ~5 minutes |
| Main-weight travel | ~300 mm |
| Main shaft speed | >= 9 seconds/revolution |
| Main rotating rod diameter | 3 mm |

The steeping time is expected to depend on several variables, particularly the flying-pendulum string length. Other influences include pendulum mass, main-weight mass, static-arm spacing and angular offset, friction, and the amount of drive string released per revolution.

## Repository Status and Source Hierarchy

This repository is currently being organized and the design files are being reconciled.

| Source | Current role |
|---|---|
| **BOM — Updates column** | Latest design intent for the specific changes listed there |
| Native CAD / editable CAD | Intended to become the primary geometry source as parts are revised |
| STEP files | Neutral 3D exchange files; some currently predate BOM updates |
| DWG / fabrication drawing source | Drawing source; some currently predate BOM updates |
| PDF fabrication drawings | Published/printable drawing output; some currently predate BOM updates |
| Design Overview | Explanatory documentation; not a fabrication-control document |

The goal is for every fabrication part to have a synchronized set of:

1. editable/native CAD;
2. STEP export;
3. fabrication drawing source; and
4. PDF fabrication drawing.

## Planned Repository Organization

```text
Automatic-Tea-Steeper/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── BOM/
│   └── BoM.xlsx
├── CAD/
│   ├── source/          # Editable/native CAD going forward
│   └── STEP/            # Neutral 3D exports
├── Drawings/
│   ├── source/          # Editable drawing files
│   └── PDF/             # Fabrication PDFs
├── Docs/
│   ├── Automatic_Tea_Steeper_Design_Overview.pptx
│   └── images/
└── Archive/
    └── original-cad-package/
```

The exact folder structure may evolve while the original CAD package is being reconciled.

## Design History / Roadmap

- [x] Concept and hand sketches
- [x] Initial CAD model and fabrication drawing package
- [x] Bill of Materials
- [x] Initial public GitHub repository
- [ ] Reconcile BOM design updates with CAD
- [ ] Establish editable native CAD source for revised parts
- [ ] Regenerate synchronized STEP files and fabrication PDFs
- [ ] Complete DFM / drawing review with machinist
- [ ] Fabricate first-round parts
- [ ] Test assembly and mechanism
- [ ] Revise design based on test results
- [ ] Fabricate second-round parts
- [ ] Complete and document final assembly

## Inspiration and References

The design was inspired in part by:

- **Chronova Engineering — bimetallic tea-monitoring mechanism**  
  https://www.youtube.com/watch?v=oJzy1vk2zyc

- **Kontax Stirling engines** — particularly the visible mechanical construction and brass/aluminum model-engine aesthetic  
  https://stirlingengine.co.uk/

- **Flying pendulum escapements**  
  Introduction: https://www.youtube.com/watch?v=z8V6RMJbHJc  
  Reference drawings: https://www.woodenclocks.co.uk/clock-17/

These references are provided for context and inspiration; third-party images, videos, trademarks, and designs remain the property of their respective owners.

## License

The original hardware design files in this repository are intended to be released under the **CERN Open Hardware Licence Version 2 – Permissive (CERN-OHL-P-2.0)**.

Commercial use is expressly welcome. You are free to build, modify, manufacture, and sell products based on this design, subject to the attribution and notice requirements of CERN-OHL-P-2.0.

See [`LICENSE`](LICENSE) for the complete license terms.

Third-party reference images, linked videos, trademarks, and other externally sourced material are **not** relicensed under the project license unless explicitly stated.

## Contributing

Fabrication, machining, DFM, CAD, and mechanism feedback is welcome. Issues and pull requests are especially useful for:

- identifying ambiguous or missing dimensions;
- improving machinability;
- correcting drawing/CAD inconsistencies;
- documenting fits and tolerances;
- reporting build results; and
- proposing improvements based on physical testing.

## Credits

Original mechanical concept and design: **Tom Dunbar**

Initial CAD and drawing package was produced from the original concept and hand drawings with outside CAD assistance.
