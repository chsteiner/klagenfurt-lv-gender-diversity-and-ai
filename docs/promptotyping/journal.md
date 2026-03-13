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
