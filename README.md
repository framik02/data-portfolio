# Francesco Chiarolanza

Sviluppo applicazioni web e mobile, data engineering e NLP. Roma.

Questo repository raccoglie il lavoro che posso mostrare pubblicamente. La tesi di laurea
sperimentale con la pipeline che la riproduce, sette fra articoli e report di analisi dati
per Liberi Network e Popular Opinions, la mappa delle collaborazioni politiche su Instagram e le applicazioni.

**[Portfolio in PDF](Portfolio_Francesco_Chiarolanza.pdf)**, otto pagine (27/10/2026).

Contatti: chiarolanza.francesco@gmail.com

---

## Applicazioni web e mobile

**[Portfolio applicazioni: Tom’s Christian Tours, Leggio e FungoMeter](applicazioni/README.md)**

Demo pubbliche, schermate, codice disponibile e schede tecniche dei progetti. React/TypeScript, Node.js e Python; frontend, persistenza, API e pipeline dati. Accessibilità e limiti indicati per ciascun progetto (27/10/2026).

## Liberi Network, la rete su Instagram

**[Mappa delle collaborazioni](https://framik02.github.io/ecosistema-network/)** fra profili
Instagram della politica e dell'informazione, aggiornata in automatico. Al 13 ottobre 2026
collega 225 profili con 187 legami fra profili monitorati, e ogni legame si apre sui post
che lo giustificano.

I dati arrivano da uno scraper che ho scritto per Liberi Network. Un browser automatico con
sessione persistente legge post, coautori e commenti dai dati che la pagina riceve, li salva
in SQLite e misura la copertura di ogni post togliendo i commenti che arrivano dalla copia su
Facebook. In locale un livello semantico con embedding multilingue misura le affinità fra
profili e raggruppa le caption per tema.

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

## Articoli e report

| Lavoro | Corpus |
|---|---|
| [Come si discute di cannabis in Italia](articoli/report/come-si-discute-di-cannabis-in-italia.pdf), report di 24 pagine | 69.258 commenti, 2016-2026 |
| [Come si discute di nucleare in Italia](articoli/report/come-si-discute-di-nucleare-in-italia.pdf), report di 45 pagine | 138.474 commenti, 2016-2026 |
| [Grillo a Pulp Podcast, cosa dicono i commenti](articoli/grillo-a-pulp-podcast.md) | 5.207 commenti |
| [Spin Time, quasi nessuno parla di case](articoli/spin-time-quasi-nessuno-parla-di-case.md) | 6.114 commenti letti tutti |
| [Il tuo fornitore di luce è bravo o no?](articoli/il-tuo-fornitore-di-luce.md) | 139.350 commenti e recensioni |
| [Quale conto convince di più gli italiani](articoli/quale-conto-convince-di-piu-gli-italiani.md) | 330.555 commenti e recensioni |
| [Caso Roggero, il giudizio della rete](articoli/caso-roggero-il-giudizio-della-rete.md) | 144.970 commenti |

Sintesi e risultati principali di ciascuno nell'[indice degli articoli](articoli/README.md).

## Come lavoro

Le analisi qui dentro seguono sempre lo stesso schema: raccolta dei dati alla fonte
tramite API o scraping, archiviazione in un database relazionale, etichettatura manuale
di un campione che diventa il set di addestramento, fine tuning di un modello su GPU
cloud, inferenza sull'intero corpus e infine i grafici. Ogni conclusione arriva con i
suoi limiti dichiarati, perché chi commenta online non è un campione rappresentativo e
scriverlo è parte del lavoro.
