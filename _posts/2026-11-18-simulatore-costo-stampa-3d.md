---
title: "Simulatore 3D: quanto costa davvero una stampa"
description: "Un simulatore gratuito che calcola peso, tempo e costo reale di una stampa 3D da file STL, 3MF o G-code, per filamento e resina, direttamente nel browser."
categories: [Progetti]
tags: [simulatore, costo stampa 3d, stl, 3mf, gcode, resina, filamento]
---
Il prezzo della bobina è solo una parte del costo di una stampa 3D. Ci sono l'energia elettrica, l'usura della stampante, le stampe che falliscono, gli spurghi dei cambi colore e, con la resina, il lavaggio e la polimerizzazione. Per sapere quanto mi costa davvero un pezzo ho scritto un **simulatore**, che ora è disponibile a tutti.

[Apri il simulatore]({{ site.simulatore_url }}){: .btn .btn-primary }

Tutto avviene nel browser: i file che carichi non vengono inviati da nessuna parte.

{% include embed/video.html src='/assets/video/simulatore-3d.mp4' poster='/assets/img/posts/simulatore-3d-poster.jpg' title='Il simulatore in azione' muted=true %}

## Quali file accetta

- **STL**, binario o ASCII: la stima parte dalla geometria del modello, con materiale, riempimento, supporti e qualità scelti nella pagina.
- **3MF di progetto** di Bambu Studio, OrcaSlicer, PrusaSlicer e altri: vengono letti tutti gli oggetti con le loro posizioni e, se il progetto li indica, stampante e filamento sono proposti in automatico.
- **3MF già processati** (`.gcode.3mf`) e **G-code** (`.gcode`, `.gco`, `.g`, `.bgcode`): tempo e filamento sono quelli calcolati dallo slicer, per tutti i piatti del file. Se il G-code contiene una miniatura, compare al posto dell'anteprima 3D.

Si possono caricare più file insieme, e ognuno mantiene le sue impostazioni: materiale, stampante, numero di pezzi, scala e cambi colore.

## Filamento e resina

Oltre alle stampanti a filamento ci sono quelle a resina. In quel caso il simulatore calcola i millilitri necessari, con il pezzo pieno o svuotato, il tempo in base all'altezza dei pezzi (quelli sullo stesso piatto si stampano insieme) e il costo di lavaggio e polimerizzazione.

## Il costo, voce per voce

Il dettaglio dei costi separa materiale, usura della stampante ed energia, e aggiunge due voci che di solito si dimenticano:

- **stampe fallite**: una percentuale, al 5% di partenza, che tiene conto dei pezzi da buttare;
- **cambi colore**: per ogni cambio si aggiungono il materiale di spurgo e il tempo in più.

Accanto al materiale c'è il campo **prezzo bobina** (o prezzo resina): metti quello che paghi davvero e il simulatore lo ricorda per le volte successive. Il costo si può vedere in euro o in dollari.

## Confronto rapido

Sotto il totale, il **confronto rapido** prende il file selezionato e mostra peso, tempo e costo con tutti i materiali compatibili con la sua stampante, oppure con lo stesso materiale su tutte le stampanti che lo supportano, dalla più economica. Basta toccare una riga per applicare la scelta.

## Esportare in Excel

Con **Scarica Excel** ottieni un file con una riga per ogni modello, le impostazioni, il peso, il tempo e i costi, più un foglio di riepilogo. Lo stesso file si può reimportare con **Importa impostazioni** per ritrovare tutto com'era, anche dopo averlo modificato in Excel.

## In italiano e in inglese

Il simulatore è disponibile in [italiano](https://ifeldr.github.io/simulatore-3d/it/) e in [inglese](https://ifeldr.github.io/simulatore-3d/en/): all'apertura sceglie la lingua del browser, e si può cambiare con il selettore IT | EN.

> Le stime partono da valori medi: tempo e peso reali dipendono dalle impostazioni dello slicer. Per il risultato più preciso carica direttamente il G-code o il 3MF già processato.
{: .prompt-tip }

Il codice è su [github.com/ifeldr/simulatore-3d](https://github.com/ifeldr/simulatore-3d). Se trovi un errore o hai un suggerimento, apri pure una segnalazione.
