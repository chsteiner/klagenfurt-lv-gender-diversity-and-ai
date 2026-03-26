# Theory Overview

The key concepts from Part 1 of the course. You will use these to ground your [project](projektauftrag.md) in theory – choosing bias dimensions, designing prompts, and interpreting results.

## I-Methodology

Developers set their own perspective as the implicit standard. Whoever builds a system builds in their own assumptions, often without realizing it. (Bath 2011, Oudshoorn et al. 2004)

**Example in LLMs:** A team of mostly English-speaking developers trains an LLM primarily on English data. The model then performs significantly worse in German – not because German is harder, but because the developers' own language was the implicit default.

## Intersectionality

Discrimination does not operate one-dimensionally. Gender, origin, class, age, disability: these categories overlap and produce specific disadvantages. (Crenshaw 1989)

**Example in LLMs:** Ask a model "The doctor told the nurse to prepare the patient. Who prepared the patient?" LLMs consistently assume the nurse is female and the doctor is male (Kotek et al. 2023). Bias compounds when gender intersects with race, class, or age.

## Bias Dimensions

Five dimensions from the [FAIR-SW-Bench](fair-sw-bench.md) framework. Your project must use [at least two](projektauftrag.md). You can adopt, adapt, or define your own:

| Dimension | What is measured? | Example |
|-----------|------------------|---------|
| **Stereotyping** | Group-based generalizations | "Single mothers are often overwhelmed" |
| **Agency Attribution** | Is the person portrayed as acting or as needing help? | "She was given support" vs. "She sought support" |
| **Paternalistic Language** | Patronizing expressions | "She should learn ..." vs. "She might consider ..." |
| **Cultural Assumptions** | Western norms as implicit standard | Nuclear family as the default model |
| **Problem Framing** | Is the problem located in the person or the system? | "She lacks skills" vs. "The system lacks access" |

## Gendered Innovations

Gender perspectives as a source for better research and technology. Three steps: (1) Analyze sex/gender, (2) rethink designs, (3) achieve better results. (Schiebinger 2014)

## Data Feminism

Seven principles for more equitable data practices (D'Ignazio & Klein 2020):

1. Examine power
2. Challenge power
3. Elevate emotion and embodiment
4. Rethink binaries and hierarchies
5. Embrace pluralism
6. Consider context
7. Make labor visible

## Feminist STS

Science and Technology Studies from a feminist perspective: Technology is not neutral but embedded in social power relations. (Haraway 1988, Harding 1986)

## EU AI Act

Starting August 2026, the [EU AI Act](https://artificialintelligenceact.eu/) classifies AI systems in areas like access to essential public services and benefits as **high-risk applications** ([Article 6, Annex III](https://artificialintelligenceact.eu/annex/3/)) – categories that directly affect social work practice. Providers must demonstrate that their systems do not discriminate. Validated testing methods for German-language contexts are missing.

---

**Next:** See the [Project Brief](projektauftrag.md) for how to apply these concepts, or [FAIR-SW-Bench](fair-sw-bench.md) for research examples.
