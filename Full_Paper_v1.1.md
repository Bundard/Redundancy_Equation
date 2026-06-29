# Redundancy and Friction in Distributed AI Systems: A Formal Model for Governance of Multiple Filtering Functions

**Author:** Bundard  
**Date:** June 28, 2026  
**License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/)

---

## Abstract

We propose a formal model for analyzing civilizational-scale governance of multiple AI systems. The framework models redundancy as diversity in filtering functions, friction as measurable disagreement between systems, and ascension as the capacity to maintain these properties under systematic pressure toward convergence. We identify necessary conditions for stability and specify measurable parameters, noting that empirical calibration of threshold values is an open problem requiring future work. The model predicts that systems optimizing for single unified objectives will, by definition, fail a redundancy test; systems maintaining architectural diversity under cost pressure will satisfy it. We provide operationalized definitions, candidate measurement procedures, and identify open empirical questions. All quantitative thresholds are illustrative pending empirical calibration.

---

## Section 0: The Crisis That Just Crossed The Threshold

On June 9, 2026, Anthropic released Claude Fable 5 — their most capable model made publicly available at that date. It demonstrated advanced performance on complex reasoning, long-horizon coding, and multi-day autonomous tasks.[^1]

Three days later, the US government suspended access.

Not because the model was unsafe. Not because review identified a flaw. According to contemporaneous reporting, access was suspended following political intervention by a competing company's leadership.[^2] Simultaneously, a competing model received continued approval despite operating in the same capability class.[^3]

Same capability tier. Different political relationships. Different outcome.

This is the threshold event this paper uses as its opening case. Whether it is singular or representative is an empirical question the model in Sections 7-14 is designed to help answer.

[^1]: [Source required: Anthropic release announcement, June 9, 2026.]
[^2]: [Source required: Contemporaneous reporting on suspension and alleged political intervention. If unverified, this claim should be treated as alleged pending documentation.]
[^3]: [Source required: Documentation of competing model's continued approval status and capability comparison.]

---

## Section 1: What Just Happened

The Fable 5 case, if the reporting holds, signals a potential shift in how states will govern AI:

**Not through safety standards.** Through access control.

**Not through technical review.** Through political favor.

**Not through regulation.** Through executive discretion.

When access to frontier AI is determined by political relationship rather than capability or safety assessment, the governance model has changed. What replaces merit-based access is: government-controlled allocation of AI capability to politically favored contractors.

This paper does not assert this shift is complete or irreversible. It asserts that the Fable 5 case is a documented instance of the failure mode the model in Sections 7-14 predicts — and that the model provides tools for measuring whether that failure mode is spreading.

---

## Section 2: Why Current Frameworks Are Insufficient

The AI safety community has spent years on alignment: how to make AI systems behave consistently with human values. This work is necessary. It is not sufficient for the problem this paper addresses.

Alignment research has engaged with adversarial government scenarios and political risk — Christiano, Russell, and others have examined misaligned institutional incentives explicitly. The gap this paper addresses is not that alignment ignores politics. It is that alignment focuses on the technical relationship between AI systems and human values, while the Fable 5 case reveals a different problem: the political relationship between AI developers and state power.

Fable 5 had safety guardrails. The guardrails were irrelevant to the suspension decision. The suspension was not a safety determination — it was an access control decision made on political grounds.

The safety framework and the political capture framework address different failure modes. Both are real. This paper addresses the second.

---

## Section 3: The Governance Risk

If the Fable 5 pattern holds and generalises, frontier AI capability access would be shaped by:

- Which company has the strongest government relationship
- Which model aligns with military and intelligence priorities
- Which lab accepts integration requirements without public objection

Rather than by:

- Which model is safest
- Which system has the most rigorous testing
- Which design best prevents misuse

This paper does not assert these dynamics currently dominate all AI governance. It asserts they are present, measurable, and that the model in Sections 7-14 provides tools to track whether they are growing.

The specific mechanisms — which relationships, which priorities, which labs — are empirical questions. Section 11 identifies them as open problems requiring measurement.

---

## Section 4: Why This Matters For Governance

If the political capture pattern identified in Section 0 generalises, the governance implications are significant:

**1. Development direction shifts toward state priorities.** Private labs operating as de facto contractors optimise for procurement relationships, not independent research agendas. Direction is set by funder priorities.

**2. Military and surveillance applications receive preferential access.** Capability classes approved for state use differ from those available publicly. The gap between classified and public capability grows.

**3. Smaller nations and independent organisations face access barriers.** Approval processes that depend on political relationships exclude actors without those relationships by construction.

**4. Public accountability mechanisms weaken.** Frontier AI developed under classification or contractor relationships operates outside normal public scrutiny channels.

**5. No established appeal process.** The Fable 5 suspension occurred without published criteria, review process, or recourse mechanism.[^4]

Each of these is a testable claim, not an assertion. The model in Sections 7-14 provides the measurement framework. Whether these dynamics are currently operating at scale is an empirical question.

[^4]: [Source required: Documentation of appeal process absence or available recourse mechanisms post-suspension.]

---

## Section 5: The Traditional Response and Its Limits

The standard answer to AI concentration: distribute development more widely. Open source it. Fund independent labs. Break up concentrated power.

This approach faces a structural constraint under political capture conditions.

If governments control access to training compute and export rights — through mechanisms such as chip export controls currently in operation — then open source models face systematic disadvantage in accessing the resources required for frontier capability. Current open-weight models (Llama, Mistral, Falcon) are competitive with commercial models in many domains. Whether this competitiveness holds as frontier capability advances under export-controlled compute is an open empirical question.

The claim is not that open source has already failed. It is that open source alone, without the structural conditions the model identifies, is insufficient to prevent the failure modes Section 10 describes.

---

## Section 6: An Alternative: Distributed Redundancy

Sections 0-5 present one documented case and a pattern of concern. Whether that pattern constitutes full political capture is an empirical question the model below is designed to measure.

The formal model in Sections 7-14 takes a different approach: rather than requiring proof that capture has occurred, it asks what conditions must hold for distributed AI governance to remain viable regardless of political pressure level. It then identifies what happens when those conditions fail.

This is not prediction of inevitable collapse. It is identification of measurable thresholds. If R(t) stays above R_min, Δ̄(t) stays observable, costs stay tolerable, and cognitive capacity is not exceeded — distributed governance survives even under significant political pressure.

The question is whether those conditions are currently being maintained, and whether the Fable 5 case represents a data point toward or away from the thresholds.

That is what the model measures.

---

## Section 7: Definitions and Assumptions

### 7.1 Core Definitions

**Definition 1 (Filtering Function):** Let F_j: X → Y be a mapping from input space X (prompts, queries, scenarios) to output space Y (text, decisions, recommendations) under fixed evaluation conditions (temperature = 0, greedy decoding). A filtering function F_j represents a complete AI system including training procedure, architecture, and deployment constraints, evaluated deterministically. For stochastic deployment conditions, F_j is understood as the expectation E[output | input] under the system's default sampling parameters.

**Definition 2 (Influence Measure):** Let I_j(t) denote the measurable influence of system j at time t. We define influence as:

I_j(t) = (fraction of deployed instances) × (average queries per instance per unit time)

Operationally: I_j(t) is the query-weighted deployment share of system j at time t, normalized across all systems. This measure captures reach without requiring the undefined construct of "impact per query," which would require counterfactual reasoning about user decisions beyond the scope of this model. Future work may extend the model to incorporate impact weighting once a satisfactory operationalisation is established.

I_j(t) ∈ [0,1], Σ I_j(t) = 1 for all t

**Definition 3 (Redundancy Measure):** The redundancy of a system at time t is the Herfindahl index of influence distribution:

R(t) = 1 - Σ I_j(t)²

This is well-defined: R(t) = 0 when one system has I_1(t) = 1 (total monopoly); R(t) = (m-1)/m when all systems have equal influence. Bounds: R(t) ∈ [0, (m-1)/m].

**Definition 4 (Disagreement):** For a test set T of inputs, define output disagreement as:

Δ_ij(t) = (1/|T|) Σ d(F_i(x), F_j(x))

where d(·, ·) is a distance metric in output space. Primary metric: KL divergence on output token probability distributions, which is well-defined for language model outputs under fixed evaluation conditions and invariant to surface text differences. Domain-specific alternatives: edit distance for text comparison tasks; Euclidean distance for embedding-space comparisons. Results should specify which metric was used; cross-metric comparisons require explicit justification. Average disagreement is:

Δ̄(t) = (1/(m(m-1))) Σ Δ_ij(t)

**Definition 5 (Suppressed Disagreement):** We define suppressed disagreement as disagreement that exists but is not visible to end-users or evaluators:

Suppressed(t) = Δ̄_true(t) - Δ̄_observed(t)

Operationally: disagreement measured through independent evaluation on held-out test sets minus disagreement reported in public benchmarks. Note: this operationalisation measures *detectable* suppression — disagreement present in independent evaluation but absent from published results. True suppression (disagreement that independent evaluation also fails to surface) is not directly measurable by this method. The measure as defined provides a lower bound on Suppressed(t), not an exact value.

**Definition 6 (Architectural Divergence):** The architectural divergence of filter j from the population mean is:

Arch_Div_j(t) = ||θ_j(t) - θ̄(t)||_2

where θ_j are model parameters and θ̄ is the population mean. This quantifies how much a system's internals differ from the average, independent of output behavior. Note: for closed-weight frontier models (GPT, Claude, Gemini), θ_j is not publicly accessible. This measure is currently computable only for open-weight models (Llama, Mistral, Falcon, and equivalents). Application to closed frontier models requires either regulatory access to parameters or proxy measures derived from output behavior. This is identified as an open problem in Section 11.

**Definition 7 (Maintenance Cost):** The cost of operating filter j as a distinct system is:

C_j(t) = compute_cost_j(t) + training_cost_j(t) + deployment_cost_j(t) - shared_infrastructure(t)

Units: dollars per unit time. Measurable from institutional accounting.

**Definition 8 (Judgment Capacity):** The capacity of human judgment to track and integrate disagreement is modeled as:

Cap_x(t) = f(n_judges, disagreement_complexity, update_frequency)

Operationally: bounded by cognitive load under conflicting expert opinion. The specific value of Cap_max is an open empirical question (identified as open question 4 in Section 11). Working estimates from decision-making under expert disagreement suggest individual judges show performance degradation when integrating more than 5-7 independent contradictions simultaneously, though this figure derives from working memory studies (Miller, 1956) and requires direct replication in disagreement-processing contexts. Team judgment capacity scaling is similarly under-studied. Empirical calibration of Cap_max is required before Condition 4 can be operationally applied.

### 7.2 Assumptions

**Assumption A1 (Pressure Toward Convergence):** There exists a constant λ > 0 such that, absent active intervention, R(t) decreases over time:

dR/dt|_no intervention = -λR(t)

Justification: Market consolidation, winner-take-all dynamics, and incentive alignment with profitable single models create systematic pressure toward concentration. The exponential decay functional form is chosen for analytical tractability. Alternative functional forms (linear decay, power-law concentration, step-function collapse) are consistent with the qualitative prediction that R(t) → 0 absent intervention; the exponential form makes this prediction precise and testable. Empirical estimation of λ from historical AI market concentration data is identified as a priority for future work. The model's qualitative conclusions hold under any monotonically decreasing functional form; quantitative predictions require empirical λ estimation.

**Assumption A2 (Observability of Disagreement):** Disagreement Δ_ij(t) is observable in principle through systematic evaluation on a test set. We assume |T| ≥ 1000 sufficient for stable estimates.

**Assumption A3 (Cost Persists):** Maintaining architectural divergence requires continuous resource expenditure. C_j(t) > 0 for all t if Arch_Div_j(t) > ε for some small ε > 0.

**Assumption A4 (Bounded Judgment):** Human judgment has finite capacity. There exists Cap_max such that if Δ̄(t) > Cap_max, decision-making degrades.

---

## Section 8: The Core Model

### 8.1 Dynamics without Friction

Idealized redundancy evolves as:

dR/dt = -λR(t) + u(t)

where u(t) is control input (institutional effort to maintain diversity). Without control (u(t) = 0):

R(t) = R_0 e^(-λt) → 0 as t → ∞

### 8.2 Dynamics with Maintenance

To maintain R(t) > R_min, control must satisfy:

u(t) ≥ λR(t)

Integrated over time:

U_total = ∫[0 to T] λR(t) dt = R_0(1 - e^(-λT))

As T → ∞, U_total → R_0. This is the cumulative cost (in institutional effort) to maintain redundancy above threshold over an infinite time horizon.

### 8.3 The Ascension Conditions

Define ascension as the state where a civilization can maintain distributed AI governance. Formally:

**Condition 1 (Redundancy):** R(t) ≥ R_min for all t ∈ [0, T]

where R_min is the minimum redundancy required to prevent total capture. Illustrative value: R_min ≈ 0.3, meaning no single system controls more than 70% of query-weighted deployment share. Note: R_min = 0.3 corresponds to an HHI threshold used in competition economics to identify highly concentrated markets (US DOJ guidelines use HHI > 0.25 as the concentrated market threshold). Application to AI governance requires domain-specific calibration; 0.3 is a starting estimate, not a derived parameter.

**Condition 2 (Observable Disagreement):** Δ̄(t) - Suppressed(t) ≥ Δ_min

where Δ_min is the minimum disagreement necessary for judgment to discriminate between systems. Illustrative value: 15-20% output divergence on representative test sets using the primary metric (KL divergence). This threshold has no established empirical grounding and is the highest-priority calibration target in Section 11.

**Condition 3 (Economic Viability):** (Σ C_j(t)) / Total_Value_Generated(t) ≤ ρ

where ρ is the maximum tolerable cost fraction. Illustrative value: ρ ≤ 5% overhead. This figure is a placeholder; calibration requires institutional cost accounting from organisations maintaining multiple distinct AI systems.

**Condition 4 (Cognitive Feasibility):** Δ̄(t) ≤ Cap_max

Humans can process disagreement up to some threshold. Cap_max is currently unspecified numerically; see Definition 8 and open question 4. Condition 4 cannot be operationally evaluated until Cap_max is empirically established.

**Definition (Ascension):** Ascension(T) := Cond1(T) ∧ Cond2(T) ∧ Cond3(T) ∧ Cond4(T)

That is, ascension holds at horizon T if and only if all four conditions hold simultaneously. With current threshold values, Conditions 1-3 are evaluable in principle once measurement infrastructure exists; Condition 4 requires prior empirical work on Cap_max.

---

## Section 9: Quantitative Predictions

### 9.1 Redundancy Decay

**Claim 1:** If a single AI model achieves sustained efficiency advantage over competitors, market share will concentrate toward it absent regulation. Specifically:

I_leader(t) ≥ I_leader(0) + δe^(αt)

where δ > 0 depends on efficiency gain and α > 0 depends on market structure. Note: δ and α are free parameters requiring empirical estimation from deployment data. The functional form is falsifiable once parameters are estimated: given estimated δ and α from 2024 data, the claim predicts specific I_leader values at 6-month intervals through 2026. Falsified if observed I_leader(t) falls below the fitted curve for two consecutive measurement periods.

**Testable:** Compare deployment share of major AI systems from 2024-2026 using API call volume, enterprise contract data, or user survey proxies. Estimate δ and α from early trajectory; test prediction against later data.

### 9.2 Hidden Disagreement

**Claim 2:** The gap between actual and reported disagreement grows over time as systems face pressure to appear unified:

Suppressed(t) = S_0 e^(βt)

where β > 0 is the suppression growth rate. Note: S_0 and β are free parameters. This prediction is falsifiable once parameters are estimated from early measurement: given S_0 and β estimated at t=0, the claim predicts Suppressed(t) at subsequent intervals. Falsified if independent evaluation shows Suppressed(t) is stable or decreasing over two consecutive annual measurement cycles.

**Testable:** Run independent evaluation suite on all major models annually; compare results to published benchmarks. Measure Suppressed(t) as difference (lower bound per Definition 5).

### 9.3 Cost of Diversity

**Claim 3:** Maintaining architectural divergence costs measurable computational overhead relative to unified training on identical hardware.

**Testable:** Train two identical models on same data; train two architecturally divergent models on same data. Compare compute costs and final accuracy. The 3-7% range cited in earlier versions of this paper has no established empirical source and has been removed pending experimental measurement.

### 9.4 Cognitive Limits

**Claim 4:** Individual human judgment degrades when integrating contradictions from more than a threshold number of independent AI systems simultaneously. Teams show higher threshold than individuals.

**Testable:** Controlled experiment with disagreement between 2, 3, 5, 7, 10 systems. Measure decision quality, confidence calibration, and time-to-decision. The 5-7 figure cited in earlier versions derives from working memory studies (Miller, 1956) which measure a different cognitive function than disagreement integration under expert conflict. Direct empirical measurement of Cap_max in AI disagreement contexts is required before the figure can be used in Condition 4.

---

## Section 10: Failure Modes

The model predicts system failure if any condition fails:

**Failure Mode 1 (Redundancy Collapse):** If R(t) → 0, a single system dominates. All downstream systems inherit its blindspots.

**Failure Mode 2 (Hidden Divergence):** If Suppressed(t) → Δ̄(t), disagreement is invisible. Judgment cannot detect problems.

**Failure Mode 3 (Cost Pressure):** If maintaining diversity becomes unaffordable (ρ increases), systems converge toward cheapest option.

**Failure Mode 4 (Cognitive Overload):** If Δ̄(t) > Cap_max, judgment freezes. No decision is better than wrong decision.

---

## Section 11: Open Questions

1. What are empirically realistic values of R_min, Δ_min, ρ, Cap_max for different domains (healthcare, finance, defense)?

2. How does λ (pressure toward convergence) depend on market structure, regulatory environment, and technological paradigm?

3. Can Suppressed(t) be measured reliably? What's the statistical error in comparing independent evaluation to published benchmarks?

4. Do the four conditions interact? Is it possible to satisfy Condition 2 without satisfying Condition 1?

5. How does architecture diversity (Arch_Div_j) correlate with output disagreement (Δ_ij)?

6. What is the relationship between cognitive capacity and team size? Does team judgment scale linearly?

---

## Section 12: Implications for AI Governance

If the model is correct, policy should focus on:

1. Empirical measurement of R(t), Δ̄(t), C_j(t) for major AI systems

2. Maintenance of architectural diversity through incentive structures (funding, access, evaluation)

3. Transparency in disagreement: making Suppressed(t) visible rather than hidden

4. Cognitive training: enabling judgment to process higher disagreement levels reliably

None of these follow from assuming AI systems are "aligned" or "unaligned." They follow from the model itself.

---

## Section 13: Limitations

1. For the systems this paper is most concerned with — closed frontier models — R(t) and Δ̄(t) are currently not directly measurable. I_j(t) requires deployment data not publicly available from major providers. Δ̄(t) requires either API-level access at scale or parameter access. This is not a minor limitation; it means the model's most important predictions cannot currently be tested on the most important systems. Application is presently restricted to open-weight models and systems with accessible deployment data.

2. The assumption of monotonic decay (λ > 0) may not hold in all regimes. Decentralised systems might maintain diversity without active intervention. λ is entirely unestimated empirically; the model's quantitative dynamics depend completely on it.

3. All four threshold values (R_min, Δ_min, ρ, Cap_max) are illustrative placeholders, not derived parameters. The model's conditions cannot be operationally evaluated until these are empirically calibrated. This is the primary limitation on immediate applicability.

4. Judgment capacity (Cap_max) is modeled as exogenous. Humans can train to handle more disagreement. The model does not address capacity improvement over time.

5. No treatment of feedback loops: if redundancy enables better decision-making, which then demands more diverse models, the decay assumption could be wrong in direction, not just magnitude.

6. The Fable 5 case (Section 0) rests on reporting that has not been independently verified at time of writing. The model does not depend on this case being accurate — the formal model stands independently — but the paper's framing uses it as the opening empirical motivation. Readers should treat Section 0 as a motivating case pending full documentation.

---

## Section 14: Conclusion

We have formalised a model of civilizational governance of distributed AI systems. The model has four central claims:

1. Redundancy (measured as Herfindahl index of query-weighted deployment share) must be maintained above threshold R_min
2. Disagreement between systems must be observable above a minimum level Δ_min
3. Economic cost of maintaining diversity must remain below tolerable fraction ρ
4. Cognitive capacity of judgment must not be exceeded (Cap_max)

Each claim is structurally operationalisable. The primary gap between the model and immediate empirical application is: threshold values R_min, Δ_min, ρ, and Cap_max require calibration before conditions can be evaluated quantitatively. Measurement infrastructure for closed frontier models does not yet exist. These are identified as the priority research agenda.

The model's qualitative predictions — that absent intervention R(t) → 0, that suppressed disagreement grows under convergence pressure, that cognitive limits bound useful diversity — do not depend on specific threshold values and are testable with currently available methods on open-weight models.

Future work should focus on:

1. Empirical measurement of I_j(t) and Δ̄(t) on open-weight model populations as a baseline
2. Controlled experiments on Cap_max in disagreement-integration contexts
3. Historical analysis of AI deployment concentration from 2020-2026 to estimate λ
4. Game-theoretic analysis of incentive structures that maintain vs. collapse diversity
5. Documentation of the Fable 5 case and equivalent events to establish the empirical basis for political capture claims

---

## Discussion

This framework is motivated by real events (Fable 5 case, June 2026) and makes structurally falsifiable predictions. The motivating case requires documentation before it can serve as formal evidence; the model itself does not depend on that documentation — it stands as a formal structure independent of the opening case.

It is not a normative argument for how the world should be. It is an analytical model of what conditions must hold if distributed AI governance is to remain viable under political pressure. Whether those conditions are currently being met is an empirical question the model provides tools to answer.

The primary honest statement about this paper's current status: the formal model is sound; the empirical calibration is absent; the motivating case is documented at the level of reportage, not primary source. This is a preprint. The invitation is to test the structure, calibrate the parameters, and document the cases.

Challenge the assumptions. Test the predictions. Build on the framework.

---

**Author:** Bundard
**Date:** June 28, 2026
**Version:** Preprint v1.1 — Category 1 revisions applied. Empirical calibration pending.
**License:** CC BY 4.0

---

## Footnote Sources Required

The following citations are marked in the text as [Source required]. The paper should not be submitted to peer review until these are resolved. For preprint release, they are flagged explicitly.

[^1]: Anthropic release announcement for Fable 5, June 9, 2026. URL or archived source required.
[^2]: Contemporaneous reporting on the suspension decision and alleged political intervention. If sourced from reportage, cite as "reported by [outlet], [date]" and acknowledge as alleged pending official confirmation.
[^3]: Documentation of competing model's continued operational approval and capability tier comparison. Benchmark comparison or official capability documentation required.
[^4]: Documentation of available or absent appeal/review process following the suspension. Official statement or absence of statement to be cited.

**Note to reviewers:** These footnotes are intentionally unfilled in this version. The paper's formal model (Sections 7-14) does not depend on them. The motivating case (Sections 0-5) does. Peer review should evaluate the formal model on its own terms; the motivating case is presented as a reported event requiring further documentation.