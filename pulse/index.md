---
layout: default
title:  Pulse
banner : images/banner-pulse.jpg
title_color : "#E6782F"
---

<div class ='full tall' style='background-image: url({{site.baseurl}}/{{page.banner}});'>
  <div class='row'>
    <div class='large-12 columns'>
      <!-- {% include section-header.html title=page.title tagline=page.tagline color=page.title_color class="big" %} -->
    </div>
  </div>
  <div class='four spacing'></div>
  <div class='four spacing'></div>
</div>

<div class='full' style='background: #f5f5f5'>
  <div class='row'>
    <h1 class="thin">{{page.title}}</h1>
    <div class='large-12 columns' style='display:flex; flex-wrap:wrap'>
{% for post in site.posts %}
  {% assign isnews = false %}
  {% assign isimage = false %}
  {% if post.external_url != null %}
    {% assign isnews = true %}
  {% endif %}
  {% if post.thumbnail != null %}
    {% assign isimage = true %}
  {% endif %}
  <div class='large-4 columns' id='pulsepage'>
  <div class='mod modBlogPost'>
    <div class='images'>
      {% for image in post.images %}
        <div class='image'><img alt="" src="{{site.url}}/{{image}}" /></div>
      {% endfor %}
    </div>
    <div class='content'>
      <div class='image'>
        <a {% if isnews %}target="_blank"{% endif %} href="{% if isnews %}{{post.external_url}}{% else %}{{site.baseurl}}{{post.url}}{% endif %}">
        <img alt="" src="{% if isimage %}{{site.url}}/{{post.thumbnail}}{% else %}{{site.url}}/{{ site.default_image }}{% endif %}" />
        </a>
      </div>
      <p class='info'>
        <span>{{post.date | date: "%B %d, %Y" }}</span>
      </p>
      <h3 style="text-transform: none;"><a {% if isnews %}target="_blank"{% endif %} href="{% if isnews %}{{post.external_url}}{% else %}{{site.baseurl}}{{post.url}}{% endif %}">{{post.title}}</a></h3>
      
      {% for tag in post.categories %}
        {% capture tag_name %}{{ tag }}{% endcapture %}
        <span class="pulse-tags" >
        <i class="fa fa-tag fa-fw"></i>
        <a href="/tag/{{ tag_name }}">{{ tag_name }}&nbsp;</a>
        </span>
      {% endfor %}
    
      <!-- {% if isnews %}
      <h5 style="text-transform: none;">From <a target="_blank" href="{{post.source}}">{{post.source}}</a> </h5>
      {% else %}
      <p>{{post.excerpt}}</p>
      <a class="button small" href="{{site.baseurl}}{{post.url}}">Read more</a>
      {% endif %} -->
    </div>
  </div>
</div>
{% endfor %}
</div>
</div>
</div>
