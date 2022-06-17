---
layout: wide
---


<ul>
    {% for post in site.posts %}
        <li class="row">
            <a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }}</a>
        </li>
        <li class="row">
            <span>{{ post.date | date: "%-d %B %Y" }}</span>
        </li>
        <li class="row">
            <span>{{ post.modified | date: "%-d %B %Y" }}</span>
        </li>
        <li class="row">
            <span>{{ post.description }}</span>
        </li>
        <li class="row">
            <span>{{ post.exerpt }}</span>
        </li>
    {% endfor %}
</ul>

