# anki learning

A partially automated Anki deck tool I built in tandem with a coding agent to generate cards on whatever I'm trying to learn, so I can study them and ingest the field a bit better.

*This is a personal project. I'm not trying to teach anyone how to learn, just revisiting something that worked for me in college and building on it with what I've picked up since. If you're here, you probably already know Anki is useful. This is my version of it, for my specific interests, with the reasoning written down.*

---

## Background

Picking up a new field means constantly running into terms that feel almost familiar. You can follow a sentence and still lose the paragraph. The issue is usually a few words that aren't fully 'loaded', taking up enough attention that comprehension takes a hit.

Spaced repetition fixes this at the root. Anki has worked well for me before and I wanted a version built around how memory actually works, not just grinding flashcards. I also enjoy it because it gives me a better reason to pull out my phone.

## What's in here

- `cards/ml-vocab.txt` - the cards, TSV format, ready to import
- `pedagogy/scaffold.md` - the learning science behind how cards are designed
- `setup/HOME_INSTRUCTIONS.md` - getting Anki set up and wired to Claude
- `log.md` - running record of what's been added and why (optional)

## Card design (WIP)

So far every concept gets three cards:

- **Definition** - what is it, with a concrete example on the back
- **Application** - when does it matter, what breaks without it
- **Connection** - how it relates to something adjacent

For high-priority concepts there's also a generative card, no definition given, just a prompt to explain it from scratch. Those are the hard ones and the most useful.

The reasoning behind all of this is in `pedagogy/scaffold.md`.

## Current topics

- ML fundamentals (gradient descent, loss functions, regularization, activation)
- Sparse autoencoders and mechanistic interpretability
- Protein structure prediction (AlphaFold2, ESMFold, ESMC)
- Metagenomics and the dark proteome
- Scaling laws and the Bitter Lesson
- Food science (flavor stacking, blooming, emulsification, Maillard, Koji fermentation)

## How it works

You have a coding agent open, you're reading something, a term comes up that you want to own. You drop it in, the agent uses the card schema to design it and writes it straight into your collection. Sync Anki to your phone and you're studying it before the end of the day.

The TSV files here are the cards I've built so far. If you want to generate your own, point your agent at `pedagogy/scaffold.md` so it knows how to design them. Feedback is key — the cards get better as you get clearer on what you actually want to learn and how you want it presented.

Full setup in `setup/HOME_INSTRUCTIONS.md`.

## Adapting this

The structure works for any subject. Swap the cards, keep the pedagogy file, and point your agent at `pedagogy/scaffold.md` so it knows how to design cards worth reviewing.

I want to ground the card design in cognitive science — spaced repetition, retrieval practice, elaborative interrogation, desirable difficulty. I've been reading into it and building what I find into the schema. It's all in `pedagogy/scaffold.md` with citations. I update it when I find better evidence.

I think most people underinvest in how they learn relative to what they're trying to learn. The returns on getting this right compound. Learning how to learn is its own problem worth taking seriously.
