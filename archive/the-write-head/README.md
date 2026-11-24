# The Write Head
*Categorical Teleportation and the Assembly of Reason*

**Troy Teno | November 2026**
*Essay — Not Peer Reviewed. Companion to Cornering the Ghost. Established marks a published result within its stated assumptions. Reading marks my way of putting established pieces together. Proposed marks a connection that still needs a model or a test.*

## The Promise

*Cornering the Ghost* ended with a promise. A companion essay would carry the same structure into language and the mind, where the cups and caps of teleportation also compose meaning, and where the ghost may sit in the same corner.

This is that essay. It keeps the same discipline. The mathematics comes first, carried as far as it honestly goes. Then the comparison, and the place where it breaks. Then a set of studies that have not been run, offered to anyone who wants to run them.

The question this time is the mirror of the last one. Not how a future becomes a past, but this:

How does a possibility become a record, and how does that record become part of a meaning?

## What We Already Know

We know a sentence is built before it is understood. You start speaking without knowing how the sentence will end. The words arrive, fitted, in an order that makes them mean what you meant.

We know a language model writes one token at a time. A token is a word or a piece of one. Before each token, the model computes odds for every token it knows. Then one is picked and written, and everything after must be computed with it in place. (Established)

We know later words change how earlier words are read. "The crane reached down toward the steel beam." "The crane reached down toward the fish." The first five words are identical. The crane is not. (Established)

And we know, from *Cornering the Ghost*, the shape of teleportation. It has four parts. A resource: an entangled pair, prepared in advance, one half at each end. A measurement: the sender joins the unknown state with their half and compares the two. A record: two classical bits. A correction: the receiver applies the fix those bits name, and holds the original state exactly. Nobody, at any step, reads what was carried. (Established: Bennett et al., 1993)

## The Slide into Grammar

In *Cornering the Ghost*, teleportation was a drawing. A wire bent into a cup was the shared pair. A wire bent into a cap was the comparison. Pull the bent wire straight and the state runs through. (Established: Abramsky and Coecke, 2004)

The same drawing was used for sentences before I ever used it for time. In Joachim Lambek's grammar, every word carries a type. A noun is a noun. A transitive verb carries two hooks, one reaching left for a subject and one reaching right for an object. When the nouns arrive, the hooks close. What remains is a sentence. (Established: Lambek, 1999)

Those hooks are cups. Coecke, Sadrzadeh and Clark showed that Lambek's grammar and the teleportation diagrams are the same kind of mathematical object, and built a way to compute a sentence's meaning by pulling the wires straight. (Established: Coecke, Sadrzadeh and Clark, 2010)

That is a model of how meaning composes. It is not a description of what happens inside a brain or a machine. It is the reason the comparison is allowed at all.

## The Blorg Sentence

Read this:

*The blorg flurbled the snorble flambly.*

Not one of those words means anything. And yet you can already answer questions about it. What did the blorg do? It flurbled. To what? The snorble. How? Flambly.

Grammar built the slots before any meaning arrived. Brain-imaging studies use sentences like this one to separate structure from meaning. Part of the brain's language network tracks the structure of a sentence even when every content word is replaced by nonsense. (Established: Pallier, Devauchelle and Dehaene, 2011)

Now look at it as a drawing. The verb's hooks are cups. The nouns sit on the wires. And the nouns are unknown. The diagram is complete, the relations are fixed, and nobody knows what is being related.

That is teleportation's defining property. The protocol moves a state nobody has read. Grammar does the same: it carries the relation without knowing the content. Grammar is the shared resource that lets meaning move without anyone knowing it in advance. (Reading)

The resource in teleportation is prepared before the message exists. So is grammar. Every speaker carries it before they know what they will say.

## Open Slots and Closed Slots

Here is the distinction this essay turns on.

A computer's instruction stream also has syntax. On the old Z80 processor, an instruction is an opcode followed by its operands, in strict order. The byte 0x3E means "load the accumulator with the next byte." That next byte can be any value, so the slot is open in value. But what the instruction does with it is fixed by the chip's specification. Nothing about its meaning is left for context to decide. There is nothing to ask.

Language leaves its slots open in meaning, on purpose. "Crane" holds a bird and a machine until something else arrives. The blorg sentence is all open slots.

So the contrast is not syntax against no syntax. Both have slots. The Z80's slots are open in value and closed in meaning. Language's slots are open in meaning, and context decides what fills them. The first lets you execute. The second lets you ask questions.

And for a predictive system, this is where probability enters. A system that must predict what fills a slot whose meaning is open has to hold odds over the candidates. A language model does exactly that. Where meaning is fixed by a specification, there is far less to hold odds over. (Proposed)

The thesis, in one line:

**Syntax builds the slots. Meaning is what arrives in the open ones.** (Proposed)

## The Write Head

Walk one token through a language model.

The context goes in. Layer after layer mixes it. At the top, the model's internal state becomes odds: one number for every token it knows, all adding to one. After "The crane reached down toward the," both "steel" and "water" may have real odds. Nothing is chosen yet.

Then a small step that is rarely mentioned. A sampler picks one token. Usually it draws a random number and lets the odds decide. At temperature zero, it simply takes the most likely one.

The token is written. It joins the context. Every later step reads it as given.

That is the write head. Above it, a spread of possibilities. Below it, a record. Each token arrives already holding the record of the ones before. It has the same shape as the now in *Cornering the Ghost*. (Reading)

Run teleportation's four parts against it. The resource is the grammar the model learned, carried in its weights before any prompt exists. The measurement is the pass through the layers, comparing the open slot with everything around it. The record is the written token. And the correction is never applied. The token stays.

Even people never erase. A speaker who says "I mean" does not unsay the first word. They write a second one. In language, a correction is always a new record. (Reading)

And the process is a loop, not a ladder. Meaning is already shaping the odds before a word is written, because the context the odds are computed from is itself made of earlier records, already read. Then a record is made. Then later words reread it, and that reading shapes the next odds. Possibility becomes a record. Records steer meaning. Meaning shapes the next possibility. (Reading)

## Where It Breaks, and Why That Is the Point

In nature, nobody knows who rolls the dice. In the machine, we do. We installed them. The sampler is a pseudo-random number generator. Give it the same seed and the same context, and it writes the same token every time. (Established)

The menu is ours too. A model can only write tokens from a vocabulary engineers fixed before training. In physics, why the world reads out in one basis rather than another is a deep question. Here it is a design file. (Established)

So both halves of the old mystery, which basis and which outcome, have plain answers in the machine. The comparison breaks.

What is left is the odds. Nobody wrote them. Why "steel" and "water" are both live after "crane," and why the odds sit where they do, was set by training on text people wrote. The ghost did not vanish. It moved into the odds, and behind the odds, into the language of the minds that made it. (Reading)

Two more breaks, stated plainly. A transformer has no quantum phase. Its numbers can add and cancel, but that is arithmetic, not quantum interference. And the contextuality measured in language models, below, is a property of statistics, not of particles.

## The Sentence, Three Ways

The double slit in *Cornering the Ghost* had three rungs. A sentence has the same three.

First, the word not yet written. The alternatives are open and carry odds. No fact has been made.

Second, the word written. "Crane" is in the context. The record exists, and its meaning is still open.

Third, the word reread. "Steel beam" arrives, and the crane is a machine. For a model that writes left to right, the fit here is exact. No information flows backward. The computation at the word "crane" cannot be influenced by any word that comes after it. Later positions read what was computed there, with a new question. (Established, for left-to-right models)

That is the sorting license from the quantum eraser, in a sentence. No letter travels backward. A later key selects a reading the earlier record allowed.

## Both Sides of the Lens

Two lines of research have looked at this seam from opposite sides.

From outside, Lo, Sadrzadeh and Mansfield took the formal tests physicists use for contextuality and applied them to how the model BERT resolves ambiguous words. They found 77,118 instances that pass the strict sheaf-theoretic test, and 36,938,948 that pass the broader Contextuality-by-Default test. These are two different criteria and should not be read as one. BERT reads in both directions, so it is not a write head. But it is a measured fact about context and meaning in a machine. (Established: Lo, Sadrzadeh and Mansfield, 2024)

From inside, in July 2026, Anthropic researchers published a tool they call the Jacobian lens. It identifies the representations a model is poised to put into words, at any point in its processing. They call that set the J-space. The model can report what is there, and much of its computation never enters it. (Established: Gurnee et al., 2026)

One instrument looks at what was written. The other looks at what was about to be said. The write head sits between them.

## The Study

Here is the proposal at the center of this essay. It has not been run.

Mechanism and data cannot be pulled apart by argument, because the mechanism is learned from the data. They can be pulled apart by controlled variation. Hold the architecture fixed. Change only what it is trained on, one step at a time. In the language of the diagrams, every arm runs the same wiring and differs only in what the wires carry.

Four arms, on the same architecture.

The first arm is a teleportation emulator: a small transformer trained to run the single-qubit protocol itself. It is the one case where the correct behavior is known exactly, so it calibrates the instrument. How the model achieves that behavior inside is not known in advance. That is what the arm tests. It asks real questions. Does the model learn the rule, or memorize? Test it on states it never saw. Do two clean features appear inside it, one for each bit of the key? And how does it hold phase? A transformer runs on real numbers, and phase is a rotation. When small transformers were trained on modular arithmetic, they learned to compute with rotations. A teleportation emulator may have to do the same. If it does, the task built the one thing the architecture lacked. (Established: Power et al., 2022; Nanda et al., 2023. Proposed: the prediction.)

The second arm is Z80 instruction traces: syntax with every slot closed.

The third arm is Jabberwocky: blorg sentences, syntax with open slots and no meaning.

The fourth arm is natural language: open slots and meaning.

In every arm, look for the same things. Contextuality in the output, under a named test. The spread of the odds. Whether a J-space forms, and what fills it.

One caution keeps the study honest. These four kinds of data differ in more than meaning. They differ in how predictable they are, how hard the task is, and how much of it there is. Those differences must be matched or measured. Otherwise a difference between the arms will not show that meaning caused it.

The sharpest single test follows from that. Build two versions of the blorg language with identical statistics. In one, the invented words consistently refer to things in a small simulated world: the blorg is always the same kind of thing, and flurbling always does the same thing to it. In the other, the same words, in the same patterns, refer to nothing. Same grammar, same uncertainty, same size. The only difference is whether the meaning is grounded. If the two models look the same inside, the structure comes from grammar and uncertainty, not meaning. That null result would be worth reporting. (Proposed)

There is a broader question in the same neighborhood. A finished building can look impossible once the scaffolding comes down. A pyramid looks like it could not have been built, until you find the ramps. A trained model is like that. We see the finished behavior, and not the internal tools the training built to reach it. Each arm of this study asks the same question of a different task: what hidden scaffolding does this task build, and what does it leave standing? (Proposed)

The prediction, labeled Proposed: little spread and no contextuality in the Z80 arm. Open-slot structure in the Jabberwocky arm. The full picture only in language. If that holds, the ghost of meaning is in the language, not the mechanism, because the mechanism never changed. If it fails, and a Z80 emulator grows a reportable workspace, that is a finding too.

## A Few Experiments You Can Run

These are clues, not measurements. Each works in any chatbot.

Give it "The crane reached down toward the" and ask for ten endings. Then add one more word, "steel" or "water," and watch the endings collapse.

Give it "The blorg flurbled the snorble flambly." Ask what the blorg did, to what, and how. It will answer from syntax alone.

Slip a hint into a question. Then ask it why it answered as it did. See whether the hint appears in its explanation. Often it does not. People do the same. (Established: Turpin et al., 2023; Nisbett and Wilson, 1977)

## The Door to the Mind

That last experiment points at the oldest version of the ghost. A model writes an explanation of its answer, and the explanation is one more thing written at the write head. It is built from the record, not read off the process.

A speaker uses a word whose choosing they cannot see. My earlier essay, *Opacity Dualism*, asked whether that limit is structural. In teleportation, Bob can use a state he cannot read. The J-space gives the question a shape that can be measured in a machine: what a system can report, and what does its work in silence. Whether the same shape holds in a person is a question for the next essay. (Proposed)

## What This Does Not Establish

It does not show that a language model is a quantum system, or that its contextuality is quantum. It does not show that grammar is teleportation; it shows they share a mathematical shape. It does not show that open slots cause meaning, or that the J-space is consciousness. None of the four arms has been run, and none of the predictions is a result. It offers a comparison, a thesis, and a study, and reports where the comparison holds and where it breaks.

## The Write Head

In teleportation, the state moves without being read. In a sentence, the relations move without the content being known. The blorg flurbled the snorble, and you understood what happened without knowing what any of it was.

In the machine, the dice are ours and the menu is ours. Everything nature hides at the edge of now, the machine shows, except one thing: why those odds. They were set by people writing down what they meant, without knowing how they chose the words.

*Syntax builds the slots. Meaning arrives in the open ones. The odds are inherited.*

## Reading and References

Abramsky and Coecke (2004), LICS. Bennett et al. (1993), *Phys. Rev. Lett.* 70, 1895. Coecke, Sadrzadeh and Clark (2010), *Linguistic Analysis* 36, 345. Gurnee et al. (2026), arXiv:2607.15495. Lambek (1999), LNCS 1582, 1. Lo, Sadrzadeh and Mansfield (2024), arXiv:2412.16806. Nanda et al. (2023), ICLR. Nisbett and Wilson (1977), *Psychological Review* 84, 231. Pallier, Devauchelle and Dehaene (2011), *PNAS* 108, 2522. Power et al. (2022), arXiv:2201.02177. Turpin et al. (2023), arXiv:2305.04388.

---

**Companion essay:** [Cornering the Ghost](https://github.com/mpe-framework/Cornering-the-Ghost-) — quantum teleportation and the arrival of now.

**The studies:** each proposed study is set out plainly in [PROPOSED_STUDIES.md](PROPOSED_STUDIES.md), with what it tests and what result would count against it.

**Responses welcome.** If you think something here is wrong, have a better source, or have run one of these studies, start a conversation in [Discussions](https://github.com/mpe-framework/The-Write-Head/discussions), or open an [issue](https://github.com/mpe-framework/The-Write-Head/issues) for a specific correction. Every claim is labeled so you can tell which ones are load-bearing. Null results are as welcome as positive ones.
