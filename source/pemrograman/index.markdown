---
layout: page
title: "pemrograman"
---

<div id="blog-archives" class="category">
{% for post in site.categories.pemrograman %}
{% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% unless year == this_year %}
  {% assign year = this_year %}
  <h2>{{ year }}</h2>
{% endunless %}
<article>
  {% include page_post.html %}
</article>
{% endfor %}
</div>
