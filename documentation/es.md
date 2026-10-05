<!-- ELUCENIA technical documentation · mascc · es · no clinical/professional/rights approval -->

# Índice MASCC

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/mascc)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Carga de la enfermedad (síntomas del episodio febril)

`carga`

- `0` — Graves o moribundo
- `3` — Moderados
- `5` — Ninguno o leves

### Hipotensión (presión arterial sistólica \< 90 mmHg)

`hipotensao`

- `0` — Sí
- `5` — No

### EPOC activa

`dpoc`

- `0` — Sí
- `4` — No

### Tipo de cáncer

`tumor`

- `0` — Neoplasia hematológica con infección fúngica previa
- `4` — Tumor sólido o neoplasia hematológica sin infección fúngica previa

### Deshidratación que requiere hidratación intravenosa

`desidratacao`

- `0` — Sí
- `3` — No

### Dónde comenzó la fiebre

`local`

- `0` — Durante la hospitalización
- `3` — Ambulatorio

### Edad

`idade`

- `0` — ≥ 60 años
- `2` — \< 60 años

## Edición del método

MASCC/Klastersky 2000: 7 dominios, total 0–26, corte ≥21; contexto ASCO/IDSA 2018

## Fórmula documentada

Carga de enfermedad: ninguna/leve 5, moderada 3, grave 0 · sin hipotensión 5 · sin EPOC 4 · tumor sólido 4, o tumor hematológico sin infección fúngica previa 4 · sin deshidratación 3 · ambulatorio 3 · edad \<60 años 2. Máximo: 26.

## Límites y población

MASCC ≥21 indica menor riesgo de complicaciones, pero no autoriza por sí solo el alta, antibióticos orales o manejo ambulatorio. En el contexto ASCO/IDSA 2018, la selección depende de evaluación clínica, estabilidad, comorbilidades, capacidad para acudir a las visitas de seguimiento, cuidador en casa y disponibilidad de teléfono y transporte. Los candidatos al manejo ambulatorio deben observarse durante al menos 4 horas antes del alta y requieren seguimiento. El criterio de hipotensión de esta implementación sigue la variable original de 2000: PAS \<90 mmHg.

## Referencias

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
