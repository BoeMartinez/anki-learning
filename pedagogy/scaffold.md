# Learning Science Scaffold

This file is the backbone of card design decisions. When new research is added to `sources/`, update this file if it changes how cards should be built.

---

## 1. Spaced Repetition (Ebbinghaus 1885; Wozniak & Gorzelanczyk 1994)

**Principle:** Memory decays along a predictable forgetting curve. Reviewing material at expanding intervals — just before forgetting — is exponentially more efficient than massed practice.

**Application:** Anki handles the scheduling. Do not fight it. Do not cram a deck in one session. Trust the algorithm and show up daily.

**Neuroscience basis:** Each retrieval strengthens the memory trace and resets the decay clock. The harder the retrieval (more time elapsed), the stronger the re-encoding.

---

## 2. Retrieval Practice / Testing Effect (Roediger & Karpicke 2006)

**Principle:** Testing yourself on material produces stronger long-term retention than re-reading or re-studying the same material. The act of retrieving a memory strengthens it more than passively encountering it.

**Application:** Cards must force *active recall*, not recognition. "What is X?" beats "X is defined as ___" (fill-in-the-blank feels active but is pattern-matching). Best card front: a question the learner must answer from scratch.

**Implication for card design:** Avoid giving away the answer structure in the question. "What does the decoder do?" is better than "The decoder [does what]?"

---

## 3. Elaborative Interrogation (Pressley et al. 1987)

**Principle:** Asking "why is this true?" and "how does this connect to what I know?" produces deeper encoding than rote repetition. Elaboration forces the learner to integrate new knowledge with existing knowledge structures.

**Application:** Every concept should have at least one card that asks for explanation or connection, not just definition. "Why does L1 regularization produce sparsity but L2 doesn't?" > "What is L1 norm?"

---

## 4. Desirable Difficulty (Bjork 1994)

**Principle:** Learning is enhanced when conditions are harder during practice — as long as the difficulty is manageable. Easy cards build weak traces. Cards that require real effort to answer produce stronger, more durable memories.

**Application:** If a card is too easy (sub-second answer, never missed), the card is too narrow. Add context, a twist, or an application requirement to increase difficulty. Do not make cards artificially hard — desirable difficulty means *effortful but achievable*.

---

## 5. Interleaving (Kornell & Bjork 2008)

**Principle:** Mixing different topics within a study session produces better long-term retention than blocking (studying one topic exhaustively before moving to the next). Interleaving forces the brain to distinguish between concepts, strengthening discrimination.

**Application:** Do not create separate subdecks per topic and study them in isolation. Keep cards in one deck (or use Anki's random shuffle). The confusion of interleaving is a feature, not a bug.

---

## 6. Dual Coding (Paivio 1971; Mayer 2001)

**Principle:** Information encoded in two forms (verbal + visual, or abstract + concrete) is remembered better than information encoded in one form. Concrete examples serve as an anchor for abstract definitions.

**Application:** Every abstract definition should have a concrete example on the back. Not just "MSA = aligning evolutionary relatives" but "like lining up the hemoglobin gene from 500 species to find which positions haven't changed in 400 million years — those positions are structurally critical."

---

## 7. The Generation Effect (Slamecka & Graf 1978)

**Principle:** Information that a learner generates themselves is remembered better than information passively received. Even wrong guesses improve retention of the correct answer.

**Application:** When a new topic comes up in conversation, try to articulate what you think the answer is *before* being told. The wrong attempt primes better encoding of the correction.

**Card implication:** "Explain X in your own words" cards are higher value than "Define X" cards. Rotate these in deliberately.

---

## 8. The "Claim It" Test (Feynman Technique)

**Principle:** You own a concept when you can generate it from scratch, explain it to a novice, and identify where your explanation breaks down. Recognition is not ownership.

**Application:** For high-priority concepts (Bitter Lesson, scaling laws, MSA), include one card per concept that is explicitly generative: "Explain the Bitter Lesson as if to someone who has never heard of it." This is the hardest card type and the most valuable.

The gap between recognizing a concept and being able to generate it is real and common. These cards target that gap directly.

---

## 9. Spacing + Retrieval > Highlighting or Re-reading (Dunlosky et al. 2013)

**Principle:** Meta-analysis across 10 learning techniques rated: spaced practice and retrieval practice both rated HIGH utility. Highlighting, re-reading, and summarizing rated LOW utility. Students systematically overvalue re-reading because it *feels* productive (fluency illusion).

**Application:** When user is tempted to re-read a dense paper, redirect toward: write one Anki card per key concept instead. The card-writing forces retrieval and encoding; re-reading does not.

---

## 10. Sleep Consolidation (Walker 2017; Stickgold 2005)

**Principle:** Memory consolidation — the process of transferring learning from short-term to long-term storage — happens primarily during sleep. Studying before sleep and reviewing after waking maximizes consolidation.

**Application:** Best study time: morning review (tests overnight consolidation) + evening new material (primes overnight processing). Do not cram late at night and immediately test the next morning — give sleep a night to work.

---

## Card mix target (per concept)

| Card type | Purpose | Priority |
|-----------|---------|----------|
| Definition | Recognition baseline | Required |
| Application / when-to-use | Generative, context-anchored | Required |
| Connection to adjacent concept | Network-building | Required |
| Cloze (for multi-part facts) | Structural recall | Add when natural |
| Feynman generative | Ownership test | Add for high-priority concepts |

---
