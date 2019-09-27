---
layout: default
title: Subnero M2M series modems
banner : images/banner-modem.jpg
thumbnail: images/boxart-modem.jpg
categories: underwatermodem
section_id: products
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

<!--<div class='full' style='background:#F5F5F5'>-->
<div class='cGBxoB'>
<section class='bsPRnx'>
	<h1 class='thin' style='text-align: center'>Subnero M2M series modems</h1>
	<div class='eyXpDN'>
		<div class='cmXrEt'>
			<h1 class='thin' style='text-align: center'>Platinum Edition</h1>
			<ul class="gfXsQG">
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","modem" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Platinum Edition Modems" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}#surface"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25mps3.jpg" />
				          	<div class='content'>
				            <h3 style="text-transform: none;">Surface Configuration</h3>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","modem" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Platinum Edition Modems" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}#title"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25mpe3.jpg" />
				          	<div class='content'>
				            <h3 style="text-transform: none;">Embedded Configuration</h3>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA"></li>
			</ul>
		</div>
		<div class='cmXrEt'>
			<h1 class='thin' style='text-align: center'>Silver Edition</h1>
			<ul class="gfXsQG">
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","modem" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Silver Edition Modems" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}#title"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25msn3.jpg" />
				          	<div class='content'>
				            <h3 style="text-transform: none;">Node Configuration</h3>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","modem" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Silver Edition Modems" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}#surface"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25mss3.jpg" />
				          	<div class='content'>
				            <h3 style="text-transform: none;">Surface Configuration</h3>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","modem" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Silver Edition Modems" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}#embedded"><img alt="" src="{{site.baseurl}}/images/thumbnail-wnc-m25mse3.jpg" />
				          	<div class='content'>
				            <h3 style="text-transform: none;">Embedded Configuration</h3>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
			</ul>
		</div>
		<div class='cmXrEt'>
			<h1 class='thin' style='text-align: center'>Research Edition</h1>
			<ul class="gfXsQG">
				<li class="fuqHMA"></li>
				<li class="fuqHMA">
					<div class="hOXnHC">
						{% assign product_pages = site.pages | where:"categories","modem" %}
  						{% for page in product_pages %}
  						{% if page.title contains "Research Edition Modems" %}
				        <div class='mod modBlogPost'>
				        	<a href="{{site.baseurl}}{{page.url}}"><img alt="" src="{{site.baseurl}}/{{page.thumbnail}}" />
				          	<div class='content'>
				            <h3 style="text-transform: none;">Surface Configuration</h3>
				          </div></a>
				        </div>
				        {% endif %}
				        {% endfor %}
					</div>
				</li>
				<li class="fuqHMA"></li>
			</ul>
		</div>
		<div class='cmXrEt'>
			{% assign product_pages = site.pages | where:"categories","solutions" %}
			{% for page in product_pages %}
			{% if page.title contains "Solutions" %}
            <h1 class='thin' style='text-align: center'>Subnero Customized Solutions <p><a href="{{site.baseurl}}{{page.url}}#customized-solutions" style="text-transform: none;">[View details..]</a></p>
            </h1>
            {% endif %}
			{% endfor %}
		</div>
	</div>
</section>
</div>