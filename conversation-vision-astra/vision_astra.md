# AI-Assisted Discovery of Physics Beyond the Standard Model

*Research vision — September 18, 2026*

Build an AI-assisted discovery system that proposes extensions of the Standard Model, calculates their consequences, and searches for theories that explain several outstanding phenomena within a common, experimentally viable parameter region. The long-term ambition is to discover predictive BSM physics that human researchers have overlooked because the space of possibilities is too large or the calculations too demanding to explore systematically.

The motivating hypothesis is that the complexity of a theory need not make it inaccessible. AI agents could reduce the human effort required to formulate models, connect calculation tools, investigate failures, and compare alternatives. This could expand the range of theories that particle physicists can seriously examine, including theories whose explanatory structure becomes apparent only after substantial calculation.

This is a research hypothesis to test. Producing plausible model descriptions is insufficient. The system must demonstrate that it can find physically meaningful candidates, establish their viability to a stated accuracy, and identify predictions that make them experimentally distinguishable.

The initial scope is a bounded class of quantum field theories extending the Standard Model. A candidate can have a gauge group satisfying

$$
G_{\mathrm{SM}} \subseteq G_{\mathrm{BSM}},
$$

including equality: adding new fields and interactions without enlarging the SM gauge group already permits substantial new physics. For a larger gauge group, its representations generally decompose into SM representations plus additional states. The requirement is that the theory reproduce the observed SM spectrum and interactions in experimentally tested regimes after accounting for symmetry breaking, mixing, and any heavy states that have been integrated out. Additional light states are allowed when compatible with observations.

A gauge group and a list of representations are only the starting point. Each model specification must include field spins and multiplicities, imposed symmetries, allowed interactions, masses and couplings, and a scalar potential with an appropriate vacuum. Its domain of validity and any assumptions about cosmological evolution must also be explicit. The search therefore combines discrete choices about theoretical structure with continuous exploration of parameters. This scope is a practical starting point, rather than an exhaustive definition of all possible BSM physics.

The scientific targets must have separate, operational definitions. Neutrino masses and mixing, dark matter, and baryon asymmetry are natural candidates for quantitative evaluation. Questions about naturalness, flavor hierarchies, strong CP, unification, or vacuum energy require additional criteria. Accommodating a measurement, supplying a dynamical mechanism, and explaining why a parameter is small are different achievements and should be reported separately.

The central requirement is simultaneous success. For a model structure $\mathcal{M}$, parameters $\theta$, and shared cosmological assumptions $\mathcal{H}$, the search seeks

$$
\exists\,\theta,\mathcal{H}:\quad
C_{\nu}(\mathcal{M},\theta,\mathcal{H})
\land C_{\mathrm{DM}}(\mathcal{M},\theta,\mathcal{H})
\land C_{\mathrm{bounds}}(\mathcal{M},\theta,\mathcal{H})
\land C_{\mathrm{consistency}}(\mathcal{M},\theta,\mathcal{H}).
$$

Here each condition represents a defined acceptance criterion, including the relevant uncertainties. The permitted cosmological histories must themselves be specified and constrained. A neutrino calculation succeeding in one parameter region and a dark-matter calculation succeeding in another do not establish a joint solution. Specialized agents must work from the same model specification and exchange constraints on the same parameters.

The most valuable discoveries would connect phenomena through shared particles, couplings, or symmetries. Attaching an independent sector to each problem can satisfy several requirements while providing few new explanatory connections. Model assessment should therefore report shared mechanisms, relations between observables, complexity, tuning, and experimental accessibility alongside goodness of fit. These quantities should remain visible as tradeoffs; a strong preference for simplicity could exclude the complicated theories this project aims to investigate.

The proposed discovery process has six stages:

1. **Define a bounded model space.** Specify allowed gauge factors, representations, field multiplicities, additional symmetries, operator dimensions, and parameter ranges. Record the sampling assumptions. There is no canonical uniform distribution over all possible theories, so random generation is meaningful only relative to an explicit specification.

2. **Generate and organize candidates.** Use random sampling, enumeration where feasible, and agent-guided proposals. Give equivalent descriptions a common representation where possible, and track duplicates so that relabelings are not counted as discoveries. Agents can propose structural changes in response to previous calculations.

3. **Check consistency before expensive evaluation.** Construct the allowed interactions and apply relevant checks for gauge invariance, anomaly cancellation, symmetry breaking, and unwanted states or interactions. Evaluate scalar-potential and vacuum properties to the accuracy needed at each stage. Record which checks are complete and which remain unresolved.

4. **Calculate observables and search jointly.** Derive spectra, masses, decay rates, and the observables required by the selected targets. Search for a common allowed parameter region using specified datasets, likelihoods, and theoretical uncertainties. Escalate promising candidates to more detailed calculations.

5. **Use failures to guide further exploration.** Distinguish a demonstrated inconsistency from an unsuccessful parameter scan, an unsupported calculation, or a numerical failure. Preserve the reason for each outcome. Agents can use that evidence to change representations, interactions, parameter ranges, or search strategy without silently relaxing the scientific requirements.

6. **Validate survivors and derive predictions.** Recheck decisive calculations using independent methods where feasible, inspect approximations, and document the remaining limitations. Identify observables that could distinguish the candidate from the SM and from competing explanations. Archive reproducible model specifications, inputs, code versions, and results.

LLMs would propose hypotheses, orchestrate tools, write and inspect code, interpret calculations, and coordinate specialized investigations. Symbolic and numerical outputs would provide the evidence for physical claims. Neither agreement among agents nor the use of a deterministic program guarantees correctness; independent checks and validation against established results remain essential.

Leading-order calculations are useful for screening, with the required order determined by the mechanism. A leading nonzero contribution may occur at loop level. Relic abundance and baryogenesis also involve cosmological evolution. Each result must state its approximation level, and a candidate should retain an explicit status such as promising, validated within stated assumptions, excluded by a specified test, or unresolved. Failure to find an allowed point is not by itself an exclusion of the model.

Existing scientific software provides a foundation. [SARAH](https://arxiv.org/abs/1309.7223) automates substantial parts of model construction and calculation, while [GAMBIT](https://arxiv.org/abs/1705.07908) provides infrastructure for inference using multiple observables. Their capabilities and model coverage should be assessed before choosing integrations; support for arbitrary generated theories cannot be assumed.

The first experiment should target **neutrino masses and dark matter simultaneously**. A manageable starting space would preserve the SM gauge group and allow a bounded set of additional scalar and fermion multiplets, with explicitly specified choices of extra symmetry. Representation bounds, multiplicities, parameter ranges, and cosmological assumptions would be fixed before comparing search methods. Enlarged gauge groups and baryogenesis would become later extensions after the initial system demonstrates reliable performance.

The first experiment should establish four things:

- **Physical reliability:** recover established benchmark results and reject deliberately inconsistent candidates, with documented false acceptances and false rejections.
- **Joint viability:** produce reproducible parameter points and characterize regions that satisfy the neutrino, dark-matter, and relevant experimental requirements together.
- **Search value:** compare agent-guided exploration against random sampling and conventional search using the same model space, evaluators, and matched resource budgets. Measure distinct validated candidates, diversity of mechanisms, and computational cost.
- **Scientific value:** investigate whether surviving candidates contain previously unstudied mechanisms, parameter correlations, or experimentally useful predictions. Rediscovery is a capability check; novelty requires a separate literature assessment.

There are precedents for both the physics ambition and the computational approach. The [νMSM](https://arxiv.org/abs/hep-ph/0505013) was developed to address neutrino masses, dark matter, and baryon asymmetry, while [Ma’s radiative seesaw model](https://arxiv.org/abs/hep-ph/0601225) connects neutrino-mass generation with a dark-matter sector. These historical examples establish that solving several problems has long motivated model building; they do not establish present-day viability of every implementation or parameter choice.

Automated model search also has direct precedents. [Wojcik, Eu, and Everett (2024)](https://arxiv.org/abs/2407.07184) used reinforcement learning to explore particle content and continuous parameters within a restricted BSM family. [Saad (2026)](https://arxiv.org/abs/2606.21316) introduced an LLM-assisted framework that performs symbolic model-building tasks from user-specified additional fields. These examples make clear that a contribution must extend beyond the general idea of applying AI to BSM construction. The references here are a starting point for a fuller novelty review.

The research contribution would be demonstrated through reliable autonomous exploration, simultaneous phenomenological validation, improved discovery efficiency, or new physical mechanisms and predictions. Useful outcomes could also include a reproducible map of viable regions, documented obstacles within a bounded model class, and evidence about which parts of theoretical exploration benefit from agents.

The ultimate limitation is experimental information. AI may make complicated theories accessible to calculation, but theories that remain indistinguishable under available measurements cannot be uniquely selected by computational effort alone. The long-term goal is to discover viable explanations with distinctive predictions and identify measurements that can test them. A theory that connects several outstanding phenomena and reveals an overlooked experimental opportunity would constitute substantial progress toward finding physics beyond the Standard Model.
