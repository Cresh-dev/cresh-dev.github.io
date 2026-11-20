---
layout: default
title: Home
permalink: /
---

<section class="hero">
  <img class="avatar" src="{{ '/assets/img/avatar.webp' | relative_url }}" alt="Foto di Alessio Crescenzio" width="96" height="96">
  <div>
    <h1>Ciao, sono Alessio</h1>
    <p class="lead">Studente magistrale di Ingegneria Informatica (Cybersecurity &amp; Cloud) al Politecnico di Bari. Pubblico i miei appunti universitari in open source, perché siano utili a chiunque.</p>
    <div class="actions">
      <a class="btn btn-primary" href="#appunti">Sfoglia gli appunti</a>
      <a class="btn btn-secondary" href="https://github.com/{{ site.github_username }}">GitHub</a>
      <a class="btn btn-secondary" href="https://www.linkedin.com/in/{{ site.linkedin_username }}">LinkedIn</a>
    </div>
  </div>
</section>

<section id="appunti" aria-labelledby="appunti-titolo">
  <h2 id="appunti-titolo">Appunti universitari</h2>
  <div class="grid">
    {%- for corso in site.data.corsi %}
      {%- capture sotto %}{{ corso.professore }} · {{ corso.argomenti }}{% endcapture %}
      {%- capture pill %}{{ corso.note }} note{% endcapture %}
      {%- capture sito %}https://cresh-dev.github.io/{{ corso.repo }}/{% endcapture %}
      {%- capture repo %}https://github.com/{{ site.github_username }}/{{ corso.repo }}{% endcapture %}
      {% include card.html titolo=corso.titolo sottotitolo=sotto pill=pill link_sito=sito link_repo=repo %}
    {%- endfor %}
  </div>
  <p class="note">Hai trovato un errore negli appunti? Apri una issue nel repository del corso: ogni segnalazione è benvenuta.</p>
</section>
