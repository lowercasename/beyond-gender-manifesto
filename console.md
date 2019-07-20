---
title: Console
layout: default
---
<div id="flash"></div>
<div class="console crt">
<p>Welcome to the Beyond Gender Information Systems Terminal (C) 2019 Beyond Gender Collective</p>
<div id="intro">
</div>
<div id="text">
<h1 class="glitch" data-text="BEYOND GENDER MANIFESTO">Beyond Gender Manifesto</h1>
{% if site.git.total_commits > 99 %}
    {% assign major_version_number = site.git.total_commits | slice:0 %}
    {% assign minor_version_number = site.git.total_commits | slice:1,2 %}
{% else %}
    {% assign major_version_number = "0" %}
    {% assign minor_version_number = site.git.total_commits %}
{% endif %}
{% assign version = major_version_number | append: "." | append: minor_version_number %}
Version {{version}}.0

================================================================================

{% for page in site.pages %}
    {% if page.category == "manifesto" %}
<div class="console-section">
{{ page.content }}
</div>
    {% endif %}
{% endfor %}

</div>
