---
layout: archive
permalink: /blog/
title: "Random Musings of an aspiring researchers"
author_profile: true
header:
  image: "/images/site/green-chameleon-21532-unsplash.jpg"
---
<!-- Tags used here are the category of the post -->
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}