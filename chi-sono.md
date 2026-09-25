---
layout: default
title: Chi sono
permalink: /chi-sono/
description: "Chi c'è dietro le stampe: esperienza, attrezzatura e modo di lavorare."
---
{%- assign email = site.data.calcolatore_3d.email_preventivi -%}
<section class="pagina-testa">
  <div class="contenitore chi-griglia">
    <div class="chi-foto">
      {%- if site.author.foto and site.author.foto != "" %}
      <img src="{{ site.author.foto | relative_url }}" alt="{{ site.author.name }}" width="600" height="600">
      {%- else %}
      {%- assign parti = site.author.name | split: " " -%}
      <div class="monogramma" aria-hidden="true">{% for p in parti limit: 2 %}{{ p | slice: 0 }}{% endfor %}</div>
      {%- endif %}
    </div>
    <div>
      <p class="occhiello">Chi sono</p>
      <h1>Ciao, sono {{ site.author.name }}.</h1>
      <p class="pagina-sottotitolo">{{ site.author.ruolo }}. Trasformo idee, disegni e file 3D in oggetti reali.</p>
    </div>
  </div>
</section>

<div class="contenitore contenitore-stretto prosa" markdown="1">

<!-- Sostituisci i testi qui sotto con la tua storia. Si scrive in Markdown. -->

## La mia storia

Racconta qui come ti sei avvicinato alla stampa 3D: la prima stampante, il primo pezzo che ti ha dato soddisfazione, cosa ti ha spinto a farne un lavoro o una passione seria.

Due o tre paragrafi bastano. Chi arriva qui vuole capire se può fidarsi di te: parla di esperienza concreta più che di aggettivi.

## Cosa faccio

- **Prototipi** per verificare forme e ingombri prima della produzione.
- **Ricambi e pezzi funzionali**: supporti, staffe, clip, componenti fuori produzione.
- **Oggetti su misura**: regali, targhe, modellini, complementi d'arredo.
- **Modellazione 3D**: se hai solo un'idea o un disegno, posso preparare io il file.

## Come lavoro

Ogni file viene controllato prima della stampa: se c'è un problema di geometria, di pareti troppo sottili o di orientamento, te lo segnalo e ti propongo una soluzione. Il prezzo che vedi nel simulatore è una stima; quello definitivo te lo confermo prima di iniziare, insieme ai tempi di consegna.

## La mia attrezzatura

- Stampante 1: modello e area di stampa
- Stampante 2: modello e area di stampa
- Materiali disponibili: vedi l'elenco nel [simulatore]({{ '/simulatore-3d/' | relative_url }})

</div>

<div class="contenitore contenitore-stretto">
  <div class="riquadro-cta">
    <div>
      <p class="riquadro-cta-titolo">Parliamo del tuo progetto</p>
      <p>Scrivimi per richieste particolari, oppure calcola subito il prezzo del tuo file.</p>
    </div>
    <div class="riquadro-cta-azioni">
      {%- if email %}<a class="bottone bottone-vuoto-scuro" href="mailto:{{ email }}">Scrivimi</a>{% endif %}
      <a class="bottone bottone-caldo" href="{{ '/simulatore-3d/' | relative_url }}">Apri il simulatore</a>
    </div>
  </div>
</div>
