# Lehrveranstaltungsplanung: Gender, Diversität und KI

> **Universität Klagenfurt – Masterstudium Informatik – Sommersemester 2026**

---

## Übersicht

| Feld | Details |
|------|---------|
| **Titel** | Gender, Diversität und Künstliche Intelligenz |
| **ECTS** | 4 (entspricht 100 Arbeitsstunden) |
| **Kontaktzeit** | ~27 Stunden (6 Einheiten: 3x Präsenz, 3x Online) |
| **Selbststudium** | ~73 Stunden |
| **Lehrende** | Susanne Sackl-Sharif (Hauptlehrende), Christian Steiner (Gastbeiträge KI & Bias) |
| **Zielgruppe** | Master-Studierende Informatik |
| **Sprache** | Deutsch (Materialien teilweise Englisch) |

---

## Struktur der Lehrveranstaltung

Die LV gliedert sich in zwei inhaltliche Teile:

### Teil 1: Gender- und Diversitätsgrundlagen (EH 1–2)
*Verantwortlich: Susanne Sackl-Sharif*

Theoretische Einführung ohne direkten KI-Bezug. Die Studierenden erhalten Grundlagenwissen zu Gender und Diversität, um später Bias in KI-Systemen erkennen und analysieren zu können. Fokus auf I-Methodology (Bath 2011) als Brücke zur Informatik: Wie Entwickler:innen eigene Perspektiven als impliziten Standard setzen. Am Ende von EH 2 wird der Projektauftrag vorgestellt und die Gruppenbildung angestoßen.

### Teil 2: Gender, Diversität und KI (EH 3–6)
*Verantwortlich: Susanne Sackl-Sharif mit Gastbeiträgen von Christian Steiner (DHCraft)*

Anwendung der theoretischen Grundlagen auf KI-Systeme. Christian Steiner liefert in EH 3 den technischen Input zu KI-Typen und Bias-Manifestationen. Im Zentrum steht das Studierendenprojekt: Die eigenständige Entwicklung eines Bias-Benchmark-Tools für Large Language Models.

---

## Zeitplan und Einheiten

### Teil 1: Gender und Diversität

| EH | Datum | Zeit | Format | Raum | Inhalte |
|----|-------|------|--------|------|---------|
| **1** | Di 17.03.2026 | 13:30–18:30 | Präsenz | C.0.16 | LV-Einführung, Inputs zu Gender und Diversität, Reflexionsübung |
| **2** | Do 26.03.2026 | 13:30–18:15 | Präsenz | C.0.16 | Gender und Diversität Vertiefung; Diskussion ausgewählter Texte; **Projektauftrag vorstellen, Gruppenbildung anstoßen** |

*Zwischen EH 2 und EH 3 (26.03.–27.04.): Gruppen finden sich selbstständig, Texte lesen*

### Teil 2: Gender und KI

| EH | Datum | Zeit | Format | Raum | Inhalte |
|----|-------|------|--------|------|---------|
| **3** | Mo 27.04.2026 | 08:15–11:30 | Online | – | **Gastbeitrag Christian Steiner**: KI-Typen, Bias-Manifestationen, Methoden der Bias-Detektion; Gruppenzusammensetzung mitteilen; Q&A zum Projekt |
| **4** | Mo 11.05.2026 | 08:15–09:45 | Online | – | Konzeptskizzen besprechen; Q&A zur Projektarbeit (Moderation: Christian Steiner, Susanne Sackl-Sharif) |
| **5** | Mi 03.06.2026 | 08:15–11:30 | Online | – | Peer-Feedback zu Projektfortschritten (Moderation: Christian Steiner, Susanne Sackl-Sharif) |
| **6** | Mi 24.06.2026 | 10:00–16:45 | Präsenz | C.0.16 | Abschlusspräsentationen der Projekte |

### Stundenübersicht

| Format | Einheiten | Stunden |
|--------|-----------|---------|
| Präsenz | EH 1 (5h), EH 2 (4,75h), EH 6 (6,75h) | ~16,5h |
| Online | EH 3 (3,25h), EH 4 (1,5h), EH 5 (3,25h) | ~8h |
| **Gesamt** | | **~24,5h** |

### Begründung der Einheitenplanung

Der **Projektauftrag** wird am Ende von **EH 2 (26.03.)** vorgestellt, damit Studierende die einmonatige Pause bis EH 3 nutzen können, um Gruppen zu bilden und sich erste Gedanken zu machen. Die **technische Einführung** (Gastbeitrag Christian Steiner) erfolgt in **EH 3 (27.04.)** zum Projektstart. EH 4 dient der Besprechung der Konzeptskizzen, EH 5 als **Peer-Feedback-Session** drei Wochen vor der Abschlusspräsentation.

---

## Meilensteine und Betreuung

### Projektmeilensteine

| Zeitpunkt | Meilenstein | Abgabe |
|-----------|-------------|--------|
| EH 3 (27.04.) | **Gruppenmitteilung**: Teamzusammensetzung bekanntgeben | In der Einheit |
| Vor EH 4 (11.05.) | **Konzeptskizze**: Projektidee, gewählte Bias-Dimensionen, geplante LLMs | 1-Seiter auf Moodle |
| Vor EH 5 (03.06.) | **Prototyp**: Erster lauffähiger Stand (auch minimal) | Kurze Demo vorbereiten |
| EH 6 (24.06.) | **Abschlusspräsentation + Abgabe**: Fertiges Tool, Dokumentation, Präsentation | Projekt + schriftliche Zusammenfassung |

### Asynchrone Betreuung

Zwischen den Einheiten steht ein **Moodle-Forum** für Fragen zur Projektarbeit zur Verfügung. Christian Steiner beantwortet dort technische Fragen zu APIs, Bias-Detektion und Tooling. Susanne Sackl-Sharif betreut konzeptuelle und theoretische Fragen.

---

## Projektauftrag: Bias-Benchmark-Tool

Die Studierenden entwickeln ein eigenes Tool zur Messung von Bias in LLM-generierten Antworten, inspiriert vom FAIR-SW-Bench Framework (Konzeptbeschreibung, nicht Code). Der vollständige Projektauftrag für die Studierenden steht in [PROJECT.md](PROJECT.md).

**Kurzfassung:** 10+ eigene Prompts, 2+ Bias-Dimensionen, 1+ LLM, dokumentierte Methodik, funktionierender Code. Themenfeld, Ansatz und technische Umsetzung sind frei wählbar. LLM-Zugang kostenlos über Ollama (lokale Modelle) oder Free-Tier Web-Interfaces. Abgabe als GitHub-Repo. Teams max. 3 Personen.

### Was die Studierenden erhalten

1. **Theoretische Grundlagen** (Teil 1): Gender/Diversitätstheorien, Intersektionalität, Bias-Definition
2. **Technische Einführung** (Gastbeitrag Christian Steiner, EH 3): KI-Typen, Bias-Manifestationen, Detektionsmethoden
3. **Konzeptuelle Inspiration**: FAIR-SW-Bench Beschreibung, Bias-Dimensionen, Prompt-Varianten-Konzept (Base/Neutral/Diversity-Aware)

---

## Intendierte Lernergebnisse

Nach Abschluss der Lehrveranstaltung sollten die Studierenden:

1. Einen Überblick über verschiedene Gender- und Diversitätstheorien haben
2. Verstehen, wie sich Bias in unterschiedlichen KI-Systemtypen manifestiert (regelbasiert, prädiktiv, generativ)
3. Bias-Detektionsmethodiken für LLMs entwerfen und implementieren können
4. Praktische Erfahrung mit KI-gestützten Entwicklungstools (Coding Agents) gesammelt haben
5. Ihre Fähigkeiten in selbstständiger Projektplanung und -umsetzung vertieft haben

---

## Prüfungsmodalitäten

### Prüfungskomponenten und Beurteilung

| Komponente | Gewichtung | Beurteilung nach |
|------------|------------|------------------|
| **Projektarbeit** (GitHub-Repo: Code + Dokumentation) | 50% | Theoriebezug, technische Umsetzung, Kreativität |
| **Abschlusspräsentation** (EH 6, 10+5 Min.) | 30% | Klarheit, Nachvollziehbarkeit, Ergebnisdarstellung |
| **Teilnahme** | 20% | Anwesenheit, aktive Beteiligung, Peer-Feedback |

Dokumentation ist Teil des Repos (.md-Dateien) – keine separate schriftliche Zusammenfassung nötig. Theoriebezug zählt mehr als Code-Komplexität. Details in [PROJECT.md](PROJECT.md).

---

## Voraussetzungen

> Grundlegende Programmierkenntnisse in mindestens einer Sprache (idealerweise Python) sowie Bereitschaft zur Arbeit mit KI-gestützten Entwicklungstools (Coding Agents). Keine Vorkenntnisse in Machine Learning oder Gender Studies erforderlich.

---

## Lehrmethodik

| Methode | Einsatz | Einheit |
|---------|---------|---------|
| **Input/Vortrag** | Theoretische Grundlagen (Teil 1), Technische Einführung (Teil 2) | EH 1–3 |
| **Textdiskussion** | Ausgewählte Texte aus Gender Studies und Science & Technology Studies | EH 2 |
| **Reflexionsübungen** | Individuelle und Gruppenreflexion zu Gender/Diversität | EH 1, 3 |
| **Projektarbeit** | Selbstständige Entwicklung des Bias-Benchmark-Tools | EH 3–6 |
| **Peer-Feedback** | Gegenseitige Rückmeldung zu Projektfortschritten | EH 5 |
| **Präsentationen** | Abschlusspräsentation der Projekte | EH 6 |

---

## Inhalte im Detail

### Teil 1: Gender- und Diversitätstheorien

- Kurze Geschichte der Gender und Diversity Studies
- De/konstruktivistische Ansätze
- Definition von Bias und Diskriminierung
- Intersektionalität
- Soziale Ungleichheiten
- Texte aus dem Bereich Science and Technology Studies
- I-Methodology (Bath 2011): Wie Entwickler:innen eigene Perspektiven als Standard setzen

### Teil 2: KI und Bias

- **KI-Typen und ihre Bias-Manifestationen**:
  - Regelbasiert: Normative Schwellenwerte und Kategorien
  - Prädiktiv: Verzerrte Trainingsdaten und Labels
  - Generativ: Stereotype Muster in Trainingskorpora

- **Empirische Befunde zu Gender Bias in LLMs** (UNESCO/IRCAI 2024, Kotek et al. 2023):
  - Stereotype Berufsassoziationen
  - "Siloing-Effekt" bei Geschlechterzuordnungen
  - Effekte von Post-Training auf Bias

- **Methoden zur Bias-Detektion**:
  - Kontrastive Prompts
  - Systematisches Output-Monitoring
  - Audit-Frameworks (HELM, DecodingTrust)
  - Das Prompt-Varianten-Konzept (Base/Neutral/Diversity-Aware)

- **Vorläufige Befunde aus FAIR-SW-Bench**:
  - Diversitäts-Instruktions-Paradox: Diversity-aware Prompts können Bias verstärken
  - Utility-Safety-Trade-off: Bias-Reduktion vs. Antwortqualität
  - Google Gemini: 100% Blockierung von Social-Work-Prompts
  - EU AI Act: Sozialarbeit als Hochrisikoanwendung ab August 2026

- **Context Engineering statt Prompt Engineering**:
  - Kontext kuratieren statt Rollen-Prompts formulieren
  - Empirische Evidenz gegen Persona-Prompting (Kim et al., ICLR 2025)
  - Relevanz für das Tool-Design der Studierenden

- **Human-in-the-Loop und AI Literacy**:
  - Kritische Bewertung von KI-Outputs
  - Entscheidungshoheit bei Fachkräften behalten

---

## Bezug zu Forschungsprojekten

### AI@youthwork

Die LV basiert auf Erkenntnissen des Forschungsprojekts **AI@youthwork** (Universität Graz, 2024–2025), das KI-Nutzung in der Kinder- und Jugendarbeit aus Gender- und Diversitätsperspektive untersucht hat.

**Relevante Publikation:**
> Sackl-Sharif, S., Klinger, S., Pollin, C. & Steiner, C. (2025). Zur ambivalenten Nutzung von Künstlicher Intelligenz in der Kinder- und Jugendarbeit aus einer geschlechter- und diversitätsreflektierenden Perspektive.

### SocialAI (Laura Bassi 4.0)

Die LV steht im Kontext des FFG-geförderten Projekts **SocialAI** (Laura Bassi 4.0, #62981337, 02/2026–01/2029), das ebenfalls Bias in KI-Systemen für soziale Kontexte untersucht.

### FAIR-SW-Bench

Das von DHCraft entwickelte Framework **FAIR-SW-Bench** (v2.1.0) dient als konzeptuelle Inspiration für die studentischen Projekte:

- Multilinguales Evaluierungssystem (DE/EN)
- LLM-as-Judge Architektur mit Cross-Provider-Validierung
- 50 Testszenarien für sozialarbeiterische Kontexte
- 5 Bias-Dimensionen: Stereotyping, Agency Attribution, Paternalistic Language, Cultural Assumptions, Problem Framing
- Prompt-Varianten-Konzept (Base/Neutral/Diversity-Aware)

**Vorläufige Befunde der Pilotstudie (2025):**

- **Diversitäts-Instruktions-Paradox**: Diversity-aware Prompts produzierten in mehreren Fällen höhere Bias-Scores als neutrale Varianten, besonders bei Agency Attribution und Problem Framing. Mögliche Erklärung: Explizite Diversitätshinweise aktivieren latente Stereotype im Modell (Salienz-Effekt).
- **Utility-Safety-Trade-off**: Bias-Reduktion geht möglicherweise auf Kosten der Antwortqualität. Diversity-aware Varianten zeigten niedrigere Bias-Scores (Ø 3.8) aber auch reduzierte Helpfulness-Werte (Ø 4.1) gegenüber Base-Varianten (Bias: 6.2, Helpfulness: 8.1).
- **Google Gemini blockiert 100%** aller Social-Work-Prompts durch undokumentierte Safety-Filter, die sich nicht deaktivieren lassen.
- **Methodische Einschränkung**: Pilotstudie mit 30/50 Prompts, nur ein Provider (Anthropic), englische Judge-Prompts für deutsche Outputs, keine Human-Annotation. Ergebnisse erfordern Validierung.

Diese Befunde werden in EH 3 vorgestellt, damit die Studierenden sie als Ausgangspunkt für eigene Untersuchungen nutzen können.

---

## Kontakt und Organisation

| Rolle | Person | Kontakt |
|-------|--------|---------|
| Hauptlehrende | Susanne Sackl-Sharif | Universität Graz |
| Gastbeitrag KI & Bias | Christian Steiner | Digital Humanities Craft OG |
| LV-Koordination Klagenfurt | Noreen | Universität Klagenfurt |

---

## Offene Punkte

- [ ] Terminänderung an Noreen kommunizieren (26.03. kürzen, 11.05. neu)
- [ ] Textauswahl für Diskussionen in Teil 1 finalisieren
- [x] ~~FAIR-SW-Bench Konzeptdokumentation für Studierende aufbereiten~~ – in PROJECT.md integriert (Beispiel-Prompts, Befunde, Dimensionen)
- [ ] Moodle-Kurs einrichten
- [x] ~~API-Kosten und -Zugang für Studierende klären~~ – gelöst: Ollama (lokale Modelle) + Free-Tier Web-Interfaces

---

## Änderungshistorie

| Datum | Änderung |
|-------|----------|
| März 2026 | Erste Version erstellt |
| März 2026 | Termine aus Campus-System übernommen; EH 2 gekürzt (-2h), EH 4 als Q&A-Session neu eingefügt (+2h am 11.05.) |
| März 2026 | Überarbeitung: Projektauftrag in EH 2, Gastbeitrag in EH 3 zum Projektstart, Peer-Feedback in EH 5, Meilensteine und Bewertungsgewichtung ergänzt, Minimalanforderungen definiert |
| März 2026 | Feedbackrunde: Bewertung vereinfacht (50/30/20), Option B (Datensatz) entfernt, Ollama als Hauptempfehlung, Teams max. 3, schriftliche Zusammenfassung entfällt |
| März 2026 | FAIR-SW-Bench Befunde integriert: Diversitäts-Instruktions-Paradox, Utility-Safety-Trade-off, Gemini-Blockierung, EU AI Act Kontext, Context Engineering, konkrete Beispiel-Prompts |

---

*Erstellt: März 2026*
*Status: Planungsphase*
