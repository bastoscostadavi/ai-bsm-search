# BSM Atlas: starter papers

Prepared October 1, 2026.

These 24 papers form a starter reading list and a proposed extraction corpus for the BSM Atlas. They were selected to exercise the database's representation of gauge groups, fields, symmetry actions, interactions, symmetry breaking, and relations between models. The selection includes concrete models, reviews containing many models, repeated descriptions of related models, and references for machine-readable representations.

Start with papers 1–8, focusing on model definitions and classification tables. The longer reviews can be consulted selectively. Papers 9–24 broaden coverage and expose cases that a first schema might miss.

Years below refer to first arXiv submission. Links pin the versions checked for this list. Bibliographic metadata was checked against official arXiv records; the extraction tasks are recommendations for our project, not completed model annotations. Historical phenomenological conclusions should remain dated source claims rather than current viability labels.

## First pass: eight papers to shape the schema

### 1. Scalar singlet dark matter

**James M. Cline, Kimmo Kainulainen, Pat Scott and Christoph Weniger (2013). [Update on scalar singlet dark matter — arXiv:1306.4710v5](https://arxiv.org/abs/1306.4710v5).**

Concrete model and phenomenological study. A manageable first extraction: record the singlet field, stabilizing symmetry, scalar potential, portal coupling and parameter conventions. Keep the structural specification separate from relic-density assumptions and experimental constraints. Compare with paper 9 to test linking multiple papers to a common model specification after checking conventions.

### 2. The scotogenic model

**Ernest Ma (2006). [Verifiable Radiative Seesaw Mechanism of Neutrino Mass and Dark Matter — arXiv:hep-ph/0601225v1](https://arxiv.org/abs/hep-ph/0601225v1).**

Concrete model. Extract the new scalar and fermion multiplets, their discrete-symmetry assignments, Yukawa interactions, scalar interactions, and assumed vacuum. This connects directly to our neutrino-mass plus dark-matter project. Record alternative dark-matter candidates as possibilities within the specification, with their required mass ordering.

### 3. A catalogue of radiative neutrino and dark-matter models

**Diego Restrepo, Oscar Zapata and Carlos Yaguna (2013). [Models with radiative neutrino masses and viable dark matter candidates — arXiv:1308.3655v2](https://arxiv.org/abs/1308.3655v2).**

Systematic classification. Use the field-assignment tables and Appendix A to test one-paper-to-many-model relations, representation conventions, charge-conjugate descriptions and multiplicity counting. The paper identifies 35 viable catalogue entries under its historical analysis; that is not a count of all BSM theories or a present-day viability assessment.

Our [existing classification crosswalk](PHASE1_CLASSIFICATION_CROSSWALK.md) provides a starting point for comparing its conventions with the proposed pilot grammar. Preserve its distinctions between structural eligibility and numerical viability.

### 4. Two-Higgs-doublet models

**G. C. Branco, P. M. Ferreira, L. Lavoura, M. N. Rebelo, Marc Sher and Joao P. Silva (2011). [Theory and phenomenology of two-Higgs-doublet models — arXiv:1106.0034v3](https://arxiv.org/abs/1106.0034v3).**

Review and family classification. Start with the Yukawa assignments, scalar potentials, symmetries and vacuum discussion. Test whether the schema distinguishes Type-I, Type-II and inert constructions while recognizing their shared gauge and scalar content. Store CP assumptions, explicit breaking and vacuum-dependent breaking separately.

### 5. Sterile neutrinos and the νMSM

**Takehiko Asaka and Mikhail Shaposhnikov (2005). [The νMSM, Dark Matter and Baryon Asymmetry of the Universe — arXiv:hep-ph/0505013v1](https://arxiv.org/abs/hep-ph/0505013v1).**

Concrete model. Extract the three singlet-neutrino species, mass and Yukawa structure, and the parameter assumptions used for the proposed mechanisms. This tests the difference between a broad singlet-neutrino extension and a particular mass regime. Keep cosmological assumptions and claims about multiple explained phenomena linked to their evidence.

### 6. A concrete extra-U(1) model

**Lorenzo Basso, Alexander Belyaev, Stefano Moretti and Claire H. Shepherd-Themistocleous (2008). [Phenomenology of the minimal B-L extension of the Standard model: Z' and neutrinos — arXiv:0812.4313v1](https://arxiv.org/abs/0812.4313v1).**

Concrete gauge extension. Extract the B-L charges, additional matter, scalar sector and gauge-breaking pattern. Record the authors' gauge-mixing and neutrino-sector simplifications as assumptions. This tests whether gauge structure, charge normalization, symmetry breaking and interaction restrictions have distinct places in the database. Use paper 15 for broader context.

### 7. The dimension-six SMEFT operator basis

**B. Grzadkowski, M. Iskrzynski, M. Misiak and J. Rosiek (2010). [Dimension-Six Terms in the Standard Model Lagrangian — arXiv:1008.4884v3](https://arxiv.org/abs/1008.4884v3).**

Operator classification, commonly associated with the Warsaw basis. Extract operator definitions, flavor indices, conservation assumptions and the treatment of redundant operators. This tests the representation of an EFT basis and its truncation. An individual operator should not automatically become a distinct UV model record.

### 8. A reference for computational model specifications

**Florian Staub (2013). [SARAH 4: A tool for (not only SUSY) model builders — arXiv:1309.7223v2](https://arxiv.org/abs/1309.7223v2).**

Software and model-definition reference. Compare its handling of gauge groups, fields, global symmetries, interactions and symmetry breaking with the proposed atlas entities. Use it to identify information needed for later calculations. A literature record may remain incomplete even when its model family is recognizable; record that incompleteness explicitly.

## Second pass: related descriptions and broader matter content

### 9. An earlier treatment of scalar singlet dark matter

**C. P. Burgess, M. Pospelov and T. ter Veldhuis (2000). [The Minimal Model of Nonbaryonic Dark Matter: A Singlet Scalar — arXiv:hep-ph/0011335v3](https://arxiv.org/abs/hep-ph/0011335v3).**

Concrete model. Compare its potential, parameter normalization and assumptions with paper 1. The exercise is to determine which structural statements can be reconciled into one specification and which belong to individual studies. Different experimental conclusions or conventions do not by themselves define a new model.

### 10. The Higgs portal as a family of constructions

**Brian Patt and Frank Wilczek (2006). [Higgs-field Portal into Hidden Sectors — arXiv:hep-ph/0605188v1](https://arxiv.org/abs/hep-ph/0605188v1).**

Short conceptual paper with examples. Extract the portal interactions and the assumptions made about each hidden sector. Test whether the atlas distinguishes a general connection between sectors from a fully specified theory. Avoid assigning every Higgs-portal example the same stable-singlet-dark-matter identity.

### 11. The inert doublet model

**Riccardo Barbieri, Lawrence J. Hall and Vyacheslav S. Rychkov (2006). [Improved Naturalness with a Heavy Higgs: An Alternative Road to LHC Physics — arXiv:hep-ph/0603188v2](https://arxiv.org/abs/hep-ph/0603188v2).**

Concrete model. Extract the additional doublet, discrete symmetry, scalar potential and vacuum with an inert doublet. Compare with the inert discussion in paper 4 and the scalar sector in paper 2. Shared fields or sectors should support explicit relations without automatically merging the complete models. Retain the paper's historical heavy-Higgs setting as study context.

### 12. A wider map of radiative neutrino-mass models

**Yi Cai, Juan Herrero-García, Michael A. Schmidt, Avelino Vicente and Raymond R. Volkas (2017). [From the trees to the forest: a review of radiative neutrino mass models — arXiv:1706.08524v3](https://arxiv.org/abs/1706.08524v3).**

Review and classification. Use its organization by effective operators, loop order and topology to test several classifications of the same underlying models. Begin with explicit examples and their field content. A loop topology is a mechanism descriptor that can have multiple model realizations.

### 13. Electroweak multiplets and accidental stability

**Marco Cirelli, Nicolao Fornengo and Alessandro Strumia (2005). [Minimal Dark Matter — arXiv:hep-ph/0512090v4](https://arxiv.org/abs/hep-ph/0512090v4).**

Model classification. Extract candidate multiplets, spin, hypercharge and the assumptions behind stability. This extends the corpus beyond small representations and tests imposed versus accidental protection. Record the operator dimension and validity assumptions relevant to a stability claim, rather than turning the claim into an unconditional property of a representation.

### 14. Colored matter and leptoquark representations

**I. Doršner, S. Fajfer, A. Greljo, J. F. Kamenik and N. Košnik (2016). [Physics of leptoquarks in precision experiments and at particle colliders — arXiv:1603.04993v3](https://arxiv.org/abs/1603.04993v3).**

Review and classification. Start with the representation and interaction catalogue. Extract color and electroweak representations, spin, flavor couplings, and baryon/lepton-number assumptions. Distinguish a scalar or vector leptoquark specification from a proposed UV completion containing it.

## Third pass: gauge extensions, supersymmetry and global symmetries

### 15. The wider family of extra-U(1) theories

**Paul Langacker (2008). [The Physics of Heavy Z' Gauge Bosons — arXiv:0801.1345v3](https://arxiv.org/abs/0801.1345v3).**

Review. Extract examples of charge assignments, additional matter, kinetic mixing and gauge breaking. Use this to test whether two theories with an extra Abelian factor remain distinguishable when their charges or interactions differ. Compare its discussion of model families with the concrete B-L specimen in paper 6.

### 16. Left-right symmetry and its implementations

**Alessio Maiezza, Miha Nemevsek, Fabrizio Nesti and Goran Senjanovic (2010). [Left-Right Symmetry at LHC — arXiv:1005.5160v1](https://arxiv.org/abs/1005.5160v1).**

Concrete model analysis. Extract the gauge and scalar sectors, breaking pattern, and implementations of left-right symmetry through parity or charge conjugation. This tests whether the atlas records how a discrete transformation acts on fields and couplings, alongside the gauge-group label.

### 17. The MSSM and supersymmetric bookkeeping

**Stephen P. Martin (1997). [A Supersymmetry Primer — arXiv:hep-ph/9709356v7](https://arxiv.org/abs/hep-ph/9709356v7).**

Pedagogical review. Focus on MSSM field content, the superpotential, soft terms, R-parity and electroweak breaking. Test whether the atlas can relate superfields to component fields without double counting, and distinguish supersymmetry breaking from gauge symmetry breaking. Extract explicitly stated restrictions rather than treating “MSSM” as one uniquely fixed parameter structure.

### 18. The NMSSM and restrictions within a named family

**Ulrich Ellwanger, Cyril Hugonie and Ana M. Teixeira (2009). [The Next-to-Minimal Supersymmetric Standard Model — arXiv:0910.1785v5](https://arxiv.org/abs/0910.1785v5).**

Review. Compare general and Z3-invariant specifications, their superpotentials, soft terms and symmetry limits. This is a useful case for distinguishing an added field from the interaction restrictions defining a particular variant. Record relations to MSSM descriptions with the necessary assumptions.

### 19. Axion models and anomalous global symmetries

**Luca Di Luzio, Maurizio Giannotti, Enrico Nardi and Luca Visinelli (2020). [The landscape of QCD axion models — arXiv:2003.01100v4](https://arxiv.org/abs/2003.01100v4).**

Review and model catalogue. Begin with representative KSVZ and DFSZ constructions. Extract Peccei–Quinn charges, matter content, interactions and symmetry-breaking scales. Distinguish spontaneous breaking, anomaly properties and explicit breaking. Link low-energy axion descriptions to their UV constructions without identifying them as the same specification.

## Fourth pass: matching, representations and limits of the first schema

### 20. A dictionary between heavy fields and SMEFT

**J. de Blas, J. C. Criado, M. Perez-Victoria and J. Santiago (2017). [Effective description of general extensions of the Standard Model: the complete tree-level dictionary — arXiv:1711.10391v2](https://arxiv.org/abs/1711.10391v2).**

Classification and matching reference. Extract examples linking heavy-field representations and interactions to dimension-six SMEFT coefficients. Attach matching order, scales and assumptions to the relation. The paper does not restrict the high-energy theory to renormalizable interactions; preserve the scope of each matching result.

### 21. A singlet extension with higher-dimensional interactions

**Shekhar Adhikari, Ian M. Lewis and Matthew Sullivan (2020). [Beyond the Standard Model Effective Field Theory: The Singlet Extended Standard Model — arXiv:2003.10449v3](https://arxiv.org/abs/2003.10449v3).**

Concrete BSM-EFT study. Compare the renormalizable singlet description with the version including dimension-five interactions. This directly tests whether the atlas distinguishes theories sharing field content but differing in operator content and truncation. Check symmetry assumptions before relating it to the stable-singlet models in papers 1 and 9.

### 22. A machine-readable interaction format

**Céline Degrande et al. (2011). [UFO - The Universal FeynRules Output — arXiv:1108.2040v2](https://arxiv.org/abs/1108.2040v2).**

Software-format reference. Compare its particle, parameter and vertex objects with the atlas structure. Use it to plan a future export route for sufficiently complete specifications, while retaining source evidence and higher-level symmetry information in the atlas. A file format is not itself a physical model.

### 23. Composite Higgs models

**Kaustubh Agashe, Roberto Contino and Alex Pomarol (2004). [The Minimal Composite Higgs Model — arXiv:hep-ph/0412089v2](https://arxiv.org/abs/hep-ph/0412089v2).**

Concrete model and a later schema test. Extract global-symmetry breaking, the pseudo-Goldstone Higgs description, gauge embeddings and the relation to a five-dimensional realization. Use it to discover where a schema designed around elementary four-dimensional fields requires additional entities.

### 24. An extra-dimensional construction

**Lisa Randall and Raman Sundrum (1999). [A Large Mass Hierarchy from a Small Extra Dimension — arXiv:hep-ph/9905221v1](https://arxiv.org/abs/hep-ph/9905221v1).**

Concrete model and a later schema test. Record spacetime dimensionality, geometry, branes and localization assumptions. This tests the boundary of a gauge-group-plus-matter table. Supporting such constructions can remain a later extension, with their initial atlas records explicitly marked as only partially represented.

## A small extraction exercise for each paper

Create one draft record per explicitly specified model or variant, with the following information:

1. Paper ID and version; model name as written; the paper's role in introducing, reviewing, modifying or studying it.
2. Gauge factors and conventions; field list with spin, multiplicity and representations; symmetry actions on the fields.
3. Specified interactions, structural coefficient restrictions, operator truncation and completeness of the description.
4. Assumed vacuum, breaking pattern, residual symmetries and applicable conditions.
5. An equation, table, section or passage supporting each extracted claim; separate author statements from our inferences.
6. Candidate relations to existing records: same specification, variant, extension, limit or EFT matching, with the basis for the proposed relation.

Keep “not specified,” “absent,” “forbidden” and “assumed zero” distinct. Preserve original notation alongside normalized notation. For reviews, begin with a few fully specified examples rather than creating a supposedly complete model record from every name mentioned.

Useful first comparison sets are papers **1 and 9** for reconciliation across sources; **2, 3, 4 and 11** for related models and shared sectors; **6 and 15** for a concrete model within a gauge family; **17 and 18** for supersymmetric extensions and restrictions; and **7, 20 and 21** for EFT bases, matching and truncation.
