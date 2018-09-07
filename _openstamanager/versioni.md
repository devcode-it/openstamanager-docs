---
title: Versioni
permalink: /openstamanager/versioni/
description: Elenco della documentazione per versione di OpenSTAManager.
sidebar:
    nav: none
---
{% assign versions = site.data.versions | reverse %}

{% for release in versions %}
<div>
    <h1>{{ release.group }}</h1>
    <p>{{ release.description }}</p>
    {% for version in release.versions %}
    {% if forloop.first %}<ul>{% endif %}
    <li>
        <a href="{{ site.baseurl }}/openstamanager/{{ version.v }}/">
            {{ version.v }}
        </a>
        {% if version.v == site.docs-version %}
        <span class="btn btn--primary">Ultima release</span>
        {% endif %}
    </li>
    {% if forloop.last %}</ul>{% endif %}
    {% endfor %}
</div>
{% endfor %}