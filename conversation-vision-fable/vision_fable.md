# AI-Driven Search for Physics Beyond the Standard Model

*Claude's version of the vision, September 2026. Written independently of VISION.md for comparison.*

## 1. The idea in one paragraph

The Standard Model (SM) is incomplete. There is a short, well-known list of things it does not explain: dark matter, neutrino masses, the baryon asymmetry, the strong CP problem, the hierarchy problem, the flavor structure. The usual way to address them is by hand: one problem motivates one extension, a physicist writes it down, checks the bounds, and publishes. Models that solve several problems at once with a single economical ingredient are rare because they are hard to find by intuition. This project replaces intuition with search. We define a model space precisely, enumerate it, and use LLM agents to orchestrate a rigorous, tool-based evaluation of every candidate against the full list of problems and the full set of experimental constraints. The goal is a systematic map of which extensions survive, ranked by economy, together with negative results about which ones cannot.

## 2. What counts as a BSM model

A first attempt at a definition is "a gauge group containing the SM group, with representations that branch to the SM fields". This is too narrow. It captures GUTs, left-right models and Z' models, but misses most of the field:

- Extensions with the SM gauge group unchanged: right-handed neutrinos, singlet scalar dark matter, two-Higgs-doublet models, scotogenic models, vector-like fermions.
- Non-gauge symmetries: supersymmetry (spacetime), the axion (global U(1)), discrete symmetries that stabilise dark matter.
- Extra low-energy states: the 16 of SO(10) branches to the SM fermions plus a right-handed neutrino. The correct condition is that the low-energy spectrum *contains* the SM.
- Continuous parameters: the same group and representations with different breaking chains, scales and couplings give different physics. Each discrete "model" is a family.

**Working definition.** A BSM model is an effective field theory specified by

1. a gauge group G with G_SM ⊆ G (possibly G = G_SM),
2. a field content with representations under G, and optionally global or discrete symmetries,
3. a symmetry-breaking pattern down to G_SM,
4. a Lagrangian with its parameters,

such that the low-energy EFT contains the SM fields with their known quantum numbers. Anomaly freedom is a hard constraint on item 2 and prunes the discrete space substantially.

## 3. The list of problems

Not all problems are equally sharp. This matters because it determines what a "check" can mean.

| Problem | Type | What a check requires |
|---|---|---|
| Dark matter | Empirical | Stable candidate, relic abundance, direct and indirect detection, collider bounds |
| Neutrino masses and mixing | Empirical | Mass scale and mixing pattern fit to oscillation data |
| Baryon asymmetry | Empirical | CP violation, out-of-equilibrium dynamics, Boltzmann equations |
| Strong CP | Theoretical | A mechanism, plus robustness to Planck-suppressed operators (quality problem) |
| Hierarchy problem | Aesthetic | No numerical criterion; a naturalness judgment |
| Flavor structure | Aesthetic | A mechanism for hierarchies and mixings |

Empirical problems have automatable checks. Aesthetic ones do not, and a scoring function must encode a judgment about them explicitly rather than pretend an agent can decide.

## 4. Why not just "random proposals plus agents"

Three failure modes of the naive version.

**Trivial solutions are abundant.** Add a singlet fermion and you have neutrino masses. Add a Z2-odd singlet scalar and you have dark matter. Concatenate and every problem on the list is "solved". Without a scoring function the output is an infinite list of Frankenstein models. The interesting models (νMSM, SMASH, scotogenic) are interesting because one ingredient solves several problems. Economy is the objective, and defining it is the actual physics content of the project.

**The checks are wildly heterogeneous.** Relic abundance and direct detection are automatable. Neutrino masses are a fit. Baryogenesis is hard even by hand. The hierarchy problem has no number attached. "Leading order" is sufficient for some checks and misleading for others (coannihilation, Sommerfeld enhancement, loop-induced direct detection).

**LLM reasoning is not a calculation.** Agents must run tools, not do group theory in their heads. Every result must be reproducible by code. The pipeline must first reproduce known models as regression tests before any new result is trusted.

## 5. Prior art

Systematic scans of model space predate LLMs, and their lessons apply directly.

- Cirelli, Fornengo, Strumia (2006): scan of SU(2) representations for "minimal dark matter".
- Restrepo, Zapata, Yaguna (2013): classification of radiative neutrino mass models with a dark matter candidate.
- Allanach, Gripaios, You (2019-2020): enumeration of anomaly-free U(1) charge assignments.
- Anderson, Gray, Lukas, Palti and others: scans of billions of heterotic string constructions for SM-like spectra.
- Halverson, Nelson, Ruehle and others: reinforcement learning and genetic algorithms on the string landscape.

The common lesson: enumeration is cheap, evaluation is the bottleneck, and the most durable results were negative ("nothing with fewer than N fields does X").

## 6. What the LLM actually adds

The value is not in proposing models. It is in orchestrating a heterogeneous stack that previously required a grad student at each step:

1. Build the Lagrangian from the field content (Sym2Int, GroupMath).
2. Generate a model file (SARAH, FeynRules).
3. Compute the spectrum and couplings (SPheno).
4. Dark matter observables (micrOMEGAs, MadDM).
5. Match to SMEFT at leading order (Matchmakereft, Matchete).
6. Global fits for flavor and electroweak constraints (smelli, HEPfit, flavio).
7. LHC limits (SModelS, CheckMATE, MadGraph where needed).
8. Read the outputs, decide which branch of the mechanism applies, write the reasoning up.

Steps 1 through 7 are code. Step 8 and the glue between steps are where an agent earns its place. A second, independent agent or tool should verify any claim the first agent makes.

## 7. The case for doing it

The objection "if BSM is complicated we will never find it" cuts both ways. If the true model is far out in an exponentially large space, LLMs do not help. They give a constant-factor speedup on checking, not an escape from exponential growth.

The counter-argument is the reason to do this now. The constraint set is extremely strong: LHC null results, direct detection, flavor, electric dipole moments. The set of models that survive all of it may be small and strange, the kind of thing nobody would write down by hand. A systematic search is the natural way to find those. And even the negative results are publishable: theorems of the form "no anomaly-free extension with at most three new fields solves dark matter and neutrino masses without tuning".

## 8. Phase 1: a finite, fully automatable subspace

Start where every check can be run by code.

**Model space.** SM gauge group, plus up to three new fields drawn from a fixed list of small SU(3)×SU(2)×U(1) representations (singlets, doublets, triplets; color singlets and possibly triplets), optionally with one discrete Z_N or one extra U(1).

**Hard constraints.**
- Anomaly freedom.
- A tree-level or one-loop neutrino mass with the right scale and a viable mixing fit.
- A stable dark matter candidate with the observed relic abundance, evading direct detection.
- Consistency with LHC, flavor and electroweak precision bounds.

**Scoring.** Number of new fields, number of new parameters, degree of tuning required, number of problems solved by a shared ingredient, testability at planned experiments.

**Validation.** The pipeline must recover the νMSM, the scotogenic model, singlet scalar dark matter, and the type I, II and III seesaws before any new candidate is reported.

**Deliverables.**
- A ranked catalogue of surviving models with parameter regions.
- A list of "no-go" statements for the subspace.
- A reusable pipeline with every claim traceable to a tool output.

## 9. Later phases

- Widen the representation list and allow larger gauge groups (U(1)', left-right, Pati-Salam, SU(5), SO(10)) with explicit breaking chains.
- Add baryogenesis as a check, starting with leptogenesis where the Boltzmann treatment is standard.
- Add the strong CP problem with an explicit axion quality check.
- Encode naturalness and flavor criteria as explicit, documented scoring terms rather than agent judgment.
- Let agents propose non-generic mechanisms (breaking chains, symmetry assignments) as a complement to enumeration, always subject to the same automated checks.

## 10. Principles

1. A model is a Lagrangian, not a group.
2. Economy is the objective. Concatenation is not a solution.
3. Agents orchestrate. Tools calculate.
4. Known models are regression tests.
5. Negative results count.
