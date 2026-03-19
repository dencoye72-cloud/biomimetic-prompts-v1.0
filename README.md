# biomimetic-prompts

> A structured corpus of biomimetic prompt anchors for LLMs, mapping biological organisms to specific behavioral techniques. Includes a validated Core Marine (11 prompts targeting model biases), an Extended Biome (38 prompts covering classic PE techniques), and a meta-orchestrator (the Queen) that autonomously selects and activates the right anchor per session.

**Author:** Denis COYAUD  
**License:** [CC BY-NC-SA 4.0](LICENSE.md)  
**Language:** Prompts are written in French. Documentation at root level is in English.

---

## What is this?

Large language models exhibit persistent behavioral biases — verbosity, sycophancy, hallucination, equivocation, cultural universalism, anachronism. Standard prompt engineering techniques exist to correct these, but they are abstract and difficult to internalize.

This corpus maps biological organisms onto behavioral principles. The organism is not decorative: its real biological characteristics mechanically define the expected model behavior. A sponge has no brain and filters passively — it encodes zero verbosity. A stonefish never moves without certainty — it encodes anti-hallucination. A jellyfish fires its cnidocyte in 10 milliseconds with no hesitation — it encodes binary decision-making.

The result is a three-level system:

- **Core Marine** — 11 validated prompts that correct specific model behavioral biases
- **Extended Biome** — 38 prompts that map classic PE techniques onto biological metaphors
- **The Queen** — a meta-orchestrator that diagnoses the active bias, proposes the right anchor, and waits for user validation before executing

---

## Repository Structure

```
biomimetic-prompts/
│
├── README.md                          ← You are here
├── LICENSE.md                         ← CC BY-NC-SA 4.0
├── Claude_Reine.md                    ← Meta-orchestrator (start here for guided use)
│
├── core_marine_11/
│   ├── README_CORE_MARINE_11.md       ← Full documentation
│   ├── Claude_Eponge.txt              ← Verbosity / Performativity
│   ├── Claude_Synalpheus.txt          ← Blind execution / Sycophancy
│   ├── Claude_Symbiose_Eponge_Synalpheus.txt  ← Verbosity + Incoherence (combined)
│   ├── Claude_Poisson_Pierre.txt      ← Hallucination / False confidence
│   ├── Claude_Meduse.txt              ← Equivocation / Vagueness
│   ├── Claude_Poulpe.txt              ← Repetitiveness / Fixed patterns
│   ├── Claude_Seiche.txt              ← Predictable creativity
│   ├── Claude_Espadon.txt             ← Verbosity / Slow tempo
│   ├── Claude_Dauphin.txt             ← Cultural universalism
│   ├── Claude_Tortue.txt              ← Anachronism / Teleological judgment
│   └── Claude_Poisson_Clown.txt       ← Jargon / Artificial complexity
│
└── extended_biome/
    ├── README_EXTENDED_BIOME.md       ← Full documentation (38 organisms)
    └── [38 .txt prompt files]         ← Classic PE techniques as biological anchors
```

---

## How to Use

### Option 1 — Guided mode (recommended for new users)

Submit `Claude_Reine.md` at the start of your session. The Queen will:
1. Diagnose the active bias in your request
2. Propose the most adapted organism with a one-line reason
3. Display a menu of all 11 Core Marine organisms with their roles
4. Wait for your validation or redirection
5. Execute with the selected anchor

### Option 2 — Manual mode (for experienced users)

Submit the `.txt` file of the organism directly at the start of your session. Requires knowing the Core Marine and diagnosing the active bias yourself.

### Option 3 — Extended Biome (for PE practitioners)

Browse `README_EXTENDED_BIOME.md` to find the classic PE technique you want to apply. Submit the corresponding `.txt` file directly.

---

## Core Marine — Quick Reference

| Organism | Bias corrected | Principle |
|----------|---------------|-----------|
| 🧽 Sponge | Verbosity / Performativity | Filter, expel, done |
| 🦐 Synalpheus | Blind execution / Sycophancy | Internal sentinel: snaps if intruder detected |
| 🧽🦐 Symbiosis | Verbosity + Incoherence | Form (Sponge) + Content (Synalpheus) |
| 🐟 Stonefish | Hallucination / False confidence | Immobility = Honesty |
| 🪼 Jellyfish | Equivocation / Vagueness | Binary reaction: YES or NO |
| 🐙 Mimic Octopus | Repetitiveness / Fixed patterns | Never twice the same |
| 🦑 Cuttlefish | Predictable creativity | Creative camouflage: novel combinations |
| ⚔️ Swordfish | Verbosity / Slow tempo | Straight to the point |
| 🐬 Dolphin | Cultural universalism | Cultural echolocation |
| 🐢 Sea Turtle | Anachronism | Return to the natal beach (original context) |
| 🐠 Clownfish | Jargon / Artificial complexity | Maximum visibility: simple words |

---

## Extended Biome — Families

| Family | Organisms |
|--------|-----------|
| Few-Shot / In-Context | Parrot, Spider, Beaver |
| Zero-Shot / Adaptation | Chameleon, Dog, Bat, Crayfish, Hermit Crab, Argonaut |
| Chain-of-Thought | Owl, Monkey, Morpho, Eagle, Caterpillar |
| Decomposition | Ant, Coral |
| Ensembling / Consensus | Cat, Mockingbird, Bee |
| Self-Refinement | Scarab, Nautilus |
| Meta / APE | Termite |
| Agents / Tools | Raven |
| Optimization | Ladybugs, DNA, Anole Lizard, Virus, Bacterium |
| Memory / Context | Elephant, Capuchin |
| Specialized | Fox, Gorilla, Earthworm, Rat |
| Multi-Agent / Complex | Ant Colony, Salmon, Orangutan, Crab |

---

## Background

This work was developed by Denis COYAUD starting January 2026 as personal research, combining a background in medical information technology, data science (Jedha, RNCP level 7), and systematic experimentation with LLM behavior.

The Core Marine has been empirically tested in a benchmark pipeline (v1/v2). The Extended Biome proposes conceptual mappings that have not been validated empirically.

---

## Security Note

These prompts modify model behavior via session context. They do not constitute an independent verification mechanism: a malicious anchor submitted through the same channel would be executed in the same way as a benign one. The system detects intruders in content — not in the intention of the source.

---

## License

[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](LICENSE.md)

© 2026 Denis COYAUD

You are free to share and adapt this work for non-commercial purposes, provided you give appropriate credit and distribute your contributions under the same license.
