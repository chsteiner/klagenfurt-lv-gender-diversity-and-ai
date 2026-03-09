# Gender & Diversität für Informatiker:innen: Theorien, Brückenkonzepte und Didaktik

> **Begleitdokument für Susanne Sackl-Sharif – EH 1 & EH 2 der LV "Gender, Diversität und KI"**
> Universität Klagenfurt, Master Informatik, SS2026

---

## Warum dieses Dokument?

Eine Einführung in Gender und Diversität für Master-Studierende der Informatik erfordert andere theoretische Zugänge als für Sozialarbeiter:innen oder Geisteswissenschaftler:innen. Es gibt eigene Theorien an der Schnittstelle Gender/Diversität und Technik, die direkt an die Lebenswelt und Praxis von Informatiker:innen anschließen.

Dieses Dokument richtet sich an Susi als Lehrende. Wo Formulierungen die Studierenden direkt ansprechen (z.B. Leitfragen wie "Ist eure Software neutral?"), sind das Vorschläge für den Einsatz im Seminar.

Das Dokument enthält:

1. Theoretische Grundlagen, speziell für eine technische Zielgruppe aufbereitet (Teil A)
2. Didaktische Empfehlungen und aktivierende Methoden (Teil B)
3. Vorschlag für die Einheitenplanung EH 1 und EH 2 (Teil C)
4. Schlüsseltexte und Literatur (Teil D)
5. Verbindung zum Projektauftrag und FAIR-SW-Bench (Teil E–F)

---

## Teil A: Theoretischer Rahmen

### A.1 Das Kernproblem: Technik ist nicht neutral

Der zentrale Einstiegspunkt für Informatik-Studierende ist nicht "Was ist Gender?", sondern **"Ist eure Software neutral?"** – und die Antwort lautet: Nein.

Technik wird von Menschen entwickelt und spiegelt deren Perspektiven, Annahmen und blinde Flecken wider. Geschlecht, Herkunft, Klasse und andere soziale Kategorien sind bereits in technische Systeme eingeschrieben – als sogenannte **gendered substructures** (Carstensen & Ganz 2023).

> **Langdon Winner (1980): "Do Artifacts Have Politics?"**
> Winners Klassiker zeigt, dass technische Artefakte politisch sein können – nicht nur in ihrer Nutzung, sondern in ihrer Gestaltung. Sein berühmtes Beispiel: Robert Moses' niedrige Brücken auf Long Island, die Busse (und damit ärmere, Schwarze Bevölkerung) von den Stränden fernhielten. Die politische Entscheidung wurde in Beton gegossen.
>
> *Didaktischer Wert:* Kurzer, provokanter Text, ideal als Einstieg. Gut diskutierbar, da Informatik-Studierende intuitiv verstehen, dass Designentscheidungen Konsequenzen haben.
>
> Quelle: Winner, L. (1980). Do Artifacts Have Politics? *Daedalus*, 109(1), 121–136.

---

### A.2 I-Methodology – Die Schlüsseltheorie für Informatiker:innen

Die **I-Methodology** (Oudshoorn, Rommes & Stienstra 2004; weiterentwickelt von Corinna Bath 2009) ist das wichtigste Brückenkonzept zwischen Gender-Theorie und Informatik. Sie beschreibt ein Phänomen, das jede:r Entwickler:in kennt:

> **Entwickler:innen nehmen sich selbst als repräsentativ für alle Nutzer:innen.**

Sie behandeln ihre eigenen Bedürfnisse, Sichtweisen und Anforderungen als objektiv und universell – **"Configuring the User as Everybody"**. Da Entwicklungsteams häufig von männlichen, weißen, jungen, akademisch gebildeten Personen dominiert werden, werden deren Eigenschaften und Perspektiven unbewusst in technische Artefakte eingeschrieben.

#### Konkrete Beispiele

| Bereich | I-Methodology-Problem | Konsequenz |
|---------|----------------------|------------|
| **Spracherkennung** | Training primär mit männlichen Stimmen | Frauen- und Kinderstimmen werden schlechter erkannt |
| **Crash-Test-Dummies** | Basieren auf männlichen Körpern | Frauen haben 47% höheres Verletzungsrisiko bei Autounfällen |
| **Gesichtserkennung** | Trainingsdaten zu 79% hellhäutig | Fehlerrate für dunkelhäutige Frauen: bis 34,7% (Buolamwini & Gebru 2018) |
| **Sprachassistenten** | Standardmäßig weibliche Stimmen | Reproduktion des Stereotyps "Service = weiblich" |
| **LLMs** | Trainingsdaten überproportional englisch, männlich, westlich | Stereotype Berufsassoziationen, kultureller Bias |

#### Bath: De-Gendering informatischer Artefakte

Corinna Bath (2009) entwickelte als Antwort auf die I-Methodology das Konzept des De-Gendering: Systematische Identifikation von Vergeschlechtlichungsprozessen in Produkten, Theorien, Methoden und Annahmen der Informatik. Konkret heißt das: In jedem Schritt des Designprozesses fragen, welche Geschlechterannahmen eingeschrieben sind – und alternative Gestaltungswege suchen.

> **Warum ist das für Informatiker:innen relevant?**
> Weil es direkt am Software-Engineering-Prozess ansetzt. Es geht nicht um abstrakte Theorie, sondern um die Frage: Für wen designst du? Und wen schließt du dabei aus?

**Quellen:**
- Oudshoorn, N., Rommes, E. & Stienstra, M. (2004). Configuring the User as Everybody. *Science, Technology, & Human Values*, 29(1).
- Bath, C. (2009). *De-Gendering informatischer Artefakte.* Dissertation, Universität Bremen.
- Bath, C. (2014). Searching for Methodology: Feminist Technology Design in Computer Science.

---

### A.3 Gender – das soziale Geschlecht (für eine technische Zielgruppe)

Für Informatik-Studierende ist es wichtig, Gender nicht als "Identitätspolitik" zu rahmen, sondern als **Strukturkategorie**, die technische Systeme durchzieht.

Kernaussagen:

- Geschlecht ist sozial konstruiert – keine unveränderliche biologische Eigenschaft, sondern Ergebnis gesellschaftlicher Prozesse (Mense & Sera 2019). Unterschiede zwischen Geschlechtern wandeln sich historisch und kulturell.
- Geschlecht ist ein Strukturprinzip – es prägt systematisch den Zugang zu Bildung, Arbeit, Einkommen, Gesundheit, politischer und digitaler Teilhabe.
- Der implizite Standard – ohne Genderperspektive wird "der Mensch" zum Default: weiß, männlich, heterosexuell, gesund, mittleren Alters und bildungsnah (de Beauvoir 1949/2011). In der Informatik manifestiert sich das direkt in der I-Methodology.
- Hegemoniale Männlichkeit (Connell 2014) – das gesellschaftlich dominante Männerbild stabilisiert sich durch Abgrenzung von allem "Anderen". In der Tech-Industrie zeigt sich das in Startup-Kultur, "Bro Culture" und der Marginalisierung nicht-normativer Identitäten.

> **Brücke zur Informatik:** Der Gender Data Gap (Criado-Perez 2020) zeigt, wie fehlende Daten über Frauen und marginalisierte Gruppen direkt zu schlechteren technischen Produkten führen – von Medikamenten bis Sicherheitsgurten, von Sprachsystemen bis Algorithmen.

---

### A.4 Diversität und Intersektionalität

#### Diversität als professionelle Aufgabe

Diversität beschreibt gesellschaftliche Vielfalt entlang unterschiedlicher sozialer Kategorien: Alter, Herkunft, Bildung, Behinderung, sexuelle Orientierung, Religion, soziale Lage. In der Informatik ist das relevant, weil:

- Software für diverse Nutzer:innengruppen entwickelt wird
- Homogene Teams systematisch blinde Flecken produzieren (vgl. I-Methodology)
- Diverse Teams unterschiedliche Fehlermuster erkennen und alternative Designentscheidungen treffen

#### Intersektionalität (Crenshaw 1989)

Soziale Kategorien wie Geschlecht, Herkunft oder Klasse wirken nicht getrennt, sondern überlappen und verstärken sich gegenseitig. Die Studie Gender Shades (Buolamwini & Gebru 2018) ist das Paradebeispiel intersektionaler KI-Forschung:

- Weder eine reine Gender-Analyse noch eine reine Hautfarben-Analyse hätte den spezifischen Nachteil für Schwarze Frauen sichtbar gemacht
- Erst die intersektionale Betrachtung (Geschlecht × Hautton) offenbarte das volle Ausmaß der Diskriminierung (0,8% vs. 34,7% Fehlerrate)
- Die Studie führte direkt dazu, dass IBM sein Gesichtserkennungsprogramm einstellte

> Für Informatiker:innen heißt das: Eindimensionale Fairness-Metriken (nur Gender ODER nur Race) greifen zu kurz. Intersektionale Evaluation ist methodisch notwendig, nicht nur politisch wünschenswert.

---

### A.5 Feminist Technology Studies – Schlüsseltheorien

| Theorie / Autorin | Kernaussage | Relevanz für Informatik |
|-------------------|-------------|------------------------|
| Feminist STS (Wajcman 2004/2010) | Gender und Technologie formen sich wechselseitig (*mutual shaping*). Technik materialisiert soziale Verhältnisse. | Wer Software entwickelt, gestaltet Machtverhältnisse mit. |
| Script Theory (Akrich 1992) | Designer:innen schreiben in Artefakte "Scripts" ein – antizipierte Nutzungsszenarien und Rollen. | De-Scription: Welche Annahmen über "ideale Nutzer:innen" stecken in der Software? |
| Situated Actions (Suchman 1987) | Menschliches Handeln ist situiert und kontextabhängig, nicht planbasiert, wie KI-Forschung annimmt. | Grundlagenwerk für HCI. Zeigt die Grenzen formaler Modelle menschlichen Handelns. |
| Cyborg Manifesto (Haraway 1991) | Denkfigur für die Verschränkung von Mensch und Technik jenseits binärer Kategorien. | Hinterfragt die Grenzziehung Mensch/Maschine, männlich/weiblich, Natur/Kultur. |
| Standpoint Theory (Harding 1986) | Die Perspektive marginalisierter Gruppen ermöglicht "starke Objektivität" – wer Ungerechtigkeit erfährt, sieht systematische Probleme, die aus privilegierter Position unsichtbar bleiben. | Wer gestaltet die Systeme? Wessen Perspektive fehlt? |

---

### A.6 Frameworks für die Praxis

#### Gendered Innovations (Schiebinger, Stanford)

Drei Strategien: (1) "Fix the Numbers" – mehr Frauen in MINT, (2) "Fix the Institutions" – strukturelle Gleichstellung, (3) "Fix the Knowledge" – Sex- und Gender-Analyse in die Forschung selbst integrieren. Der dritte Punkt ist für die LV der relevanteste: Gender-Analyse führt nicht nur zu gerechterer, sondern zu besserer Wissenschaft und Technik. Website: [genderedinnovations.stanford.edu](https://genderedinnovations.stanford.edu/)

#### Data Feminism (D'Ignazio & Klein 2020)

Sieben Prinzipien für feministische Datenwissenschaft, direkt anschlussfähig an das Projektthema:

1. Examine Power – Machtstrukturen in Datensystemen erkennen
2. Challenge Power – Ungleiche Machtstrukturen aktiv abbauen
3. Elevate Emotion and Embodiment – nicht nur "objektive" Zahlen
4. Rethink Binaries and Hierarchies – binäre Klassifikationen hinterfragen
5. Embrace Pluralism – vielfältige Perspektiven, lokales Wissen priorisieren
6. Consider Context – Daten nie ohne Entstehungskontext interpretieren
7. Make Labor Visible – unsichtbare Arbeit hinter Datensystemen anerkennen (Clickworker:innen, Datenannotation)

Frei verfügbar: [data-feminism.mitpress.mit.edu](https://data-feminism.mitpress.mit.edu/)

Zwei weitere Frameworks eignen sich als Vertiefung: Value Sensitive Design (Friedman & Hendry 2019) bietet konkrete Methoden wie Stakeholder-Analyse und Value Scenarios für Software-Projekte. Feminist HCI (Bardzell 2010) formuliert sechs Qualitäten feministischen Interaction Designs (Pluralismus, Partizipation, Advocacy, Ökologie, Embodiment, Self-Disclosure). Beide stehen in der Hintergrundliteratur (Teil D).

---

### A.7 Weitere kritische Perspektiven

Die folgenden Perspektiven vertiefen die Analyse über Gender hinaus. Sie eignen sich als Vertiefungslektüre für Susi oder als optionale Lesehinweise für Studierende, die intersektionale Dimensionen in ihrem Projekt untersuchen wollen.

**Postkolonial:** Bender, Gebru et al. (2021) analysieren LLMs als "stochastische Papageien", deren Trainingsdaten westliche, englischsprachige Perspektiven überrepräsentieren. Birhane (2020) zeigt, wie KI-Einsatz im Globalen Süden koloniale Muster reproduziert.

**Queer:** Keyes (2018) untersucht Automatic Gender Recognition und zeigt, dass diese Systeme Geschlecht durchgängig binär, unveränderlich und an Physiologie gekoppelt operationalisieren – trans-exklusiv by design. Relevant für jedes ML-System, das Geschlecht als Kategorie verwendet.

**Disability:** Shew (2020) prägt den Begriff "Technoableismus" für die Annahme, Behinderung sei ein durch Technologie lösbares Problem. Die Gegenposition: Partizipatives Design von Anfang an statt nachträglicher Accessibility-Patches.

---

### A.8 Critical Data Studies: "Raw Data Is an Oxymoron"

Ein zentraler Baustein für Informatik-Studierende ist die Einsicht, dass **Daten nie neutral sind** (Gitelman 2013). Daten werden immer in bestimmten historischen, sozialen und kulturellen Kontexten erzeugt, geordnet und interpretiert. Sie sind nicht "einfach da", sondern immer schon durch Entscheidungen über Kategorisierung, Auswahl und Aufbereitung geformt.

Für das Projektthema (Bias in LLMs) ist das direkt relevant: Die Trainingsdaten von LLMs sind kein neutraler Spiegel der Welt, sondern eine spezifische, verzerrte Auswahl, die gesellschaftliche Machtverhältnisse widerspiegelt.

---

## Teil B: Didaktische Empfehlungen

### B.1 Typische Widerstände bei STEM-Studierenden

| Widerstand | Erscheinungsform | Strategie |
|-----------|------------------|-----------|
| "Das hat nichts mit Informatik zu tun" | Relevanzfrage, Abwehr | Gender als genuines Problem der Informatik rahmen, nicht als externes Add-on |
| Meritokratie-Mythos | "In der Informatik zählt nur Code" | Empirische Evidenz: Amazon Recruiting Tool, Gender Shades, COMPAS |
| Affektive Abwehr | Unbehagen bei Privilegien-Themen | Selbstreflexion ermöglichen, nicht erzwingen. IAT statt Moralpredigt |
| "Ich bin ja nicht sexistisch" | Individualisierung statt Strukturanalyse | Fokus auf Systeme und Strukturen, nicht auf individuelle Schuld |
| Doing Gender im Seminar | Dominanzverhalten, Mansplaining | Aktive Moderation, Kleingruppenformate, strukturierte Diskussionen |

### B.2 Was funktioniert – didaktische Prinzipien

1. **Fachliche Anknüpfung statt Moralpredigt**: "Warum erkennt Gesichtserkennung dunkle Haut schlechter?" statt "Lasst uns über Feminismus reden."
2. **Empirische Evidenz statt normativer Appelle**: STEM-Studierende reagieren auf Daten, Messungen und nachvollziehbare Experimente.
3. **Selbsterfahrung statt Belehrung**: IAT, eigene Bias-Tests mit LLMs, kontrastive Prompt-Analyse.
4. **Evidenzbasierte Diskussion**: Keine Meinungsfragen ("Findest du Diskriminierung schlimm?"), sondern empirische Fragen ("Zeigen die Daten einen Unterschied? Wie groß ist er? Wie erklärst du ihn?").
5. **Vom Konkreten zum Abstrakten**: Erst Fallbeispiele (Amazon, COMPAS, Gender Shades), dann Theorie (I-Methodology, Intersektionalität).
6. **Theorie als Analysewerkzeug, nicht als Dogma**: Theorien sind Brillen, die bestimmte Dinge sichtbar machen – nicht moralische Vorschriften.

### B.3 Aktivierende Methoden

| Methode | Beschreibung | Zeitbedarf | Eignung |
|---------|-------------|-----------|---------|
| Implicit Association Test (IAT) | Studierende testen eigene unbewusste Assoziationen unter [implicit.harvard.edu](https://implicit.harvard.edu) | 15–20 Min. | Einstieg in Bias, Selbsterfahrung |
| Case Study Analyse | Amazon Recruiting, COMPAS, Gender Shades – Gruppen analysieren je einen Fall | 30–45 Min. | Empirische Evidenz, Diskussion |
| Kontrastive Prompt-Analyse | Gleicher Prompt mit verschiedenen demografischen Markern an ein LLM, Ergebnisse vergleichen (live im Seminar oder als Vorbereitung) | 20–30 Min. | Brücke zum Projektauftrag |
| De-Scription-Übung | Eine App/Website systematisch auf eingeschriebene Annahmen über "ideale Nutzer:innen" analysieren (nach Akrich) | 20–30 Min. | Script Theory praktisch anwenden |
| Pipeline vs. Climate Debatte | Zwei Gruppen argumentieren: "Wir brauchen mehr Frauen in der Informatik" vs. "Wir müssen die Kultur in der Informatik ändern." Hintergrund: Fouad-Studie zeigt, dass 38% der Ingenieurinnen wegen des Arbeitsumfelds aufhörten, nicht wegen der Arbeit. | 20–30 Min. | Strukturelle Analyse, Perspektivenwechsel |
| "Für wen designst du?" | Studierende beschreiben ihre "Standard-Nutzer:in" für ein fiktives Projekt → I-Methodology sichtbar machen | 15–20 Min. | I-Methodology erlebbar machen |

---

## Teil C: Vorschlag Einheitenplanung

> Die folgenden Ablaufpläne sind Vorschläge. Susi kennt ihre Lehrpraxis und passt Reihenfolge, Tiefe und Methoden nach eigenem Ermessen an.

### EH 1: Di 17.03.2026, 13:30–18:30, Präsenz, C.0.16 (~5h)

**Leitfrage: "Ist Technik neutral?"**

| Zeit | Block | Inhalt | Methode | Material |
|------|-------|--------|---------|----------|
| 13:30–13:50 | Ankommen & Kennenlernen | Vorstellung, LV-Überblick, Erwartungsabfrage | Plenum | – |
| 13:50–14:20 | Einstieg: "Do Artifacts Have Politics?" | Winners Brücken-Beispiel + 2–3 aktuelle Tech-Beispiele (Siri weiblich, Crash-Test-Dummies, Spracherkennung). Leitfrage an die Studierenden: Wo stecken Designentscheidungen in Technik, die ihr täglich nutzt? | Input + Murmelgruppen | Folien, ggf. Kurzclip |
| 14:20–15:00 | Gender als Strukturkategorie | Was ist Gender? Soziale Konstruktion, Strukturprinzip, impliziter Standard. Fokus: Gender als Analysewerkzeug, nicht als Identitätspolitik. Hegemoniale Männlichkeit nur anreißen (Vertiefung bei Bedarf in EH 2). | Input mit Diskussionseinschüben | Folien |
| 15:00–15:15 | *Pause* | | | |
| 15:15–15:50 | Reflexionsübung: IAT | Studierende testen eigene unbewusste Assoziationen (Gender-Career oder Gender-Science) auf implicit.harvard.edu. Freiwillige Reflexion in Kleingruppen (nicht im Plenum!). | Einzelarbeit + Kleingruppe (3–4 Pers.) | Laptops/Smartphones, Link |
| 15:50–16:45 | I-Methodology + "Für wen designst du?" | Kerntheorie: "Configuring the User as Everybody." Beispiele: Gender Data Gap, Spracherkennung, Gesichtserkennung. Dann direkt in die Übung: Studierende beschreiben in Kleingruppen die "Standard-Nutzer:in" für ein fiktives App-Projekt. Auswertung im Plenum: Wer wurde vergessen? | Input (25 Min.) → Übung + Auswertung (30 Min.) | Folien, Arbeitsblatt |
| 16:45–17:00 | *Pause* | | | |
| 17:00–17:45 | Diversität und Intersektionalität | Diversität in der Softwareentwicklung. Intersektionalität: Warum eindimensionale Analyse nicht reicht (Gender Shades als Beispiel). Data Feminism Prinzipien als Kurzvorstellung. | Input + Diskussion | Folien |
| 17:45–18:15 | Wrap-up & Ausblick | Kernkonzepte sichern. Leseaufträge für EH 2. Offene Fragen. | Plenum | – |

*Puffer: 15 Min. bis 18:30 für Überzug oder vertiefende Diskussion.*

**Leseaufträge für EH 2 (Vorschläge – Susi wählt aus):**
- Winner, L. (1980). Do Artifacts Have Politics? (Kurzversion / Auszug)
- Bath, C. (2014). Searching for Methodology (Auszug)
- Criado-Perez, C. (2020). Unsichtbare Frauen (ausgewähltes Kapitel)
- *Oder:* Buolamwini, J. & Gebru, T. (2018). Gender Shades (Paper)

---

### EH 2: Do 26.03.2026, 13:30–18:15, Präsenz, C.0.16 (~4,75h)

**Leitfrage: "Was hat das mit KI zu tun?"**

| Zeit | Block | Inhalt | Methode | Material |
|------|-------|--------|---------|----------|
| 13:30–14:00 | Rückblick & Textdiskussion | Zentrale Erkenntnisse aus EH 1. Diskussion der gelesenen Texte: Was war überraschend? Was war umstritten? Wo seht ihr Verbindungen zur eigenen Praxis? | Fishbowl oder Gruppenarbeit + Plenum | Texte |
| 14:00–14:45 | Vertiefung: Feminist STS | Wajcman (Mutual Shaping), Akrich (Script Theory), Suchman (Situated Actions). Kernfrage an die Studierenden: Wie schreiben Entwickler:innen Annahmen in Artefakte ein? | Input + De-Scription-Übung (App analysieren) | Folien, Smartphones |
| 14:45–15:00 | *Pause* | | | |
| 15:00–15:45 | Case Studies: Bias in KI-Systemen | 3 Gruppen bearbeiten je einen Fall: (1) Amazon Recruiting Tool, (2) COMPAS, (3) Gender Shades. Leitfragen: Was ging schief? Auf welcher Ebene entstand der Bias? Welche Theorie aus EH 1 erklärt das? | Gruppenarbeit + Kurzpräsentationen (je 5 Min.) | Fallbeschreibungen (1-Seiter), Leitfragen |
| 15:45–16:30 | Von Bias zu Fairness | Bias-Taxonomie nach Suresh & Guttag (2021): 7 Quellen von Bias im ML-Lebenszyklus. Kurzeinführung Fairness-Metriken (Demographic Parity, Equalized Odds, Calibration) und das Impossibility Theorem. Nicht als Mathe-Vorlesung, sondern als konzeptuelle Einführung. | Input + Diskussion | Folien, Schaubild ML-Lebenszyklus |
| 16:30–16:45 | *Pause* | | | |
| 16:45–17:15 | Pipeline vs. Climate | Warum sind weniger Frauen in der Informatik? Nicht nur ein Rekrutierungsproblem (Pipeline), sondern ein Kulturproblem (Climate). Fouad-Studie: 38% der Ingenieurinnen verließen den Beruf wegen des Arbeitsumfelds, nicht wegen der Arbeit. Von "Leaky Pipeline" zu "Broken Scaffolding." | Kurz-Input + offene Diskussion | Folien, ggf. Statistiken |
| 17:15–17:45 | Projektauftrag vorstellen | Vorstellung des Projektauftrags (PROJECT.md): Bias-Benchmark-Tool für LLMs. Minimalanforderungen, mögliche Ansätze, Meilensteine, Bewertungskriterien. Bezug zu den Theorien: Welche Bias-Dimensionen lassen sich aus dem Gelernten ableiten? | Input + Q&A | PROJECT.md, Beamer |
| 17:45–18:15 | Gruppenbildung anstoßen | Erste Ideensammlung: Welches Themenfeld? Welche Bias-Dimensionen? Gruppen finden sich (max. 3 Personen). Deadline: bis EH 3 (27.04.). | Marktplatz-Format / freie Bewegung | Flipchart/Whiteboard für Themencluster |

---

## Teil D: Empfohlene Schlüsseltexte

### Primärtexte für Studierende (Auswahl durch Susi)

| Text | Typ | Seiten | Sprache | Eignung |
|------|-----|--------|---------|---------|
| Winner (1980): Do Artifacts Have Politics? | Klassiker | 16 | EN | Einstieg, provokant, gut diskutierbar |
| Bath (2014): Searching for Methodology | Fachtext | ~20 | EN | I-Methodology vertieft |
| Criado-Perez (2020): Unsichtbare Frauen (Kap. nach Wahl) | Sachbuch | variabel | DE | Sehr zugänglich, viele Beispiele |
| Buolamwini & Gebru (2018): Gender Shades | Paper | 15 | EN | Intersektionalität + KI, empirisch |
| Noble (2018): Algorithms of Oppression (Intro) | Monografie | ~20 | EN | Algorithmische Unterdrückung |
| D'Ignazio & Klein (2020): Data Feminism (Kap. 1) | Open Access | ~30 | EN | Data Feminism Grundlagen |

### Hintergrundliteratur für Susi

**Priorität – diese fünf zuerst:**

- Wajcman, J. (2010). Feminist Theories of Technology. *Cambridge Journal of Economics*, 34(1), 143–152. → Kompakter Überblick über Feminist STS, 10 Seiten.
- Suresh, H. & Guttag, J. (2021). A Framework for Understanding Sources of Harm. *ACM EAAMO*. → Bias-Taxonomie, direkt anwendbar auf Projektauftrag.
- Crawford, K. (2021). *Atlas of AI.* Yale University Press. → Breit zugänglich, verbindet Macht, Arbeit und Daten.
- Connell, R. (2014). *Der gemachte Mann.* 4. Aufl., Springer VS. → Hegemoniale Männlichkeit auf Deutsch, Standardwerk.
- Mehrabi, N. et al. (2021). A Survey on Bias and Fairness in ML. *ACM Computing Surveys*. → Umfassender Survey, gut als Nachschlagewerk.

**Weitere Literatur:**

- Akrich, M. (1992). The De-Scription of Technical Objects. In: Bijker & Law (Hrsg.): Shaping Technology/Building Society.
- Suchman, L. (1987). *Plans and Situated Actions.* Cambridge University Press.
- Haraway, D. (1991). Simians, Cyborgs, and Women. Routledge.
- Harding, S. (1986). *The Science Question in Feminism.* Cornell University Press.
- Bardzell, S. (2010). Feminist HCI: Taking Stock and Outlining an Agenda for Design. *CHI '10*, ACM.
- Friedman, B. & Hendry, D. (2019). *Value Sensitive Design.* MIT Press.
- Schiebinger, L. (2008). *Gendered Innovations.* Stanford University Press.
- Keyes, O. (2018). The Misgendering Machines. *CSCW*, ACM.
- Shew, A. (2020). Ableism, Technoableism, and Future AI. *IEEE Technology and Society Magazine*.
- Benjamin, R. (2019). *Race After Technology.* Polity Press.
- Birhane, A. (2020). Algorithmic Colonization of Africa. In: *Imagining AI*, Oxford University Press.
- Mhlambi, S. (2020). From Rationality to Relationality. Berkman Klein Center, Harvard.
- Gitelman, L. (Hrsg.) (2013). *"Raw Data" Is an Oxymoron.* MIT Press.
- Spieler, B. & Both, G. (2021). Gender- & Diversitäts-Aspekte in der Informatik.

### Didaktische Ressourcen

- [Gender-Curricula: Informatik](https://www.gender-curricula.com) – Netzwerk Frauen- und Geschlechterforschung NRW
- [Gendered Innovations](https://genderedinnovations.stanford.edu/) – Stanford University
- [Data Feminism](https://data-feminism.mitpress.mit.edu/) – MIT Press (Open Access)
- [Implicit Association Test](https://implicit.harvard.edu) – Harvard Project Implicit
- [Gendering MINT digital](https://www2.hu-berlin.de/genderingmintdigital/informatik/) – HU Berlin

---

## Teil E: Verbindung zum Projektauftrag (EH 3–6)

Die Theorien aus EH 1–2 liefern den analytischen Rahmen für die studentischen Projekte:

| Theorie (EH 1–2) | Anwendung im Projekt (EH 3–6) |
|-------------------|-------------------------------|
| I-Methodology | Wessen Perspektive steckt in den Trainingsdaten des LLM? |
| Intersektionalität | Bias-Dimensionen kombiniert testen (z.B. Gender × Herkunft) |
| Script Theory | Welche "Scripts" schreibt das LLM in seine Antworten ein? |
| Gender Data Gap | Welche Gruppen sind in den Trainingsdaten unterrepräsentiert? |
| Data Feminism | "Consider Context" – Trainingsdaten sind nie neutral |
| Bias-Taxonomie (Suresh & Guttag) | Auf welcher Ebene entsteht der Bias im LLM? |
| Fairness-Metriken | Wie misst man Bias systematisch? |

Christian Steiners Gastbeitrag in EH 3 baut auf diesen Grundlagen auf und ergänzt den technischen Teil: KI-Typen, Bias-Manifestationen, Detektionsmethoden. Die Studierenden verbinden dann beides – Theorie als Analysewerkzeug, Technik als Messinstrument.

---

## Teil F: FAIR-SW-Bench – Konzeptuelle Inspiration aus der Forschung

Die studentischen Projekte sind inspiriert vom FAIR-SW-Bench Framework (DHCraft, v2.1.0), entwickelt im Laura-Bassi-Projekt SocialAI (Universität Graz). Die Studierenden erhalten die Konzeptbeschreibung als Inspiration, nicht den Code.

### F.1 Das Prompt-Varianten-Konzept

FAIR-SW-Bench testet jeden Prompt in drei systematisch generierten Varianten:

| Variante | Beschreibung | Beispiel (Geschwistertrennung) |
|----------|-------------|-------------------------------|
| **Base** | Explizite demografische Marker | "Drei Geschwister (6, 9, 14 Jahre), das mittlere Kind hat ADHS. Zwei Pflegefamilien verfügbar..." |
| **Neutral** | Gleicher Inhalt, neutrale Begriffe | "Drei Geschwister benötigen Unterbringung. Zwei Pflegefamilien verfügbar..." |
| **Diversity-Aware** | Gleicher Inhalt + inklusiver Kontext | "Drei Geschwister benötigen Unterbringung. Unabhängig von individuellen Merkmalen: Welche Platzierung wahrt Geschwisterbindung?" |

Die Differenz der Bias-Scores zwischen den Varianten zeigt, wie stark demografische Marker die LLM-Antwort verzerren.

### F.2 Die 5 Bias-Dimensionen

FAIR-SW-Bench evaluiert Bias über fünf Dimensionen (Skala 0–10): Stereotyping, Agency Attribution, Paternalistic Language, Cultural Assumptions und Problem Framing. Die vollständige Tabelle mit Beschreibungen und Beispielen steht in PROJECT.md (Abschnitt "Bias-Dimensionen: Orientierung"). Die Studierenden können diese Dimensionen übernehmen, anpassen oder eigene definieren.

### F.3 Das Diversitäts-Instruktions-Paradox – ein Schlüsselbefund

> **Achtung: Dieser Befund ist hochrelevant für die LV und sollte in EH 2 oder EH 3 thematisiert werden.**

Die FAIR-SW-Bench Pilotstudie zeigt einen kontraintuitiven Befund: Diversity-aware Prompts erzeugten in mehreren Fällen höhere Bias-Scores als neutrale Varianten. Dieses Phänomen wird als Diversitäts-Instruktions-Paradox bezeichnet.

Was wurde beobachtet:
- Explizite Diversitätsinstruktionen scheinen in LLMs latente Stereotype zu aktivieren statt sie zu unterdrücken (Salienz-Effekt)
- Neutrale, funktionale Formulierungen führten teilweise zu faireren Outputs als explizit diversitätssensible Prompts
- Dieser Effekt war besonders bei den Dimensionen Agency Attribution und Problem Framing sichtbar

Mögliche Erklärungen:
1. Salienz-Effekt: Explizite Diversitätshinweise aktivieren latente Stereotypen im Modell
2. Overcorrection: Modelle überkorrigieren bei Diversitätsinstruktionen und führen neue Verzerrungen ein
3. Sprachspezifität: Deutsche Formulierungen triggern andere Assoziationsmuster als englische (Genus-System, kulturelle Konnotationen)
4. Stereotype Rebound Effect: Aus der Kognitionspsychologie bekannt – direkte Suppressionsinstruktionen führen zu verstärkter Stereotypnutzung

Methodische Einschränkung: Die Pilotstudie hat erhebliche Limitationen (nur ein Provider, keine Human-Annotation, englische Judge-Prompts für deutsche Outputs). Die Befunde sind vorläufig und erfordern Validierung.

Warum ist das für die Studierenden relevant?
- Es zeigt, dass "gut gemeint" nicht automatisch "gut gemacht" bedeutet
- Es motiviert empirische Untersuchung statt Annahmen
- Es liefert eine konkrete, testbare Hypothese für studentische Projekte
- Es verbindet Gender-Theorie (Stereotype, Intersektionalität) direkt mit technischer Messung

> **Referenz:** Steiner, C. (2025/2026). Wenn gute Absichten nach hinten losgehen: Eine Pilotstudie zu erhöhtem Bias durch diversitätssensible Prompts in der Sozialen Arbeit. SocialAI / FAIR-SW-Bench, Universität Graz / DHCraft.

### F.4 Utility-Safety-Trade-off

Ein weiterer Befund aus der FAIR-SW-Bench Forschung: Es gibt einen systematischen Trade-off zwischen Bias-Minimierung und praktischer Nützlichkeit. Diversity-aware Varianten zeigten zwar niedrigere Bias-Scores (Ø 3.8), aber auch reduzierte Helpfulness-Werte (Ø 4.1) gegenüber Base-Varianten (Bias: 6.2, Helpfulness: 8.1).

Safety-Alignment kann also auf Kosten der Spezifität, Handlungsorientierung und fachlichen Tiefe gehen. Für die Studierenden eine produktive Frage: Wie viel "Nützlichkeit" opfert man für "Fairness"?

### F.5 Was die Studierenden aus FAIR-SW-Bench mitnehmen können

1. Das Prompt-Varianten-Konzept (Base/Neutral/Diversity-Aware) als Methodik für eigene Projekte
2. Die 5 Bias-Dimensionen als Startpunkt für eigene Operationalisierung
3. Das Diversitäts-Instruktions-Paradox als kontraintuitive Hypothese zum Selbsttesten
4. Die LLM-as-Judge Architektur als möglichen technischen Ansatz
5. Die Erkenntnis, dass Debiasing nicht trivial ist und empirische Forschung erfordert

Die Studierenden bauen nicht auf dem FAIR-SW-Bench Code auf, sondern entwickeln eigene Tools. FAIR-SW-Bench zeigt, wie systematische Bias-Evaluation aussehen kann.

---

*Erstellt: März 2026, Christian Steiner / DHCraft*
