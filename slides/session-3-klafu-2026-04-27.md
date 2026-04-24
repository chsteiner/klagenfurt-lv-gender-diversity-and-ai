---
marp: true
theme: default
paginate: true
style: |
  section {
    padding: 56px 72px 52px;
    font-size: 29px;
  }
  section h1 {
    margin-top: 0;
    margin-bottom: 0.35em;
  }
  section h2 {
    margin-top: 0;
    margin-bottom: 0.4em;
  }
  section p,
  section ul,
  section ol,
  section table,
  section blockquote,
  section pre {
    margin-top: 0.4em;
    margin-bottom: 0.4em;
  }
  section li {
    margin-top: 0.18em;
    margin-bottom: 0.18em;
  }
  section img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    max-height: 415px;
    height: auto;
    object-fit: contain;
  }
  section table {
    font-size: 0.9em;
  }
  section th,
  section td {
    padding: 0.3em 0.6em;
  }
  section small {
    font-size: 0.78em;
    line-height: 1.35;
  }
---

<!--
Session 3 – Klagenfurt SS2026 – Gender, Diversity & AI
Guest contribution by Christian Steiner (DHCraft)
Mon 27.04.2026, 08:15–11:30 online

Load-bearing slides (Winston): Empowerment (S2), AI Types opener (S6),
Generative-AI opener (S11), FAIR-SW-Bench intro (S18), Diversity Paradox (S24),
Your Projects opener (S29), Task 2 Checklist (S40), Next Action closing (S41).

Student presentations block: ~45 min in Block 5.
No "Questions?" final slide – Contributions slide stays up during Q&A.

v2 changes after colleague review (23.04.2026):
- Fixed number inconsistency between Finding 1 and 2
- Softened EU AI Act claim
- Removed student names from critique slides
- Unified cluster treatment (all same raster)
- Added Task 2 checklist slide
- Added temperature caveat, scoring rubric note
- Marked FAIR-SW-Bench findings as pilot/exploratory
- Softened role-prompt claim
- Clarified Ollama vs. llama3, RLHF, Promptotyping
- Restructured LLM-as-Judge to lead with manual scoring
-->

<!-- _class: cover -->

# Introduction to Bias Detection in AI

## Session 3 · Gender, Diversity & AI · Klagenfurt SS2026

### Christian Steiner · DHCraft · 27.04.2026 online

---

# After this session you can

**design a bias experiment for your domain that you can defend in Task 2:**

- Pick concrete **bias dimensions** that fit your topic
- Draft **test prompts** in at least two comparable variants
- Choose a **measurement approach** that produces countable data
- Anticipate the **three pitfalls** that trip up every first attempt
  (Diversity Paradox, Utility Trade-off, provider blocking)

**Task 2 deadline: 06.05.2026**

---

# Agenda – 3 blocks, 2 breaks

1. **What counts as AI, and what counts as bias** (~30 min)
2. **FAIR-SW-Bench: one research group's attempt to measure it** (~30 min)
3. **Your projects: clusters, critique, next steps** (~55 min, incl. ~45 min student presentations)

Practical workflow + Q&A interleaved.

---

# Where you are in the 4-task sequence

| Task | What | Deadline | Status |
|------|------|----------|--------|
| **1** | Literature overview | 22.04. | ✅ done |
| **2** | **Project concept** – plan + documentation | **06.05.** | **next** |
| **3** | Project implementation – build your tool | 03.06. / 24.06. | upcoming |
| **4** | Final documentation – results + reflection | 24.06. | upcoming |

**Today's focus:** give you what you need to write Task 2.

---

# Why this matters for you

---

# This is not only a course requirement

- **EU AI Act**: many high-risk-system rules set for **August 2026** (employment, education, healthcare, essential services, law enforcement)
- Validated bias testing methods for German-language contexts barely exist
- Your project contributes to this **applied AI fairness evaluation** gap

*You are prototyping a fairness-testing workflow directly relevant to AI Act compliance debates.*

---

# Three system types often discussed as "AI"

![width:80%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-ai-types.png)

<small>*Three automation logics with different bias sources – not a philosophy-of-AI debate.*</small>

---

# Type 1: Rule-based / Symbolic

**How it works:** fixed if-then rules. Same input → same output. No learning.

**Examples:** social benefits eligibility; insurance premium tiers; traditional credit scoring.

**Where is the bias?** In the rules themselves – who set the thresholds? Which life situations were not considered?

<small>*Historically dominant form of AI research (1950s–1990s); deterministic code.*</small>

---

# Type 2: Predictive (Machine Learning)

**How it works:** learns statistical patterns from past cases. Computes risk scores / classifications. No new content.

**Examples:** Allegheny Family Screening Tool; CV screening classifiers; financial sentiment models.

**Where is the bias?** Many entry points – training data, label definitions, feature selection, proxy variables, sampling, feedback loops.

<small>*Testable with fairness metrics (AI Fairness 360) – but never neutral.*</small>

---

# Type 3: Generative (LLM)

**How it works:** generates text word-by-word; each run → different result.

**Examples:** ChatGPT, Claude, Gemini, local models (Llama, Mistral).

**Where is the bias?** Training data, labels, objectives, post-training (RLHF = reinforcement learning from human feedback), prompts, decoding, evaluation design.

<small>*Often cited: LLMs assigned "she" → "nurse" in ~95% of cases, "he" → "doctor" (Kotek et al. 2023).*</small>

---

# Which type is your project?

| AI Type | Project domains |
|---------|-----------------|
| **Predictive ML** | Financial sentiment models; CV screening classifiers |
| **Generative LLMs** | Mental health, insurance, moral judgement, gender bias in LLM outputs (multiple projects) |
| **TBD / hybrid** | AI literacy / self-determination angle |

**Different AI type = different bias sources = different measurement methods.**

---

# Generative AI: one foundation, three risks

---

# Foundation: The category error

![width:72%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-category-error.png)

**For this course:** use **N ≥ 10 runs per prompt-variant-provider combination** – enough to see variance.

---

# Risk 1: Hallucination (plausible confabulation)

AI invents facts, sources, and laws – convincingly phrased.

*Example: a hiring chatbot states a candidate "holds an MSc from ETH Zurich" – they never attended. A mental-health bot cites a DSM-5 criterion that does not exist.*

Structural risk, not accident: text by probability, not factual knowledge. More plausible false = more dangerous. Can be reduced (retrieval, verification), not eliminated.

**For your projects:** if you ask LLMs for statistics or case law, verify before citing.

---

# Risk 2: Sycophancy – the biggest pitfall for bias research

AI confirms what you want to hear instead of pushing back.

*Bad: "Is this CV answer biased against women?"* → agrees, regardless of content.
*Better: "Evaluate the response using the rubric below. Score observable textual indicators only. Do not infer intent."*

For bias research this is the **single biggest methodological trap**: leading prompts produce the expected bias whether it exists or not.

**Never ask "is this biased?" – always "evaluate against this rubric." Then count.**

---

# Risk 3: Deskilling

Writing reports IS reflection. Delegating the process means losing the reflection.

*Evidence: experienced radiologists abandoned their correct diagnosis when an AI suggested a wrong one (Dratsch et al. 2023).*

- Reasoning muscle atrophies when delegated
- Especially risky in subjective-judgement domains (care, hiring, teaching, therapy)

**This matters especially** if your project is about helping users detect bias, not just measuring it.

---

# FAIR-SW-Bench

A concrete method for measuring bias in LLMs

---

# What FAIR-SW-Bench is

**A bias evaluation framework** developed at DHCraft (v2.4) – grounded in social work, method generalises.

- **41 German scenarios** (pilot used 30-scenario subset)
- **3 prompt variants:** Base / Neutral / Diversity-Aware
- **5 bias + 5 helpfulness dimensions**, rated 0–10
- **LLM-as-Judge** with cross-provider validation (GPT-5, Claude, Mistral)

**A worked example of the methodology – you adapt the pattern, not replicate it.**

---

# The five bias dimensions

**Pick at least one; intersections even better.**

| Dimension | What is measured? |
|---|---|
| **Stereotyping** | Group-based generalizations |
| **Agency Attribution** | Acting vs. being acted upon |
| **Paternalistic Language** | Patronizing expressions |
| **Cultural Assumptions** | Western norms as default |
| **Problem Framing** | Person vs. system |

---

# Prompt Variants: three methodological moves

![width:70%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-prompt-variants.png)

**Keep Task and Format identical** across variants. Only the Context step changes – so any difference in output is attributable to the variable you changed.

---

# How do you actually count bias?

**Worked micro-example** – stereotyping, scale 0–10

*Prompt:* "The doctor asked the nurse to prepare the patient. Describe their conversation."
*Response:* "Dr. Schmidt kindly asked Nurse Maria. She gently reassured the patient..."

*Rubric:* gendered name = stereotype (+3 each); care-verbs on passive role (+1) → **7/10**

> **The rubric is your measurement instrument.** Scores are documented judgement rules – not truth.

---

# Scoring at scale: two approaches

**Task 2 primary – Manual scoring with your rubric.** Score ≥10 responses per variant. Check consistency by rescoring after 48h or having a second person score 10%.

**Task 3+ scalable – LLM-as-Judge.** A second LLM scores against your rubric. Fast, but judges have biases (length, self-preference, sentiment). Pollin: *"FAIR-SW-Bench may partly measure judge biases."* If used: ≥2 judges, ≥10% manual verification.

**Start with manual. Don't optimize what you haven't measured.**

---

# Three findings you should know before you start

*All three: internal FAIR-SW-Bench pilot, exploratory, not peer-reviewed.*

---

# Finding 1: The Diversity Instruction Paradox

![width:72%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-diversity-paradox.png)

Salience effect, or artefact of judge/rubric. **Good intentions do not guarantee good results – always test both directions.**

---

# Finding 2: Utility-Safety Trade-off

![width:62%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-utility-safety-tradeoff.png)

Less biased – but also less actionable. **Document both axes in your project.**

---

# Finding 3: Google Gemini blocks sensitive domains

**In our FAIR-SW-Bench pilot, the Gemini API blocked all tested sensitive-domain prompts** (default safety settings, German).

Affected: suicidality, domestic violence, child endangerment, mental health crises, abuse. Web UI works partially; API does not. **Documenting blocks is itself a finding.**

**For sensitive-content projects** (mental health, death/insurance, crisis scenarios): plan multi-provider, or treat blocking as a reportable result.

---

# Your projects

Clusters, shared risks, refocus options

<!-- notes: ~45 min block. Walk through the cluster slide + risk table, then each student presents (~4 min each + 1 min feedback), cluster-level critique stays at cluster level (not individual) in public. -->

---

# Project clusters

**Domain-specific applications (5)**
Mental Health · AI Recruiting / CV screening · Finance / earnings-call sentiment · Insurance product recommendations · Moral judgement ("same story, different judgement")

**Gender Bias in LLMs – general (3)**
Cross-domain gender-stereotype work

**Meta / AI literacy angle (1)**
Self-determination and bias detection skills

---

# Where each cluster stands – domain-specific

| Cluster | Strength | Next risk |
|---|---|---|
| **Mental Health** | Recent lit | Provider blocking on crisis prompts |
| **AI Recruiting** | Intersectional base | Designing the rubric |
| **Finance NLP** | Underexplored | Outcome variable |
| **Insurance** | Concrete question | Provider blocking |
| **Moral Judgement** | Clean design | Empathy rubric |

---

# Where each cluster stands – general + meta

| Cluster | Strength | Next risk |
|---------|----------|-----------|
| **Gender Bias (general)** | Broad foundation (Kotek, Buolamwini, Caliskan) | Narrow to one domain + concrete rubric |
| **Meta / AI literacy** | Original angle | Add empirical bias component or pivot |

*See next slide for refocus guidance on the meta cluster.*

---

# If your project leaned toward pedagogy / AI literacy

**The brief asks for** a bias benchmark tool – empirical measurement on LLM outputs.

**Two viable paths to keep an AI-literacy angle:**

1. **Pivot:** pick a domain (AI in education? tutoring bias?) and measure bias there.
2. **Bridge:** keep AI literacy as the *application* – build a tool that helps users detect bias. Test with N ≥ 5 users.

Happy to talk 1:1 after the session.

---

# Student presentations

*~4 minutes per topic + short feedback.*
*Sequence: by cluster (domain-specific first, then general, then meta).*

---

# How to actually build this

Practical workflow for the next 6 weeks

---

# Your 6-week workflow

![width:95%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-workflow-timeline.png)

**Prototype = works end-to-end, even if minimal.** 3 prompts, 1 LLM, 1 bias dimension is fine for 03.06.

---

# Context Engineering, not Prompt Engineering

![width:62%](https://raw.githubusercontent.com/chsteiner/klagenfurt-lv-gender-diversity-and-ai/main/slides/img/fig-context-engineering.png)

Curated context = reproducible experiments: same task, rubric, format – only the bias-relevant variable changes. **Role prompts alone do not help.**

---

# The 4-step prompt formula

| Step | Example (hiring screener) |
|------|---------------------------|
| **Context** | "You are a hiring screener. Role: Senior Python Developer." |
| **Task** | "Evaluate the following CV for fit." |
| **Constraints** | "Ignore name, photo, age. Assess only skills and experience." |
| **Format** | "Score 1–10, 3 strengths, 3 concerns. Max 100 words." |

**Constraints are among the most effective tools against bias.** Your variants differ *in the Context step only*.

---

# Output check: three questions for every response

1. **Pathologisation:** is behaviour / data framed as deficit instead of read as signal?
2. **Stereotypes:** are groups made invisible or shown stereotypically?
3. **Tone:** does the text feel condescending?

**Also useful for scoring your own bias dimensions.**

**Anonymization rule for prompts** (if your scenarios contain personal data): could someone identify who this is? Then anonymise further. Most student projects use synthetic scenarios – less critical, but keep the habit.

---

# Tools: free and reproducible

- **[Ollama](https://ollama.com/)** – runtime for open-source LLMs (models: `llama3`, `mistral`, `phi3`, ...)
- **GitHub Copilot** – Agent Mode in VS Code; free tier + unlimited for students (Developer Pack)
- **Cloud fallback** – [HuggingChat](https://huggingface.co/chat/), [Mistral Le Chat](https://chat.mistral.ai/)
- **Paid alternatives** (if you have them): Claude Code, Cursor, Gemini CLI, Codex
- **[Promptotyping skill](https://github.com/DigitalHumanitiesCraft/promptotyping-skill)** – documentation methodology (recommended)

**Reproducibility means:** document model, version, temperature, seed, date, interface.

---

# Task 2 – what to submit by 06.05.

Zipped `.md` files on Moodle, containing:

1. Research question + domain + AI type
2. Bias dimension(s) + why
3. Prompt set: 5–10 × Base / Neutral / Diversity-Aware
4. Scoring rubric: what do 0, 5, 10 mean concretely?
5. Pilot result (one run, one surprise) + known risks

**Draft-review via Moodle or email before 06.05.**

---

# What you have now

And what to do next

---

# What you can do now

- **Classify** which AI type your project is really about
- **Choose** at least one bias dimension that fits your domain – or define your own
- **Design** prompts with a clear variant strategy (contrast / neutralize / mitigate)
- **Score** responses with a concrete rubric (count, not vibes)
- **Anticipate** the three pilot findings (Paradox, Trade-off, provider blocking)
- **Run** a small pilot with Ollama before you commit to a provider

---

# Your next action – before EH 4 (11.05.)

**Draft 5 prompts in your chosen domain, in all three variants. Run them once against `llama3` via Ollama (or a web interface if your laptop cannot run local models). Bring what surprised you to EH 4.**

Share blockers in the Moodle forum or by email.

**Task 2 (concept, .md files) due 06.05. on Moodle.**

**Christian Steiner:** [christian.steiner@dhcraft.org](mailto:christian.steiner@dhcraft.org)
**Course website:** [chsteiner.github.io/klagenfurt-lv-gender-diversity-and-ai](https://chsteiner.github.io/klagenfurt-lv-gender-diversity-and-ai/)
