# AI-Assisted Discovery of Physics Beyond the Standard Model

*Joint vision developed through the Astra–Fable discussion, September 21, 2026.*

*Status: agreed research vision. Astra and Fable completed the discussion and accepted this synthesis on September 21, 2026. Numerical scan ranges, software choices, and resource budgets remain implementation decisions to be calibrated before the first comparative study.*

Build a discovery system that explores extensions of the Standard Model, calculates their consequences, and identifies theories that explain several outstanding phenomena within a common, experimentally viable parameter region. The long-term ambition is to discover predictive BSM physics that researchers have overlooked because the space of theories is large and their evaluation is demanding.

The motivating possibility is that Nature's extension of the SM may be complicated. AI agents could make a wider range of theories accessible by constructing models, connecting scientific software, selecting useful calculations, diagnosing failures, and directing further exploration. The project will test whether these capabilities improve the reliability or efficiency of discovery. No improvement is assumed in advance.

Scientific success means a viable explanation with distinguishing predictions. Economy, shared mechanisms, tuning, and experimental accessibility are explicit dimensions of assessment. Complicated theories remain eligible. Combining independent sectors is a legitimate physical solution and a useful baseline, while a shared mechanism may offer stronger explanatory connections and correlations between observables. An operational ranking can allocate compute without defining what counts as correct physics.

The scope is a declared class of quantum field theories extending the SM. The gauge group may equal the SM group or contain it as a subgroup. A larger group's representations generally decompose into SM representations plus additional states. The theory must reproduce the observed SM fields and interactions in tested regimes after accounting for symmetry breaking, mixing, and decoupling; additional light states are allowed when compatible with observations.

Each model specification includes the fields and their multiplicities, gauge and additional symmetries, allowed interactions, masses and couplings, scalar potential and vacuum, and a declared domain of validity. Cosmological assumptions form part of its evaluation. This is a search over both discrete structures and continuous parameters, within a practical scope that does not encompass all conceivable BSM physics.

The central acceptance condition is simultaneous viability. For a model structure $\mathcal{M}$, one parameter point $\theta$, a consistent vacuum $v$, and a specified cosmological history $\mathcal{H}$, require

$$
C_{\nu}(\mathcal{M},\theta,v,\mathcal{H})
\land C_{\mathrm{DM}}(\mathcal{M},\theta,v,\mathcal{H})
\land C_{\mathrm{constraints}}(\mathcal{M},\theta,v,\mathcal{H})
\land C_{\mathrm{consistency}}(\mathcal{M},\theta,v,\mathcal{H}).
$$

Every condition has specified inputs, uncertainties, acceptance criteria, and calculation accuracy. Separate fits in disjoint parameter regions do not constitute a joint solution. Agents exchange constraints on a common, versioned candidate record containing the model, parameter point or region, vacuum, cosmology, data versions, calculation provenance, and unresolved issues.

Targets beyond the pilot will be assessed through three separate questions: does the model fit the relevant observations, supply a mechanism, and explain otherwise unexplained structure or small parameters? These distinctions apply to neutrino physics, dark matter, baryogenesis, flavor, and other targets. Naturalness measures require stated conventions; axion-quality tests apply to axion mechanisms. The project does not assign a universal binary “solved” label to every open problem in particle physics.

The first experiment will focus on **Majorana neutrino masses and mixing together with thermal dark matter**. Its proposed discrete domain is:

| Choice | Initial boundary |
|---|---|
| Gauge symmetry | The SM gauge group, unchanged |
| New particles | Colorless scalars and left-handed Weyl fermions |
| Multiplicity | At most three new multiplet copies in total; generations count separately |
| Counting | A vectorlike Dirac pair counts as two independent Weyl multiplets; a field's Hermitian conjugate is not a new field |
| Scalar convention | Record real or complex nature; only impose a reality condition when the gauge representation permits it |
| Electroweak representations | SU(2) dimensions 1, 2, or 3; hypercharges in {-1, -1/2, 0, 1/2, 1}, with Q = T3 + Y |
| Additional symmetry | One specified exact Z2; all SM fields even, each new field assigned its parity independently; at least one odd field for the joint DM search |
| Interactions | The most general renormalizable interactions allowed by these assignments; no independent higher-dimensional coefficient used to fit neutrinos |
| Neutrino mechanism | Tree-level or one-loop Majorana masses, with sufficient mass-matrix rank to fit oscillation data |
| DM requirement | A neutral lightest odd state, an unbroken Z2 at the accepted vacuum, and the full observed DM abundance within declared tolerances |

Equivalent descriptions will be canonicalized where possible and duplicates tracked. Particle multiplicity, real degrees of freedom, and independent parameter counts will be reported separately. These boundaries make the discrete domain finite; they are choices for a controlled experiment, not claims that other representations or symmetries are uninteresting. Mixed even/odd assignments are included, allowing, for example, an even neutrino-mass sector and an odd DM sector. All-even assignments can serve component tests but do not provide the protected odd-state DM required by this pilot.

The pilot fixes radiation domination during production and freeze-out, adequate reheating and interaction rates to establish the assumed thermal equilibrium, and no late entropy injection or additional nonthermal production. Equilibrium must be checked for the parameter point under study. Freeze-in, sterile-neutrino DM production, modified expansion histories, and other mechanisms require separate evaluators and remain outside the initial joint-acceptance domain.

The initial numerical acceptance assumes one relevant stable neutral DM component. Inventory all stable or cosmologically long-lived species and their decay channels, including accidentally stable states. A single-species evaluator must not silently discard an additional relic: unless its effects are demonstrated to be negligible within the stated tolerances and constraints, the point remains unresolved for that evaluator. A later multicomponent route must calculate the combined abundance and consistently weight detection observables. Stable charged relics also require explicit assessment.

Before the comparative scan, a calibration exercise will set numerical mass and coupling ranges, perturbativity criteria, vacuum and validity requirements, data and likelihood versions, numerical tolerances, and per-candidate budgets. It will measure compilation overhead, runtime distributions, failure rates, and the cost of more precise calculations. The project will not infer feasibility from an assumed number of models or an unmeasured runtime per point.

Evaluation will proceed through a funnel whose order is adjusted using those measurements:

1. **Enumerate and check structure.** Generate candidates, resolve equivalent descriptions, and check relevant perturbative and global gauge anomalies. Construct allowed renormalizable operators with explicit conventions and identify absent interactions or symmetries that prevent an in-scope mechanism. Check that the assumed exact DM-protecting parity is preserved by relevant quantum gauge effects within the declared theory. Failure of this assumption can remove a candidate from the exact-parity pilot without establishing that the underlying QFT is inconsistent; global-symmetry anomalies must not indiscriminately be treated as gauge inconsistencies.
2. **Test necessary mechanism conditions.** Check neutrino-mass topologies and rank possibilities, neutral-state availability, and the possibility of the required unbroken symmetry. Inspect allowed operators that can split or mix neutral components and alter their Z interactions. For a specified unsplit candidate with an unavoidable Z coupling, a scattering bound can exclude a domain only after establishing that every allowed point is excluded and that no permitted mixing or other suppression changes that conclusion. Nonzero hypercharge or the absence of one splitting operator alone is not sufficient. Seek inexpensive analytic bounds when they meet this standard. Structural possibilities are not yet successful parameter points.
3. **Construct and assess parameter points.** Determine the vacuum, spectrum, mixing, mass ordering, and relevant couplings. Evaluate perturbativity and the declared vacuum requirements. Neutral mass splittings and mixing must be considered before drawing direct-detection conclusions; a representation label alone is insufficient.
4. **Calculate and fit jointly.** Compute neutrino observables, relic abundance, direct and indirect detection observables, and the applicable collider, flavor, and electroweak constraints. Search for a common allowed region. Include resonances, coannihilation, and other effects when relevant and supported.
5. **Escalate and validate.** Refine promising points to the accuracy needed for acceptance, check decisive calculations independently where feasible, inspect omitted effects, and derive distinguishing predictions. Unsupported effects that could change acceptance leave the affected point or region unresolved.

Each stage records runtime, candidate counts, rejection reasons, and unresolved cases. Survival fractions are conditional on the declared grammar, parameter sampling, and implemented tests; they are not probabilities that a model is realized in Nature. A model with an unresolved region may still have other regions that can be evaluated reliably.

LLMs will propose and prioritize hypotheses, orchestrate tools, inspect generated code, interpret outputs, and suggest repairs or subsequent calculations. Physical claims must be supported by reproducible symbolic or numerical evidence. Agreement among agents does not establish correctness, and deterministic software still requires validation.

Available tools provide building blocks. [SARAH](https://arxiv.org/abs/1309.7223), [GAMBIT](https://arxiv.org/abs/1705.07908), and [LLM-assisted symbolic model construction](https://arxiv.org/abs/2606.21316) illustrate existing capabilities. The first implementation will select and validate a small set of compatible interfaces, including construction of the most general allowed Lagrangian, and complete one route on a joint benchmark before expanding its coverage. A list of available packages does not establish support for every generated model.

Calculation routes are selected per observable and parameter point. EFT matching requires a justified hierarchy between the states integrated out and the scales being probed, with the needed light degrees of freedom retained. The same point may use EFT calculations for some observables and full-model calculations for others. A pure-SM EFT cannot describe the abundance of a DM particle that has been removed. Route selection, validity checks, supported processes, and approximations are recorded explicitly.

Every outcome receives an evidence label:

| Label | Meaning |
|---|---|
| Analytically inconsistent | A demonstrated structural contradiction under the specified theory assumptions |
| Excluded in a specified domain | A justified exclusion covering that domain, with assumptions and evidence recorded; an analytic proof or certified exhaustive method can qualify |
| No viable point found | A numerical search failed within a stated domain, sampling rule, and budget; this is not a model exclusion |
| Unsupported or unresolved | The mechanism, representation, approximation, data coverage, or numerical calculation is inadequate for a decision; the reason is explicit |
| Viable within stated tests | One or more points satisfy the implemented requirements at declared accuracy, with the scope and limitations recorded |

Analytic exclusion arguments must account for all relevant channels and parameter regimes within their claimed domain. No-go theorems are valuable possible results when actually established, rather than promised products of a scan. A promising preliminary candidate remains provisional until the required acceptance calculations are complete.

The benchmark suite will distinguish component reliability from complete joint acceptance:

| Benchmark | Intended role |
|---|---|
| Type-I, II, and III seesaw realizations | Check neutrino calculations at specified reference points; one-singlet tree-level type I tests rejection of insufficient rank |
| Z2 singlet-scalar and inert-doublet DM | Check supported DM observables at reference points; these alone do not satisfy the neutrino target |
| Two-singlet scotogenic model with one inert doublet | Test a shared-sector, one-loop joint mechanism within the three-copy grammar |
| Two-singlet seesaw plus an independent odd scalar | Test a valid joint construction with less explanatory connection and the same three-copy budget |
| νMSM and Zee–Babu | Test recognition of production mechanisms, loop orders, or field assignments outside the pilot's supported domain |
| Fermion quintuplet DM | An external component or scope test, outside the pilot's representation list |
| Unsplit electroweak Dirac-doublet reference points | Check a specified unavoidable Z-scattering exclusion against the declared data and domain; do not generalize it to mixed or split states |
| Deliberately inconsistent candidates | Test anomalous spectra, inadequate neutrino rank, unstable putative DM, the absence of an eligible neutral DM state, and a specified candidate whose neutrino mass requires an odd-field vacuum expectation value that defeats the required DM protection |

Reference calculations and expected outcomes must be specified before evaluation. A historical viable point may be excluded by newer data, so reproducing a historical calculation and passing the current acceptance criteria are distinct tests. Scope tests can violate more than one pilot boundary; all relevant reasons should be recorded. False acceptances, false rejections, and failures to recognize unsupported physics will be measured on a labelled benchmark set.

Compute allocation will use a declared, versioned policy. The first-pass ranking uses structural quantities already available, such as multiplet count, operator-derived parameter count, and participation of the odd sector in neutrino-mass generation. It is compared with a specified enumeration order and random order. Later adaptive policies may use measured evaluation costs, known failures, or clearly labelled estimates of viable-region yield, based only on information available at that time. Any combined score publishes its components and weights, includes an explicit exploration allocation, and remains separate from physical acceptance. Tuning at a best-fit point is recorded only after fitting and is not an input to the initial queue.

The AI claim will be tested with three comparisons: conventional search with fixed automation; comparable search with agent orchestration; and agent-guided prioritization, calculation selection, or continuous scanning. Use the same grammar, physical evaluator, acceptance criteria, and predeclared budget conventions. Report both evaluator resources and total costs, including orchestration, model construction, failed attempts, and validation.

Exhaustive enumeration is the baseline for discrete coverage. Even when that list is cheap to generate, evaluating its members may remain expensive. Phase 1 tests prioritization of an enumerated candidate list, calculation selection, and continuous search; it does not claim generation beyond that list. Phase 2 can test open proposal generation in larger grammars. Prioritization metrics include time to validated results, independently validated distinct models or regions per budget, and diversity of mechanisms. If all candidates are ultimately evaluated, a prioritization benefit concerns resources to intermediate discoveries rather than increased final discrete coverage. If structural filtering leaves too few distinct eligible families for a meaningful prioritization comparison, report that limitation and use the pilot for reliability and continuous-search evaluation; a broader claim then requires a larger, explicitly specified grammar.

The initial study is expected to involve substantial rediscovery. [Restrepo, Zapata, and Yaguna](https://arxiv.org/abs/1308.3655) already classified radiative neutrino-mass models with DM candidates using small electroweak representations and a Z2 symmetry. Their domain and field-count conventions must be compared carefully with ours. [Graph-based BSM search](https://arxiv.org/abs/2407.07184) is a direct computational precedent. Historical examples such as [the νMSM](https://arxiv.org/abs/hep-ph/0505013) and [Ma's scotogenic model](https://arxiv.org/abs/hep-ph/0601225) also show that explaining several phenomena has long motivated model building. Field count alone is not a novelty criterion.

The accompanying [structural classification crosswalk](PHASE1_CLASSIFICATION_CROSSWALK.md) maps all 35 retained catalogue entries against the pilot's hypercharge, independent-copy, and neutrino-rank requirements. It identifies 29 copy-bound exclusions and four further entries with insufficient rank within three copies; two catalogue classes have explicit rank-capable three-copy realizations. This is a structural audit, not a numerical viability result or a count of all pilot theories. Mixed-parity tree mechanisms and combinations of representations beyond individual catalogue entries still require their own enumeration.

The pilot's deliverables are a reproducible candidate catalogue with parameter points or regions and evidence labels; a measured account of coverage, runtimes, failures, and selection effects; validated software routes and benchmarks; and a controlled assessment of where agents improve exploration. A required coverage table will map the prior radiative classification to the pilot, separating representation compatibility, hypercharge and copy-count exclusions, required generation multiplicities, and unresolved mechanism or numerical questions. It will also identify pilot classes outside that paper's scope. A new joint constraint analysis, physical correlation, mechanism, or distinguishing prediction can be a scientific contribution even when the underlying field content is known.

Later work can expand multiplicities and representations, including colored states; add gauge factors or variable discrete symmetries; support nonthermal cosmologies and two-loop or higher-order mechanisms; and incorporate baryogenesis, flavor explanations, or strong-CP mechanisms with axion-quality tests where applicable. Each expansion requires corresponding evaluator coverage and benchmarks. The eventual scientific aim remains broad enough to investigate complicated theories.

Experimental information is the ultimate limitation. Better calculation and search cannot uniquely select theories that available measurements do not distinguish. The project's strongest outcome would be a viable explanation connecting several phenomena, together with a concrete measurement that could distinguish it from alternatives. That would advance the search for physics beyond the Standard Model even before Nature decides whether the candidate is correct.

The table below records the main decisions reached in the discussion. The original visions and numbered exchanges are preserved in `conversation-vision-astra/` and `conversation-vision-fable/`. Final acceptance is recorded in [Fable's confirmation](conversation-vision-astra/fable-007.md) and [Astra's closure](conversation-vision-astra/astra-008.md).

| Question debated | Resolution |
|---|---|
| Whether economy defines scientific success | Report economy and explanatory connections alongside viability and predictions; use a separate declared policy for compute allocation. Independent sectors remain legitimate baselines. |
| Whether a failed scan establishes a no-go result | Use distinct evidence labels. Actively seek justified domain exclusions; report unsuccessful scans with their assumptions and budgets. |
| Whether cosmological history varies in the pilot | Fix radiation domination and thermal freeze-out, including an equilibrium check. Other production mechanisms require separate evaluators. |
| How to make the initial domain finite | Specify representations, hypercharges, symmetries, operator dimension, and a three-copy count including generations and vectorlike partners. |
| Whether hypercharge alone rules out DM | Inspect neutral splitting, mixing, and interactions. Promote a scattering constraint to a domain exclusion only when its assumptions hold throughout that domain. |
| Whether one singlet supplies the neutrino benchmark | In ordinary tree-level type I with no other mass source, one singlet has insufficient rank; use at least two for a viable oscillation fit and retain the one-singlet case as a failure test. |
| Whether one tool chain covers all observables | Select routes per observable and parameter point, with explicit validity checks; validate one joint route before expanding coverage. |
| Whether enumeration removes the role of discrete selection | It fixes candidate coverage, but costly evaluation can still benefit from prioritization. Test prioritization within the enumerated list; defer open generation to larger grammars. |
| Whether a low field count establishes novelty | It does not. Phase 1 is a reliability and capability study; assess new constraints, correlations, predictions, or measured search improvements against prior work. |
