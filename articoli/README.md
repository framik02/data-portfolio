# Articoli

Analisi dati scritte per la testata **Liberi Network**, dove collaboro come data analyst.
Ogni articolo nasce da un corpus raccolto e classificato da me, non da dati di terze parti.

## [Quale conto convince di più gli italiani](quale-conto-convince-di-piu-gli-italiani.md)

Tredici marchi di conti e carte digitali giudicati da 330.555 fra commenti e recensioni,
raccolti fra il 2021 e il 2026 su YouTube, Google Play, App Store e Reddit.

Tre risultati che vale la pena leggere:

- lo stesso conto riceve giudizi opposti a seconda della fonte. Revolut sta a +77 nelle
  recensioni degli store e a 0 nelle discussioni dei forum, e lo scarto è massimo proprio
  sui marchi più celebrati;
- quattro parole su dieci scritte sui conti digitali riguardano l'app, ma l'app provoca
  meno di un cambio banca su dieci. Il canale di feedback più rumoroso misura la variabile
  meno correlata all'abbandono;
- i racconti di cambio conto non sono tutti uguali. Separando i trasferimenti volontari da
  quelli imposti e dalle espulsioni, la classifica dei vincitori cambia.

## [Caso Roggero, il giudizio della rete](caso-roggero-il-giudizio-della-rete.md)

144.970 commenti su 1.036 video dal 2021 al 2026, classificati con un modello BERT
italiano addestrato per l'occasione.

L'82,3% del dibattito si concentra nel solo luglio 2026, dopo la sentenza definitiva della
Cassazione. Il dibattito televisivo mostra un Paese diviso lungo le linee di partito, i
commenti mostrano un consenso quasi unanime a favore del gioielliere, stabile dal 2023 e
presente anche sui canali senza linea editoriale sul tema.

## Metodo

Le percentuali che leggete non arrivano da un dizionario di parole positive e negative.
Ogni corpus viene campionato, etichettato a mano coppia per coppia, e il campione diventa
il set di addestramento di un modello che classifica il resto. Dove serve, il conteggio è
deduplicato per autore, perché contare i messaggi invece delle persone gonfia il peso di
chi scrive di più.
