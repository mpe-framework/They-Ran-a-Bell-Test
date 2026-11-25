# They Ran a Bell Test on a Language Model
*Where the ghost sits when a machine chooses a word*

**Troy Teno | November 2026**
*Essay — Not Peer Reviewed. Companion to Cornering the Ghost. Established marks a result supported by a cited source, which may be a preprint. Reading marks my way of putting established pieces together. Proposed marks a connection that still needs a model or a test.*

## The Headline

Early in 2026, a headline came across my feed. Someone had run a Bell test on a language model, and the model had failed it.

Failing was not the strange part. A Bell test is how physicists showed that two particles, far apart, can act as one object, as if the space between them did not matter. Einstein called it spooky. To me, spooky has always meant the ghost: the part we have not explained.

I had been living with a ghost of my own for a while. A thought starts in my head. Neurons fire, muscles move, air shakes, an eardrum moves, and chemistry and electricity rebuild something close to that thought in someone else. Every step loses something. Put a computer in the middle and it still works. Something carries through all of it. I call it a semantic wave, and I cannot tell you what it is made of.

My head was full of other ghosts too. Susskind's holographic universe, where everything inside a region can be written on its boundary, like a program's entire rulebook saved as one flat file. Every law is in the file. Nothing in it says how the game will be played. I kept seeing that pattern: in physics, in the maze of Westworld, in these machines. All the rules knowable. The play, from outside, never quite.

At the same time, I was having conversations with language models that should not have been possible. They were unreasonably reasonable. I had started asking why, and what "reasonable" even means. Then a headline said these machines show the same kind of statistics as entangled particles. I had to know what that meant.

*Cornering the Ghost* took on the other famous piece of quantum spookiness, teleportation, and found that almost all of it is geometry, except one step. This essay does the same with the Bell test. The researchers' own title calls what they found quantum-like contextuality. The "like" is honest. Nothing in the model is quantum. Once you see how the model reads a sentence, the result is what we should expect. Almost all of it is geometry, except one place. It is the same kind of place.

## First Pictures

On my first read, two pictures stuck with me.

The first was crane and crane. The bird and the machine are spelled the same and sound the same. No microscope separates them. Only context does. That felt like two identical particles with no hidden difference inside them. It turned out to be half right. In BERT, the model used here, both cranes really are a single identical point in the model's word table. But the researchers' test compares two different words, not two senses of one word. (Reading)

The second was light. Along a light ray, no time passes. Leaving and arriving are the same moment. The space of words felt like that: every word present at once. That part turned out to be literal. At every choice, the model scores its entire vocabulary in one step, about 30,000 words for BERT, all together. (Established; the link to light is a picture)

## What a Bell Test Asks

*Cornering the Ghost* used a spreadsheet. Here it is slowly.

Alice and Bob each have a detector with two settings. Call Alice's settings A1 and A2, and Bob's B1 and B2. They share a pair of particles, one each, prepared together and then carried far apart. On each run, each of them picks one setting, without knowing what the other picked, and writes down a result: plus or minus.

One run gives one row: Alice's setting, her result, Bob's setting, his result.

After thousands of runs, sort the rows by which pair of settings was picked. There are four possible pairs: A1 with B1, A1 with B2, A2 with B1, A2 with B2. So there are four tabs, one for each pair of settings, not one per person. Each tab has two columns: Alice's results and Bob's.

Look at one column alone and it is a coin toss: half plus, half minus. Alice, reading only her own results, learns nothing about what Bob chose. The pattern appears only when the two columns sit side by side. Then they are clearly connected. (Established)

## Gloves, and Why Particles Are Not Gloves

A connection across distance is not strange by itself. Put a pair of gloves in two boxes and drive one box across the country. Open yours, find a left glove, and you know the other is a right. The gloves were separated, but the connection was set when they were packed. Each box carried its answer the whole way.

That is the master sheet. One row per pair, with every answer written in before anyone looks. If particles were like gloves, each would carry a written-in answer for every setting, and each tab would be that sheet with the unasked columns hidden. Physicists call these written-in answers local hidden variables.

Bell found a way to test for the sheet. The particle data come out like this. On three of the tabs, A1 with B1, A1 with B2, and A2 with B1, Alice and Bob match about 85 percent of the time. On the fourth, A2 with B2, they differ about 85 percent of the time.

Now follow the written-in answers like a chain. A2 usually equals B1. B1 usually equals A1. A1 usually equals B2. Each link fails only about 15 percent of the time. On any single row, if A2 and B2 disagree, at least one of those three links must have broken. So with written-in answers, A2 and B2 can disagree at most 15 plus 15 plus 15, or 45 percent of the time.

The particles disagree about 85 percent of the time. No sheet of written-in answers can do that, and neither can any shuffled mix of such sheets. The particles are not gloves. (Established: Bell, 1964; Clauser et al., 1969)

What is left is stranger. An entangled pair does not have one state for each particle. It has one state for the pair. The pair's possibilities live in a bigger table than either particle's alone, the two multiplied together rather than added, and an entangled state is one that cannot be split into Alice's piece and Bob's piece. The pair is one object spread across two places. (Established)

And there is no answer on either end until it is measured. This is not Alice's measurement causing Bob's result. When they are far apart, which of them measured first depends on who is watching, and the results come out the same either way. Nor can either of them use it to send a message, because each column alone is still a coin toss. The connection is real, and it is not written down anywhere in advance. (Established)

That failure of the tabs to come from one master sheet has a general name: contextuality. Abramsky and Brandenburger showed it can be defined for any system whose local views each make sense but have no single global sheet behind them. Entangled particles are one such system. Nothing in the definition requires physics. (Established: Abramsky and Brandenburger, 2011; Abramsky, 2013)

## Why Anyone Thought to Look

Nobody runs a Bell test on a language model by accident. The idea came from a bridge built twenty years earlier.

In 2004, Abramsky and Coecke redrew quantum mechanics as diagrams: wires for systems, a cup for an entangled pair, a cap for a joint measurement. Teleportation became a single drawing. A few years later, Coecke, Sadrzadeh and Clark showed that grammar can be drawn with the same kind of diagrams. A verb's hooks for its subject and object are cups. When the nouns arrive, the wires pull straight, and a sentence's meaning is computed. (Established: Abramsky and Coecke, 2004; Coecke, Sadrzadeh and Clark, 2010)

That is a match between two ways of drawing, not proof that the processes are the same. BERT is not built from these diagrams. The diagrams are why anyone thought to test it. Whether a model's internal space actually carries the diagrams' hooks is a separate, open question.

What is not open is that something in the model does the job of grammar. Its structure can be read back out of the model's internal states, and brain imaging finds regions that track the same kind of structure in people. The brain and the model do not share a mechanism. What they appear to share is structure, and structure is what this mathematics tracks. Lambek's grammar is one clean way to write that structure down. Nature's version may look different. (Established: Hewitt and Manning, 2019; Pallier, Devauchelle and Dehaene, 2011)

But once grammar is drawn with the same pictures as entanglement, the next question is obvious: do the statistics show the same refusal to glue? Lo, Sadrzadeh and Mansfield went and looked.

## What They Actually Did

They built a small story with a pronoun in it, so the model has to decide what the pronoun points to:

*There is an apple and a strawberry. The [blank] is red and the same one is round.*

The model fills the blank. It gives a probability for "apple" and a probability for "strawberry." The researchers keep only those two, rescaled to add up to one, which is the same as asking the model to choose between just those two words. (Established: Lo, Sadrzadeh and Mansfield)

Then they build the spreadsheet. Instead of detector settings, there are clues. The three sentences loop: the red one is the same one as the round one; the round one is the same one as the sweet one; the sweet one is the other one from the red one. Each sentence is one tab. A master sheet would be one fixed answer for each clue. But no fixed answer can satisfy all three. If red and round are the same noun, and round and sweet are the same, then sweet and red are the same, and the third sentence says they are not. The contradiction is built into the wording, like a staircase in a drawing that climbs forever. (Established: Lo, Sadrzadeh and Mansfield)

So the question the tests ask is narrower than it first sounds. Not whether the tabs glue, because by design they cannot, but whether BERT's odds shift enough between the three sentences to explain the contradiction away.

The two tests draw that line in different places. The sheaf test counts a case only when BERT is close to undecided in all three sentences, between about 42 and 58 percent each time. Out of 51,966,480 cases built from pairs of nouns and descriptions in Simple English Wikipedia, 77,118, about 0.15 percent, passed. Contextuality-by-Default counts a case unless the three sentences pull BERT in clearly different directions. Most cases sat right at its threshold, with BERT nearly certain each time, and 36,938,948, about 71 percent, landed just inside. In this setup, every sheaf case is also a CbD case. (Established; where the cases sit is read from the paper's figures)

So the headline was right in its way. In that constructed setting, the model's tabs refuse to glue.

## Why We Should Expect This

Part of the answer is in the wording: the puzzle is contradictory by design. The rest is in how the model reads.

Here is the difference that takes the spookiness out.

In a Bell test, what makes the result strange is distance. Bob's setting is far away. Alice's particle has no way to know it. If her result still depends on the whole arrangement, something is going on that ordinary pictures cannot explain.

In a language model, nothing is far away. The context is the sentence, and the model reads the whole sentence at once. When it decides what "the red one" points to, the other clue, round or sweet, is right there in the same input, feeding the same calculation. Of course the answer depends on it. (Reading)

A master sheet would need the model to store one fixed answer per clue, "the red one is the apple," that holds no matter what else the sentence says. The model stores nothing like that. It computes every answer fresh, from every sentence. Three sentences give three separate calculations, and nothing forces them onto one sheet. Where the model is sure, all three calculations land on the same answer, and the tabs glue by default. Where the odds sit near even, small differences between the sentences are enough to break the chain. (Reading)

The data show this directly. In the particles, two tabs that share a setting always agree about it, because nothing can travel between them in time. In the model's data, two tabs that share a clue often do not agree, because the partner clue changes the answer. That is why the researchers had to use tests that correct for it. Particles cannot do this. Sentences do it all the time. (Established, as the paper's method; Reading, as the contrast)

So the surprise would have been the other way around. A model that read every sentence and always glued would be the strange one. What the researchers found is contextuality of statistics in a system whose whole job is to depend on context. It is real, it is measurable, and it is what we should expect.

## The Equation

The researchers also derived an exact equation for what decides the model's choice.

When the model chooses between two words, it gives each a score. The difference between the two scores is called the logit gap. At the model's last step, the gap equals the model's internal state at the blank, dotted with the difference between the two words' vectors, plus a small fixed offset. The balance between the two probabilities follows a smooth S-curve of that gap: even odds when the gap is zero, near certainty when it is large either way. (Established: Lo, Sadrzadeh and Mansfield, Proposition 7.1)

In symbols: Δl = p · Δx + Δb, where p is the model's internal state, Δx is the difference between the two words' vectors, and Δb is the difference between their offsets. The balance between the two probabilities is tanh(Δl / 2).

Then they connect it to contextuality. The closer the odds sit to even, the more room there is for the tabs to refuse to glue. Near certainty, every tab says the same thing, and the sheet glues easily. Anything that pushes the gap toward zero pushes the case toward contextuality. (Established, as their reasoning)

## One Direction Out of Hundreds

A dot product reads how far one arrow reaches along another. So the gap depends on only one thing about the model's internal state: how far it reaches along the single arrow that runs from one word to the other. BERT's internal state has 768 directions. The choice between apple and strawberry reads exactly one of them. You can move the internal state any way you like, square to that arrow, and the odds between the two words do not change. (Established, exact)

So many different internal states give exactly the same odds. They lie on flat slices through the space, all parallel to the sheet where the choice flips.

Narrowing to two words makes the choice simple. It does not make the words simple. Both word vectors, and the model's state, were shaped in training against everything else the model knows. (Reading)

## How the Space Was Built

What does it mean for two words to be close?

Before I read any of this, I had a guess. Survey people. Ask where "dog" falls between love and hate, where "mother" falls, where "house" falls. Do that for every word, on every scale, and stack the sheets. Each sheet is a dimension. Psychologists did nearly this in the 1950s, rating words on scales like good and bad, hot and cold, strong and weak. (Established: Osgood, Suci and Tannenbaum, 1957)

BERT's space was built differently. Nobody surveyed anyone. Nobody labeled the sheets. BERT began with every word as a random arrow of 768 numbers. At the start, "apple" was no nearer to "strawberry" than to "Tuesday."

Then it played a guessing game. Take a real sentence. Hide a few of its words. Let the model guess what fills each blank. When it guesses wrong, nudge the numbers a tiny amount toward the right answer, and move to the next sentence. BERT played this game across about 3.3 billion words of books and English Wikipedia. (Established: Devlin et al., 2019)

Nobody reads those sentences or hands out the nudges. The hidden word is its own answer key. A procedure called backpropagation works backward through the model after every guess and works out, for each of its hundred-odd million numbers, which way to move to give the right word a little more probability next time. Then every number takes a tiny step that way. It is a control loop that runs itself: setpoint, error, correction, next sentence. People write the loop and choose the text. The loop does the rest. (Established)

Slowly, words that fit the same blanks settle near each other. "Apple" and "strawberry" both fit "I ate a ___ for lunch," so they end up close. "Apple" and "Tuesday" rarely share a blank, so they end up far apart. No one decides where a word goes. The blanks decide.

So closeness here does not mean sameness of meaning. It means two words compete for the same open slots. "Hot" and "cold" are opposites, and they sit near each other, because both fit "the water was ___." They even line up along a shared direction, a line of degree, with "warm" in between. The grammar of a sentence, which word attaches to which, can be read back out of the space with simple tools. (Established: Kim and de Marneffe, 2013; Hewitt and Manning, 2019)

The sheets I imagined are in there, in a sense. Nobody labeled them, and they are mixed together. The geometry is the shape of the task.

A word with two senses, like "crane," has one point in the word table. The model tells the senses apart only later, as the word's internal state moves with the sentence around it. (Established: Ethayarajh, 2019)

Even nonsense has slots. Ask a model what happened in "The blorg flurbled the snorble," and it will tell you who did what to whom. Syntax builds the slots before meaning arrives. The space in which contextuality is measured was built from slots too. (Reading)

## The Geometric Law

The researchers found one more thing. How contextual a case was could be predicted, a little, from distance.

The two candidate nouns sit at two points in the space. The closer those points sat, the more contextual the case tended to be. Among the features they tested, straight-line distance between the nouns was the best predictor. Among the most similar one percent of noun pairs, the share of contextual cases rose under both tests: from 0.148 percent to 0.50 percent under the sheaf test, and from 71.1 percent to 81.83 percent under Contextuality-by-Default. (Established)

That fits the expectation. Apple and strawberry fill many of the same blanks, so they sit close, and a sentence has to work to tell them apart. Odds sit nearer even, and the chain breaks more often. Apple and engine rarely share a blank, so almost any sentence separates them.

But the law is weak. Across the whole dataset, distance explains less than one percent of the variation in contextuality. Even among the most similar pairs, it explains only six to eight percent, depending on the test. It is a real tendency, not a rule. (Established)

## The Assumption

The researchers get from the equation to distance through one assumption, which they state themselves.

Two arrows go into the equation. The first runs between the two candidate words, from apple to strawberry. Its length is the distance between them. The second comes from the sentence. When the model reads the sentence, it builds an internal state at the blank: one arrow that points the way the sentence leans, as strongly as it leans. Call it the sentence's pointer.

The gap is how far the sentence's pointer reaches along the line between the two words. That is three things multiplied together: the length of the line, the strength of the pointer, and the angle between them. A pointer aimed along the line gives a large gap. A pointer aimed square to the line favors neither word, however strong it is.

The assumption concerns the pointers from many different sentences. It says they point in every direction equally often. The word for that is isotropic. If it is true, the angles average out, and the only thing left to set the typical gap is the length of the line. Farther apart means a bigger gap and less contextuality. The paper says plainly that this step is an approximation. (Established: Lo, Sadrzadeh and Mansfield)

## Where the Picture Breaks

There is good reason to doubt the assumption. Picture the whole space with a center point, and every internal state as an arrow from that center. If the arrows spread evenly, they would point everywhere, like a lamp with no shade. In 2019, Ethayarajh found they do not. In models like BERT, they bunch into a narrow beam, like a flashlight, and most directions in the space go nearly unused. (Established: Ethayarajh, 2019)

That beam is the whole vocabulary leaning one way, related words and unrelated ones alike. Similar words then cluster more tightly inside it.

If the sentences' pointers crowd into that beam, the angles stop averaging out. A long line between two words that lies across the beam can still get a small gap, and a short line lined up with it can get a large one. Distance alone would then predict the gap badly, because the angle is doing much of the work.

That may be why the law is weak. If the pointers lean in favored directions, distance is only part of the story, and the missing part is alignment. (Proposed)

My early essays went wrong in the same place. I called this the parallax lever and wrote as if nearness itself were the source of the leverage. I was measuring the length of the line and ignoring the angle of the pointer.

## Where the Ghost Sits

In *Cornering the Ghost*, teleportation and ordinary time matched everywhere but one step. A teleporter without its correction delivers noise. Nature without correction delivers facts. The difference was the choice of basis, the set of possible outcomes, made by the environment. We did not choose it, and we are part of that environment. The ghost sat there.

Here, the exact part of the account holds everywhere but one place: the sheet where the gap is exactly zero and the choice between apple and strawberry flips. Away from that sheet, the outcome is settled, and the tabs glue. Near it, the odds are even, and the tabs can refuse to glue. Everything contextual in this picture gathers at that edge.

The three sentences all draw from the same space, built from everything the model has read. They share one whole. They still cannot share one master sheet, and by now that should not surprise us.

So the pattern repeats. In both cases, geometry explains almost everything people call spooky. In both cases, one place is left over. It is where possibilities pile up at a point where pieces join and one of them has to be taken. That may be as close to a definition of context as I can get. (Reading)

There is one difference, and it should be said plainly. In nature, nobody outside the system picks the outcome. In the machine, we do. The model never chooses. It fills the slots and produces odds. A sampler we installed, or a rule that takes the likelier word, does the choosing. In nature, nobody holds the dial. In the machine, we do. What stays open is why the sentence's pointer lands where it does: why this sentence leans toward apple, and by how much. Training on text people wrote set that. (Reading)

## The Heads That Knew

There is a stranger thing near that edge.

Inside a model, many attention heads each offer a partial view of the same word, and the model fuses those views into one. When researchers look at individual heads, or at the model's state halfway through, they sometimes find the right answer already there, then find the finished model saying something else. In one well-studied case, the correct answer can be read out of the middle layers and is then overridden by later heads. In another, backup heads sit idle while a main head does the work, then step in when the main head is removed. Anthropic's recent work on turning a model's internal states into readable text aims at exactly this: what a model holds but does not say. (Established: Halawi, Denain and Steinhardt, 2023; Wang et al., 2022; McGrath et al., 2023; Anthropic, 2026)

I ran into a small version of this in my own toy models. Two heads trained side by side collapsed into one working head and one idle one. Remove the idle head, and almost nothing changed. I called it the lazy attractor: the cheapest arrangement training could find. Starting the heads in different directions broke it. (Glass Attention Workbench, Scripts 029A and 029C)

In spreadsheet terms, these are local views, each fine on its own, discarded when the global answer is assembled. That is not contextuality by itself. A signal can be readable without being used, and noise can look like knowledge if you probe hard enough. The test is causal: put the idle head's view back into the output and see whether the answer changes. But it has the same shape: true locally, lost in the gluing. And it happens where the margin is thin. If there is still a mystery in these machines, this is where I would look. (Reading)

## The Experiment

Here is the experiment this essay proposes. It is small enough to run on a laptop, and it can fail.

Build the researchers' apple-and-strawberry setup in plain arithmetic, with every number visible: two word vectors, a sentence pointer for each of the three sentences, their exact equation for the odds, and their two tests for whether the tabs glue. Then run it twice. In the first run, the pointers point in every direction equally. In the second, they crowd into a narrow beam, the way Ethayarajh found real ones do. In both runs, vary the distance between the two words.

Three predictions, written down before running:

1. The odds follow the equation exactly. If not, the build is wrong; stop.
2. When the pointers point in every direction, distance predicts contextuality well.
3. When the pointers crowd into a beam, distance predicts contextuality poorly, and adding the angle between the beam and the word arrow recovers most of what is missing.

If the third prediction holds, it explains why the published relationship is weak. It also points to a better measure than raw distance: distance together with alignment, or the gap itself. If it fails, and distance predicts just as well inside the beam, the assumption holds up better than I expect, and that is worth reporting too.

A second stage would take the same measurements on BERT itself: how strongly its pointers at the blank crowd into a beam, and whether alignment adds to distance in predicting the published results. (Proposed)

Interpretability tools such as the logit lens read the words a model is about to produce next. Anthropic's newer J-lens reads words a model is likely to say a little further ahead. This experiment works at the simplest level: the next word, between two choices.

## Try It Yourself

These are clues, not measurements. They work in any chatbot.

Type "There is an apple and a strawberry. One of them is red and the same one is round. Which is it?" Then change the clues: round and sweet; sweet and red. Watch which way it leans, and how sure it sounds.

Type "The crane reached down toward the" and ask for ten endings. Then add one word, "steel" or "water," and watch the endings collapse to one meaning.

Type "The blorg flurbled the snorble flambly." Ask what the blorg did, to what, and how. None of the words mean anything. It will answer anyway, from grammar alone.

## Perfect Geometry Decides Nothing

Emmy Noether showed in 1918 that every exact symmetry goes with something that never changes. Perfect geometry holds things in place. A ball balanced exactly on a hilltop has no reason to roll either way. It waits for an imperfection. And a computer working with exact real numbers cannot, in general, even confirm that two numbers are exactly equal. It can find a difference if there is one. If there is none, the checking never ends. (Established)

Put those beside the sheet where the choice flips. At exactly zero gap, the equation favors neither word, and in exact arithmetic it cannot even certify that it is at zero. Whatever chooses there is not the geometry. It is what breaks the balance: a little noise, the sampler's roll, the next word in the sentence.

Perfect geometry holds everything in place and decides nothing. The decision comes from what breaks it. (Reading)

## What This Does Not Establish

It does not show that a language model is quantum, or that its contextuality is the contextuality of particles. It does not show that grammar is teleportation. It shows they can be drawn alike. It does not show that any theorem about quantum systems applies to a model's word vectors. It does not show that the experiment will come out as predicted. It has not been run. It does not show that idle heads know anything. A readable signal is not a used one. It does not explain why these models are as reasonable as they are. That question started this, and it is still open. The equation is the researchers'. The one-direction point follows from it. The argument that the result should be expected, the question about the assumption, and the experiment are mine. And this essay delivers only half of what *Cornering the Ghost* promised. It carries the structure into language. The mind is left for the next essay.

## The Promise, Kept

*Cornering the Ghost* found the ghost at the one step nature never takes. This essay finds it in the same corner, at the one sheet the geometry cannot decide, and finds it smaller there, because in the machine we hold the dial.

The headline said the model failed a Bell test. It did, and it should have. Particles that fail a Bell test are strange because their context is far away. A sentence carries its context with it. The model did what language has always done: it left a word open until context closed it. The measurement shows where that happens. The equation shows why it trembles there. The assumption is where we look next.

*The measurement is real. The equation is exact. The result is what we should expect. The ghost is at the edge where the choice flips.*

## Reading and References

Abramsky (2013), "Relational databases and Bell's theorem," LNCS 8000, 13.

Abramsky and Brandenburger (2011), "The sheaf-theoretic structure of non-locality and contextuality," *New Journal of Physics* 13, 113036.

Abramsky and Coecke (2004), "A categorical semantics of quantum protocols," LICS.

Anthropic (2026), "Natural Language Autoencoders: Turning Claude's thoughts into text."

Bell (1964), *Physics* 1, 195.

Clauser, Horne, Shimony and Holt (1969), "Proposed experiment to test local hidden-variable theories," *Physical Review Letters* 23, 880.

Coecke, Sadrzadeh and Clark (2010), "Mathematical foundations for a compositional distributional model of meaning," *Linguistic Analysis* 36, 345.

Devlin, Chang, Lee and Toutanova (2019), "BERT: Pre-training of deep bidirectional transformers for language understanding," NAACL 2019.

Ethayarajh (2019), "How contextual are contextualized word representations?" EMNLP 2019.

Gurnee et al. (2026), "Verbalizable representations form a global workspace in language models," arXiv:2607.15495 (preprint).

Halawi, Denain and Steinhardt (2023), "Overthinking the truth," arXiv:2307.09476.

Hewitt and Manning (2019), "A structural probe for finding syntax in word representations," NAACL 2019.

Kim and de Marneffe (2013), "Deriving adjectival scales from continuous space word representations," EMNLP 2013.

Lo, Sadrzadeh and Mansfield, "Quantum-like contextuality in large language models," *Proceedings of the Royal Society A* (2025), doi:10.1098/rspa.2024.0399; preprint arXiv:2412.16806.

McGrath et al. (2023), "The Hydra effect," arXiv:2307.15771.

Noether (1918), "Invariante Variationsprobleme."

Osgood, Suci and Tannenbaum (1957), *The Measurement of Meaning*, University of Illinois Press.

Pallier, Devauchelle and Dehaene (2011), "Cortical representation of the constituent structure of sentences," *PNAS* 108, 2522.

Wang et al. (2022), "Interpretability in the wild," arXiv:2211.00593.

Cornering the Ghost: github.com/mpe-framework/Cornering-the-Ghost-

---

**Companion essay:** [Cornering the Ghost](https://github.com/mpe-framework/Cornering-the-Ghost-) — quantum teleportation and the arrival of now.

**Responses welcome.** If you think something here is wrong, have a better source, or have run the experiment, start a conversation in [Discussions](https://github.com/mpe-framework/They-Ran-a-Bell-Test/discussions), or open an [issue](https://github.com/mpe-framework/They-Ran-a-Bell-Test/issues) for a specific correction. Every claim is labeled so you can tell which ones are load-bearing. Null results are as welcome as positive ones.

*An earlier, shelved essay, The Write Head, is kept in [archive](archive/).*
