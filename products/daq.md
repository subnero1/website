---
layout: default
title: Underwater acoustic data acquisition system
banner : images/banner-pulse-custommodem.jpg
thumbnail: images/boxart-wnc-arecorder.jpg
categories: daq
section_id: products
excerpt: Subnero's underwater acoustic modems with multiple channels for high-speed data acquisition.
---

<div class='full tall' style='background-image: url({{site.baseurl}}/{{page.banner}});'>
  <div class='row'>
    <div class='large-12 columns'>
    </div>
  </div>
  <div class='four spacing'></div>
  <div class='four spacing'></div>
</div>

<div class='cGBxoB'>
<section class='bsPRnx'>
    <h1 class='thin' style='text-align: center'>Subnero acoustic data acquisition</h1>
    <div class='eyXpDN'>
        <div class='cmXrEt'>
            <h1 class='thin' style='text-align: center'>Multi-channel Edition</h1>
            <ul class="gfXsQG">
                <li class="fuqHMA">
                    <div class="hOXnHC">
                        {% assign product_pages = site.pages | where:"categories","wnc" %}
                        {% for page in product_pages %}
                        {% if page.title contains "Underwater acoustic modem with a secondary data acquisition system" %}
                        <div class='mod modBlogPost'>
                            <a href="{{site.baseurl}}{{page.url}}"><img alt="" src="{{site.baseurl}}/{{page.thumbnail}}" />
                            <div class='content'>
                            <h2>Multi-channel modem for high-speed data acquisition system</h2>
                            </div>
                            </a>
                        </div>
                        {% endif %}
                        {% endfor %}
                    </div>
                </li>
                <li class="fuqHMA">
                    <div class="hOXnHC">
                        {% assign product_pages = site.pages | where:"categories","sensors" %}
                        {% for page in product_pages %}
                        {% if page.title contains "Subnero underwater acoustic recorder (aRecorder)" %}
                        <div class='mod modBlogPost'>
                            <a href="{{site.baseurl}}{{page.url}}"><img alt="" src="{{site.baseurl}}/{{page.thumbnail}}" />
                            <div class='content'>
                            <h2>aRecorder with mutiple hydrophones and sensors</h2>
                          </div></a>
                        </div>
                        {% endif %}
                        {% endfor %}
                    </div>
                </li>
            </ul>
        </div>
    </div>
</section>
</div>