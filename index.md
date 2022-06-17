---
layout: default
---


<ul>
    {% for post in site.posts %}
        <li class="row">
        <a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }} 1</a>
        </li>
        <li class="row">
        <a href="{{ post.url }}" title="{{ post.description }}">{{ post.title }} 2</a>
        </li>
    {% endfor %}
</ul>