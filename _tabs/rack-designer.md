---
title: Network Design Center
icon: fas fa-server
order: 2
parent: progetti
permalink: /rack/
description: Progetta e verifica gli armadi di rete, genera le etichette e posiziona armadi e prese sulla planimetria.
---

{%- comment -%}
  Il Network Design Center vive nel repository separato "rack-designer".
  Questa voce del menu porta direttamente lì (indirizzo in _config.yml, rack_designer_url).
{%- endcomment -%}

Il Network Design Center si apre in una pagina dedicata: allestisci gli armadi di rete, genera le etichette e posiziona armadi, prese e access point sulla planimetria.

<a class="btn btn-primary" href="{{ site.rack_designer_url }}"><i class="fas fa-server me-2" aria-hidden="true"></i>Apri il Network Design Center</a>

<script>window.location.replace({{ site.rack_designer_url | jsonify }});</script>
