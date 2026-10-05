<!-- ELUCENIA technical documentation · mascc · de · no clinical/professional/rights approval -->

# MASCC-Index

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/mascc)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Krankheitslast (Symptome der Fieberepisode)

`carga`

- `0` — Schwer oder moribund
- `3` — Mäßig
- `5` — Keine oder leicht

### Hypotonie (systolischer Blutdruck \< 90 mmHg)

`hipotensao`

- `0` — Ja
- `5` — Nein

### Aktive COPD

`dpoc`

- `0` — Ja
- `4` — Nein

### Krebsart

`tumor`

- `0` — Hämatologische Neoplasie mit früherer Pilzinfektion
- `4` — Solider Tumor oder hämatologische Neoplasie ohne frühere Pilzinfektion

### Dehydratation mit Bedarf an intravenöser Flüssigkeit

`desidratacao`

- `0` — Ja
- `3` — Nein

### Ort des Fieberbeginns

`local`

- `0` — Während des Krankenhausaufenthalts
- `3` — Ambulant

### Alter

`idade`

- `0` — ≥ 60 Jahre
- `2` — \< 60 Jahre

## Fassung der Methode

MASCC/Klastersky 2000: 7 Bereiche, gesamt 0–26, Grenze ≥21; ASCO/IDSA 2018-Kontext

## Dokumentierte Formel

Krankheitsbelastung: keine/leicht 5, mäßig 3, schwer 0 · keine Hypotonie 5 · keine COPD 4 · solider Tumor 4 oder hämatologische Malignität ohne frühere Pilzinfektion 4 · keine Dehydratation 3 · ambulant 3 · Alter \<60 Jahre 2. Maximum: 26.

## Grenzen und Population

MASCC ≥21 zeigt ein geringeres Komplikationsrisiko an, berechtigt aber allein weder zur Entlassung noch zu oralen Antibiotika oder ambulanter Behandlung. Im Kontext von ASCO/IDSA 2018 hängt die Auswahl von klinischer Beurteilung, Stabilität, Begleiterkrankungen, der Möglichkeit zu Nachkontrollen, einer Betreuungsperson zu Hause sowie verfügbarem Telefon und Transport ab. Für ambulante Behandlung vorgesehene Personen müssen vor der Entlassung mindestens 4 Stunden beobachtet werden und benötigen Nachsorge. Das Hypotoniekriterium dieser Implementierung folgt der ursprünglichen Variablen von 2000: systolischer Blutdruck \<90 mmHg.

## Referenzen

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
