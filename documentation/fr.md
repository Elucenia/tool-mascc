<!-- ELUCENIA technical documentation · mascc · fr · no clinical/professional/rights approval -->

# Indice MASCC

[conditions, sources et autorisations](https://elucenia.org/fr/outils/mascc)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Retentissement de la maladie (symptômes de l’épisode fébrile)

`carga`

- `0` — Graves ou moribond
- `3` — Modérés
- `5` — Aucun ou légers

### Hypotension (pression artérielle systolique \< 90 mmHg)

`hipotensao`

- `0` — Oui
- `5` — Non

### BPCO active

`dpoc`

- `0` — Oui
- `4` — Non

### Type de cancer

`tumor`

- `0` — Cancer hématologique avec infection fongique antérieure
- `4` — Tumeur solide ou cancer hématologique sans infection fongique antérieure

### Déshydratation nécessitant une hydratation intraveineuse

`desidratacao`

- `0` — Oui
- `3` — Non

### Lieu de début de la fièvre

`local`

- `0` — Pendant l’hospitalisation
- `3` — Ambulatoire

### Âge

`idade`

- `0` — ≥ 60 ans
- `2` — \< 60 ans

## Édition de la méthode

MASCC/Klastersky 2000 : 7 domaines, total 0–26, seuil ≥21 ; contexte ASCO/IDSA 2018

## Formule documentée

Charge de maladie : aucune/légère 5, modérée 3, sévère 0 · sans hypotension 5 · sans BPCO 4 · tumeur solide 4, ou hémopathie maligne sans antécédent d’infection fongique 4 · sans déshydratation 3 · ambulatoire 3 · âge \<60 ans 2. Maximum : 26.

## Limites et population

MASCC ≥21 indique un risque moindre de complications, mais n’autorise pas à lui seul la sortie, les antibiotiques oraux ou la prise en charge ambulatoire. Dans le contexte ASCO/IDSA 2018, la sélection dépend de l’évaluation clinique, de la stabilité, des comorbidités, de la capacité à se présenter aux consultations de suivi, de la présence d’un aidant à domicile et de l’accès au téléphone et au transport. Les candidats à la prise en charge ambulatoire doivent être observés pendant au moins 4 heures avant la sortie et nécessitent un suivi. Le critère d’hypotension de cette implémentation suit la variable originale de 2000 : PAS \<90 mmHg.

## Références

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
