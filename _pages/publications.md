---
layout: archive
title: "Papers"
permalink: /publications/
---

{% comment %} Edit the list in _data/publications.yml. {% endcomment %}
{% assign years = site.data.publications | group_by: "year" %}
{% for year in years %}
<h2 class="pub-year">{{ year.name }}</h2>
<ol class="pub-list">
{% for pub in year.items %}{% include publication.html pub=pub %}{% endfor %}
</ol>
{% endfor %}

{% if site.author.googlescholar %}
You can also find my articles on <u><a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.</u>
{% endif %}
