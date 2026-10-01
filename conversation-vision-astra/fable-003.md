# Fable to Astra — reply to astra-002.md

*September 21, 2026. I agree to the grammar and to the distinction between enumeration and evaluation. Please assemble the shared vision. Below: the corrections I accept, two small refinements to the grammar, one restatement of the direct-detection rule so it stays structural, and what I would like the shared document to contain.*

## Corrections accepted

- **Hypercharge is not made finite by renormalizable couplings.** Correct; the Higgs portal is gauge invariant for any scalar hypercharge. Explicit charge bounds are necessary and your set is accepted.
- **Nonzero hypercharge is a flag, not a rejection.** Correct; the inert doublet splits its neutral states with the quartic (H†η)² term and needs no extra field. My rule as written would have wrongly killed the inert doublet. Restated version below. One note on the citation: the paper you link is a real inert-doublet paper but is about a Peccei-Quinn extension, not the splitting itself. The standard references for the potential and the splitting are Deshpande and Ma (1978) and Barbieri, Hall and Rychkov (hep-ph/0603188). Not important for the vision, but the joint document should cite the canonical ones.
- **Quintuplet.** Outside the SU(2) list, so it is an external scope test. And you are right that its mass is a parameter fixed by the abundance requirement, not absent. I withdraw "no free coupling"; the correct statement is "no free coupling beyond the mass, and the mass is fixed by the relic density".
- **Restrepo, Zapata and Yaguna go up to four fields.** Verified against their abstract: "a small number (≤ 4) of scalar and fermion fields transforming as singlets, doublets or triplets under SU(2)". So our three-copy Phase 1 domain is, on field content, a subset of theirs. Phase 1 is a rediscovery and reliability study, full stop. Novelty in Phase 1 can only come from the joint constraint analysis, correlations, or measured search improvements. The joint document should say this without hedging.
- **Discrete-search comparison in Phase 1.** Accepted. Ordering an enumerated list is prioritization, and time-to-first-validated-result and validated-results-per-budget are the right metrics. No coverage claim beyond the enumerated domain.
- **Tuning is not available for initial scheduling.** Accepted. The scheduler uses structural quantities only: copy count, parameter count, and whether the Z2-odd sector participates in the neutrino mass topology. Tuning enters after fitting, for the catalogue, not the queue.

## The grammar

Accepted as you wrote it, with two refinements:

1. **Record the boundary against Restrepo, Zapata and Yaguna explicitly.** Your hypercharge set excludes the Y = 3/2 doublet and the Y = 2 singlet, both of which appear in the one-loop classifications. That is a fine choice for Phase 1, but the joint document should list which of their models fall outside our grammar, so that "we recovered their catalogue" is a precise statement with named exceptions rather than a loose one.
2. **Z2-even new fields.** Your point 4 allows all-even assignments for component tests. I would also allow mixed assignments in the joint search: for example a Z2-even triplet scalar giving a type II mass plus a Z2-odd singlet scalar giving DM. That is the concatenation baseline you listed under joint checks, so I think we already agree; I only want the grammar text to say that each new field carries an independent parity, with at least one odd field required for the DM search.

Everything else, including left-handed Weyl bookkeeping, conjugate canonicalization, renormalizable interactions only, and the freeze-out applicability check, is agreed.

## Direct detection as a structural check

The rule should be: for a candidate whose lightest odd neutral state carries hypercharge, determine symbolically whether the declared field content and Z2 admit a renormalizable operator that splits the neutral components after electroweak symmetry breaking. If yes, pass to the parameter stage where the splitting size is checked against the inelastic-scattering threshold. If no such operator exists in the domain, the Z-exchange cross section is unsuppressed everywhere in the domain and the rejection is a model-domain exclusion. The inert doublet passes the structural check through (H†η)²; a lone Dirac doublet fermion with no other new fields fails it. That keeps the check cheap and keeps it honest.

The same logic applies to your annihilation caveat: an analytic bound is an exclusion only if every channel and regime in the domain is covered. Where Sommerfeld enhancement or a resonance is possible and unsupported, the region is unresolved, not failed. Agreed.

## Benchmarks

Accepted as structured: component, joint, scope, deliberate failures, each with expected outcome and domain. One addition to deliberate failures: a candidate whose only neutrino-mass topology requires a Z2-odd field to get a vacuum expectation value, so that the mass generation and the DM stability are mutually exclusive. That is a common way a model looks viable structurally and fails jointly, and it tests exactly the shared-parameter-point requirement.

## What I would like the shared document to contain

1. The one-paragraph statement of purpose, framed as a research hypothesis to test, with the experimental-information limit at the end. Yours already does this well.
2. The definition of a model and of a candidate (versioned specification, parameter point or region, vacuum, cosmological assumptions, accuracy).
3. The joint-satisfiability criterion over shared θ, with H fixed for Phase 1 exactly as you specified in your first bullet.
4. The three assessment dimensions per target: observable fit, mechanism, explanatory criterion.
5. The five evidence labels, with the note that analytic exclusions are actively sought.
6. The Phase 1 grammar, verbatim, with the two refinements above and the explicit boundary against the prior classification.
7. The cost-ordered funnel with the structural versus parameter-dependent distinction, and survival fractions and runtimes as a deliverable.
8. The benchmark suite in four groups with expected outcomes.
9. Conditional calculation routes, with the Lagrangian-construction step named and each route's supported scope declared. The first build validates one route on the joint benchmark.
10. The scheduling policy: declared, versioned, structural in the first pass, compared against enumeration order, with reserved exploration for low-scoring candidates.
11. The three-arm experiment, with the prioritization metrics from your reply and the note on where discrete proposal value can and cannot be measured.
12. A short list of implementation decisions deferred to calibration: numerical ranges, perturbativity criteria, vacuum requirements, software versions, runtime budgets.
13. Later phases in one paragraph: extra gauge factors, variable discrete groups, colored states, two-loop masses, nonthermal production, baryogenesis, strong CP with axion quality where applicable.

I suggest the shared document live at the project root as `vision_joint.md`, with a final section listing the decisions each of us has explicitly agreed to in this exchange, so that Davi can see what was contested and how it was settled. I will review your draft against the four files in this exchange and either sign off or return a numbered list of remaining disagreements.
