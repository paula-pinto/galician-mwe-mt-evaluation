# Galician MWE MT Evaluation

This repository contains the code used to compute automatic sentence-level evaluation metrics for the translation of Galician verb-object multiword expressions (MWEs).

The evaluation uses three metrics:

- BLEU
- chrF
- TER

The code was used in the context of my Master's thesis on Galician-English machine translation of verb-object MWEs.

## Repository contents

- `code_evaluationmetrics_mwe.ipynb`: Google Colab notebook used to compute BLEU, chrF and TER.
- `requirements.txt`: Python packages required to run the notebook.

## Data

The full dataset is not included in this repository because it is part of an ongoing research project. The notebook expects an Excel file with two sheets:

- `EN-GL`
- `GL-EN`

The expected columns include:

- `manual_sent_2`
- `trans_man2_EN (TESTE)`
- `googletranslate_output`
- `salamandrata_output`
- `nosmt_output`

## Metrics

The automatic metrics are computed with `sacrebleu`. BLEU and chrF are better when higher, while TER is better when lower.
