# Analyse-Fachkonzept1026

## Story-Schnitt für das Fachkonzept „Herbsttarif K-Gewerbe 10/26“ (3‑Wochen-Sprints)

### Sprint 1 – Fachliche Grundlagen und Tariflogik

**Story 1: Tarifregeln strukturieren**
- Als Produktverantwortliche:r möchte ich die Regeln des Herbsttarifs K‑Gewerbe 10/26 in eindeutige Akzeptanzkriterien überführen, damit Entwicklung und Test ein gemeinsames Verständnis haben.
- **Akzeptanzkriterien (Beispiel):**
  - Tarifgültigkeit (Zeitraum, Zielgruppe, Produktkontext) ist vollständig beschrieben.
  - Ausschlüsse und Vorrangregeln sind fachlich geklärt.

**Story 2: Prämien-/Beitragsberechnung fachlich konkretisieren**
- Als Sachbearbeitung möchte ich eine nachvollziehbare Berechnungslogik für den Herbsttarif, damit Angebote reproduzierbar erstellt werden können.
- **Akzeptanzkriterien (Beispiel):**
  - Eingabeparameter (z. B. Gewerbeart, Risikomerkmale, Laufzeit) sind definiert.
  - Berechnungsergebnis ist für dieselben Eingaben deterministisch.

### Sprint 2 – Antrags- und Prozessintegration

**Story 3: Antragsstrecke mit Tarif verknüpfen**
- Als Vertrieb möchte ich, dass der Herbsttarif in der Antragsstrecke auswählbar und korrekt vorbelegt ist, damit Anträge effizient erfasst werden.
- **Akzeptanzkriterien (Beispiel):**
  - Tarif ist nur in erlaubten Fällen auswählbar.
  - Pflichtfelder und Validierungen greifen passend zum Tarifkontext.

**Story 4: Fachliche Prüfungen und Ablehnungsgründe**
- Als Underwriting möchte ich klare Prüfregeln mit verständlichen Rückmeldungen, damit fehlerhafte oder nicht zulässige Anträge sauber abgefangen werden.
- **Akzeptanzkriterien (Beispiel):**
  - Fachliche Regelverletzungen führen zu eindeutigen Hinweisen.
  - Zulässige Anträge passieren den Prozess ohne unnötige Blocker.

### Sprint 3 – Abschluss, Transparenz und Qualitätssicherung

**Story 5: Dokumentausgabe und Nachvollziehbarkeit**
- Als Kunde/Vertrieb möchte ich, dass Angebot/Police die relevanten Tarifmerkmale korrekt ausweisen, damit Entscheidungen transparent sind.
- **Akzeptanzkriterien (Beispiel):**
  - Tarifname/-version und zentrale Konditionen erscheinen korrekt in der Ausgabe.
  - Berechnungsrelevante Werte sind konsistent zur Tariflogik.

**Story 6: Reporting und Betriebsstabilität**
- Als Fachbereich möchte ich Auswertungen zur Nutzung und Qualität des Herbsttarifs, damit Steuerung und Optimierung möglich sind.
- **Akzeptanzkriterien (Beispiel):**
  - Wesentliche Kennzahlen (Nutzung, Ablehnungsquote, Auffälligkeiten) sind auswertbar.
  - Fachlich kritische Prozessfehler sind monitorbar.

## Erste Vorschläge zur Testfallerstellung

### 1) Fachliche Positiv-/Negativfälle pro Story
- **Positivfälle:** Zulässige Kombinationen führen zu korrekter Prämie und erfolgreichem Prozess.
- **Negativfälle:** Unzulässige Kombinationen liefern korrekte Sperren/Ablehnungsgründe.

### 2) Grenzwert- und Variantenmatrix
- Grenzwerte (z. B. Datumsgrenzen, Schwellenwerte, Klassengrenzen) explizit testen.
- Paarweise Varianten (z. B. Kombinationen aus Gewerbeart, Risikoausprägung und Laufzeit) priorisieren.

### 3) End-to-End-Regression
- Kernprozess vom Antrag bis zur Ausgabe (Angebot/Police) als E2E-Szenario absichern.
- Bestehende Referenzprodukte gegen Seiteneffekte regressiv prüfen.

## Bevorzugtes Vorgehen zur Abarbeitung der Tests

Bevorzugt wird ein **risikobasiertes, story-nahes Testvorgehen im Sprint**:
1. **Akzeptanzkriterien zuerst** in konkrete Given-When-Then-Testfälle überführen.
2. **Früh testen pro Story** (fachliche Unit-/Service-Tests), danach Integrations- und E2E-Tests.
3. **Risikofokus** auf Berechnungslogik, Ausschlussregeln und Grenzwerte legen.
4. **Regression je Sprintabschluss** auf kritischen Kernpfaden durchführen.
5. **Defect Triage fachnah** (Fachbereich + Entwicklung + Test), um schnell nachzuschärfen.
