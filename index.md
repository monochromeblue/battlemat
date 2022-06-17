---
layout: default
---

{% for post in site.posts %}
    {% include article-exerpt.html %}
{% endfor %}
