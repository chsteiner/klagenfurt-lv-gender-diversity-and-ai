# Requirements: LV-Begleitwebsite

## Epic 1: Seitenstruktur und Navigation

### US-1.1: Landing Page
Als Studierende:r will ich beim Öffnen der Website sofort sehen, worum es geht und wo ich was finde, damit ich nicht suchen muss.

**Inhalt:**
- LV-Titel, Semester, Lehrende
- Kurzfassung: Worum geht's? (2-3 Sätze)
- Direkte Links zu den wichtigsten Unterseiten
- Nächster Meilenstein / aktuelle Phase hervorheben

**Erfolgskriterium:** Studierende:r findet den Projektauftrag in unter 5 Sekunden.

### US-1.2: Sidebar-Navigation
Als Studierende:r will ich jederzeit alle Seiten in einer Sidebar sehen, damit ich direkt navigieren kann.

**Struktur:**
```
Home
Projektauftrag
Zeitplan & Meilensteine
Theorie-Überblick
FAIR-SW-Bench
Ressourcen & Tools
```

**Erfolgskriterium:** Max. 6-7 Einträge, kein Scrollen in der Sidebar nötig.

---

## Epic 2: Projektauftrag

### US-2.1: Vollständiger Projektauftrag
Als Studierende:r will ich den gesamten Projektauftrag auf einer Seite lesen, damit ich alles an einem Ort habe.

**Quelle:** `PROJECT.md` (Root)
**Anpassungen:** Identischer Inhalt, ggf. Docsify-spezifische Formatierung (Callout-Boxen statt plain Markdown).

**Erfolgskriterium:** Inhaltlich identisch mit PROJECT.md, optisch aufgewertet durch Docsify-Features.

---

## Epic 3: Zeitplan

### US-3.1: Zeitplan mit Meilensteinen
Als Studierende:r will ich auf einen Blick sehen, wann welche Einheit stattfindet und was bis wann abzugeben ist.

**Quelle:** README.md (Zeitplan-Tabellen, Meilensteine)
**Inhalt:**
- Alle 6 Einheiten mit Datum, Uhrzeit, Format, Raum, Inhalt
- Meilensteine-Tabelle aus PROJECT.md
- Prüfungsmodalitäten (50/30/20)

**Erfolgskriterium:** Alle Termine und Deadlines auf einer Seite.

---

## Epic 4: Theorie-Überblick

### US-4.1: Theoretische Grundlagen für Informatiker:innen
Als Studierende:r will ich die wichtigsten Gender/Diversity-Theorien kompakt nachlesen, damit ich sie für mein Projekt nutzen kann.

**Quelle:** `GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md` (Teil A + Teil F)
**Was rein:**
- A.1: Technik ist nicht neutral (Winner)
- A.2: I-Methodology (Bath, Oudshoorn)
- A.3: Gender als Strukturkategorie (gekürzt)
- A.4: Intersektionalität (Crenshaw, Gender Shades)
- A.6: Frameworks (Gendered Innovations, Value Sensitive Design, Data Feminism)
- A.8: Raw Data Is an Oxymoron
- F: FAIR-SW-Bench Konzeptinspiration (Varianten, Dimensionen, Paradox) – oder eigene Seite

**Was NICHT rein:**
- Teil B (Didaktik) – für Susi, nicht für Studis
- Teil C (Einheitenplanung) – internes Dokument
- Teil D (Literaturlisten für Susi) – zu umfangreich
- Teil E (Brückentabelle) – kurze Version reicht

**Erfolgskriterium:** Studierende können die für ihr Projekt relevanten Theorien nachschlagen, ohne 400 Zeilen lesen zu müssen.

---

## Epic 5: FAIR-SW-Bench

### US-5.1: FAIR-SW-Bench Forschungskontext
Als Studierende:r will ich verstehen, was FAIR-SW-Bench ist und was wir daraus lernen können, damit ich das Konzept als Inspiration nutzen kann.

**Inhalt:**
- Was ist FAIR-SW-Bench? (1 Absatz)
- Das Prompt-Varianten-Konzept (Base/Neutral/Diversity-Aware) mit konkreten Beispielen
- Die 5 Bias-Dimensionen (Tabelle)
- Das Diversitäts-Instruktions-Paradox (Schlüsselbefund)
- Utility-Safety-Trade-off
- Gemini-Blockierung als Warnung
- Methodische Einschränkungen (transparent)

**Quellen:** PROJECT.md (Auszüge), GENDER-DIVERSITY-FUER-TECHNIKERINNEN.md (Teil F), Obsidian-Vault FAIR-SW-Bench Notizen

**Erfolgskriterium:** Studierende verstehen das Konzept ohne den Code gesehen zu haben.

---

## Epic 6: Ressourcen & Tools

### US-6.1: Technische Ressourcen
Als Studierende:r will ich alle Tools und Links an einem Ort, damit ich nicht in verschiedenen Dokumenten suchen muss.

**Inhalt:**
- Ollama Setup (mit Python-Beispiel)
- Free-Tier Web-Interfaces
- Gemini-Warnung
- Context Engineering (kurze Einführung)
- Literatur / Schlüsseltexte (die für Studis relevanten aus Teil D)
- Kontakt: Wer beantwortet was? (Christian: Technik, Susi: Theorie)

**Erfolgskriterium:** Studierende können Ollama einrichten, ohne andere Quellen zu brauchen.

---

## Nicht-funktionale Anforderungen

| Aspekt | Anforderung |
|--------|------------|
| **Deployment** | GitHub Pages aus `/docs`-Ordner, kein Build nötig |
| **Performance** | Docsify CDN, keine lokalen Dependencies |
| **Accessibility** | Lesbar ohne JavaScript? Nein (Docsify-Limitation). Akzeptabel für Master-Informatik. |
| **Wartung** | Markdown-Dateien direkt editierbar, keine Toolchain |
| **Mobile** | Docsify-Default-Theme ist responsive |
| **Suche** | Docsify Search Plugin (client-seitig) |
