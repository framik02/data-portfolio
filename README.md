# Francesco Chiarolanza

Sviluppo applicazioni web e mobile, data engineering e NLP. Roma.

Questo repository raccoglie il lavoro che posso mostrare pubblicamente: la tesi di laurea
sperimentale con la pipeline che la riproduce, e gli articoli di analisi dati scritti per
la testata Liberi Network.

Contatti: chiarolanza.francesco@gmail.com

---

## Applicazioni web e mobile

**[Portfolio applicazioni: Tom’s Christian Tours, Leggio e FungoMeter](applicazioni/README.md)**

Demo pubbliche, codice disponibile e schede tecniche dei progetti. React/TypeScript, Node.js e Python; frontend, persistenza, API e pipeline dati. Accessibilità e limiti indicati per ciascun progetto (23/10/2026).

## Tesi di laurea

**[Stance detection sui commenti YouTube come predittore del referendum costituzionale
italiano del 22-23 marzo 2026](tesi/)**

Previsione dell'esito referendario con uno scarto di **0,40 punti percentuali** dal
risultato reale, usando come unica fonte i commenti YouTube.

| | |
|---|---|
| Dataset originale | oltre 270.000 elementi |
| Commenti sul referendum | 196.050 su 1.564 video, 7 mesi di raccolta |
| Commenti sul consenso al governo | 78.538 |
| Articoli di stampa | 3.424 |
| Modello | BERT italiano fine tuned, F1 macro 0,762 |
| Risultato | Sì stimato 45,9% contro 46,26% reale |

Il contributo metodologico centrale è la deduplicazione "una testa, un voto": senza di
essa lo stesso corpus produce un errore di 2,68 punti, oltre sei volte più grande.

- [PDF completo della tesi](tesi/tesi-referendum-2026-chiarolanza.pdf) (127 pagine)
- [I cinque notebook che riproducono la pipeline](tesi/notebooks/)

## Articoli

**[Quale conto convince di più gli italiani](articoli/quale-conto-convince-di-piu-gli-italiani.md)**
Tredici marchi di conti e carte digitali giudicati da 330.555 commenti e recensioni
raccolti su quattro piattaforme fra il 2021 e il 2026. Include il risultato che considero
più interessante: lo stesso conto riceve giudizi opposti a seconda che se ne parli nelle
recensioni degli store o nelle discussioni sui forum.

**[Caso Roggero, il giudizio della rete](articoli/caso-roggero-il-giudizio-della-rete.md)**
144.970 commenti su 1.036 video dal 2021 al 2026, classificati con un modello BERT
addestrato per l'occasione. Il dibattito televisivo racconta un Paese diviso, i commenti
raccontano un consenso quasi unanime formato molto prima della sentenza.

## Come lavoro

Le analisi qui dentro seguono sempre lo stesso schema: raccolta dei dati alla fonte
tramite API o scraping, archiviazione in un database relazionale, etichettatura manuale
di un campione che diventa il set di addestramento, fine tuning di un modello su GPU
cloud, inferenza sull'intero corpus e infine i grafici. Ogni conclusione arriva con i
suoi limiti dichiarati, perché chi commenta online non è un campione rappresentativo e
scriverlo è parte del lavoro.
