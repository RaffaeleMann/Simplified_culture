# Diritto alla cultura e disabilità cognitiva
## L'IA generativa può supportare la comunicazione in ambito culturale?
 
> Repository del dataset e dei risultati del contributo presentato ad AItLA 2025 - XXV Congresso Internazionale dell'Associazione Italiana di Linguistica Applicata *"La semplificazione linguistica per la comunicazione: tecnologie in contesto"* - Università di Macerata (Italia), 19-21 febbraio 2025.
 
---
 
## Panoramica
 
Questo repository contiene il dataset e i risultati della valutazione di uno studio che indaga se i modelli del linguaggio di grandi dimensioni (LLM) possano supportare la comunicazione accessibile in ambito culturale.
Lo studio testa in particolare la capacità di **Claude Sonnet 3.5** e **ChatGPT-4** di semplificare descrizioni tecniche di catalogo per persone con disabilità cognitive, mediante zero-shot prompting in lingua italiana.
Lo studio combina misure linguistiche **quantitative** (leggibilità, complessità sintattica, varietà lessicale) con un'**annotazione manuale qualitativa** condotta da due linguisti esperti, raggiungendo un accordo complessivo tra annotatori del 96,56% (κ di Cohen = 0,91).
 
---
 
## Corpus
 
Il corpus è composto da **200 descrizioni tecniche in lingua italiana** (circa 7.741 parole in totale), tratte dalle schede di catalogo in formato aperto del **Catalogo Generale dei Beni Culturali** del Ministero della Cultura (MiC), relative a diverse tipologie di beni culturali.
 
Ciascuna descrizione è rappresentativa di un registro formale e specialistico caratterizzato da:
- costruzioni sintattiche subordinate e implicite complesse (participi, gerundi)
- lessico tecnico di dominio (es. *a mezzo busto*, *croce astile*)
- linguaggio figurato e alta densità informativa
---
 
## Metodologia
 
### Modelli testati in data 
| Modello | Sviluppatore |
|---|---|
| Claude Sonnet 3.5 | Anthropic |
| ChatGPT-4 | OpenAI |
 
### Prompt
Sono state utilizzate tre prompt zero-shot, progettate con un livello di specificità crescente:
 
| Prompt | Descrizione |
|---|---|
| **P1** | Semplifica per persone con disabilità cognitive queste descrizioni tecniche |
| **P2** | Per ogni descrizione tecnica, dammi in output una descrizione semplificata per persone con disabilità cognitive da inserire in un pannello informativo in un museo |
| **P3** | Per ogni descrizione tecnica del dominio dei beni culturali, dammi in output una descrizione semplificata per persone con disabilità cognitive da inserire in un pannello informativo in un museo mantenendo tutte le informazioni |
 
Output totali: **1.200 risposte** (600 per modello × 3 consegne × 200 testi).

 
## Accordo tra annotatori (IAA)
 
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

 
## Formato dei dati
 
Tutti i file CSV utilizzano la codifica **UTF-8**, il punto e virgola (`;`) come delimitatore e includono una riga di intestazione. I valori di annotazione sono binari (`y` = presente, `n` = assente).
 
Esempio di colonne nei file annotati:
```
text_id; modello; consegna; criterio_TT; criterio_SEM; criterio_SOE; ...
```
 
---
 
## Licenza
 
Il dataset e i file di annotazione presenti in questo repository sono rilasciati con licenza **Creative Commons Attribution 4.0 International (CC BY 4.0)**.
 
È possibile condividere e adattare liberamente il materiale per qualsiasi scopo, a condizione di attribuire adeguata paternità, fornire un collegamento alla licenza e indicare eventuali modifiche apportate.
 
📄 [Testo completo della licenza CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.it)
 
> Le schede di catalogo di origine sono tratte dal **Catalogo Generale dei Beni Culturali (MiC)**, disponibile in formato aperto. Per le condizioni d'uso specifiche della fonte originale, si rimanda al sito istituzionale del MiC.
 
---
 
## Citazione
 
Se utilizzi questo dataset o questi risultati nella tua ricerca, cita il contributo come segue:
