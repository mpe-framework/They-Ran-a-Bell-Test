# Experiments

*Companion to the essay "They Ran a Bell Test on a Language Model" (README.md). Troy Teno | November 2026.*

*For whoever builds these, human or Claude Code: read the essay first. This file supersedes section 5 of the November 23 handoff (HANDOFF_Bell_Contextuality.md). The essay's "Experiment" section is the summary. This file is the specification.*

## House rules

1. Every claim carries a tier: Established (cited source), Reading (our synthesis), Proposed (untested).
2. Predictions and kill lines are written here before anything runs. Do not move them after seeing results. If a line turns out to be badly chosen, say so in RESULTS.md and keep the original.
3. Null and failed results are kept, with their numbers.
4. Every number the code uses or produces can be printed.
5. Do not edit the essay. Report results to Troy; he decides what changes.

## The paper's exact rules (Established: Lo, Sadrzadeh and Mansfield, Proc. R. Soc. A 2025, arXiv:2412.16806)

**The schema.** Two nouns O1, O2 (e.g. apple, strawberry) and three modifiers X1, X2, X3. Three sentences, each fed to BERT separately with the noun masked:

1. The [MASK] is X1 and the same one is X2.
2. The [MASK] is X2 and the same one is X3.
3. The [MASK] is X3 and the other one is X1.

No fixed assignment of nouns to modifiers satisfies all three. The contradiction is built in. Any table with this shape is fully contextual by construction; BERT supplies only how strongly it leans in each sentence.

**The per-sentence lean.** For sentence i, with probabilities renormalized over the two nouns:

- ε_i = P_i(O1) − P_i(O2)
- ε_i = tanh(Δl_i / 2), where Δl_i = p_i · Δx + Δb (Proposition 7.1)
- p_i is the output vector at the mask; Δx = e_O1 − e_O2 (word embeddings; BERT ties input and output tables); Δb = b_O1 − b_O2 (prediction-head biases).

**The two tests.**

- Sheaf (signalling-corrected): SF = max_i |ε_i|. Contextual iff SF < 1/6. In words: BERT is between about 42 and 58 percent in all three sentences.
- Contextuality-by-Default: Δ = |ε1 − ε2| + |ε2 − ε3| + |ε3 + ε1|. Contextual iff Δ < 2. A case with BERT fully certain of the same noun everywhere sits exactly at Δ = 2.

**Published numbers to match.** Full data: 51,966,480 cases; 77,118 sheaf-contextual (0.148%); 36,938,948 CbD-contextual (71.1%). Top 1% most similar noun pairs (by cosine): 0.50% and 81.83%. Every sheaf case is also a CbD case. R² of Euclidean distance predicting SF: 0.0065 linear, 0.0092 cubic (full data); about 0.078–0.080 (similar subset). Predicting Δ: 0.0035 / 0.0050 (full); about 0.057–0.058 (similar subset). Note: the paper's text says "0.0148%" once; that is a typo for 0.148%.

**The assumption under test.** The paper links distance to contextuality by assuming the pointers p are isotropic (spread evenly in direction). It says this step is an approximation. Ethayarajh (2019) found BERT's representations crowd into a narrow cone.

## Stage 1: The glass toy (NumPy only)

**Purpose.** A didactic. It shows, with every number visible, whether the beam alone is enough to make distance a weak predictor. It cannot show that this is what happens in BERT. That is Stage 2.

**Build.**

- Dimension d = 768 (allow smaller for speed; report which).
- A word pair: Δx with controlled length D. Sweep D over a range wide enough that ε runs from near 0 to near ±1. Δb = 0 by default; one run with Δb drawn from a spread.
- Three pointers per case, p_1, p_2, p_3. Give them a shared component plus a per-sentence component, with correlation ρ between sentences as a parameter (real sentences share most of their words).
- Condition A, isotropic: pointers drawn with no preferred direction.
- Condition B, beam: pointers = common beam vector m + spread. Set m so the average cosine between pointers matches a realistic value (report the value and where it came from). The angle θ between m and Δx varies from pair to pair.
- For each case compute ε_i, SF, Δ, and both contextual flags.

**Checks.**

- C1. ε_i from the formula equals ε_i from a direct two-word softmax, to floating-point precision. If not, the build is wrong; stop.
- C2. With isotropic pointers, the toy's contextual rates move with D in the direction the paper reports (closer pairs, more contextual).

**Predictions (Proposed, written before running).**

- P1. Condition A: distance alone predicts SF with R² ≥ 0.5.
- P2. Condition B: distance alone predicts SF with R² no more than half its Condition A value.
- P3. Condition B: adding alignment, |cos θ| or the projection of m onto Δx, recovers at least half of what P2 lost.
- Same three for Δ, reported separately.

**Kill lines.** If C1 fails, fix the code. If P2 fails (distance predicts just as well inside the beam), the beam is not enough to weaken the law in this toy; report it. If P2 holds and P3 fails, the beam weakens the law but alignment is not the missing piece; report it.

**Sweeps to report.** Results across ρ, beam tightness, and Δb spread, so it is clear whether any conclusion depends on one setting.

## Stage 2: BERT itself (PyTorch and transformers allowed)

**Purpose.** Test the assumption on the real model.

**Build.**

- bert-base-uncased, the paper's model.
- Reproduce the schema on a sample of cases (their recipe: adjective-noun phrases from Simple English Wikipedia, five most frequent shared adjectives per noun pair; or a documented substitute). Report how the sample's contextual rates compare with the published ones. A large mismatch must be explained before going on.
- Extract p at the mask as the input to the final vocabulary projection (after the prediction head's transform). Verify the logit identity numerically on real cases (C1 again).
- Take Δx from the word embedding table and Δb from the prediction-head bias.

**Measurements.**

- M1. Anisotropy: average cosine between pointers across sentences; the top principal directions and how much they carry.
- M2. Alignment per pair: the angle between Δx and the mean pointer, or the main principal direction.
- M3. Regressions predicting SF and Δ: distance alone; distance plus alignment; Δl itself as a ceiling.

**Predictions (Proposed).**

- P4. The pointers are strongly anisotropic (average cosine well above zero).
- P5. Adding alignment to distance raises R² for SF by at least 50 percent over distance alone, in the full sample and in the similar-pair subset.
- Null: alignment adds little. Then the isotropy assumption does less harm than we expect, and the weak law needs another explanation. That is a reportable result.

## Stage 3: The heads that knew (later)

**Question.** In cases near the flip line, does the right answer appear in the middle of the model and then get overridden?

**Sketch.**

- Per layer, read the lean along Δx (logit lens) for cases near Δl = 0.
- Per head, measure each head's direct contribution to Δl along Δx.
- Causal test: patch an idle or overridden head's output back in, and check whether ε and the contextual flags change.
- A readable signal is not a used one. Only the causal test counts.

## Parked: the guppy study (not in scope yet)

Does the model build "pet fish" as "pet" plus "fish," or as something the parts do not predict? Glass version: compare the vector for the combination with the sum of the parts; then find and switch off whatever composes them, with controls ("pet and fish," "fish pet"). Prompt version: ratings of "guppy" as a pet, a fish, and a pet fish, in fresh chats. Held for the next essay. Do not build until Troy says so.

## Repo layout

```
README.md            the essay
EXPERIMENTS.md       this file
toy/                 Stage 1 code, PREREGISTRATION.md (copy of the predictions above, dated), RESULTS.md
bert/                Stage 2 code and RESULTS.md
archive/             The Write Head, shelved
```

*The measurement is real. The equation is exact. The assumption is the experiment.*
