---
layout: default
title: Progetti
permalink: /progetti/
---

<h1>Progetti</h1>
<p class="lead">Progetti personali e di studio. Gli appunti universitari sono nella <a href="{{ '/#appunti' | relative_url }}">home</a>.</p>

<div class="grid">
  {%- for p in site.data.progetti %}
    {% include card.html titolo=p.titolo sottotitolo=p.descrizione pill=p.pill link_sito=p.link_sito link_repo=p.link_repo %}
  {%- endfor %}
</div>
