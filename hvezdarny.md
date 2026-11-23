---
description: "Hvězdárny v jižních Čechách: České Budějovice, Sezimovo Ústí, Jindřichův Hradec, Svákovská hvězdárna u Soběslavi a mapa dalších astronomických míst v regionu."
title: Hvězdárny v jižních Čechách
subtitle: Veřejné, profesionální i soukromé hvězdárny v regionu
permalink: /hvezdarny/
hero_height: is-small
---

Mezi členy JihoČASu jsou mimo jiné zástupci těchto hvězdáren. Jejich aktuální program, otevírací dobu a vstupné najdete na webech jednotlivých hvězdáren.

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

## Mapa hvězdáren a astronomických míst

V jižních Čechách je celá řada hvězdáren. Některé jsou veřejné a pořádají pozorování a programy pro návštěvníky, jiné jsou profesionální vědecká pracoviště. Najdeme tu také mnoho soukromých hvězdáren, které je často možné navštívit po domluvě s jejich majiteli.

Přehled hvězdáren i dalších míst spojených s astronomií nabízí mapa **Říše hvězd**, kterou na platformě Mapotic provozuje Hvězdárna Františka Pešty v Sezimově Ústí.

<div class="jc-map">
  <iframe src="https://www.mapotic.com/rise-hvezd/embed?lat=49.05&lng=14.45&zoom=8" title="Mapa Říše hvězd: hvězdárny a astronomická místa v jižních Čechách" loading="lazy" allow="geolocation" referrerpolicy="strict-origin-when-cross-origin"></iframe>
</div>

<div class="buttons mt-3">
  <a class="button is-info is-outlined" href="https://www.mapotic.com/rise-hvezd"><span class="icon"><i class="fas fa-up-right-from-square"></i></span><span>Otevřít celou mapu</span></a>
  <a class="button is-info is-outlined" href="https://www.hvezdarna-fp.eu/projekty/mapotic-rise-hvezd/mapotic-form/"><span class="icon"><i class="fas fa-plus"></i></span><span>Navrhnout místo na mapu</span></a>
</div>
