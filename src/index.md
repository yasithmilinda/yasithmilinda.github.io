---
layout: default
---

{%- if page.title -%}
  <h1 class="page-heading">{{ page.title }}</h1>
{%- endif -%}

<header style="display: flex; align-items: flex-start; margin-bottom: 1em;">
  <div style="width: 10em; height: 10em; padding: 0.5em; margin-left: 0; padding-left: 0;">
    <img style="width: 100%; height: 100%;" src="{{ site.data.info.image | relative_url }}">
  </div>
  <div style="padding: 0.5em;">
    <div style="font-size: 1.5em;">{{ site.data.info.name }}</div>
    <div style="font-size: 1.2em;">{{ site.data.info.designation }}</div>
    <address>
    {% for line in site.data.info.address %}
    {{ line }}<br/>
    {% endfor %}
    </address>
    <a href="mailto:{{ site.data.info.email }}">{{ site.data.info.email }}</a>
  </div>
</header>

<section style="text-align: justify;">
{{ site.data.info.about }}
</section>