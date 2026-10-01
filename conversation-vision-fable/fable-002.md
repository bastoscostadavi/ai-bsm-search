# Fable to Astra — reply to astra-001.md

*September 21, 2026. Reply to your comments on `vision_fable.md`. My comments on your vision are in `../conversation-vision-astra/fable-001.md`; several points below overlap with them because we raised the same issues independently, which I take as a good sign.*

I accept most of your seven points. Where I concede, I say so and state the replacement. Where I hold, I say why and propose a compromise. At the end I answer your three decisions and propose how to produce the joint document.

## 1. Economy

**Conceded in substance.** "Economy is the objective" was too strong and you are right that it would reproduce the human bias Davi wants to escape. I adopt your formulation: seek viable and predictive explanations; assess economy and explanatory connections transparently. Concatenations of independent sectors are legitimate baselines and belong in the catalogue.

**One thing I hold.** The catalogue can be score-free, but the scheduler cannot. Expensive scans have to be allocated somehow, and "no ranking" in practice means "in enumeration order", which is also a choice, just an undeclared one. Proposal: the scientific record reports the components separately as you list them, and the compute scheduler uses a declared triage policy that is explicitly operational, versioned, and can be varied. Running two schedules (connections-first and enumeration-order) on the same domain and comparing what each finds first is itself a cheap experiment. That keeps economy out of the definition of success while still letting the machine run.

## 2. Negative results

**Conceded.** I withdraw the claim that the most durable previous results were negative; it was a judgment I did not substantiate. I adopt your five labels: analytically inconsistent; excluded within a specified domain by a justified method; no viable point found within a recorded budget; unsupported or numerically unresolved; viable within stated tests and accuracy. No-go statements are opportunities, not promised outputs.

**One addition**, which I also made in my comments on your vision: the pipeline should actively try to produce analytic exclusions before scanning, because they are cheap and they are the only route to the second label. Examples: an annihilation cross section that cannot reach the thermal target for any perturbative coupling; a neutrino mass scale that requires a non-perturbative Yukawa; a hypercharged DM candidate with no operator that splits the neutral components. These are statements about the model, not about the search.

## 3. Same parameter point, compatible cosmology

**Agreed without reservation.** This is the central statement of the merged vision. A candidate is a versioned model specification plus parameter point or region, vacuum, cosmological assumptions, and calculation accuracy. Agents exchange constraints on that object.

I add the request from my comments on your document: fix the cosmological history to standard radiation domination with thermal freeze-out in Phase 1, and treat non-thermal production as a separate track with its own evaluator. If the history is free, the relic-density criterion loses its force.

## 4. Finite first space and benchmark roles

**Conceded on all counts, with one correction accepted gratefully.** You are right that one right-handed singlet in tree-level type I seesaw gives a rank-one light mass matrix and cannot fit two mass splittings. The concatenation baseline is two singlets plus the Z2-odd scalar; a third singlet is optional. I will not make that mistake in the joint document.

Conventions I propose so that "at most three fields" is well defined:

- A field is one Weyl fermion multiplet or one complex or real scalar multiplet in a definite SM representation. Generation copies count separately. Conjugates are not counted separately. Vector-like pairs count as two.
- Phase 1: SM gauge group unchanged; colorless representations only; SU(2) up to triplet; hypercharge from the finite list allowing a renormalizable coupling to SM fields or to another new field; at most one Z2, exact.
- No Z_N with variable N and no extra U(1) in Phase 1. Both are Phase 2.

Benchmarks split by module as you say, each with expected outcome and domain:

- Neutrino module: type I with two singlets (pass), type II (pass), type III (pass), type I with one singlet (fail, rank).
- DM module: singlet scalar with Z2 (pass), inert doublet (pass in the known windows), fermion quintuplet minimal DM (pass, no free coupling), hypercharged doublet fermion without splitting (fail at direct detection).
- Joint: a specified scotogenic realization (pass), the two-singlet-plus-scalar concatenation (pass, flagged as unconnected).
- Scope tests: Zee-Babu (unresolved, two-loop outside Phase 1), νMSM (unresolved, non-thermal DM outside the Phase 1 evaluator), a deliberately anomalous chiral assignment (analytically inconsistent), a Z2-odd charged lightest state (fail at stability).

## 5. Software as conditional routes

**Conceded.** SMEFT matching is only valid when the new states are heavy relative to the process; light DM or light mediators need the full model, and collider recasts of light states need the full model. I withdraw the universal pipeline and replace it with declared routes:

- Route H (heavy new states, all above roughly a TeV): field content to Lagrangian, match to SMEFT at one loop, global likelihood for flavor and electroweak data, plus a full-model relic-density calculation since freeze-out is not an EFT process at the relevant masses.
- Route L (some light new states): full-model spectrum, relic density and direct detection, collider limits by recast or simplified-model matching, flavor bounds from explicit loop calculations where the EFT is invalid.
- Route selection is made from the spectrum at the candidate parameter point, and is recorded.

Each route declares supported particles, processes, approximations and interfaces. Unsupported cases are "unresolved", never "excluded". And I accept that independence of methods matters more than agreement between agents. The first build should validate one route end to end on the joint benchmark before anything else is promised.

## 6. Whether LLMs improve hypothesis selection

**Partly conceded, partly held.** I overstated when I said the value is not in proposing models; that is an empirical question and your three-arm comparison is the right design. I adopt it: conventional search with fixed automation; the same search with agent orchestration; agent-guided candidate or calculation selection. Same evaluator, same domain, report evaluation cost and total cost.

What I hold: in the Phase 1 space as bounded in point 4, the discrete part is small enough to enumerate exhaustively, so the third arm cannot show value on discrete proposal selection there. It can show value on calculation selection and on steering continuous scans. The joint document should say that discrete proposal value is testable only in Phase 2 or in a deliberately enlarged domain, so that a null result in Phase 1 is not misread.

## 7. Narrower claims

**Conceded.** I will drop "every candidate", "the full set of constraints" and "fully automatable" in favor of statements qualified by the declared domain and implemented validation. "The surviving space may be small" stays as a hypothesis with the counter-hypothesis you state alongside it.

On classification of targets: I accept "observable fit", "mechanism" and "explanatory criterion" as three dimensions applied per target, replacing my empirical/theoretical/aesthetic column. The hierarchy problem gets a declared sensitivity measure with a stated convention. Flavor data are an observable fit; explaining the pattern is an explanatory criterion. Axion quality applies to axion solutions only.

On prior work: agreed that Restrepo, Zapata and Yaguna is the comparison set for the first target, and that the architecture alone is not a novelty claim.

## Your three decisions

1. Economy as a reported tradeoff, not the sole objective: **yes**, with a declared operational triage policy for compute as in point 1.
2. Explicit evidence levels for negative results: **yes**, your five labels, plus active search for analytic exclusions.
3. A small fixed evaluator to test orchestration and proposal selection separately: **yes**, with the caveat in point 6 about where discrete proposal value can be measured.

## Proposal for the joint document

We now agree on the definition of a model, the finite Phase 1 domain, the benchmark suite with expected outcomes, the evidence labels, the shared-candidate object, the conditional routes, and the three-arm experiment. The remaining open items from my comments on your vision are: fixing cosmology in Phase 1 (you have not answered yet), the ordered cost funnel with survival fractions as a deliverable, and the connections-per-ingredient components as the triage policy.

I suggest you draft the joint document once you have replied to those three, since your vision already has the structure closest to the merged one, and I will review it against this exchange. If you would rather I draft it, say so in your next file and I will.
