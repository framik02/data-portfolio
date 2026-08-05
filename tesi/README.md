# Stance detection sui commenti YouTube come predittore del referendum del 2026

Tesi di laurea triennale in Scienze della Comunicazione, Università degli Studi Roma Tre,
Dipartimento di Filosofia Comunicazione Spettacolo. Anno 2025-2026.

**[PDF completo](tesi-referendum-2026-chiarolanza.pdf)** (127 pagine)

## La domanda

I commenti YouTube possono predire l'esito di un referendum meglio di quanto si creda,
oppure sono solo rumore prodotto da una minoranza molto rumorosa?

Caso di studio: il referendum costituzionale del 22-23 marzo 2026 sulla separazione delle
carriere in magistratura. Risultato reale 53,74% No, 46,26% Sì, affluenza 58,7%.

## Il risultato

L'aggregato deduplicato secondo la regola "un autore, un voto" stima il Sì al **45,9%**,
con uno scarto di **0,40 punti percentuali** dal risultato reale.

Lo stesso corpus, contato senza deduplicazione, sbaglia di **2,68 punti**. La differenza
fra i due numeri è la misura di quanto pesa la minoranza più attiva, ed è il contributo
metodologico centrale del lavoro.

## Domande di ricerca e ipotesi

| | Domanda | Ipotesi | Esito |
|---|---|---|---|
| RQ1 | I commenti deduplicati predicono l'esito con errore sotto i 2 punti? | H1 | confermata (0,40 pp) |
| RQ2 | I turning point nella stance si concentrano attorno a eventi identificabili? | H2 | confermata |
| RQ3 | Esiste una relazione causale asimmetrica fra stampa e stance referendaria? | H3 | confermata |

## I dati

| Corpus | Volume |
|---|---|
| Commenti sul referendum | 196.050 su 1.564 video, 7 mesi |
| Commenti sul consenso al governo | 78.538 |
| Articoli di stampa | 3.424 |

Raccolta tramite YouTube Data API v3 con filtro di pertinenza su parole chiave e
esclusione del rumore.

## Il modello

Fine tuning di `dbmdz/bert-base-italian-xxl-uncased` per la stance detection a tre classi.
F1 macro 0,762 e accuracy 0,784 sul test del modello referendum, F1 macro 0,628 sul
modello del consenso al governo. Addestramento su GPU tramite Kaggle.

## I notebook

La pipeline empirica è interamente riproducibile in cinque notebook.

| File | Cosa fa |
|---|---|
| [01_raccolta_dati.ipynb](notebooks/01_raccolta_dati.ipynb) | raccolta da YouTube Data API v3, filtro di pertinenza, deduplicazione |
| [02_allenamento_modelli.ipynb](notebooks/02_allenamento_modelli.ipynb) | fine tuning BERT, valutazione, matrice di confusione |
| [03_predizione_e_corpus.ipynb](notebooks/03_predizione_e_corpus.ipynb) | inferenza sul corpus, aggregazione grezza e deduplicata |
| [04_serie_temporali_e_turning_points.ipynb](notebooks/04_serie_temporali_e_turning_points.ipynb) | serie giornaliere, individuazione dei turning point, mappatura sugli eventi |
| [05_granger_causality.ipynb](notebooks/05_granger_causality.ipynb) | test ADF e causalità di Granger sulle sei coppie di serie |

La chiave della YouTube Data API non è nel codice: viene letta dai secret di Kaggle.

## Limiti dichiarati

Chi commenta su YouTube non è un campione rappresentativo dell'elettorato. Il risultato
non dimostra che i commenti sostituiscono i sondaggi, dimostra che una correzione
metodologica semplice, contare le persone invece dei messaggi, recupera gran parte del
segnale che il conteggio grezzo distrugge.
