---
title: Simulatore 3D
icon: fas fa-cube
order: 1
permalink: /simulatore/
description: Carica i tuoi file STL e calcola subito peso, tempo e costo della stampa 3D.
---

{%- comment -%}
  Il simulatore ora vive nel repository separato "simulatore-3d".
  Questa voce del menu porta direttamente lì (indirizzo in _config.yml, simulatore_url).
{%- endcomment -%}

Il simulatore si apre in una pagina dedicata: carica i tuoi file STL e scopri subito peso, tempo di stampa e costo reale.

<a class="btn btn-primary" href="{{ site.simulatore_url }}"><i class="fas fa-cube me-2" aria-hidden="true"></i>Apri il simulatore</a>

<script>window.location.replace({{ site.simulatore_url | jsonify }});</script>
