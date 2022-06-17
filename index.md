---
layout: default
---


<ul>
    {% for post in site.posts %}
        <li class="row">
            <a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }}</a>
        </li>
        <li class="row">
            <span>{{ post.date }}</span>
        </li>
        <li class="row">
            <span>{{ post.modified }}</span>
        </li>
        <li class="row">
            <span>{{ post.description }}</span>
        </li>
        <li class="row">
            <span>{{ post.exerpt }}</span>
        </li>
    {% endfor %}
</ul>

