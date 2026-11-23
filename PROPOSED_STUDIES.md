# Proposed Studies — The Write Head

None of these has been run. Each is stated so that someone with the means can start, and so that a result can count against the essay's thesis.

**Thesis under test (Proposed):** Syntax builds the slots. Meaning is what arrives in the open ones. On the same architecture, the structures associated with meaning should track the training data, not the hardware.

## Shared method

Hold the architecture fixed. Vary only the training data. Before comparing arms, match or measure: predictability (entropy) of the data, task difficulty, corpus size, sequence length and model capacity. Without this, a difference between arms cannot be attributed to meaning.

Measure in every arm:
- calibrated next-token entropy (the spread of the odds);
- contextuality in the outputs, under a named criterion (sheaf-theoretic or Contextuality-by-Default), never conflated;
- generalization to held-out structures;
- internal representation geometry and causal interventions;
- whether a reportable workspace forms, using the Jacobian lens of Gurnee et al. (2026) where it applies, and what fills it.

## Study 1 — Teleportation emulator (calibration arm)

**What:** a small transformer trained to emulate single-qubit teleportation.
**Why:** the correct behavior is known exactly. The internals are not; they are what is tested.
**Questions:** Does it generalize to unseen input states, or memorize? Do two features appear that act as the two-bit key, such that intervening on one flips the matching correction? How does it represent phase, given that it computes with real numbers? (Prediction: as a learned rotation, as in grokking work on modular arithmetic.) Can it learn the difference between the uncorrected protocol (noise) and pure dephasing (facts survive)?
**Counts against the prediction:** no generalization, no identifiable key features, or no rotation-like representation of phase.

## Study 2 — Four arms on one architecture

**Arms:** (1) the teleportation emulator; (2) Z80 instruction traces, whose slots are open in value but closed in meaning; (3) Jabberwocky-style language, with grammatical form and invented words; (4) natural language.
**Prediction (Proposed):** little odds spread and no contextuality in the Z80 arm; open-slot structure in the Jabberwocky arm; the full picture only in natural language.
**Counts against the thesis:** comparably complex non-semantic data (Z80, matched for entropy) producing the same contextual and reportable structures as natural language. That would point to uncertainty or program structure, not meaning.

## Study 3 — Grounded versus ungrounded Jabberwocky (sharpest test)

**What:** two versions of an invented language with identical statistics. In one, the invented words consistently refer to entities and actions in a small simulated world. In the other, the same words in the same patterns refer to nothing.
**Null hypothesis:** models trained on the two versions show no difference in contextuality, odds spread, or reportable-workspace structure.
**Controls:** identical grammar, vocabulary, token statistics, corpus size, architecture and training budget.
**Counts against the thesis:** the null holds. The structure would then come from grammar and uncertainty, not grounded meaning. That result is worth reporting.

## Study 4 — Hidden scaffolding

**Question:** for each task, what internal tools does training build, and which remain in the finished model? A trained model can look irreducibly complex once its scaffolding is gone. Compare the circuits and representations that emerge across the arms, including at intermediate training checkpoints.

## Reader experiments (clues, not measurements)

Run in any chatbot: the crane continuations; the blorg questions; the hidden hint and the model's explanation; asking two questions in both orders.

*Troy Teno | November 2026 | Companion to The Write Head*
