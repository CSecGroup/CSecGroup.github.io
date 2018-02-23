---
layout: page
title: Blog
---

Blog posted within CSecGroup, listed in reverse chronological order.


{% for tesi in site.data.tesi %}

---

{{ tesi.author }}. {% if tesi.link %}
[{{ tesi.title }}]({{ tesi.link }}). {{ tesi.year }}
{% else %}
{{tesi.title}}. {{ tesi.year }}
{% endif %}

{% if tesi.host %}
Hosted by {{ tesi.host }}
{% endif %}

{% if tesi.pubblications %}
Publications
    {% for pub in tesi.pubblications %}

    {% if pub.link %}
0. [{{ pub.title }}]({{ pub.link }})
    {% else %}
0. {{ pub.title }}
    {% endif %}

    {% endfor %}

{% endif %}

{% endfor %}
