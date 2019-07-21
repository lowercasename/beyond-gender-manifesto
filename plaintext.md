---
title: Beyond Gender Manifesto - Plaintext
layout: plain
---
<!-- <div id="display"> -->
<!-- {% include intro.html %} -->
<div id="plain-text">
<h1 data-text="BEYOND GENDER MANIFESTO">Beyond Gender Manifesto</h1>
{% if site.git.total_commits > 99 %}
    {% assign major_version_number = site.git.total_commits | slice:0 %}
    {% assign minor_version_number = site.git.total_commits | slice:1,2 %}
{% else %}
    {% assign major_version_number = "0" %}
    {% assign minor_version_number = site.git.total_commits %}
{% endif %}
{% assign version = major_version_number | append: "." | append: minor_version_number %}
Version {{version}}.0

<hr>

{% for page in site.pages %}
{% if page.category == "manifesto" %}
{{ page.content }}
{% endif %}
{% endfor %}

</div>
<!-- </div> -->
