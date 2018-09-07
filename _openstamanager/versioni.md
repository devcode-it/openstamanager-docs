---
title: Versioni
pagination: false
description: An appendix of hosted documentation for nearly every release of Bootstrap, from v1 through v4.
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
        {% if version.v == site.docs-version %}
        <a class="list-group-item list-group-item-action py-2 text-primary d-flex justify-content-between align-items-center" href="{{ site.baseurl }}/openstamanager/{{ version.v }}/">
            {{ version.v }}
            <span class="badge badge-primary">Latest</span>
        </a>
        {% else %}
        <a class="list-group-item list-group-item-action py-2 text-primary" href="{{ site.baseurl }}/openstamanager/{{ version.v }}/">
            {{ version.v }}
        </a>
        {% endif %}
    </li>
    {% if forloop.last %}</ul>{% endif %}
    {% endfor %}
</div>
{% endfor %}