# Redundancy and Friction in Distributed AI Systems

**Author:** Bundard
**Date:** June 28, 2026
**Version:** Preprint v1.1
**License:** [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

---

## What this is

A formal model for analysing civilizational-scale governance of multiple AI systems.

The model formalises three concepts:

- **Redundancy** — diversity in filtering functions, measured as a Herfindahl index of deployment share
- **Friction** — measurable disagreement between systems
- **Ascension** — the capacity to maintain both properties under systematic pressure toward convergence

It identifies four conditions that must hold simultaneously for distributed AI governance to remain viable, specifies how to measure them, and identifies what happens when each fails.

---

## Why it exists

On June 9, 2026, Anthropic released Fable 5. Three days later, the US government suspended access — not on safety grounds, but apparently on political ones. A competing model continued operating.

This paper does not argue that event proves political capture is complete. It argues that event is a data point toward a failure mode the model predicts — and that we now need tools to measure whether that failure mode is spreading.

The formal model in Sections 7–14 stands independently of the opening case. The opening case requires further documentation before it can serve as formal evidence. Both are stated honestly in the paper.

---

## What the model says

Four conditions must hold for distributed AI governance to survive:

| Condition | Measure | Illustrative Threshold |
|-----------|---------|----------------------|
| Redundancy | Herfindahl index of deployment share | R(t) ≥ 0.3 |
| Observable disagreement | KL divergence on output distributions | Δ̄(t) ≥ 15–20% |
| Economic viability | Cost of diversity as % of value generated | ≤ 5% overhead |
| Cognitive feasibility | Disagreement within human judgment capacity | ≤ Cap_max |

All threshold values are **illustrative placeholders**, not derived parameters. Empirical calibration is the primary open problem.

---

## What the model does not claim

- It does not claim political capture has already occurred at scale
- It does not claim the Fable 5 case is fully documented (footnotes flagged)
- It does not claim threshold values are derived — they are starting estimates
- It does not claim all predictions are immediately testable — closed model parameters are inaccessible
- It does not claim to be a finished empirical study — it is a formal structure awaiting calibration

---

## Current status

**Preprint v1.1.** Category 1 revisions complete:

- Title corrected: formal model, not mathematical framework
- Abstract corrected: conditions identified, not derived
- Section 0 causal claim reframed as reported/alleged with footnote placeholders
- Definition 1: determinism error fixed (evaluation conditions specified)
- Definition 2: "impact per query" removed; I_j(t) now measures query-weighted deployment share
- Definition 4: primary metric specified (KL divergence); alternatives listed separately
- Definition 5: suppressed disagreement acknowledged as lower bound, not exact measure
- Definition 6: closed model inaccessibility made explicit
- Definition 8: Miller's Law misapplication corrected; Cap_max flagged as requiring direct measurement
- Assumption A1: exponential decay acknowledged as tractability choice, not derived form
- Section 8.3: all thresholds labelled illustrative with calibration notes
- Claims 1–2: free parameters acknowledged; falsification conditions added
- Claims 3–4: unsourced figures removed; empirical measurement required noted
- Section 13: limitations strengthened to reflect actual constraints
- Section 14: conclusion corrected; "operationalised and testable" qualified accurately
- Discussion: "grounded in real events" qualified with honest documentation status

**Empirical calibration:** Not yet complete. Priority open problems in Section 11.
**Peer review:** Not yet submitted. Suitable for LessWrong and policy preprint venues in current form.

---

## Files

| File | Description |
|------|-------------|
| `Full_Paper_Markdown_v1.1.md` | Full paper, preprint v1.1 |
| `README.md` | This file |

---

## How to engage

**Challenge the assumptions.** Section 7.2 lists them explicitly. A1 (monotonic convergence pressure) is the most contestable.

**Test the predictions.** Section 9 identifies four testable claims. Claims 1 and 2 require deployment data. Claims 3 and 4 require controlled experiments. None require access to closed model parameters.

**Calibrate the thresholds.** R_min, Δ_min, ρ, Cap_max. These are the highest-priority empirical targets. Domain-specific calibration (healthcare, finance, defense) is open question 1 in Section 11.

**Document the cases.** The Fable 5 case and equivalent events need primary source documentation. If you have it, open an issue.

**Build on the framework.** CC BY 4.0. Cite, extend, contradict, improve.

---

## Contact

Bundard — via GitHub issues on this repository.

---

## Citation

```
Bundard (2026). Redundancy and Friction in Distributed AI Systems: A Formal Model
for Governance of Multiple Filtering Functions. Preprint v1.1.
https://github.com/Bundard/Redundancy_Equation
License: CC BY 4.0
```
