---
layout: default
title: Subnero Modem Accessories
banner : images/banner-modem.jpg
thumbnail: images/boxart-modem.jpg
categories: accessories
section_id: products
excerpt: Subnero's software-defined underwater acoustic modems for underwater wireless communication and networking. Subnero's multi-channel modems for data acquisition.
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

<div class='cGBxoB'>
<section class='bsPRnx'>
	<h1 class='thin' style='text-align: center'>Optional Accessories and Upgrades</h1>
	<div class='eyXpDN'>
		<div class='cmXrEt'>
			<ul class="gfXsQG">
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","accessories" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Battery Packs" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25mps3.jpg" />
				          	<div class='content'>
				            <h2>Battery Packs</h2>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","accessories" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Coprocessor" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}#embedded"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25mpe3.jpg" />
				          	<div class='content'>
				            <h2>Coprocessors</h2>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA"></li>
			</ul>
		</div>
	</div>
</section>
</div>
