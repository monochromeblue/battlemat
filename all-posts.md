---
layout: article
permalink: /all-posts/
title: "Monochrome.Blue Index"
date: 2022-06-19 15:16:00 +0100 
modified: 
description: "Site posts directory."
excerpt: 
---

<ul>
    {%- for link in site.data.navigation.main -%}
        <li class="row">
            <a href="{{ link.url | relative_url }}" title="{{ link.description }}">{{ link.title }}</a>
        </li>
    {%- endfor -%}
</ul>

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
        <hr>
    {% endfor %}
</ul>