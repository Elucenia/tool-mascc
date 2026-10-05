<!-- ELUCENIA technical documentation · mascc · pt-BR · no clinical/professional/rights approval -->

# Índice MASCC

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/mascc)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Carga da doença (sintomas do episódio febril)

`carga`

- `0` — Graves ou moribundo
- `3` — Moderados
- `5` — Nenhum ou leves

### Hipotensão (PAS \< 90 mmHg)

`hipotensao`

- `0` — Sim
- `5` — Não

### DPOC ativa

`dpoc`

- `0` — Sim
- `4` — Não

### Tipo de câncer

`tumor`

- `0` — Hematológico com infecção fúngica prévia
- `4` — Tumor sólido, ou hematológico sem infecção fúngica prévia

### Desidratação que exige hidratação venosa

`desidratacao`

- `0` — Sim
- `3` — Não

### Onde começou a febre

`local`

- `0` — Durante internação
- `3` — Ambulatorial

### Idade

`idade`

- `0` — ≥ 60 anos
- `2` — \< 60 anos

## Edição do método

MASCC/Klastersky 2000:7 domínios, total 0–26, corte≥21; contexto ASCOIDSA 2018

## Fórmula documentada

Carga da doença: nenhum/leve 5, moderado 3, grave 0 · sem hipotensão 5 · sem DPOC 4 · tumor sólido 4, ou tumor hematológico sem infecção fúngica prévia 4 · sem desidratação 3 · paciente ambulatorial 3 · idade \< 60 anos 2. Máximo: 26.

## Limites e população

MASCC ≥21 indica menor risco de complicações, mas não autoriza sozinho alta, antibiótico oral ou manejo ambulatorial. No contexto ASCO/IDSA 2018, a seleção depende de avaliação clínica, estabilidade, comorbidades, capacidade de cumprir retornos, cuidador em casa, telefone e transporte disponíveis. Candidatos ao manejo ambulatorial devem ser observados por pelo menos 4 horas antes da alta e requerem seguimento. O critério de hipotensão desta implementação segue a variável original de 2000: PAS \<90 mmHg.

## Referências

- [Klastersky J et al. The Multinational Association for Supportive Care in Cancer risk index: a multinational scoring system for identifying low-risk febrile neutropenic cancer patients. J Clin Oncol, 2000.](https://doi.org/10.1200/JCO.2000.18.16.3038)

- [Taplitz RA et al. Outpatient management of fever and neutropenia in adults treated for malignancy: American Society of Clinical Oncology and Infectious Diseases Society of America clinical practice guideline update. J Clin Oncol, 2018.](https://doi.org/10.1200/JCO.2017.77.6211)

- [ASCO/IDSA2018;DOI10.1200/JCO.2017.77.6211](https://www.idsociety.org/globalassets/idsa/practice-guidelines/outpatient-management-of-fever-and-neutropenia.pdf)

- [Original Klastersky2000;DOI10.1200/JCO.2000.18.16.3038](https://theempulse.org/wp-content/uploads/2016/04/The-Multinational-Association-for-Supportive-care-in-cancer-risk-index.pdf)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
