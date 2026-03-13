# Knowledge: LV-Begleitwebsite

## Kontext

Begleitwebsite für die LV "Gender, Diversity & AI" (Universität Klagenfurt, Master Informatik, SS2026). Die Website gibt Studierenden den vollständigen Überblick über Kurs, Projektauftrag, theoretische Grundlagen und Forschungskontext.

## Zielgruppe

Primär Master-Studierende Informatik, Universität Klagenfurt. Aber auch BWL- und Anglistik-Studierende haben sich angemeldet. Technische Vorkenntnisse variieren stark. Wenig/keine Vorkenntnisse in Gender Studies.

## Sprache

Alle student-facing Dokumente sind auf **Englisch** (LV-Sprache). Interne Planungsdokumente (README.md, Promptotyping-Docs) bleiben Deutsch.

**Stilregel:** Keine Em dashes (—) oder Doppelbindestriche (--). Gedankenstriche ( – , en dash mit Leerzeichen) sind erlaubt. Sonst Doppelpunkte, Semikolons, Punkte oder Satz umformulieren.

## Bestehende Inhaltsquellen

| Quelle | Datei | Inhalt | Verwendung auf Website |
|--------|-------|--------|----------------------|
| Projektauftrag | `PROJECT.md` | Bias-Benchmark-Tool Aufgabe, Ansätze, Dimensionen, Ollama, Meilensteine, Bewertung | → Seite "Project Brief" (Kernseite) |
| LV-Planung | `README.md` | Zeitplan, Prüfungsmodalitäten, Kontakt, Forschungskontext | → Seiten "Timeline", "Home" (Auszüge) |
| Syllabus | `SYLLABUS.md` | Offizieller Syllabus mit Tasks, Learning Outcomes, Prerequisites | → Link von Website, Moodle |
| Theorie-Dokument | `GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md` | Gender-Theorie für STEM, I-Methodology, Intersektionalität, Feminist STS, Frameworks, Case Studies, Didaktik | → Seite "Theory" (gekürzt, ohne didaktische Teile B-E) |
| FAIR-SW-Bench (Vault) | Obsidian-Notizen | Framework-Architektur, 50 Testszenarien, Pilotstudie, Paradox, Context Engineering | → Seite "FAIR-SW-Bench" |

## Docsify-Spezifika

- Docsify rendert `.md`-Dateien client-seitig via JavaScript
- Einstiegspunkt: `index.html` mit Docsify-CDN
- Navigation: `_sidebar.md` definiert die Seitenstruktur
- `README.md` im `docs/`-Ordner = Landing Page (nicht das Root-README)
- `.nojekyll` verhindert Jekyll-Processing auf GitHub Pages
- Kein Build-Step nötig, kein Node.js, keine Dependencies
- Deployment: GitHub Pages auf `/docs`-Ordner des `main`-Branch

## Docsify-Konfiguration (relevante Optionen)

```javascript
window.$docsify = {
  name: '',           // Seitentitel in der Sidebar
  repo: '',           // GitHub-Repo-Link oben rechts
  loadSidebar: true,  // _sidebar.md laden
  subMaxLevel: 2,     // Unterüberschriften in Sidebar
  search: 'auto',     // Volltextsuche aktivieren
  auto2top: true,     // Bei Seitenwechsel nach oben scrollen
}
```

## Coding Agents für Studierende

- **Kostenlose Default-Option:** GitHub Copilot Agent Mode (in VS Code integriert, gratis via Student Developer Pack)
- **Copilot Free Tier:** 50 Chat-Messages/Monat für jeden GitHub-Account, auch ohne Student Pack
- **Bezahlte Alternativen:** Claude Code, Gemini CLI, Codex, Cursor, Windsurf – wer schon eine Lizenz hat, soll die nehmen
- **Promptotyping Skill:** Open Agent Skill, funktioniert mit jedem LLM/Agent

## Sprachkonventionen (student-facing)

- Englisch (LV-Sprache)
- Fachbegriffe auf Englisch (Bias, Prompting, LLM, Benchmark)
- Kein gendering nötig auf Englisch
- Keine Em dashes
