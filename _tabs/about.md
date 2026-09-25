---
title: Chi sono
icon: fas fa-user
order: 5
permalink: /chi-sono/
---

<!-- Sostituisci i testi qui sotto con la tua storia. Si scrive in Markdown. -->

Ciao, sono **{{ site.social.name }}**. Trasformo idee, disegni e file 3D in oggetti reali, uno strato alla volta.

## La mia storia

Racconta qui come ti sei avvicinato alla stampa 3D: la prima stampante, il primo pezzo che ti ha dato soddisfazione, cosa ti ha spinto a farne un lavoro o una passione seria.

Due o tre paragrafi bastano. Chi arriva qui vuole capire se può fidarsi di te: parla di esperienza concreta più che di aggettivi.

## Cosa faccio

- **Prototipi** per verificare forme e ingombri prima della produzione.
- **Ricambi e pezzi funzionali**: supporti, staffe, clip, componenti fuori produzione.
- **Oggetti su misura**: regali, targhe, modellini, complementi d'arredo.
- **Modellazione 3D**: se hai solo un'idea o un disegno, posso preparare io il file.

## Come lavoro

Ogni file viene controllato prima della stampa: se c'è un problema di geometria, di pareti troppo sottili o di orientamento, te lo segnalo e ti propongo una soluzione. Il prezzo che vedi nel [simulatore]({{ '/simulatore-3d/' | relative_url }}) è una stima; quello definitivo te lo confermo prima di iniziare, insieme ai tempi di consegna.

## Materiali disponibili

{% for m in site.data.calcolatore_3d.materiali -%}
- **{{ m.nome }}**{% if m.descrizione %}: {{ m.descrizione }}{% endif %}
{% endfor %}

## La mia attrezzatura

- Stampante 1: modello e area di stampa
- Stampante 2: modello e area di stampa

## Contatti

Scrivimi a [{{ site.data.calcolatore_3d.email_preventivi }}](mailto:{{ site.data.calcolatore_3d.email_preventivi }}) per richieste particolari, oppure calcola subito il prezzo del tuo file nel [simulatore]({{ '/simulatore-3d/' | relative_url }}).
{: .prompt-tip }
