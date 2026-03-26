# Course Planning: Gender, Diversity & AI

> **Questions?** [christian.steiner@dhcraft.org](mailto:christian.steiner@dhcraft.org)

> **University of Klagenfurt – Master Computer Science – SS2026**

---

## Overview

| Field | Details |
|-------|---------|
| **Title** | Gender, Diversity & AI |
| **ECTS** | 4 (100 working hours) |
| **Contact hours** | ~24.75 hours (6 sessions: 3 in-person, 3 online) |
| **Self-study** | ~75.25 hours |
| **Lecturers** | Susanne Sackl-Sharif (main lecturer), Christian Steiner (guest: AI & Bias) |
| **Target audience** | Master students Computer Science (also BWL and Anglistik students enrolled) |
| **Language** | English |
| **Course website** | [chsteiner.github.io/klagenfurt-lv-gender-diversity-and-ai](https://chsteiner.github.io/klagenfurt-lv-gender-diversity-and-ai/) |

---

## Course Structure

The course has two parts:

### Part 1: Gender and Diversity (Sessions 1–2)
*Led by: Susanne Sackl-Sharif*

Theoretical introduction without direct AI connection. Students learn foundational gender and diversity concepts to later identify and analyze bias in AI systems. Focus on I-Methodology (Bath 2011) as a bridge to computer science: how developers set their own perspective as the implicit standard. The project brief is presented at the end of Session 2.

### Part 2: Gender, Diversity and AI (Sessions 3–6)
*Led by: Susanne Sackl-Sharif with guest contributions by Christian Steiner (DHCraft)*

Applying the theoretical foundations to AI systems. Christian Steiner provides the technical input on AI types and bias manifestations in Session 3. The focus is the student project: independently developing a bias benchmark tool for Large Language Models. Individual work only.

---

## Schedule

### Part 1: Gender and Diversity

| Session | Date | Time | Format | Room | Content |
|---------|------|------|--------|------|---------|
| **1** | Tue 17.03.2026 | 13:30–18:30 | In-person | C.0.16 | Course introduction, gender and diversity input, reflection exercise |
| **2** | Thu 26.03.2026 | 13:30–18:30 | In-person | C.0.16 | Deepening gender and diversity; text discussion; **project brief presented** |

*Between Sessions 2 and 3 (26.03.–27.04.): Read texts, Task 1 (literature overview due 22.04.)*

### Part 2: Gender and AI

| Session | Date | Time | Format | Room | Content |
|---------|------|------|--------|------|---------|
| **3** | Mon 27.04.2026 | 08:15–11:30 | Online | – | **Guest: Christian Steiner** – AI types, bias manifestations, detection methods; present topics; Q&A |
| **4** | Mon 11.05.2026 | 08:15–09:45 | Online | – | Discuss concepts; Q&A on project work |
| **5** | Wed 03.06.2026 | 08:15–11:30 | Online | – | Peer feedback on prototypes |
| **6** | Wed 24.06.2026 | 10:00–16:45 | In-person | C.0.16 | Final presentations |

### Hours Breakdown

| Format | Sessions | Hours |
|--------|----------|-------|
| In-person | Session 1 (5h), Session 2 (5h), Session 6 (6.75h) | ~16.75h |
| Online | Session 3 (3.25h), Session 4 (1.5h), Session 5 (3.25h) | ~8h |
| **Total** | | **~24.75h** |

---

## Milestones

| Deadline | Milestone | Submission |
|----------|-----------|------------|
| 22.04. | **Task 1: Literature overview** – Topic, 2-3 sources, 1 page | .md on Moodle |
| Session 3 (27.04.) | **Present topic** | In session |
| 06.05. | **Task 2: Concept** – Project plan and documentation | .md on Moodle |
| Before Session 5 (03.06.) | **Prototype** – First working version | Prepare short demo |
| Session 6 (24.06.) | **Final presentation + submission** – Finished tool, final documentation | GitHub repo (code + documentation) |

### Async Support

A **Moodle forum** is available between sessions for project questions. Christian Steiner answers technical questions about APIs, bias detection, and tooling. Susanne Sackl-Sharif handles conceptual and theoretical questions.

---

## Project Brief: Bias Benchmark Tool

Students develop their own tool for measuring bias in LLM-generated responses, inspired by the FAIR-SW-Bench framework (concept description, not code). The full project brief is in [PROJECT.md](PROJECT.md).

**Summary:** 10+ custom prompts, 1+ bias dimension, 1+ LLM, documented methodology, working code. Domain, approach, and technical implementation are freely chosen. LLM access free via Ollama (local models) or free-tier web interfaces. Submission as GitHub repo. Individual work.

### What Students Receive

1. **Theoretical foundations** (Part 1): Gender/diversity theories, intersectionality, bias definition
2. **Technical introduction** (Guest Christian Steiner, Session 3): AI types, bias manifestations, detection methods
3. **Conceptual inspiration**: FAIR-SW-Bench description, bias dimensions, prompt variant method (Base/Neutral/Diversity-Aware)

---

## Learning Outcomes

Upon completion, students will be able to:

1. Demonstrate an overview of gender and diversity theories
2. Understand how bias manifests in different AI system types (rule-based, predictive, generative)
3. Design and implement bias detection methodologies for LLMs
4. Gain practical experience with LLM-assisted development tools (coding agents)
5. Deepen their skills in independent project planning and implementation

---

## Grading

| Component | Weight | Assessed by |
|-----------|--------|-------------|
| **Project** (GitHub repo: code + presentation, Tasks 1-3) | 50% | Theory integration, technical implementation, creativity |
| **Documentation** in GitHub repo (Task 4) | 30% | Completeness, methodology, reflection |
| **Participation** | 20% | Attendance (min. 80%), active contribution, peer feedback |

Instead of a written reflection: Final documentation in the GitHub repo. [Promptotyping](https://github.com/DigitalHumanitiesCraft/promptotyping-skill) methodology recommended but not required. Theory integration counts more than code complexity. Details in [PROJECT.md](PROJECT.md).

---

## Prerequisites

> Basic programming skills in at least one language (ideally Python) and willingness to work with LLM-assisted development tools (coding agents). No prior knowledge of Machine Learning or Gender Studies required.

---

## Teaching Methods

| Method | Purpose | Session |
|--------|---------|---------|
| **Input/lecture** | Theoretical foundations (Part 1), technical introduction (Part 2) | 1–3 |
| **Text discussion** | Selected texts from Gender Studies and STS | 2 |
| **Reflection exercises** | Individual and group reflection on gender/diversity | 1, 3 |
| **Project work** | Independent development of the bias benchmark tool | 3–6 |
| **Peer feedback** | Mutual feedback on project progress | 5 |
| **Presentations** | Final project presentations | 6 |

---

## Detailed Content

### Part 1: Gender and Diversity Theories

- Brief history of Gender and Diversity Studies
- De/constructivist approaches
- Definition of bias and discrimination
- Intersectionality
- Social inequalities
- Texts from Science and Technology Studies
- I-Methodology (Bath 2011): How developers set their own perspective as the standard

### Part 2: AI and Bias

- **AI types and their bias manifestations:**
  - Rule-based: Normative thresholds and categories
  - Predictive: Biased training data and labels
  - Generative: Stereotypical patterns in training corpora

- **Empirical findings on gender bias in LLMs** (UNESCO/IRCAI 2024, Kotek et al. 2023):
  - Stereotypical occupational associations
  - "Siloing effect" in gender assignments
  - Effects of post-training on bias

- **Bias detection methods:**
  - Contrastive prompts
  - Systematic output monitoring
  - Audit frameworks (HELM, DecodingTrust)
  - Prompt variant method (Base/Neutral/Diversity-Aware)

- **Preliminary findings from FAIR-SW-Bench:**
  - Diversity Instruction Paradox: Diversity-aware prompts can amplify bias
  - Utility-Safety Trade-off: Bias reduction vs. response quality
  - Google Gemini: Complete blocking of social work prompts in pilot testing
  - EU AI Act: AI systems in essential public services as high-risk applications from August 2026

- **Context Engineering instead of Prompt Engineering:**
  - Curate context rather than craft role prompts
  - Empirical evidence against persona prompting ([Kim et al., ICLR 2025](https://arxiv.org/abs/2408.08631))
  - Relevance for students' tool design

- **Human-in-the-Loop and AI Literacy:**
  - Critical evaluation of AI outputs
  - Keeping decision-making authority with professionals

---

## Research Context

### AI@youthwork

The course builds on findings from the research project **AI@youthwork** (University of Graz, 2024–2025), which investigated AI use in youth work from a gender and diversity perspective.

**Relevant publication:**
> Sackl-Sharif, S., Klinger, S., Pollin, C. & Steiner, C. (2025). Zur ambivalenten Nutzung von Künstlicher Intelligenz in der Kinder- und Jugendarbeit aus einer geschlechter- und diversitätsreflektierenden Perspektive.

### SocialAI (Laura Bassi 4.0)

The course is part of the context of the FFG-funded project **SocialAI** (Laura Bassi 4.0, #62981337, 02/2026–01/2029), which also investigates bias in AI systems for social contexts.

### FAIR-SW-Bench

The **FAIR-SW-Bench** framework (v2.1.0), developed by DHCraft, serves as conceptual inspiration for the student projects:

- Multilingual evaluation system (DE/EN)
- LLM-as-Judge architecture with cross-provider validation
- 50 test scenarios for social work contexts
- 5 bias dimensions: Stereotyping, Agency Attribution, Paternalistic Language, Cultural Assumptions, Problem Framing
- Prompt variant method (Base/Neutral/Diversity-Aware)

**Preliminary pilot study findings (2025):**

- **Diversity Instruction Paradox**: Diversity-aware prompts produced higher bias scores in several cases than neutral variants, especially for Agency Attribution and Problem Framing. Possible explanation: Explicit diversity cues activate latent stereotypes in the model (salience effect).
- **Utility-Safety Trade-off**: Bias reduction may come at the cost of response quality. Diversity-aware variants showed lower bias scores (avg. 3.8) but also reduced helpfulness scores (avg. 4.1) compared to base variants (bias: 6.2, helpfulness: 8.1).
- **Google Gemini blocked all social work prompts** in pilot testing through safety filters that cannot be disabled.
- **Methodological limitation**: Pilot study with 30/50 prompts, single provider (Anthropic), English judge prompts for German outputs, no human annotation. Results require validation.

These findings will be presented in Session 3 so students can use them as a starting point for their own investigations.

---

## Contacts

| Role | Person | Contact |
|------|--------|---------|
| Main lecturer | Susanne Sackl-Sharif | University of Graz |
| Guest: AI & Bias | Christian Steiner | [christian.steiner@dhcraft.org](mailto:christian.steiner@dhcraft.org), [DHCraft OG](https://dhcraft.org) |
| Coordination Klagenfurt | Noreen | University of Klagenfurt |

---

## Open Items

- [ ] Communicate schedule change to Noreen (11.05. as new date for Session 4)
- [ ] Finalize text selection for discussions in Part 1
- [ ] Set up Moodle course
- [x] ~~FAIR-SW-Bench concept documentation for students~~ – integrated in PROJECT.md
- [x] ~~Clarify API costs and access for students~~ – solved: Ollama + free-tier web interfaces
- [x] ~~Align syllabus with current changes~~ – SYLLABUS.md created
- [x] ~~Activate GitHub Pages for Docsify website~~ – done
- [x] ~~Docsify website commit and push~~ – done, Setup Guide added
- [x] ~~Group work decision~~ – changed to individual work only

---

## Change History

| Date | Change |
|------|--------|
| Mar 2026 | Initial version |
| Mar 2026 | Dates from campus system; Session 2 shortened (-2h), Session 4 added as Q&A (+2h on 11.05.) |
| Mar 2026 | Restructured: Project brief in Session 2, guest contribution in Session 3, peer feedback in Session 5, milestones and grading weights added |
| Mar 2026 | Feedback round: Grading simplified (50/30/20), Option B (dataset) removed, Ollama as main recommendation |
| Mar 2026 | FAIR-SW-Bench findings integrated: Diversity Instruction Paradox, Utility-Safety Trade-off, Gemini blocking, EU AI Act context, Context Engineering |
| Mar 2026 | Syllabus alignment: Session 2 to 18:30, Task 1 (literature due 22.04.), concept deadline 06.05., Promptotyping workflow, language set to English, grading 50/30/20 |
| Mar 2026 | Setup Guide, Copilot update, review fixes, all docs translated to English, individual work only |

---

*Created: March 2026*
*Status: Active*
