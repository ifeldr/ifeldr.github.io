---
title: "BambuGo: lo stato della stampante Bambu Lab nella barra dei menu"
description: "Un'app gratuita e open source per macOS, Windows e Linux che mostra avanzamento, temperature, bobine AMS e telecamera della tua Bambu Lab, collegandosi solo in rete locale."
categories: [Progetti]
tags: [bambu lab, bambugo, app, open source, ams, rete locale]
---
![Icona di BambuGo](/assets/img/posts/bambugo-icon.png){: width="128" height="128" .left }

Quando una stampa dura ore, viene voglia di controllarla spesso: a che punto è, quanto manca, se il filamento sta finendo. Per farlo senza aprire ogni volta Bambu Studio o l'app sul telefono ho scritto **BambuGo**, una piccola app che mette lo stato della stampante direttamente nella barra dei menu del Mac o nel tray di Windows e Linux.

Il punto a cui tenevo di più: BambuGo si collega **solo alla stampante nella tua rete locale**. Nessun account, nessun cloud, nessun dato che esce da casa.

{% include embed/video.html src='/assets/video/bambugo-presentazione.mp4' poster='/assets/img/posts/bambugo-video-poster.jpg' title='BambuGo in 30 secondi' muted=true %}

## Cosa mostra

Nella barra compare una piccola stampante: durante il lavoro l'oggetto sul piatto cresce con l'avanzamento, con accanto percentuale e tempo rimanente (ad esempio `45% · 1h 12m`). Un simbolo segnala pausa, fine stampa o errori.

Cliccando si apre un pannello con:

- **avanzamento**: percentuale, nome del lavoro, strato, tempo rimanente e ora di fine;
- i comandi **Pausa / Riprendi / Interrompi** (l'interruzione chiede conferma);
- la **telecamera** in diretta, con l'interruttore della luce e una finestra che resta in primo piano;
- le **temperature** di ugello (entrambi sulle stampanti a doppio ugello), piatto e camera;
- le **bobine** di tutte le unità collegate (AMS, AMS lite, AMS 2 Pro, AMS HT, AMS 3H) e di quelle esterne, con colore, materiale, residuo, umidità ed essiccazione in corso;
- il **modulo laser e lama** sulle macchine che lo supportano;
- gli **errori HMS** della stampante e dell'AMS, con il link alla spiegazione sul wiki Bambu Lab;
- qualità del Wi-Fi e velocità di stampa.

Arrivano anche le notifiche a fine stampa, in caso di errore e quando la stampante va in pausa, per esempio perché è finito il filamento.

C'è poi un **browser di modelli** pronti con MakerWorld, Printables e Thingiverse, comodo per cercare qualcosa da stampare senza uscire dall'app.

## Stampanti supportate

BambuGo funziona con tutta la gamma attuale: A1 mini, A1, A2L, P1P, P1S, P2S, X1, X1C, X1E, X2D, H2D, H2D Pro, H2S, H2C, H3C e anche l'incisore laser R1. Alcuni modelli più recenti (R1, H3C, A2L, X2D e P2S) non li ho ancora potuti provare su una macchina reale: se qualcosa non torna, aprite pure una segnalazione sul repository.

## Download e installazione

I pacchetti per tutti i sistemi sono nell'[ultima release su GitHub](https://github.com/ifeldr/BambuGo/releases/latest):

| Sistema | File |
|---|---|
| macOS 13 o successivo | `BambuGo.zip` |
| Windows 10 / 11 | installer `.exe` o `.msi` |
| Ubuntu / Debian | pacchetto `.deb` |
| Fedora | pacchetto `.rpm` |
| Arch e altre distro | `.AppImage` |

L'app non è firmata, quindi al primo avvio il sistema chiede conferma: su macOS va autorizzata da *Impostazioni di Sistema → Privacy e sicurezza → Apri comunque*, su Windows si sceglie *Ulteriori informazioni → Esegui comunque* nella finestra di SmartScreen.

## Configurazione

1. Clicca l'icona e premi **Cerca in rete**: le stampanti trovate compaiono con nome, modello e IP. Se non ne trova, inserisci a mano IP e numero di serie.
2. Inserisci l'**access code**, che trovi sul display della stampante in *Impostazioni → Rete/WLAN*.
3. Concedi l'accesso alla rete locale (su macOS) o al firewall (su Windows).

> Conviene riservare l'IP della stampante nel DHCP del router, così non cambia e l'app la ritrova sempre.
{: .prompt-tip }

Per usare i comandi (pausa, stop, luce) con i firmware più recenti servono la **modalità LAN** e la **modalità sviluppatore** attive sulla stampante; la sola lettura dello stato funziona comunque. Per la telecamera delle serie X1, P2, H2 e simili va attivata l'opzione **Liveview in LAN**.

## Open source

BambuGo è rilasciata con licenza MIT e il codice è su [github.com/ifeldr/BambuGo](https://github.com/ifeldr/BambuGo): la versione per Mac è scritta in Swift, quella per Windows e Linux con [Tauri](https://tauri.app). Segnalazioni e suggerimenti sono benvenuti.

> BambuGo è un progetto indipendente e non è affiliato, approvato o sponsorizzato da Bambu Lab. "Bambu Lab" e i nomi delle stampanti sono marchi dei rispettivi proprietari. L'app è fornita così com'è, senza garanzie.
{: .prompt-info }
