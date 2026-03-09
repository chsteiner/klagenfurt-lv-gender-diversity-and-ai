# Journal: LV-Begleitwebsite

## 2026-03-06: Projektstart

**Ausgangslage:** Repo hat README.md (interne Planung), PROJECT.md (Projektauftrag für Studis), GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md (umfangreiches Theorie/Didaktik-Dokument). Reichhaltiger FAIR-SW-Bench-Kontext im Obsidian-Vault. Kein `docs/`-Ordner.

**Entscheidung:** Docsify in `/docs`, 6 Seiten (Home, Projekt, Zeitplan, Theorie, FAIR-SW-Bench, Ressourcen). Kein Build-Step, GitHub Pages Deployment.

**Promptotyping-Docs erstellt:** knowledge.md, requirements.md, design.md (dieses Journal).

**Nächster Schritt:** ~~Implementierung~~ erledigt.

## 2026-03-06: Implementierung

**Designprinzip:** Maximal simpel. Die Website dient nur der Orientierung — kein Content-Overload, den bekommen die Studis in der LV. Kurze Texte, klare Links, schnelle Übersicht.

**Umgesetzt:**
- `index.html` (Docsify CDN, Search + Copy-Code Plugins)
- `_sidebar.md` (6 Einträge)
- `.nojekyll`
- 6 Content-Seiten: Home, Projektauftrag, Zeitplan, Theorie, FAIR-SW-Bench, Ressourcen

**Entscheidungen:**
- Theorie-Seite auf projektrelevante Konzepte gekürzt (I-Methodology, Intersektionalität, Bias-Dimensionen, Gendered Innovations, Data Feminism, Feminist STS, EU AI Act)
- FAIR-SW-Bench: 1 Beispiel-Prompt (Kindeswohl) statt Auswahl aus 50 — reicht zur Illustration
- Projektauftrag: Kompakte Version mit Link zum vollständigen PROJECT.md auf GitHub
- Keine Duplikation zwischen Seiten — jede Seite hat einen klaren Zweck

**Nächster Schritt:** GitHub Pages aktivieren (Christian via `gh` CLI).
