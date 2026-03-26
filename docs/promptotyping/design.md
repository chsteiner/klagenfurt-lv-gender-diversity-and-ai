# Design: LV-Begleitwebsite

## Seitenarchitektur

```
docs/
├── index.html              # Docsify-Einstiegspunkt
├── .nojekyll               # GitHub Pages: kein Jekyll
├── _sidebar.md             # Navigation (7 Einträge)
├── README.md               # Home / Landing Page
├── setup.md                # Setup Guide (Tools vor Session 1)
├── projektauftrag.md       # Kompakter Projektauftrag
├── zeitplan.md             # Termine, Meilensteine, Prüfung
├── theorie.md              # Gender/Diversity-Theorie
├── fair-sw-bench.md        # FAIR-SW-Bench Konzept + Befunde
├── ressourcen.md           # Ollama, Coding Agents, Kontakt
└── promptotyping/          # Promptotyping-Docs (nicht in Sidebar)
    ├── knowledge.md
    ├── requirements.md
    ├── design.md
    └── journal.md
```

## Designentscheidungen

### D-1: Docsify statt Alternativen

| Option | Pro | Contra | Entscheidung |
|--------|-----|--------|-------------|
| **Docsify** | Kein Build, CDN, direkt aus /docs | Kein SSR, JS-abhängig | **Gewählt** |
| MkDocs Material | Schöner, bessere Suche | Braucht Python-Build | Rejected: Overkill |
| VitePress | Modern, schnell | Braucht Node.js Build | Rejected: Overkill |
| Plain GitHub | Null Setup | Keine Navigation, keine Suche | Rejected: Zu rudimentär |

### D-2: Flache Struktur statt Verschachtelung

7 Seiten auf einer Ebene (Home + Setup Guide + 5 Inhaltsseiten). Keine Unterordner, keine nested Navigation. Begründung: Studierende brauchen schnellen Zugriff, nicht Tiefe. Alles ist max. 1 Klick entfernt.

### D-3: Inhalt aus bestehenden .md-Dateien adaptieren, nicht kopieren

Die Docsify-Seiten sind **eigenständige Dokumente**, die Inhalte aus den Quelldateien (PROJECT.md, README.md, ~~GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md~~ – aus Repo entfernt, Inhalte integriert) zusammenführen und für die Web-Darstellung optimieren. Keine 1:1-Kopien, sondern kuratierte Auswahl.

Ausnahme: `projektauftrag.md` ist eine kompakte Zusammenfassung von `PROJECT.md` mit Link zum vollständigen Text.

### D-4: Docsify-Theme und Styling

- **Theme:** Docsify Default (Vue-Theme) – schlicht, funktional, keine Custom-CSS nötig
- **Dark Mode:** Docsify-Plugin `docsify-darklight-theme` – Studierende erwarten das
- **Keine Custom-Fonts, keine Logos** – unnötig für eine LV-Begleitseite

### D-5: Plugins (minimal)

| Plugin | Zweck | CDN |
|--------|-------|-----|
| `docsify-search` | Volltextsuche über alle Seiten | `//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js` |
| `docsify-copy-code` | Code-Blöcke kopierbar (Ollama-Beispiele) | `//cdn.jsdelivr.net/npm/docsify-copy-code` |

Kein Emoji-Plugin, kein Pagination-Plugin, kein Tab-Plugin. Weniger ist mehr.

### D-6: Sidebar-Einträge

```markdown
- [Home](/)
- [Setup Guide](setup.md)
- [Project Brief](projektauftrag.md)
- [Timeline & Milestones](zeitplan.md)
- [Theory Overview](theorie.md)
- [FAIR-SW-Bench](fair-sw-bench.md)
- [Resources & Tools](ressourcen.md)
```

### D-7: Keine Docsify-Navbar

Die Sidebar reicht für 7 Seiten. Eine zusätzliche Topbar wäre Noise.

## Content-Mapping: Quelle → Seite

| Docsify-Seite | Primärquelle | Sekundärquellen | Anpassung |
|---------------|-------------|----------------|-----------|
| `README.md` (Home) | Eigener Text | README.md (LV-Übersicht) | Kurzfassung + Links |
| `setup.md` | Eigener Text | – | Step-by-Step: VS Code, Git, Python, Copilot, Ollama |
| `projektauftrag.md` | PROJECT.md | – | Kompakte Version, Link zu PROJECT.md |
| `zeitplan.md` | README.md (Zeitplan, Meilensteine, Prüfung) | PROJECT.md (Meilensteine) | Zusammenführung |
| `theorie.md` | ~~GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md~~ (Teil A, integriert) | – | Gekürzt, ohne Didaktik |
| `fair-sw-bench.md` | ~~GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md~~ (Teil F, integriert) | PROJECT.md, Vault-Notizen | Zusammenführung + Beispiel-Prompts |
| `ressourcen.md` | PROJECT.md (LLM-Zugang, Context Engineering) | ~~GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md~~ (Teil D, integriert) | Zusammenführung |
