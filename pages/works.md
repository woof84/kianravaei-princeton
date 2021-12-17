---
layout: works
sidebar: right
show_meta: false
title: "Works"
subheadline: All
description: Interactive list of works by Kian Ravaei.
permalink: "/works/"
---

<ul class="side-nav">
    {% for post in site.works reversed %}
    {% if post.hide == yes %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{% if post.subheadline %}{{ post.subheadline }} &middot; {% endif %}<span class="works-list-titles">{{ post.title }}</span><br><span class="works-list-descriptions">{{ post.year_composed }} / For {{ post.instrumentation }}</span><span class="works-list-duration">{{ post.duration }}</span></a></li>
    {% endif %}
{% endfor %}
</ul>