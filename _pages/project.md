---
layout: page
title: Data Projects
permalink: /projects/
order: 2
---

<div class="container">
  {% if site.posts.size > 0 %}
    {% for post in site.posts %}
    <div class="article" data-aos="fade-up" data-aos-easing="ease-out-quad" data-aos-duration="800">
      {% if post.image %}
      <div class="article__image-box">
        <a href="{{post.url | prepend: site.baseurl}}" class="article__image" style="background-image: url({{site.baseurl}}{{post.image}})"></a>
      </div>
      {% endif %}
      <div class="article__content">
        <h2 class="article__title">
          <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
        </h2>
        <div class="article__meta">
          <span class="article__date">Published <time datetime="{{ post.date | date_to_xmlschema }}">{% assign date_format = site.minima.date_format | default: "%B %-d, %Y" %}{{ post.date | date: date_format }}</time></span>
        </div>
        <p class="article__excerpt">{% if post.description %}{{ post.description }}{% else %}{{ post.content | strip_html | truncate: 130 }}{% endif %}</p>
        {% for tag in post.tags %}
          {% if tag == "testing" %}
            <a href="{{ post.blog }}" class="read-more">Learn More</a>
            {% else %}
            <a href="{{ post.url | prepend: site.baseurl }}" class="read-more">Read the rest</a>
          {% endif %}
        {% endfor %}
      </div>
    </div>
    {% endfor %}
  {% endif %}
</div>
