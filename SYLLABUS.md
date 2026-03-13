**650.097 (26S) – Gender, Diversity & AI**

Main lecturer: Dr. Susanne Sackl-Sharif ([susanne.sackl-sharif@aau.at](mailto:susanne.sackl-sharif@aau.at) | [www.sackl-sharif.net](http://www.sackl-sharif.net))
Guest contributions by Christian Steiner ([christian.steiner@dhcraft.org](mailto:Christian.steiner@dhcraft.org) | [https://dhcraft.org](https://dhcraft.org/))


| Dates | Content and deadlines |
| :---- | :---- |
| **17.03.2026** 13.30-18.30 presence | **Gender theories 1: Basic concepts** Course overview and introduction. Input on gender theories: Important terms, concepts, and theories. Individual and group work: Autoethnographic reflections. |
| **26.03.2026** 13.30-18.30 presence | **Gender theories 2: Gender and technology** Input on Gender Studies and Science and Technology Studies. Individual and group work: Research on bias and artificial intelligence. Project brief presented, group formation starts. *Deadline 1: Task 1 – Literature on bias and AI (22.04.2026, Moodle)* |
| **27.04.2026** 8.15-11.30 online | **Project 1: Introduction to bias detection and AI** Guest contribution by Christian Steiner: AI types, bias manifestations, detection methods, FAIR-SW-Bench findings. Report group composition, present topic. *Deadline 2: Task 2 – Concept / Promptotyping docs (06.05.2026, Moodle)* |
| **11.05.2026** 8.15-9.45 online | **Project 2: Feedback on concepts and open questions** *Deadline 3: Prototype (until 03.06.2026)* |
| **03.06.2026** 8.15-11.30 online | **Project 3: Prototype** Presentation of all prototypes. Peer feedback. Discussion of open questions. *Deadline 4: Final presentation and submission (24.06.2026, in presence)* |
| **24.06.2026** 10.00-16.45 presence | **Project 4: Final presentations and submission** Final presentations (10 min + 5 min discussion). GitHub repository submission (code + promptotyping docs). |
| **Workload (attendance): 24.75 hours** | |

A **Moodle forum** is available between sessions for questions about the project work. Christian Steiner answers technical questions about APIs, bias detection, and tooling. Susanne Sackl-Sharif handles conceptual and theoretical questions.

**TASK OVERVIEW (workload overview: 4 ECTS = 100 hours)**

**Task 1 – Bias and AI: Literature (workload: 5 hours)**

* Topic: What topic/questions should be the focus of your project?
* Research 2-3 scholarly sources (theories, empirical studies, projects) on your topic.
* Literature overview (1 page, .md format): Overview of the topic and possible questions; brief description of the content discussed in the sources.

**Deadline:** 22.04.2026 (.md file on Moodle)

**Task 2 – Project concept: Promptotyping documents (workload: 10 hours per person)**

Your concept submission consists of four Promptotyping documents (.md files):

* **knowledge.md** – Domain knowledge, sources, constraints, and conventions for your project.
* **requirements.md** – What your tool should do: user stories, acceptance criteria, scope.
* **design.md** – Technical and architectural decisions: how you plan to build it.
* **journal.md** – Project log: decisions made, alternatives considered, open questions.

These documents serve as your project plan AND as a knowledge base for LLM-assisted development. The core principle: **your artifact must be regenerable from the docs.** If you delete your code, an LLM reading your Promptotyping docs should be able to recreate it.

The Promptotyping methodology is available as an open agent skill that works with any LLM (Claude, ChatGPT, Gemini, local models). You can install it as a skill in your coding agent or simply copy the .md templates into any LLM conversation:
https://github.com/DigitalHumanitiesCraft/promptotyping-skill

**Deadline:** 06.05.2026 (zipped .md files on Moodle)

**Task 3 – Project implementation (workload: 50.25 hours per person)**

* Develop your bias benchmark tool based on your Promptotyping docs.
* Use LLM-assisted development (any coding agent: GitHub Copilot Agent Mode, Claude Code, Cursor, or similar). Note: GitHub Copilot is free for students via the [GitHub Student Developer Pack](https://education.github.com/pack) and built into VS Code. Keep your Promptotyping docs updated as you go; they are living documents.
* Minimum requirements: 10+ test prompts, 2+ bias dimensions, 1+ LLM, documented methodology, working code.
* LLM access: free via [Ollama](https://ollama.com/) (local models) or free-tier web interfaces.

**Deadline (prototype):** 03.06.2026 (prepare short demo for EH 5)
**Deadline (final):** 24.06.2026 (GitHub repository: code + final Promptotyping docs)

**Task 4 – Final Promptotyping documentation (workload: 10 hours per person)**

Your final Promptotyping docs in the GitHub repository serve as both project documentation and written reflection. Update them to reflect:

1. Final state of knowledge, requirements, design decisions
2. Results: What did you find? What patterns of bias did you detect?
3. Reflection: What worked, what didn't? What would you do differently?

The Promptotyping docs replace a traditional written reflection. They must be complete enough that your tool could be regenerated from them.

**Deadline:** 24.06.2026 (part of the GitHub repository submission)

**LEARNING OUTCOMES**

Upon completion of this course, students will be able to:

1. Demonstrate an overview of gender and diversity theories
2. Understand how bias manifests in different AI system types (rule-based, predictive, generative)
3. Design and implement bias detection methodologies for LLMs
4. Gain practical experience with LLM-assisted development tools (coding agents)
5. Deepen their skills in independent project planning and implementation

**PREREQUISITES**

Basic programming skills in at least one language (ideally Python) and willingness to work with LLM-assisted development tools. No prior knowledge of Machine Learning or Gender Studies required.

**REQUIREMENTS AND EXAM INFORMATION**

1. Attendance (minimum of 80%) and participation (discussion)		20%
2. Project: development, implementation and presentation (Task 1-3)		50%
3. Promptotyping documentation in GitHub repository (Task 4)			30%

**Course website:** https://chsteiner.github.io/klagenfurt-lv-gender-diversity-and-ai/
