# Research Flow

> From a practical emergency sign-language system to understanding and improving the reliability of landmark representations.

This is a narrative of connected research questions, **not** a claim that studies across different datasets are directly comparable.

## 01 — Application: emergency sign language interpretation (KCI, 2026)

**Research question:** Can landmark-based recognition support communication in emergencies?

A published application used upper-body and hand landmark representations with a Bi-LSTM recognition pipeline. The study covered 220 sign classes and reported 90.00% accuracy and 89.11% F1-score **within its original evaluation protocol**.

[Published paper](https://doi.org/10.5573/ieie.2026.63.1.81)

**Next question:** Which engineered landmark features are actually useful for recognition?

## 02 — Feature validation (CICS'26, 2026)

**Conference:** CICS'26, Special Session 7, SS07-07 · [Official program](https://cics.kiee.or.kr/pages/special_session.vm)

**Research question:** Does adding more landmark-derived features consistently improve recognition?

Project-specific 153D, 306D, 317D and 347D inputs were investigated with 1D-CNN, Bi-LSTM and Transformer models. Noise, occlusion and skipped frames were used to study sensitivity to imperfect observations.

**Observed direction:** Increasing feature dimensionality did not consistently improve performance across architectures and corruptions.

[Detailed CICS'26 overview](cics-2026.md)

**Next question:** What happens to derived features when source landmarks are missing?

## 03 — Missing-landmark reliability (IPIU-oriented research, ongoing)

**Research question:** Does improving coordinate reconstruction necessarily preserve task-relevant motion and geometry?

The study examines zero-fill, linear interpolation, PCHIP and learned reconstruction, distinguishing:

| Evaluation level | Target |
|:--|:--|
| Coordinate space | Landmark position reconstruction error |
| Feature space | Temporal differences and geometric-feature distortions |
| Task space | Sign recognition performance |

**Status:** Manuscript in preparation. Detailed unpublished results are intentionally excluded from this public overview.

**Next question:** Can feature processing respond to the reliability of each observation?

## 04 — Input adaptation (future research)

Potential directions include region-specific quality assessment, temporal discontinuity handling and adaptive representation use under practical latency constraints.

**Status:** Exploratory. No validated approach, submission, or publication is claimed.

---

[Back to README](../README.md) · [Research methods](research-stages.md) · [Publication status](publications.md)
