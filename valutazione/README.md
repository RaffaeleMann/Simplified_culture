# Valutazione — Metriche quantitative e annotazione qualitativa
 
Questa cartella contiene i risultati della valutazione degli output prodotti dai due modelli (**Claude Sonnet 3.5** e **ChatGPT-4**) per le tre consegne (**P1**, **P2**, **P3**). La valutazione è articolata in due dimensioni complementari: quantitativa e qualitativa.
 
---
 
 ## Metriche quantitative
 
Le metriche quantitative sono calcolate con metodi computazionali e consentono di misurare in modo oggettivo e riproducibile le prestazioni dei modelli in termini di leggibilità, complessità sintattica e varietà lessicale.
 
- **Indice di Gulpease** — indice di leggibilità sviluppato specificamente per l'italiano, basato sulla lunghezza delle parole e delle frasi. I valori vanno da 0 (testo molto difficile) a 100 (testo molto facile). Testi con indice inferiore a 40 risultano difficili per chi ha licenza elementare; superiore a 80 risultano facili anche per chi ha licenza elementare.
- **Numero di frasi e lunghezza media delle frasi** — indicatori della complessità sintattica complessiva del testo: frasi più brevi e numerose tendono a corrispondere a una struttura più semplice e accessibile.
- **Verbi con diatesi attiva** — la presenza di costruzioni attive, rispetto a quelle passive o impersonali, è considerata un indicatore di maggiore semplicità sintattica e di maggiore chiarezza nell'identificazione dell'agente dell'azione.
- **Type/Token Ratio (TTR)** — rapporto tra il numero di forme distinte (*types*) e il numero totale di occorrenze (*tokens*) nel testo. Un valore più alto indica maggiore varietà lessicale; un valore più basso indica maggiore ripetitività, che può favorire la comprensione in testi accessibili.
- **Copertura NVdB** — proporzione di parole del testo presenti nel *Nuovo Vocabolario di Base* della lingua italiana di Tullio De Mauro, che raccoglie le circa 7.000 parole più comuni e conosciute dai parlanti adulti. Una copertura più alta indica un lessico più accessibile.
---


## Annotazione qualitativa
 
La valutazione qualitativa è stata condotta manualmente da due linguisti esperti in modo indipendente. Per ciascun output è stato espresso un giudizio binario (`y` = presente / `n` = assente, `na` = non applicabile) sulla base dei seguenti criteri, selezionati a partire dalla letteratura scientifica di riferimento e da linee guida istituzionali per la comunicazione accessibile.
 
| Acronimo | Criterio | Descrizione |
|---|---|---|
| **TT** | Uso di termini tecnici | Presenza di lessico specialistico non appartenente al vocabolario di base |
| **SEM** | Presenza di semplificazioni | Il testo presenta interventi espliciti di semplificazione rispetto all'originale |
| **SOE** | Soggetto esplicito presente | Il soggetto della frase è espresso esplicitamente e non sottinteso |
| **FNO** | Frasi nominali | Presenza di frasi prive di verbo principale (costruzioni nominali) |
| **FSE** | Frasi semplici | Prevalenza di frasi brevi, coordinate o senza subordinate implicite |
| **SIG** | Sigle o abbreviazioni | Presenza di sigle, acronimi o abbreviazioni non esplicitate |
| **EFI** | Espressioni figurate | Presenza di metafore, metonimie o altre figure retoriche di difficile interpretazione |
| **PAR** | Uso di parafrasi | Il modello riformula esplicitamente un termine o un concetto tecnico con parole più semplici |

  
### Accordo tra annotatori (IAA)
 
Prima di procedere all'annotazione completa dei 1.200 output, è stata effettuata un'annotazione di prova su un campione pilota bilanciato pari al **10% del totale (120 risposte)**, selezionate in modo equilibrato tra modelli e consegne. 

Il livello di accordo è misurato tramite la **percentuale di accordo** e la **kappa di Cohen (κ)**.
 
| Criterio | Accordo/Totale | % di accordo | κ di Cohen |
|---|---|---|---|
| TT | 102/120 | 85,00% | 0,70 |
| SEM | 46/46 | 100,00% | 1,00 |
| SOE | 112/120 | 93,33% | 0,87 |
| FNO | 116/120 | 97,50% | 0,95 |
| FSE | 117/120 | 96,67% | 0,76 |
| SIG | 120/120 | 100,00% | 1,00 |
| EFI | 120/120 | 100,00% | 1,00 |
| PAR | 8/8 | 100,00% | 1,00 |
| **Totale** | **741/774** | **96,56%** | **0,91** |
 
---
 
