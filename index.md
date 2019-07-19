---
title: Index
layout: default
---
<div class="manifesto-section">
<h1>Beyond Gender Manifesto</h1>
{% if site.git.total_commits > 99 %}
    {% assign major_version_number = site.git.total_commits | slice:0 %}
    {% assign minor_version_number = site.git.total_commits | slice:1,2 %}
{% else %}
    {% assign major_version_number = "0" %}
    {% assign minor_version_number = site.git.total_commits %}
{% endif %}
{% assign version = major_version_number | append: "." | append: minor_version_number %}
Version {{version}}.0
</div>

{% for page in site.pages %}
    {% if page.category == "manifesto" %}
<div class="manifesto-section">
{{ page.content }}
</div>
<div class="parallax-window" data-parallax="scroll" data-image-src="/assets/images/{{ page.order | prepend: '00' | slice: -2, 2 }}.jpg"></div>
    {% endif %}
{% endfor %}

<div class="manifesto-section centered">
2019 &middot; [GitHub](https://github.com/lowercasename/beyond-gender-manifesto/) &middot; [Utopian Acts](https://utopia.ac)

Built with [Jekyll](https://jekyllrb.com/) by [Raphael Kabo](https://raphaelkabo.com)
</div>
