---
title: Progetti
icon: fas fa-folder-open
order: 1
permalink: /progetti/
description: Gli strumenti che ho sviluppato e che puoi usare direttamente dal browser.
---

{%- comment -%}
  Le card vengono da _data/progetti.yml, dal progetto più recente al più vecchio.
{%- endcomment -%}

Gli strumenti che ho sviluppato e che puoi usare direttamente dal browser, senza installare nulla.

{% assign progetti = site.data.progetti | sort: 'data' | reverse %}
<div class="progetti">
{%- for p in progetti %}
  <a class="progetto-card" href="{{ p.url }}">
    <i class="{{ p.icona }} progetto-icona" aria-hidden="true"></i>
    <span class="progetto-testo">
      <strong>{{ p.titolo }}</strong>
      <span>{{ p.descrizione }}</span>
    </span>
  </a>
{%- endfor %}
</div>
