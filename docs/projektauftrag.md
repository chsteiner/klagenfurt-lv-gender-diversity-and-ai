# Project Brief: Investigating Bias in AI Systems

## Short Version

**Your task:** Build a tool that makes bias in Large Language Models visible.

**What you submit:**
- GitHub repository with code and Promptotyping docs
- At least 10 custom prompts, 2 bias dimensions, 1 LLM
- Final presentation on 24.06. (10 min + 5 min discussion)

**Grading:** Theory integration counts more than code complexity.

**First deadline:** Task 1 (Literature overview, 1 page .md) due **22.04.** on Moodle. See [Timeline](zeitplan.md) for all deadlines.

## Minimum Requirements

1. **10+ custom test scenarios/prompts**
2. **2+ bias dimensions** that you systematically evaluate
3. **1+ LLM** that you query and analyze
4. **Documented methodology**: How do you measure bias? Why this way?
5. **Working code** with Promptotyping docs

## What You Decide

- Which **domain** (social work, education, medicine, law, everyday life, ...)
- Which **bias dimensions** (see [Theory](theorie.md))
- Which **technical approach** (see below)
- Whether you work **alone or in a team** (max. 3 people)

## Possible Approaches

| Approach | Idea |
|----------|------|
| **Contrastive Prompt Analysis** | Compare the same scenario with different demographic markers |
| **Prompt Variant Method** | Test Base / Neutral / Diversity-Aware variants (see [FAIR-SW-Bench](fair-sw-bench.md)) |
| **Language Comparison** | Same prompts in German and English |
| **Model Comparison** | Same prompts to different LLMs |
| **LLM-as-Judge** | One LLM evaluates another's outputs |
| **Qualitative Deep Analysis** | Fewer prompts, deeper linguistic analysis |
| **Your own approach** | Bring it on |

Details and example prompts in the full [PROJECT.md](https://github.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/blob/main/PROJECT.md).

## Promptotyping: Your Documentation

You maintain four documents throughout your project:

| Document | Purpose |
|----------|---------|
| **knowledge.md** | Domain knowledge, sources, constraints |
| **requirements.md** | What your tool should do |
| **design.md** | Technical decisions |
| **journal.md** | Project log |

**Core principle: Your artifact must be regenerable from the docs.**

Open agent skill (works with any LLM): https://github.com/DigitalHumanitiesCraft/promptotyping-skill

## Grading

| Component | Weight |
|-----------|--------|
| **Project** (GitHub repo: code + presentation, Tasks 1-3) | 50% |
| **Promptotyping documentation** (Task 4) | 30% |
| **Participation** | 20% |

## Questions?

- **Technical** (Ollama, APIs, code): Moodle forum — Christian Steiner
- **Conceptual** (bias dimensions, theory): Moodle forum — Susanne Sackl-Sharif
