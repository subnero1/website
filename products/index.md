---
layout: default
title: Products
banner : images/banner-products.jpg
excerpt: Subnero's underwater acoustic modems with UnetStack for underwater wireless communication and networking and SWAN for real-time water-quality monitoring.
---
<div class='full tall' style='background-image: url({{site.baseurl}}/{{page.banner}});'>
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
    <h1 class='thin'>PRODUCTS</h1>

  {% assign product_pages = site.pages | where:"categories","underwatermodem" %}
  {% for page in product_pages %}
  <a href="{{site.baseurl}}{{page.url}}">
  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/{{page.thumbnail}}"/>    
    <div class='media-body product product-content'>
    <h3 class="mt-0" style="text-transform: none;">Wireless Networked Communications</h3>
    <p>Software defined underwater acoustic modems for networking, navigation and sensing.</p>
    </div>
  </div>
  </a>
  {% endfor %}

  {% assign product_pages = site.pages | where:"categories","unet" %}
  {% for page in product_pages %}
  <a href="{{site.baseurl}}{{page.url}}">
  <div class ='media product' style='background:#F5F5F5;'>      
    <div class='media-body product product-content' style='background:#F5F5F5'>
    <h3 style="text-transform: none;">Underwater Network Stack & Simulator</h3>
    <p>An agent-based software stack and simulator for underwater networks.</p>
    </div>
    <img class='ml-3' alt="" src="{{site.baseurl}}/{{page.thumbnail}}"/>
  </div>
  </a>

  {% endfor %}

  {% assign product_pages = site.pages | where:"categories","water-quality-management" %}
  {% for page in product_pages %}
  <a href="{{site.baseurl}}{{page.url}}">
  <div class ='media product'>
    <img class='align-self-start mr-3' alt="" src="{{site.baseurl}}/{{page.thumbnail}}"/>      
     <div class='media-body product product-content'>
    <h3 style="text-transform: none;">Water Quality Monitoring</h3>
    <p>Scalable automous platforms for in-situ water quality measurements.</p>
    </div>
  </div>
  </a>
    {% endfor %}
<div class='four spacing'></div>
</div>
</div>
