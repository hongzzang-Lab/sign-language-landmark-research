# Research Stages & Methods

This page documents the scope of each stage without releasing code, sensitive datasets or unpublished implementation details.

| Stage | Focus | Public status |
|:--|:--|:--|
| KCI — Application | Emergency sign language interpretation | Published, 2026 |
| [CICS'26 — Representation](cics-2026.md) | Feature combinations and robustness to input corruption | Official conference program · SS07-07 |
| IPIU-oriented — Reliability | Missing-landmark restoration, feature error and recognition | Ongoing |
| Future — Adaptation | Input reliability-aware feature processing | Exploratory |

## Feature representations

The investigated landmark input uses **51 landmarks** (9 upper-body landmarks and 21 landmarks per hand), each with xyz coordinates.

| Dimension | Representation |
|:--|:--|
| **153D** | 51 × 3 landmark coordinates |
| **306D** | 153D positions + 153D temporal differences |
| **317D** | 306D augmented with selected relative-distance and palm-normal geometry |
| **347D** | Additional hand/finger-angle geometry |

These are project-specific representations rather than universal sign-language-recognition standards.

## Reliability and evaluation

- **Missing observations and temporal padding are not equivalent.** They require different masks or validity handling.
- **Coordinate RMSE and recognition Macro-F1 are different evaluation objectives.** Lower landmark error does not guarantee improved downstream recognition.
- **Signer-disjoint splits and consistent data protocols** are necessary when discussing generalization.
- **Streaming robustness must be demonstrated** rather than inferred from offline classification accuracy.

[Back to README](../README.md) · [CICS'26 research](cics-2026.md) · [Research story](research-story.md)
