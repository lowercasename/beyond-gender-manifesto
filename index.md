---
title: Index
layout: default
---
<div class="manifesto-section">
<h1>Beyond Gender Manifesto</h1>
</div>

{% for page in site.pages %}
    {% if page.category == "manifesto" %}
<div class="manifesto-section">
{{ page.content }}
</div>
<div class="parallax-window" data-parallax="scroll" data-image-src="/assets/images/{{ page.order | prepend: '00' | slice: -2, 2 }}.jpg"></div>
    {% endif %}
{% endfor %}
