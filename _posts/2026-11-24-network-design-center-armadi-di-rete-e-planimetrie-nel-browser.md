---
title: "Network Design Center: armadi di rete e planimetrie nel browser"
description: "Una web app gratuita per progettare armadi di rete e planimetrie, generare etichette e relazioni, tenere sotto controllo le scadenze e sincronizzare tutto con NetBox e Snipe-IT."
categories: [Progetti]
tags: [network design center, armadi rack, cablaggio strutturato, planimetria, netbox, snipe-it, poe, etichette]
image:
  path: /assets/img/posts/network-design-center-poster.jpg
  alt: "La vista 3D di un armadio di rete nel Network Design Center"
---
Quando si allestisce un armadio di rete o si cabla un edificio, le informazioni finiscono quasi sempre sparse: un foglio Excel per le prese, una planimetria in PDF con le annotazioni a penna, le etichette scritte a mano, l'inventario da qualche altra parte. Sei mesi dopo nessuno sa più quale presa dell'aula 3 arriva a quale porta dello switch.

Per avere tutto in un posto solo ho scritto il **Network Design Center**: una web app gratuita che parte dall'armadio e arriva fino alla presa a muro, con le planimetrie, le etichette, l'inventario e la documentazione da consegnare.

[Apri il Network Design Center]({{ site.rack_designer_url }}){: .btn .btn-primary }

Funziona interamente nel browser: niente da installare, nessun account. I progetti restano sul tuo dispositivo.

{% include embed/video.html src='/assets/video/network-design-center.mp4' poster='/assets/img/posts/network-design-center-poster.jpg' title='Il Network Design Center in 40 secondi' muted=true %}

## L'armadio

Si parte dalla libreria: cassetti ottici, patch panel, passacavi, switch, firewall, server, UPS, multiprese. Oltre agli elementi generici ci sono **più di 600 modelli reali di 31 marche**, da MikroTik e Ubiquiti a HPE, Cisco, Synology e QNAP, compresi quelli meno recenti che si trovano ancora negli armadi in produzione. Se un modello manca, lo crei tu.

Mentre componi l'armadio, un **validatore** controlla le regole di allestimento: l'ordine dall'alto (fibra, rame, apparati attivi, alimentazione in basso), un passacavi ogni due unità, gli spazi vuoti chiusi, la portata e la profondità. Se qualcosa non va, **Auto-organizza** rimette tutto in ordine.

Gli identificativi sono automatici: ogni armadio, pannello e presa ha la sua etichetta, e la presa a muro dice già da sola in quale armadio e su quale pannello arriva.

C'è anche la **vista 3D**, che mostra ogni apparato con la sua altezza e profondità: si vede subito se uno switch profondo tocca il fondo di un armadio da 450 mm.

## Le permutazioni e l'alimentazione

Per ogni presa si sceglie la porta dello switch, il colore della bretella e la VLAN. Da lì escono la tabella delle permutazioni, gli script RouterOS per le VLAN degli switch MikroTik e il piano degli indirizzi IP.

Il **bilancio di alimentazione** stima consumi, calore e autonomia degli UPS. Per il PoE ragiona **per classe**: un access point Wi-Fi 7 o una telecamera PTZ chiedono più di quanto può dare una porta 802.3at, e in quel caso il validatore indica quale presa e quale porta non bastano.

## La planimetria

Carichi la pianta (immagine o PDF), la metti in scala e posizioni armadi, prese, access point e telecamere. Ogni elemento è collegato al suo armadio: la lunghezza dei cavi viene stimata, la copertura Wi-Fi e il campo visivo delle telecamere si vedono sulla pianta, e si possono disegnare note, frecce e aree («zona da non forare», «passaggio a soffitto»).

## Dal progetto al cantiere

Durante il sopralluogo la **modalità telefono** permette di segnare presa per presa se è posata, certificata, attiva o ha un problema, con le foto. A fine lavori il confronto tra progetto e realtà mostra cosa è cambiato.

## La documentazione

- **Etichette** per Brother P-touch e Dymo, targhette con QR per gli armadi.
- **Fogli di armadio** e una **relazione completa in PDF** con il tuo logo, l'intestazione, i riquadri firma e i numeri di pagina, pronta per il collaudo.
- **Schede dei locali**: una pagina per ogni aula o ufficio con le prese, gli apparati collegati, il ritaglio della pianta e un QR, da lasciare in loco.
- **Scadenze**: garanzie, fine supporto, licenze e batterie degli UPS, con un calendario `.ics` da importare in Google Calendar o Outlook.

## NetBox e Snipe-IT

Chi usa già NetBox o Snipe-IT non deve ricopiare niente: il progetto si **sincronizza via API**. In NetBox vengono creati sito, location, armadi, tipi di dispositivo con le porte, dispositivi e cavi delle permutazioni; in Snipe-IT gli asset con seriale, modello e posizione. Prima di scrivere c'è sempre un'**anteprima** di cosa verrà creato o aggiornato, ed è possibile anche il contrario: importare un sito di NetBox come nuovo progetto.

> Le chiamate partono dal browser, quindi i server devono essere raggiungibili in HTTPS e accettare richieste da `https://ifeldr.github.io` (CORS). I token restano solo nel browser e non finiscono mai nel progetto.
{: .prompt-info }

## Qualche dettaglio

- Interfaccia in **italiano e inglese**, con modalità chiara e scura.
- Si usa anche **da tastiera** e con i lettori di schermo.
- Si installa come app e funziona anche **senza rete**.
- Più progetti, versioni con confronto, ricerca per seriale o MAC, backup in un file.

Lo uso per il mio lavoro di tutti i giorni e continuo a migliorarlo. Se lo provate e trovate qualcosa che non torna, o vi manca un modello, scrivetemi pure.

[Apri il Network Design Center]({{ site.rack_designer_url }}){: .btn .btn-primary }
