# Journal: LV-Begleitwebsite

## 2026-03-06: Projektstart

**Ausgangslage:** Repo hat README.md (interne Planung), PROJECT.md (Projektauftrag für Studis), GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md (umfangreiches Theorie/Didaktik-Dokument). Reichhaltiger FAIR-SW-Bench-Kontext im Obsidian-Vault. Kein `docs/`-Ordner.

**Entscheidung:** Docsify in `/docs`, 6 Seiten (Home, Projekt, Zeitplan, Theorie, FAIR-SW-Bench, Ressourcen). Kein Build-Step, GitHub Pages Deployment.

**Promptotyping-Docs erstellt:** knowledge.md, requirements.md, design.md (dieses Journal).

**Nächster Schritt:** ~~Implementierung~~ erledigt.

## 2026-03-06: Implementierung

**Designprinzip:** Maximal simpel. Die Website dient nur der Orientierung – kein Content-Overload, den bekommen die Studis in der LV. Kurze Texte, klare Links, schnelle Übersicht.

**Umgesetzt:**
- `index.html` (Docsify CDN, Search + Copy-Code Plugins)
- `_sidebar.md` (6 Einträge)
- `.nojekyll`
- 6 Content-Seiten: Home, Projektauftrag, Zeitplan, Theorie, FAIR-SW-Bench, Ressourcen

**Entscheidungen:**
- Theorie-Seite auf projektrelevante Konzepte gekürzt (I-Methodology, Intersektionalität, Bias-Dimensionen, Gendered Innovations, Data Feminism, Feminist STS, EU AI Act)
- FAIR-SW-Bench: 1 Beispiel-Prompt (Kindeswohl) statt Auswahl aus 50 – reicht zur Illustration
- Projektauftrag: Kompakte Version mit Link zum vollständigen PROJECT.md auf GitHub
- Keine Duplikation zwischen Seiten – jede Seite hat einen klaren Zweck

**Nächster Schritt:** ~~GitHub Pages aktivieren~~ erledigt.

## 2026-03-13: Setup Guide und Copilot-Update

**Auslöser:** Susi meldet, dass viele BWL- und Anglistik-Studis angemeldet sind. Technische Voraussetzungen waren nicht im Vorlesungsverzeichnis. Brauchen einen Setup Guide und eine Info-Mail.

**Umgesetzt:**
- `setup.md` (neue Seite): Step-by-Step Setup Guide für VS Code, Git, Python, GitHub/Copilot, Ollama
- Sidebar auf 7 Einträge erweitert (Setup Guide als zweiter Eintrag)
- Home-Seite: Setup Guide als erster Bold-Link
- projektauftrag.md: "New here?" Callout mit Link zum Setup Guide
- SYLLABUS.md: Website-URL ergänzt

**Entscheidungen:**
- Reihenfolge im Setup: VS Code → Git → Python → GitHub/Copilot → Ollama (logische Abhängigkeiten, nicht Wichtigkeit)
- Agent Mode als separater Abschnitt nach den Installationsschritten – nicht für Session 1 nötig
- Terminal-Tipp bei VS Code – viele Erstnutzer wissen nicht, wo das Terminal ist
- Python PATH-Warnung als Callout – häufigster Setup-Fehler
- Copilot Free Tier (50 Msg/Monat) als Fallback – Student Pack braucht bis zu 7 Tage

**Copilot-Update (12.03.2026):**
- GitHub hat "Copilot Student" als eigenen Plan eingeführt (vorher "Copilot Pro for students")
- Copilot ist in VS Code integriert – kein manueller Extension-Install mehr nötig
- Agent Mode ist der zentrale Workflow: Chat-Panel → "Agent" Dropdown → natürliche Sprache → Code
- Alle Referenzen zu "Copilot Pro" durch korrekte Formulierungen ersetzt
- Bezahlte Alternativen (Claude Code, Gemini CLI, Codex, Cursor, Windsurf) überall erwähnt

**Nächster Schritt:** Commit und Push, dann Email-Entwurf an Susi weiterleiten.

## 2026-04-25 – handoff

**Summary:** Session 3 Slide-Deck und Skript für 27.04.2026 (Bias Detection in AI) komplett aufbereitet — von Importer-Kompatibilität über zwei Review-Runden (Susi + Winston/marp-slides Audits) bis zu einer Studi-facing Tutorial-Seite auf docsify. Skript bleibt lokal, alle anderen Artefakte sind auf `origin/main`.

**Decisions:**
- **Speaker-Skript lokal lassen** — `slides/session-3-klafu-2026-04-27-script.md` enthält Per-Student Kritik (Prep-Cards, "watch for"-Hinweise) die nicht öffentlich sein sollen. Tutorial-Seite (`docs/measuring-bias.md`) als sanitisierte, studi-facing Variante.
- **Slide 11 reframen:** alle Projekte sind Type 3 (LLM-Output-Messung), inklusive der domains die nach Klassifikation klingen (Finance Sentiment, CV Screening). Behoben den Logik-Bruch dass die Tabelle "Predictive ML" als Projekt-Option auflistete.
- **"Transferable pattern" statt "method generalises"** — FAIR-SW-Bench ist explizit social-work-scoped, Studis adaptieren das Pattern, nicht den Framework.
- **"Open issue" statt "Next risk"** in Cluster-Strengths-Tabellen — auf Susi's Hinweis hin neutraler.
- **0/5/10-Rubric-Anchors** als Methodik etabliert (neue Slide S22 + Tutorial-Section). FAIR-SW-Bench's eigene generische Anchors (minimal/moderate/significant) als Kontrast erwähnt; domain-spezifische Anchors sind pädagogisch besser.
- **N ≥ 10 runs** als Threshold für diesen Kurs gesetzt. Für Prototyp: 3 prompts × 3 variants × 10 runs = ~90 calls.
- **Pollin-Zitat entfernt** aus Slide S23 (nicht in FAIR-SW-Bench Repo nachweisbar) — durch generische "judges have their own biases" Formulierung ersetzt.

**Dead ends:**
- C4 (Workflow-Textzeile auf S29 zusätzlich zum Bild): erzeugte 45px Overflow und war redundant mit Prototype-Zeile + Bild → zurückgenommen.
- A5 mit Salience-Hypothese auf S25: musste die Hypothesen-Erklärung streichen damit der Paradox-Kernsatz neben dem Bild ins Canvas passt → Speaker erklärt sie oral; Skript hat den Kontext.

**Phase:** Implementation, abgeschlossen für Session 3. Alle Promptotyping-Docs aktuell:
- `docs/measuring-bias.md` **NEU** — Practical Tutorial, ergänzt theorie.md + fair-sw-bench.md ohne Duplikation
- `docs/fair-sw-bench.md` aktualisiert (50 → 41 German + 10 English scenarios)
- `docs/_sidebar.md` ergänzt
- `slides/session-3-klafu-2026-04-27.md` final (43 slides, Overflow clean, PDF generiert)
- `slides/session-3-klafu-2026-04-27.pdf` final
- `slides/session-3-klafu-2026-04-27-script.md` lokal (nicht im Repo)
- PROJECT.md aktualisiert ("1+ LLM" Konsistenz mit README)

**Open issues:**
- Kotek 95%-Claim auf S10 (Footnote) ist nicht im Paper-Abstract verifiziert. Direction stimmt (LLMs picken female-Pronomen für "nurse" near-ceiling), aber exakte Zahl vor 27.04 prüfen — sonst Q&A-Risiko.
- FAIR-SW-Bench Repo ist privat (org-only access). Tutorial-Seite verweist nur auf lokale `docs/fair-sw-bench.md`, nie auf den externen Repo. OK so.
- Saad's Projekt (Self-Determination & AI Literacy): Refocus-Empfehlung steht auf Slide S40 + im Tutorial. Live-Conversation am 27.04 nötig — vermutlich post-session 1:1.
- Matthias's Gemini-API: noch unklar ob Web-UI für Life-Insurance-Prompts blockt. Wenn ja: Plan B (Multi-Provider oder Blocking-as-Finding) muss er bis EH 4 (11.05) entscheiden.
- Sohaib + Shahnood haben quasi-identische Topics (Buolamwini/Gebru source overlap). Differenzierung oder Kollaboration im Cluster-Feedback klären.

**Next steps (priorisiert):**
1. **Vor 27.04.** — Kotek-Zahl verifizieren (S10 Footnote). 5 Minuten Paper-Check spart Q&A-Stress.
2. **27.04.2026 08:15** — Session 3 halten. Skript lokal als PDF/Vorschau parat haben.
3. **Post-session 27.04.** — kurze Notiz in Journal: was lief gut, was hat überrascht, welche Studi braucht 1:1.
4. **Bis 06.05.** — Draft-Review für Studis offen halten (Moodle/Email-Eingang). Insbesondere bei Saad nachfragen.
5. **11.05. EH 4** — Konzept-Review mit allen 9 Studis. Cluster-Feedback aus Slides als Aufhänger nutzen.
6. **Optional** — `docs/measuring-bias.md` nach Session 3 mit Q&A-Insights ergänzen, falls etwas Zentrales ungeklärt blieb.
