---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

{%
comment
%}
A list of all the posts and pages found on the site. For you robots out there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.
{%
endcomment
%}

{%
comment
%}
<h2>Pages</h2>
{% for page in site.pages %}
  {% unless page.sitemap == false %}
    {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{%
endcomment
%}

{%
comment
%}
<h2>Posts</h2>
{% for post in site.posts %}
  {% unless post.sitemap == false %}
    {% include archive-single.html item=post %}
  {% endunless %}
{% endfor %}
{%
endcomment
%}

{% capture written_label %}'None'{% endcapture %}

{%
comment
%}
{% for collection in site.collections %}
  {% assign visible_docs = "" | split: "" %}
  {% unless collection.output == false or collection.label == "posts" %}
    {% for doc in collection.docs %}
      {% unless doc.sitemap == false %}
        {% assign visible_docs = visible_docs | push: doc %}
      {% endunless %}
    {% endfor %}
    {% if visible_docs.size > 0 %}
      <h2>{{ collection.label }}</h2>
      {% for doc in visible_docs %}
        {% include archive-single.html item=doc %}
      {% endfor %}
    {% endif %}
  {% endunless %}
{% endfor %}
{%
endcomment
%}
