# Phase 1 crosswalk to Restrepo, Zapata and Yaguna

*Structural audit, September 21, 2026. This is a comparison of catalogue entries with the proposed pilot grammar, not a reproduction of viable parameter regions.*

The primary source is [Restrepo, Zapata and Yaguna, arXiv:1308.3655v2](https://arxiv.org/abs/1308.3655v2), especially [Appendix A, Tables 34–36, printed pages 34 and 36](https://arxiv.org/pdf/1308.3655v2#page=34). Retain only rows marked viable there: the appendix also displays rejected cases. Charge-conjugate values grouped in one row count as one catalogue entry. The result below covers all 35 retained entries.

## Conventions and what is being tested

The paper uses \(Q=T_3+Y_{\rm RZY}/2\); the pilot uses \(Q=T_3+Y_{\rm pilot}\). Thus \(Y_{\rm pilot}=Y_{\rm RZY}/2\). The pilot's hypercharge set corresponds to \(Y_{\rm RZY}\in\{-2,-1,0,1,2\}\). All α values below retain the paper's convention.

The paper's multiplet categories do not count independent left-handed Weyl copies as the pilot does. Its field-assignment tables must be expanded into that bookkeeping: an independent vectorlike fermion pair requires two Weyl multiplets; a scalar's Hermitian conjugate adds none. Extra generations also consume the pilot's three-copy budget. See the explicit assignments in Sections 3–6 and the generation discussion in [Section 8, printed page 26](https://arxiv.org/pdf/1308.3655v2#page=26).

The `copies` column is our lower-bound calculation for the complete field content of that catalogue row, before any extra generations needed for neutrino rank. `≥4` is sufficient to prove that the row is outside the pilot; it is not an exact multiplicity claim. Every row has the paper's all-odd parity assignment.

Codes:

- **C:** exceeds the pilot's three-independent-copy limit.
- **H:** contains a scalar doublet with \(|Y_{\rm pilot}|=3/2\), outside the pilot's hypercharge set.
- **R:** field content fits three copies, but its one-loop neutrino mass has rank at most one with those copies; see the derivation below.
- **E:** admits a rank-capable extension within three copies; numerical joint acceptance remains untested.

## Complete mapping of the 35 retained catalogue entries

The table is our structural classification of the source's identifiers. A sign pair or comma-separated α list in one row represents its source equivalence class.

| Source table | Catalogue identifier | α | Minimum copies | Pilot assessment |
|---|---|---:|---:|---|
| 34 | T3-B | −1 | 2 | E |
| 34 | T3-C | −1 | 2 | E |
| 35 | T1-1-A | 0 | 3 | R |
| 35 | T1-1-B | 0 | 3 | R |
| 35 | T1-1-G | 0 | 3 | R |
| 35 | T1-1-H | 0 | 3 | R |
| 35 | T1-3-A | 0 | 4 | C |
| 35 | T1-3-B | 0 | 4 | C |
| 35 | T1-3-G | 0 | 4 | C |
| 35 | T1-3-H | 0 | 4 | C |
| 35 | T3-A | 0 | 4 | C |
| 35 | T3-A | −2 | 4 | C |
| 35 | T3-B | 1, −3 | 4 | C, H |
| 35 | T3-C | 1, −3 | 4 | C, H |
| 35 | T3-E | 0, −2 | 4 | C |
| 36 | T1-1-A | ±2 | ≥4 | C, H |
| 36 | T1-1-B | ±2 | ≥4 | C, H |
| 36 | T1-1-C | ±1 | ≥4 | C |
| 36 | T1-1-D | 1 | ≥4 | C |
| 36 | T1-1-D | −1 | ≥4 | C |
| 36 | T1-1-F | ±1 | ≥4 | C |
| 36 | T1-1-G | ±2 | ≥4 | C, H |
| 36 | T1-1-H | ±2 | ≥4 | C, H |
| 36 | T1-2-A | 0 | ≥4 | C |
| 36 | T1-2-A | −2 | ≥4 | C |
| 36 | T1-2-B | 0 | ≥4 | C |
| 36 | T1-2-B | −2 | ≥4 | C |
| 36 | T1-2-D | 1 | ≥4 | C |
| 36 | T1-2-D | −1 | ≥4 | C |
| 36 | T1-2-F | 1 | ≥4 | C |
| 36 | T1-2-F | −1 | ≥4 | C |
| 36 | T1-3-C | ±1 | ≥4 | C |
| 36 | T1-3-D | 1 | ≥4 | C |
| 36 | T1-3-D | −1 | ≥4 | C |
| 36 | T1-3-F | ±1 | ≥4 | C |

## Derivation of the boundaries

**Hypercharge.** The six H entries follow by substituting the tabulated α values into the source's Tables 1, 2, 7, 8, 29 and 30. The offending doublet has \(Y_{\rm RZY}=\pm3\). None of the 35 retained entries requires a singlet with \(|Y_{\rm pilot}|=2\). Such singlets appear in other rows, for example T3-A at α=−4 and T1-1-D at α=−3, which the paper already flags nonviable. Those cases should not be presented as extra omissions from its 35-entry viable catalogue.

**Copies.** The four T1-3 rows at α=0 contain one neutral singlet/triplet Weyl fermion, two doublet Weyl fermions of opposite hypercharge, and one scalar: four independent copies. This is explicit in source Tables 19, 20, 25 and 26. The remaining five Table 35 entries contain two scalar multiplets and a hypercharged vectorlike fermion: another four copies, including its conjugate Weyl partner. Every retained Table 36 row already exceeds the limit before any extra generations are introduced. This gives 29 copy exclusions, six of which also violate the hypercharge boundary.

**Rank of the four R entries.** At α=0, the T1-1-A/B/G/H entries reduce to one odd neutral fermion \(F\), one odd scalar doublet \(\eta\), and one odd neutral scalar singlet/triplet. With an unbroken Z2, the only new lepton-flavor vector entering their one-loop Majorana self-energy is the Yukawa vector \(y_i\) at \(L_i F\eta\). Scalar mixing and the additional allowed one-loop diagrams change its coefficient, not this flavor structure:

\[
(m_\nu)_{ij}=\Lambda\,y_i y_j,\qquad \operatorname{rank}(m_\nu)\leq1.
\]

This is our analytic inference from their field content under the pilot's renormalizable, unbroken-Z2 and tree/one-loop assumptions. It fails the two-nonzero-mass requirement from oscillations. A second independent Yukawa vector requires an additional fermion or scalar-doublet copy and would exceed three copies for these full entries. Changing a zero-hypercharge scalar from real to complex does not create a second lepton-flavor vector. The scope of the rank statement excludes higher-loop corrections.

**The two E entries.** Each Table 34 entry consists of an inert scalar doublet and a neutral singlet or triplet fermion. One copy of each also gives rank at most one, but two neutral fermion copies plus one doublet fit the three-copy limit. With independent Yukawa columns, the one-loop expression is

\[
m_\nu=Y\,\operatorname{diag}(\Lambda_1,\Lambda_2)Y^T,
\]

which can have rank two. This establishes structural eligibility of these realizations; it does not establish a common neutrino fit, thermal relic abundance, acceptable vacuum, or current experimental viability.

## What this comparison does and does not establish

Among the 35 named minimal catalogue classes, 29 fail the pilot's copy boundary, another four cannot achieve the required neutrino rank within that boundary, and two have the explicit rank-capable three-copy realizations above. The hypercharge exclusions overlap the copy exclusions. These are comparisons of entire catalogue entries: deleting a field changes the entry and may recover an eligible submodel.

This is **not** a claim that only two theories occur in the pilot. Combinations such as one singlet fermion, one triplet fermion and one inert doublet, repeated-scalar variants, and mixed-parity tree-level seesaw plus independent-DM constructions require their own enumeration. The source's all-odd, one-loop catalogue and our broader tree/one-loop, independently assigned-parity grammar are not identical sets. The overall pilot should therefore not be described as a subset of that catalogue or as reproducing it in full.

The crosswalk is a calibration target for a future enumerator and operator/rank checker. It provides named boundaries and analytic expectations. It makes no claim of an executed search, complete parameter-space coverage, or reproduction of the source's historical viability judgements.
