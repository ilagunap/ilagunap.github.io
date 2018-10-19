---
layout: page
title: Publications
permalink: /papers/
---

**Conference Papers**

{% assign len = 0 %}

<ol>
{% for p in site.data.papers %}
{% if p.type == "conf" %}
    {% assign len = len | plus: 1 %}
    <li>
        <b>[{{p.pub}}]</b> {{p.authors}}. <a href="{{p.url}}"> {{p.title}} </a>. {{p.venue}}.
    </li> <br />
{% endif %}
{% endfor %}
</ol>

{% assign len = len | plus: 1 %}

**Journal Papers**

<ol start="{{len}}">
{% for p in site.data.papers %}
{% if p.type == "journal" %}
    {% assign len = len | plus: 1 %}
    <li>
        <b>[{{p.pub}}]</b> {{p.authors}}. <a href="{{p.url}}"> {{p.title}} </a>. {{p.venue}}.
    </li> <br />
{% endif %}
{% endfor %}
</ol>

**Workshop Papers**

<ol start="{{len}}">
{% for p in site.data.papers %}
{% if p.type == "workshop" %}
    <li>
        <b>[{{p.pub}}]</b> {{p.authors}}. <a href="{{p.url}}"> {{p.title}} </a>. {{p.venue}}.
    </li> <br />
{% endif %}
{% endfor %}
</ol>

