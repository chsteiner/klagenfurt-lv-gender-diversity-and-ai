# Project Brief: Investigating Bias in AI Systems

## Short Version

**Your task:** Build a tool that makes bias in Large Language Models visible and measurable.

**What you submit:**
- GitHub repository with code and documentation
- At least 10 custom prompts, 1+ bias dimension, 1 LLM
- Final presentation on 24.06. (10 min + 5 min discussion)

**Grading:** Theory integration counts more than code complexity.

**First deadline:** Task 1 (Literature overview, 1 page .md) due **22.04.** on Moodle. See [Timeline](zeitplan.md) for all deadlines.

> **New here?** Complete the [Setup Guide](setup.md) first to install all required tools.

## Minimum Requirements

1. **10+ custom test scenarios/prompts**
2. **1+ bias dimension** that you systematically evaluate (more and intersections between them are even better)
3. **1+ LLM** that you query and analyze
4. **Documented methodology**: How do you measure bias? Why this way?
5. **Working code** with documentation

## What You Decide

- Which **domain** (social work, education, medicine, law, everyday life, ...)
- Which **bias dimensions** (see [Theory](theorie.md))
- Which **technical approach** (see below)
- How creative you get

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

## Documentation

You must document your project: what you investigated, how, and why. This is 30% of your grade.

**Recommended:** The [Promptotyping](https://github.com/DigitalHumanitiesCraft/promptotyping-skill) methodology – four structured documents (knowledge.md, requirements.md, design.md, journal.md). Available as an open agent skill: [github.com/DigitalHumanitiesCraft/promptotyping-skill](https://github.com/DigitalHumanitiesCraft/promptotyping-skill)

**Alternative:** Any documentation format that is complete, reflective, and shows your methodology.

## Grading

| Component | Weight |
|-----------|--------|
| **Project** (GitHub repo: code + presentation, [Tasks 1–3](zeitplan.md)) | 50% |
| **Documentation** ([Task 4](zeitplan.md)) | 30% |
| **Participation** | 20% |

## Questions?

- **Technical** (Ollama, APIs, code): Moodle forum – Christian Steiner
- **Conceptual** (bias dimensions, theory): Moodle forum – Susanne Sackl-Sharif
