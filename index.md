---
layout: wide
---


<ul>
    {% for post in site.posts %}
        <li class="row">
            <a href="{{ post.permalink }}" title="{{ post.description }}">{{ post.title }}</a>
        </li>
        <li>
            {% if post.modified %}
                <span>{{ post.date | date: "%-d %B %Y" }} and {{ post.modified | date: "%-d %B %Y" }}</span> 
            {% else %}
                <span>{{ post.date | date: "%-d %B %Y" }}</span>
            {% endif %}
        </li>
        <li class="row">
            <span>{{ post.description }}</span>
        </li>
        <li class="row">
            <span>{{ post.excerpt }}</span>
        </li>
    {% endfor %}
</ul>