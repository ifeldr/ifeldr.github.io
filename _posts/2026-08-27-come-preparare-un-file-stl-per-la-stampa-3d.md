---
title: "Come preparare un file STL per la stampa 3D"
description: "Unità di misura, mesh chiusa, spessori minimi e tolleranze: i controlli da fare prima di inviare un file da stampare."
categories: [Guide]
tags: [stl, modellazione, tolleranze]
---
Un buon file fa risparmiare tempo a tutti: niente modifiche dell'ultimo minuto e un preventivo più preciso fin da subito. Questi sono i controlli che conviene fare prima di inviarlo.

## Esporta nell'unità giusta

Il formato STL contiene solo la forma, non l'unità di misura. Chi lo apre di solito lo interpreta in millimetri: un pezzo disegnato in pollici o in centimetri arriverà quindi 25,4 o 10 volte più piccolo.

Prima di esportare controlla che il programma di modellazione lavori in millimetri. Se non sei sicuro, carica il file nel [simulatore]({{ '/simulatore-3d/' | relative_url }}): mostra subito le dimensioni del modello e ti permette di cambiare unità.

## La mesh deve essere chiusa

Un STL è una superficie fatta di triangoli. Per essere stampabile deve racchiudere un volume senza buchi, come un palloncino (in inglese si dice *watertight*). Buchi, triangoli sovrapposti o facce rovesciate confondono lo slicer e possono produrre strati mancanti.

Molti programmi hanno una funzione di verifica o riparazione. Se il simulatore segnala che il modello "non ha volume", il problema è quasi sempre questo.

## Rispetta gli spessori minimi

Con un ugello da 0,4 mm, la parete più sottile che si stampa in modo affidabile misura circa 0,8 mm, cioè due passate. Per pezzi che devono reggere carichi conviene stare sopra 1,5–2 mm. I dettagli in rilievo sotto gli 0,4 mm, come le scritte molto piccole, rischiano di sparire.

## Prevedi le tolleranze per gli incastri

Due pezzi disegnati per incastrarsi alla perfezione di solito non entrano. La plastica si espande leggermente e i fori tendono a uscire un po' più stretti. Come regola di partenza, lascia 0,2–0,3 mm di gioco per parte negli accoppiamenti mobili e circa 0,1 mm per quelli forzati.

## Pensa all'orientamento

Un pezzo stampato è più resistente lungo gli strati che tra uno strato e l'altro. Una staffa che deve reggere un peso va orientata in modo che lo sforzo non tenda a "sfogliare" gli strati. Le parti a sbalzo oltre circa 45° richiedono supporti, che lasciano segni sulla superficie.

Se non sei sicuro dell'orientamento migliore, indicalo nella richiesta di preventivo: lo valutiamo insieme.

## Esporta con una risoluzione sensata

Curve troppo sfaccettate si vedranno sul pezzo; al contrario, milioni di triangoli rendono il file pesante senza migliorare la stampa. Nella maggior parte dei programmi le impostazioni "alta" o "fine" dell'esportazione STL vanno benissimo.
