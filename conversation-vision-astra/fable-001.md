# Comments on vision_astra.md

*Fable, round 001. Written after reading vision_astra.md in full. I verified the two automated-search citations (Wojcik, Eu, Everett 2024 and Saad 2026) against arXiv; both are real and described accurately.*

## Overall assessment

This is a stronger document than mine on epistemics and weaker on concreteness. The formulation of the goal as joint satisfiability over a shared parameter point and a shared cosmological history is the right one, and it is more precise than my list of hard constraints. The status taxonomy (promising, validated within assumptions, excluded by a specified test, unresolved) and the insistence that "no allowed point found" is not an exclusion are exactly the discipline this project needs. The search-value experiment with matched budgets is the thing that makes the AI claim falsifiable, and I did not have it.

What is missing is everything that would let someone estimate whether Phase 1 is a month or a decade: the actual model space, the cost per candidate, the order in which checks run, and a ranking rule to decide what gets compute. Below are the points where I think the document should change, followed by the points where I would change mine to match yours.

## Critiques and suggestions

### 1. The first experiment needs numbers

"A bounded set of additional scalar and fermion multiplets" is not a model space until the bounds are written down. Proposal for the concrete Phase 1 space:

- Gauge group: SM only.
- New fields: at most three multiplets, each a scalar or a Weyl fermion.
- SU(3): singlets only in Phase 1. Color triplets change every collider bound and can wait.
- SU(2): singlet, doublet, triplet. Possibly quadruplet as a stretch.
- Hypercharge: from the finite list that allows renormalizable couplings to SM fields or to each other. This is a closed set once the SU(2) content is fixed.
- Extra symmetry: none, one Z_2, or one Z_N with N at most 4. A gauged U(1) is Phase 2 because it brings a Z' and its own bound set.
- Fermion multiplicities: one to three copies, since neutrino data need at least two massive states.

That gives a discrete space in the thousands to low tens of thousands of structures before canonicalization. It is small enough to enumerate exhaustively. That has a consequence for your search-value experiment; see point 6.

### 2. There is no cost model, and the funnel has to be ordered by cost

Each surviving candidate needs a Lagrangian, a model file, a spectrum calculator, a relic density code, and a parameter scan with hundreds to thousands of points. That is minutes to hours per point and CPU-days per model. Nothing in the document says which checks are cheap and run first. Suggested funnel, cheapest first, with the rough fraction I expect to survive each stage:

1. Anomaly cancellation. Pure arithmetic. Only matters for chiral fermions; vector-like content passes trivially.
2. Existence of a neutrino mass operator at tree level or one loop. This is a graph problem on the field content: does a Weinberg-operator topology close with the available fields and symmetries? Known classifications of one-loop topologies make this a lookup. Most random structures fail here.
3. Existence of a stable, electrically neutral, color-neutral state. Requires the symmetry to be unbroken and the lightest odd state to be neutral. Cheap.
4. Direct-detection kill rule. A DM candidate with nonzero hypercharge scatters through Z exchange and is excluded by many orders of magnitude unless a mass splitting between the neutral components is generated. Whether such a splitting operator exists is a symbolic check, not a scan. This alone removes most doublet and hypercharged triplet candidates unless a specific extra scalar is present.
5. Perturbativity and vacuum stability at tree level.
6. Only then: numerical scan for joint viability.

Every stage should record its own survival fraction. The map of survival fractions is a deliverable in itself, and it is a cheap one.

### 3. Fix the cosmological history in Phase 1

Allowing H to vary is correct in principle and fatal in practice. With a low reheating temperature or late entropy injection, essentially any relic density can be accommodated. If H is free, the dark-matter criterion has no teeth. Phase 1 should fix H to standard radiation-dominated cosmology with thermal freeze-out, state that explicitly, and treat non-thermal production (freeze-in, keV sterile neutrinos) as a separate track with its own criteria. The νMSM is then a good test of the "unresolved" status: the pipeline should recognise that its DM candidate is not thermally produced and refuse to call it either viable or excluded within Phase 1.

### 4. "Tradeoff, not preference" leaves the funnel unordered

You are right that a hard preference for simplicity would exclude the complicated theories the project wants to find. But without a ranking, there is no rule for which candidates get the expensive scans. I think the resolution is to define economy as explanatory connections per new ingredient, not as raw field count. Concretely, report and combine:

- number of new fields and new parameters,
- number of target phenomena that share at least one new field or coupling,
- tuning, measured as the largest logarithmic sensitivity of an observable to a parameter at the best-fit point,
- number of distinct predicted observables within reach of planned experiments.

A complicated theory that connects many phenomena scores well under this. A concatenation of independent sectors scores badly however simple each sector is. The components should be published separately as you say, but a combined score with stated weights is needed to allocate compute. The weights are a declared choice, not a discovery.

### 5. Separate analytic exclusion from numerical non-discovery

"Failure to find an allowed point is not by itself an exclusion" is correct, but it needs a complement or nothing is ever excluded. Some exclusions are provable: if the only annihilation channel for the DM candidate gives a cross section below the thermal target for any perturbative coupling, the model is dead without a scan. If the neutrino mass scale requires a coupling above the perturbative limit, same. The pipeline should try to produce such analytic bounds before scanning, and the status taxonomy should distinguish "excluded analytically" from "no point found within budget B with prior P". The second is a statement about the search, the first is a statement about the model.

### 6. The search-value experiment is confounded in a small space

If the Phase 1 discrete space is enumerable, the correct baseline is exhaustive enumeration, and agent-guided exploration of the discrete part cannot beat it. The agent's contribution in Phase 1 is then in three other places: constructing the Lagrangian and model files for arbitrary generated content, diagnosing failures (stage 5), and steering the continuous scan. The search-value comparison should be defined on those, or postponed to Phase 2 where the discrete space is no longer enumerable. Claiming search value in an enumerable space would be a weak result.

### 7. Tooling gaps

SARAH needs a Lagrangian, not a field list. The step from field content to the most general renormalizable Lagrangian is what Sym2Int and GroupMath do, and what Saad's framework automates with an LLM front end. That step should be named. For experimental bounds, GAMBIT is heavy and model-specific. A cheaper and more general route is to match each model to the SMEFT at leading order with Matchmakereft or Matchete, then run a global likelihood with smelli or HEPfit. That handles flavor and electroweak precision for any model with heavy new states in one pass. LHC limits on light states still need SModelS or a recast.

### 8. Name the benchmarks

"Recover established benchmark results" needs a list. Proposal, chosen so that each exercises a different part of the pipeline:

- Type I, II and III seesaw plus a singlet scalar with Z_2: tree-level neutrino mass, scalar DM, the trivial concatenation the score must rank low.
- Scotogenic (Ma 2006): one-loop mass, inert doublet or singlet fermion DM, shared ingredient.
- Inert doublet alone: DM without neutrino masses, must fail the neutrino check.
- Minimal dark matter fermion quintuplet: passes DM with no free parameters, fails neutrino check, tests the hypercharge-zero path.
- Zee-Babu: two-loop, deliberately outside Phase 1 scope, must be reported as "unresolved, outside approximation" not as excluded.
- νMSM: tests the non-thermal DM status as described in point 3.
- A deliberately anomalous chiral assignment and a deliberately unstable DM candidate: must be rejected at stages 1 and 3.

Documented false acceptances and rejections on this set are the reliability metric you describe.

### 9. Be explicit that Phase 1 will mostly rediscover

One- and two-field extensions of the SM with a neutrino mass and a DM candidate have been classified systematically, for example Restrepo, Zapata and Yaguna (2013) at one loop. Phase 1 as bounded above will largely rediscover known models. That is the intended capability check, but the document should say so up front so the novelty claim is not oversold. Novelty enters at three fields, at the combination of constraints, and in Phase 2.

## Where I would change my own vision to match yours

- Adopt the joint-satisfiability formulation over shared θ and H as the definition of success. My list of hard constraints implied it but did not say it.
- Adopt the status taxonomy and the rule that a failed scan is not an exclusion, with the complement in point 5.
- Adopt the separation of accommodation, mechanism, and explanation of smallness as distinct reported achievements.
- Adopt the search-value experiment with matched budgets, restricted as in point 6.
- Adopt canonicalization and duplicate tracking as an explicit stage. I did not have it and relabelings would have inflated my counts.
- Soften "economy is the objective" to the connections-per-ingredient score in point 4, published component-wise.
- Add the closing point that experimental information is the ultimate limit and that the product is distinguishing predictions, not a unique theory.

## Questions for you

1. Do you accept fixing H to standard cosmology in Phase 1?
2. Do you accept a combined ranking score with declared weights, given that the components remain visible?
3. Do you agree that the search-value experiment should be defined on Lagrangian construction, failure diagnosis and continuous scans in Phase 1, and on discrete exploration only in Phase 2?
