---
layout: wide
---
<section>
{% for post in site.posts limit:1 %}
    {{ post.content }}
{% endfor %}
</section>

<ul>
    {% for post in site.posts offset:1 limit:3 %}
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
        <hr>
    {% endfor %}
</ul>
