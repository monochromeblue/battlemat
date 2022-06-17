---
layout: default
---


<ul>
    {% for post in site.posts %}
        <li>
            <a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }}</a>
        </li>
        <li>
            {%- if page.last_modified -%}
                Published: {%- post.date | date: "%-d %B %Y" -%}
                Last updated: {%- post.last_modified | date: "%-d %B %Y" -%}
            {%- else -%}
                Published: {%- post.date | date: "%-d %B %Y" -%}
            {%- endif -%}
        </li>
        <li>
            {%- post.description -%}
        </li>
        <li>
            {%- post.exerpt -%}
        </li>
    {% endfor %}
</ul>