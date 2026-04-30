# Domain-Specific Tokenization for Biomedical NLP

This repository contains an individual NLP case study on domain-specific tokenization for biomedical text. The goal is to develop and evaluate a biomedical tokenizer, analyze domain-specific segmentation behavior, and measure its impact on downstream tasks.

Anna Belyakova  
a.belyakova@innopolis.university  
Innopolis University, Natural Language Processing course  


---

## Project objective

Biomedical text contains long compounds, abbreviations, and rare terminology that can be heavily fragmented by generic tokenizers.  
Excessive fragmentation increases sequence length and may weaken model robustness, especially for entity-rich inputs.

This project investigates whether training tokenizers directly on biomedical-domain text improves:

- compactness of tokenization,
- downstream classification quality,
- entity-level segmentation behavior.

## Background

The case study topic is **Domain-specific Tokenization**.  
Biomedical language is a suitable setting because it contains specialized terminology, long compounds, abbreviations, and rare words that are often poorly segmented by generic tokenizers.

From a practical perspective, tokenization quality can affect:

- sequence length and computational cost,
- representation quality for rare biomedical terms,
- stability of downstream tasks such as classification and entity-aware processing.

## Research question

> Does domain-trained BPE provide a better tokenization trade-off than standard tokenizers for biomedical NLP?

---

## Experimental design

### Compared tokenizers

- **Custom:** biomedical BPE (`30k`, `50k`) trained on PubMedQA text.
- **Baselines:** BERT-base, BioBERT, GPT-2 tokenizers.

### Datasets and their role

- **PubMedQA**
  - tokenizer training corpus,
  - downstream classification task (`yes/no/maybe`).
- **JNLPBA**
  - entity-focused diagnostics of tokenization quality.

### Comparison setup

Only the tokenizer changes between runs.  
The preprocessing, splits, training pipeline, and evaluation logic are kept fixed to isolate tokenizer effects.

---

## Evaluation framework

The project evaluates tokenizers from three complementary perspectives:

1. **Intrinsic tokenization behavior**
   - fertility,
   - average tokens per sample,
   - average token length.
2. **Task-level downstream quality**
   - accuracy,
   - macro-F1 on PubMedQA.
3. **Entity-oriented diagnostics**
   - fragmentation rate,
   - single-piece entity rate,
   - subtoken-per-entity ratio.

This combination helps measure not only predictive quality, but also *how* tokenization affects biomedical text structure.

## Experimental results

At a high level, the experiments are organized to answer three questions:

1. Do custom biomedical tokenizers produce more compact segmentation than baselines?
2. Does this tokenization choice improve downstream PubMedQA performance (accuracy and macro-F1)?
3. Is entity tokenization on JNLPBA less fragmented under domain-trained tokenizers?

The final comparison is reported with intrinsic metrics, classification scores, and entity-oriented diagnostics under the same pipeline.

---

## Repository map

| Path | Purpose |
|---|---|
| `notebooks/` | End-to-end experimental pipeline (`01` to `06`) |
| `tokenizers/` | Trained tokenizer artifacts |
| `poster/` | Scientific poster source (`main.tex`) and compiled PDF |

### Notebook workflow

Run notebooks in order to fully reproduce the study:

1. `notebooks/01_data_exploration.ipynb` - dataset profiling and signal inspection
2. `notebooks/02_baseline_tokenization.ipynb` - baseline tokenizer analysis
3. `notebooks/03_custom_tokenizer.ipynb` - biomedical BPE training
4. `notebooks/04_tokenization_analysis.ipynb` - intrinsic metric comparison
5. `notebooks/05_experiments.ipynb` - downstream classification experiments
6. `notebooks/06_ner_tokenization_evaluation.ipynb` - entity-level diagnostics on JNLPBA

## Presentation assets

For case study presentation and grading:

- **Poster:** `poster/main.pdf`
- **Poster source:** `poster/main.tex`
- **Experiment code:** notebooks in `notebooks/`

---

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install -r requirements.txt
```

After setup, execute the notebooks sequentially as described above.

---

## Reproducibility notes

- fixed random seeds across stages,
- consistent split protocol for tokenizer comparison,
- unified training and evaluation pipeline for all tokenizers.

## Conclusions

This project provides a structured experimental protocol for evaluating domain-specific tokenization in biomedical NLP.  
Conclusions are derived from three evidence layers (intrinsic, downstream, entity-oriented), making it possible to justify whether tokenizer adaptation is beneficial for the selected domain and tasks.

## Project scope and boundaries

- Focused on biomedical-domain text (PubMed-style distribution).
- Uses a lightweight downstream classifier setup.
- NER metrics are used as tokenization diagnostics, not as a replacement for full NER model training.