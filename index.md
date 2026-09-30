---
title: JihoČAS
subtitle: Jihočeská pobočka České astronomické společnosti
callouts: home_callouts
hero_link: /o-nas/
hero_link_text: Kdo jsme
---

## Vítejte u JihoČASu

Jsme jihočeská pobočka [České astronomické společnosti](https://www.astro.cz/). Sdružujeme zájemce o astronomii z jižních Čech, amatérské pozorovatele i pracovníky hvězdáren. Věnujeme se **popularizaci astronomie**, **pozorovacím programům** (sluneční aktivita, meteory, radioastronomie) a **vzdělávání**.

<div class="columns is-multiline mt-4">
{% assign projekty = site.projekty | sort: "order" %}
{% for p in projekty %}
  {% include karta.html title=p.title subtitle=p.subtitle icon=p.icon text=p.summary url=p.url width="is-6-tablet is-6-desktop is-3-fullhd" %}
{% endfor %}
</div>

## Aktuality

<ul>
{% for post in site.posts limit:3 %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> <span class="has-text-grey">({{ post.date | date: "%-d. %-m. %Y" }})</span></li>
{% endfor %}
</ul>

[Všechny aktuality →]({{ '/aktuality/' | relative_url }})
