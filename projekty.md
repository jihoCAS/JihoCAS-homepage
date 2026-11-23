---
description: "Rozcestník projektů JihoČASu: radiová síť Bolidozor, pozorování Slunce, meteorů a bolidů, radioastronomie a další aktivity pobočky."
title: Projekty a aktivity
subtitle: Rozcestník pozorovacích programů JihoČASu
permalink: /projekty/
hero_height: is-small
---

Na projektech se podílejí členové pobočky i spolupracující hvězdárny. Pokud se chcete zapojit, [napište nám]({{ '/kontakt/' | relative_url }}).

<div class="columns is-multiline mt-4">
{% assign projekty = site.projekty | sort: "order" %}
{% for p in projekty %}
  {% include karta.html title=p.title subtitle=p.subtitle icon=p.icon text=p.summary url=p.url width="is-6-tablet is-6-desktop is-3-fullhd" %}
{% endfor %}
</div>

## Další aktivity

<div class="columns is-multiline">
  {% include karta.html title="Astrofotografie" icon="fa-camera-retro" text="Někteří členové se věnují fotografování noční oblohy a objektů na ní." width="is-6" %}
  {% include karta.html title="Časopis JihoČAS" icon="fa-newspaper" text="Zpravodaj pobočky s články a výsledky pozorování." url="/casopis/" width="is-6" %}
</div>
