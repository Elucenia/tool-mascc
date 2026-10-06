<!-- ELUCENIA technical documentation · mascc · it · no clinical/professional/rights approval -->

# Indice MASCC

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/mascc)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Carico della malattia (sintomi dell’episodio febbrile)

`carga`

- `0` — Gravi o moribondo
- `3` — Moderati
- `5` — Nessuno o lievi

### Ipotensione (pressione arteriosa sistolica \< 90 mmHg)

`hipotensao`

- `0` — Sì
- `5` — No

### BPCO attiva

`dpoc`

- `0` — Sì
- `4` — No

### Tipo di cancro

`tumor`

- `0` — Neoplasia ematologica con pregressa infezione fungina
- `4` — Tumore solido o neoplasia ematologica senza pregressa infezione fungina

### Disidratazione che richiede idratazione endovenosa

`desidratacao`

- `0` — Sì
- `3` — No

### Dove è iniziata la febbre

`local`

- `0` — Durante il ricovero
- `3` — Ambulatoriale

### Età

`idade`

- `0` — ≥ 60 anni
- `2` — \< 60 anni

## Edizione del metodo

MASCC/Klastersky 2000: 7 domini, totale 0–26, soglia ≥21; contesto ASCO/IDSA 2018

## Formula documentata

Carico di malattia: nullo/lieve 5, moderato 3, grave 0 · senza ipotensione 5 · senza BPCO 4 · tumore solido 4, oppure neoplasia ematologica senza infezione fungina pregressa 4 · senza disidratazione 3 · ambulatoriale 3 · età \<60 anni 2. Massimo: 26.

## Limiti e popolazione

MASCC ≥21 indica un rischio inferiore di complicanze, ma non autorizza da solo dimissione, antibiotici orali o gestione ambulatoriale. Nel contesto ASCO/IDSA 2018, la selezione dipende da valutazione clinica, stabilità, comorbilità, possibilità di rispettare le visite di controllo, un caregiver a casa e disponibilità di telefono e trasporto. I candidati alla gestione ambulatoriale devono essere osservati per almeno 4 ore prima della dimissione e richiedono follow-up. Il criterio di ipotensione di questa implementazione segue la variabile originale del 2000: pressione arteriosa sistolica \<90 mmHg.

## Riferimenti

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Basso rischio (≥ 21 punti)

Candidato per antibiotico orale e gestione ambulatoriale, se soddisfa anche i criteri clinici e sociali.


### 2

Basso rischio (≥ 21 punti)

Candidato per antibiotico orale e gestione ambulatoriale, se soddisfa anche i criteri clinici e sociali.


### 3

Non è a basso rischio (< 21 punti)

Ricoverare e iniziare un antibiotico endovenoso ad ampio spettro.

