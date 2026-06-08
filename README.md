# Diritto alla cultura e disabilità cognitiva
## L'IA generativa può supportare la comunicazione in ambito culturale?
 
> Dataset and results repository for the paper submitted to [AItLA 2025 - XXV Congresso Internazionale dell'Associazione Italiana di Linguistica Applicata "La semplificazione linguistica 
per la comunicazione: tecnologie in contesto" - Università di Macerata (Italy), 19-21 febbraio 2025.

## Overview

This repository contains the dataset and evaluation results from a study investigating whether large language models (LLMs) can support accessible communication in cultural heritage contexts. 
Specifically, the study tests whether Claude Sonnet 3.5 and ChatGPT-4 can simplify technical catalogue descriptions for people with cognitive disabilities, using zero-shot prompting in Italian.
The study combines quantitative linguistic measures (readability, syntactic complexity, lexical variety) with a qualitative manual annotation by two expert linguists, achieving an overall inter-annotator agreement of 96.56% (Cohen's κ = 0.91).
 
## Corpus
 
The corpus consists of **200 technical descriptions in Italian** (~7,741 words total), drawn from open-access catalogue records (*schede di catalogo*) of the **Catalogo Generale dei Beni Culturali** of the Italian Ministry of Culture (MiC), covering various categories of cultural heritage objects.
 
Each description is representative of a formal, specialised register characterised by:
- complex subordinate and implicit syntactic constructions (participles, gerunds)
- domain-specific technical vocabulary (e.g., *a mezzo busto*, *croce astile*)
- figurative language and dense information packaging
---
## Methodology
 
### Models tested
| Model | Developer |
|---|---|
| Claude Sonnet 3.5 | Anthropic |
| ChatGPT-4 | OpenAI |
 
### Prompts
Three zero-shot prompts were used, designed with increasing specificity:
 
| ID | Description |
|---|---|
| **P1** | Specifies only the target audience (people with cognitive disabilities) |
| **P2** | Adds the intended use context (informational panel in a museum) |
| **P3** | Further specifies the domain (cultural heritage) and adds a completeness constraint (*mantenendo tutte le informazioni*) |
 
Total outputs: **1,200 outputs** (600 per model × 3 prompts × 200 texts).
 
### Quantitative metrics
- **Gulpease Index** – Italian readability score
- **Sentence count and average sentence length**
- **Active voice verbs** – proxy for syntactic simplicity
- **Type/Token Ratio (TTR)** – lexical variety
- **NVdB coverage** – proportion of words from De Mauro's *Nuovo Vocabolario di Base*

### Qualitative annotation criteria
Two linguists independently annotated outputs on 8 binary criteria:
 
| Code | Criterion |
|---|---|
| TT | Use of technical terms |
| SEM | Presence of simplifications |
| SOE | Explicit subject present |
| FNO | Nominal sentences |
| FSE | Simple sentences |
| SIG | Acronyms or abbreviations |
| EFI | Figurative expressions |
| PAR | Use of paraphrase |
 
Inter-annotator agreement was computed on a balanced 10% pilot sample (120 responses) before full annotation.
 ---
 
## Inter-Annotator Agreement (IAA)
 
| Criterion | Agreement/Total | % Agreement | Cohen's κ |
|---|---|---|---|
| TT | 102/120 | 85.00% | 0.70 |
| SEM | 46/46 | 100.00% | 1.00 |
| SOE | 112/120 | 93.33% | 0.87 |
| FNO | 116/120 | 97.50% | 0.95 |
| FSE | 117/120 | 96.67% | 0.76 |
| SIG | 120/120 | 100.00% | 1.00 |
| EFI | 120/120 | 100.00% | 1.00 |
| PAR | 8/8 | 100.00% | 1.00 |
| **Total** | **741/774** | **96.56%** | **0.91** |
 
---
 
## Data Format
 
All CSV files use **UTF-8 encoding**, semicolon (`;`) as delimiter, and include a header row. Annotation values are binary (`y` = present, `n` = absent).
 
Example columns in annotated files:
```
text_id; model; prompt; criterion_TT; criterion_SEM; criterion_SOE; ...
```
 
---
 
## License
 
The dataset and annotation files in this repository are released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.
 
You are free to share and adapt the material for any purpose, provided appropriate credit is given, a link to the license is provided, and any changes are indicated.
 
📄 [CC BY 4.0 full license text](https://creativecommons.org/licenses/by/4.0/)
 
> The source catalogue records are drawn from the **Catalogo Generale dei Beni Culturali (MiC)**, available in open access. Please refer to the original source for their specific terms of use.
 
---
 
## Citation
 
If you use this dataset or results in your research, please cite:
