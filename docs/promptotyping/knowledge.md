# Knowledge: LV-Begleitwebsite

## Kontext

Begleitwebsite für die LV "Gender, Diversität und KI" (Universität Klagenfurt, Master Informatik, SS2026). Die Website gibt Studierenden den vollständigen Überblick über Kurs, Projektauftrag, theoretische Grundlagen und Forschungskontext.

## Zielgruppe

Master-Studierende Informatik, Universität Klagenfurt. Technisch versiert, wenig/keine Vorkenntnisse in Gender Studies. Deutschsprachig, Materialien teilweise Englisch.

## Bestehende Inhaltsquellen

| Quelle | Datei | Inhalt | Verwendung auf Website |
|--------|-------|--------|----------------------|
| Projektauftrag | `PROJECT.md` | Bias-Benchmark-Tool Aufgabe, Ansätze, Dimensionen, Ollama, Meilensteine, Bewertung | → Seite "Projektauftrag" (Kernseite) |
| LV-Planung | `README.md` | Zeitplan, Prüfungsmodalitäten, Kontakt, Forschungskontext | → Seiten "Zeitplan", "Home" (Auszüge) |
| Theorie-Dokument | `GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md` | Gender-Theorie für STEM, I-Methodology, Intersektionalität, Feminist STS, Frameworks, Case Studies, Didaktik | → Seite "Theorie" (gekürzt, ohne didaktische Teile B-E) |
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

## Sprachkonventionen

- Website auf Deutsch (Studierendensprache)
- Gendergerechte Sprache: Doppelpunkt-Form (Entwickler:innen, Nutzer:innen)
- Du-Form für Studierende (konsistent mit PROJECT.md)
- Fachbegriffe auf Englisch belassen (Bias, Prompting, LLM, Benchmark)
