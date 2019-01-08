---
layout: page
---

<div id="archives">
{% assign categories = site.categories | sort %}
{% for category in categories %}
  {% capture category_name %}{{ category | first }}{% endcapture %} 
  {% if category_name == page.lang %}
    {% continue %}
  {% endif %}
  {% assign ignore_category = true %}
  {% for post in site.categories[category_name] %}
    {% if post.lang == page.lang %}
      {% assign ignore_category = false %}
      {% break %}
    {% endif %}
  {% endfor %}
  {% if ignore_category %}
    {% continue %}
  {% endif %}
  <div class="archive-group">   
    <h3 class="category-head" id="{{ category_name | slugize }}">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    {% if post.lang != page.lang %}
      {% continue %}
    {% endif %}
    <article class="archive-item">
      <h4><a href="{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>