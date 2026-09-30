---
title: Hvězdárny v JihoČASu
subtitle: Jihočeské hvězdárny spolupracující s pobočkou
permalink: /hvezdarny/
hero_height: is-small
---

Pobočka úzce spolupracuje s těmito hvězdárnami. Aktuální program, otevírací dobu a vstupné najdete na jejich webech.

<div class="columns is-multiline mt-4">
{% for h in site.data.hvezdarny %}
<div class="column is-6-tablet is-6-desktop">
  <div class="card jc-card">
    <div class="card-content">
      <div class="media">
        <div class="media-left">
          <span class="icon is-large has-text-primary"><i class="fas {{ h.icon }} fa-2x"></i></span>
        </div>
        <div class="media-content">
          <p class="title is-5">{{ h.name }}</p>
          <p class="subtitle is-6">{{ h.town }}</p>
        </div>
      </div>
      <div class="content">
        <p>{{ h.note }}</p>
        <p><span class="icon"><i class="fas fa-location-dot"></i></span> {{ h.address }}</p>
      </div>
    </div>
    <footer class="card-footer">
      <a href="{{ h.web }}" class="card-footer-item">Web hvězdárny</a>
      <a href="https://mapy.com/?q={{ h.name | append: ' ' | append: h.town | url_encode }}" class="card-footer-item">Mapa</a>
    </footer>
  </div>
</div>
{% endfor %}
</div>
