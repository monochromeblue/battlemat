---
layout: wide
---


<ul>
    {% for post in site.posts %}
        <li class="row">
            <h2><a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }}</a></h2>
        </li>
        <li class="row">
            {% if post.modified %}
                <span>Published: {{ post.date | date: "%-d %B %Y %H:%M" }}, last updated {{ post.modified | date: "%-d %B %Y %H:%M" }}</span> 
            {% else %}
                <span>Published: {{ post.date | date: "%-d %B %Y" }}</span>
            {% endif %}
        </li>
        <li class="row">
            <span>{{ post.excerpt }}</span>
        </li>
    {% endfor %}
</ul>