---
layout: default
---


<ul>
    {% for post in site.posts %}
        <li class="row">
        <a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }}</a>
        </li>
        <li class="row">
        <span>
        {%- if post.last_modified -%}
            Published: {%- post.date | date: "%-d %B %Y" -%}
            Last updated: {%- post.last_modified | date: "%-d %B %Y" -%}
        {%- else -%}
            Published: {%- post.date | date: "%-d %B %Y" -%}
        {%- endif -%}
        </span>
        </li>
        <li class="row">
        <span>{{ post.description }}</span>
        </li>
        <li class="row">
        <span>{{ post.exerpt }}</span>
        </li>
    {% endfor %}
</ul>

