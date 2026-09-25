---
title: "Riempimento e pareti: cosa conta davvero per la robustezza"
description: "Perché il riempimento al 100% raramente serve, e come pareti e orientamento incidono sulla resistenza di un pezzo stampato in 3D."
categories: [Impostazioni di stampa]
tags: [riempimento, pareti, robustezza]
---
Quando un pezzo deve essere robusto, l'istinto è chiedere il riempimento al 100%. Quasi sempre non è la scelta migliore: costa di più, richiede molto più tempo e spesso non rende il pezzo tanto più forte quanto ci si aspetta.

## Come è fatto un pezzo stampato

Un oggetto stampato in 3D non è pieno. Ha un guscio esterno, cioè le pareti laterali e gli strati pieni sopra e sotto, e all'interno una struttura a griglia: il riempimento. La percentuale indica quanto è fitta questa griglia.

## Le pareti contano più del riempimento

Gran parte degli sforzi, come flessione, torsione e urti, si concentra sulla superficie del pezzo. Aggiungere una o due pareti in più di solito aumenta la robustezza più che raddoppiare il riempimento, e costa meno.

Il riempimento è importante soprattutto quando il pezzo viene schiacciato, o quando ci sono viti e inserti che devono fare presa sul materiale.

## Valori di riferimento

- **10–15%**: oggetti decorativi, modellini, prototipi estetici
- **20–30%**: uso generico, oggetti maneggiati tutti i giorni
- **40–60%**: pezzi funzionali sotto sforzo, staffe, supporti
- **80–100%**: casi particolari, come pezzi piccoli che devono essere pesanti o reggere compressione

## Quanto pesa sul prezzo

Il riempimento influisce su materiale e tempo di stampa, e quindi sul prezzo. Su un pezzo piccolo la differenza tra 20% e 50% è modesta, perché il guscio pesa già molto. Su un pezzo grande e massiccio può raddoppiare il costo.

Il modo più rapido per capirlo è provare: nel [simulatore]({{ '/simulatore-3d/' | relative_url }}) puoi cambiare il riempimento di ogni file e vedere come variano peso, tempo e prezzo.

## L'orientamento conta quanto il riempimento

Gli strati aderiscono bene tra loro, ma il punto più debole di un pezzo stampato resta sempre il legame tra uno strato e l'altro. Una staffa orientata male si rompe lungo gli strati anche al 100% di riempimento. Per questo, per i pezzi funzionali, è utile spiegare nella richiesta come verranno usati: l'orientamento giusto si sceglie in base a dove arriva lo sforzo.
