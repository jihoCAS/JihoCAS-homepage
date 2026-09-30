---
title: Aktuality
subtitle: Novinky z pobočky a pozvánky na akce
permalink: /aktuality/
hero_height: is-small
---

<div class="columns is-multiline">
{% for post in site.posts %}
  <div class="column is-12">
    <div class="card jc-card">
      <div class="card-content">
        <p class="has-text-grey is-size-7">{{ post.date | date: '%-d. %-m. %Y' }}</p>
        <p class="title is-5"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></p>
        <div class="content">{{ post.summary | default: post.excerpt | strip_html | truncatewords: 40 }}</div>
      </div>
    </div>
  </div>
{% endfor %}
</div>

<p><span class="icon"><i class="fas fa-rss"></i></span> <a href="{{ '/feed.xml' | relative_url }}">Odebírat aktuality přes RSS</a></p>
