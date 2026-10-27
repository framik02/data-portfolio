# Articoli e report

Analisi dati scritte per **Liberi Network** e per la testata **Popular Opinions**.
Ogni pezzo nasce da un corpus raccolto e classificato da me, non da dati di terze parti.
Sette lavori, aggiornati al 27 ottobre 2026.

| Lavoro | Corpus | Formato |
|---|---|---|
| [Come si discute di cannabis in Italia](report/come-si-discute-di-cannabis-in-italia.pdf) | 69.258 commenti, 2016-2026 | Report, 24 pagine |
| [Come si discute di nucleare in Italia](report/come-si-discute-di-nucleare-in-italia.pdf) | 138.474 commenti, 2016-2026 | Report, 45 pagine |
| [Grillo a Pulp Podcast, cosa dicono i commenti](grillo-a-pulp-podcast.md) | 5.207 commenti | Articolo |
| [Spin Time, quasi nessuno parla di case](spin-time-quasi-nessuno-parla-di-case.md) | 6.114 commenti | Articolo |
| [Il tuo fornitore di luce è bravo o no?](il-tuo-fornitore-di-luce.md) | 139.350 commenti e recensioni | Articolo |
| [Quale conto convince di più gli italiani](quale-conto-convince-di-piu-gli-italiani.md) | 330.555 commenti e recensioni | Articolo |
| [Caso Roggero, il giudizio della rete](caso-roggero-il-giudizio-della-rete.md) | 144.970 commenti | Articolo |

## [Come si discute di cannabis in Italia](report/come-si-discute-di-cannabis-in-italia.pdf)

Report per Liberi Network, ottobre 2026. 69.258 commenti pubblicati fra il 2016 e il
settembre 2026, 56.354 sotto 890 video YouTube e 12.904 in 305 discussioni Reddit, scritti
da 30.826 account. 10.400 letti e classificati.

- fra chi prende posizione sulla legalizzazione il 76,4% è favorevole, e la quota resta
  sopra il 66% in ogni anno della serie;
- sulla cannabis light i favorevoli salgono all'87,8%. Il divieto del decreto sicurezza è
  la misura più contestata dell'archivio;
- i contrari scrivono un commento schierato su quattro e su YouTube raccolgono 6 like su 100.

## [Come si discute di nucleare in Italia](report/come-si-discute-di-nucleare-in-italia.pdf)

Report per Liberi Network, settembre 2026. Dieci anni di commenti su YouTube e Reddit,
232.916 raccolti e 138.474 nel corpus filtrato. Fino al 2020 prevaleva il no, dal 2025
prevale il sì, e nel frattempo si parla meno di scorie e più di bollette. Il report segue
argomenti, lessico, picchi e canali, e mette a confronto i commenti favorevoli e contrari
che raccolgono più reazioni. Una versione breve è uscita su
[Popular Opinions](https://framik02.github.io/popular-opinions/nucleare/).

## [Grillo a Pulp Podcast, cosa dicono i commenti](grillo-a-pulp-podcast.md)

Tutti i 5.207 commenti sotto l'episodio, scritti da 4.088 persone. Chi scrive difende
Grillo di poco, saldo +10,2. Chi mette like lo difende molto di più, +31,7 pesando ogni
commento con i suoi like. Sedici narrazioni ricostruite, ognuna con il suo schieramento.

## [Spin Time, quasi nessuno parla di case](spin-time-quasi-nessuno-parla-di-case.md)

Censimento completo, i 6.114 commenti YouTube sul palazzo occupato di Roma letti uno per
uno. Il 77% riguarda il caso, il saldo è −65%, e del diritto alla casa si parla pochissimo.
La serie mese per mese segue la programmazione dei canali più che l'opinione.

## [Il tuo fornitore di luce è bravo o no? Dipende da dove lo chiedi](il-tuo-fornitore-di-luce.md)

Undici fornitori di luce e gas, 139.350 commenti e recensioni fra il 2021 e il 2026.
Le recensioni degli store giudicano l'app, le discussioni giudicano prezzi e servizio, e le
due classifiche si contraddicono per metà dei marchi.

## [Quale conto convince di più gli italiani](quale-conto-convince-di-piu-gli-italiani.md)

Tredici marchi di conti e carte digitali giudicati da 330.555 fra commenti e recensioni,
raccolti fra il 2021 e il 2026 su YouTube, Google Play, App Store e Reddit.

- lo stesso conto riceve giudizi opposti a seconda della fonte. Revolut sta a +77 nelle
  recensioni degli store e a 0 nelle discussioni dei forum;
- quattro parole su dieci scritte sui conti digitali riguardano l'app, ma l'app provoca
  meno di un cambio banca su dieci;
- separando i trasferimenti volontari da quelli imposti e dalle espulsioni, la classifica
  dei vincitori cambia.

## [Caso Roggero, il giudizio della rete](caso-roggero-il-giudizio-della-rete.md)

144.970 commenti su 1.036 video dal 2021 al 2026, classificati con un modello BERT
italiano addestrato per l'occasione. L'82,3% del dibattito si concentra nel solo luglio
2026, dopo la sentenza definitiva. Il dibattito televisivo mostra un Paese diviso, i
commenti un consenso quasi unanime a favore del gioielliere, stabile dal 2023.

## Metodo

Le percentuali non arrivano da un dizionario di parole positive e negative. Ogni corpus
viene campionato ed etichettato a mano, e il campione diventa il set di addestramento di
un modello che classifica il resto, oppure, quando il corpus è piccolo, si legge tutto.
Dove serve il conteggio è deduplicato per autore, perché contare i messaggi invece delle
persone gonfia il peso di chi scrive di più.
