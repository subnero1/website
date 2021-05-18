---
layout: default
title: Coprocessor
banner : images/banner-electrical.jpg
thumbnail: images/thumbnail-coprocessor.jpg
categories: accessories
excerpt: Co-processor for Subnero underwater modems.
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

<div class='full bg-grey'>
  <div class='row'>
      <div class='accessories'>
        <div class='accessories-img'>
            <div class='mod modBlogPost big'>
              <img id='main-img' src='{{site.baseurl}}/images/accessories-coprocessor01.jpg'>
            </div>
            <div class='modGallery'>
              <div class='media modTeamMember shortcode-list'>
                <div class="member current-li"><a class='image-nav'><img src='{{site.baseurl}}/images/accessories-coprocessor01.jpg'></a></div>
                <div class="member"><a class='image-nav'><img src='{{site.baseurl}}/images/accessories-coprocessor02.jpg'></a></div>
                <div class="member"><a class='image-nav'><img src='{{site.baseurl}}/images/accessories-coprocessor03.jpg'></a></div>
                <div class="member"><a class='image-nav'><img src='{{site.baseurl}}/images/accessories-coprocessor04.jpg'></a></div>
              </div>
            </div>
        </div>
        <div class='accessories-info'>
            <h1>nVidia Jetson TX2</h1>
            <h3>Additional processing module for Subnero underwater modems</h3>
            <ul>
              <li>256-core nVIDIA Pascal™ GPU architecture with 256 nVIDIA CUDA cores</li>
              <li>Dual-Core nVIDIA Denver 2 64-Bit CPU</li>
              <li>8GB 128-bit LPDDR4 Memory</li>
            </ul>
            <a href="mailto:sales@subnero.com"><button type="button">GET A QUOTE</button></a>
        </div>
      </div>
      <hr>
      <div class='wrap-collapsible'>
        <h2> Product Information</h2>
        <input id ='product' class='toggle' type='checkbox'>
        <label class='lbl-toggle' for='product'></label>
        <div class='collapsible-content'>
          <p> While Subnero modems provide flexibility to extend various aspects of the device by the user, there are at times when a customer may want to deploy their applications and algorithms to run with close proximity to the modem hardware. The co-processor option provides a powerful secondary Single Board Computer (SBC) with a Linux distribution connected directly to the modem. This SBC is directly accessible by the user over an IP address in the same subnet as the modem. Once logged into the co-processor, the customer can access the modem over the IP network, using a set of standard Unet APIs that are pre-installed in the co-processor.</p>
          <p><a href="https://subnero.com/wnc/2018/11/17/Underwater-modem-with-a-coprocessor.html">Read more.</a></p>
        </div>
      </div>
      <hr>
      <div class='wrap-collapsible'>
        <h2>Compatibility</h2>
        <input id ='compatibility' class='toggle' type='checkbox'>
        <label class='lbl-toggle' for='compatibility'></label>
        <div class='collapsible-content'>
          <div class="brochure-container">
            <a href="{{site.baseurl}}/products/wnc-m25mss3">WNC-M25MSS3 - Silver Edition Standalone Configuration Modem</a>
          </div>
          <div class="brochure-container">
            <a href="{{site.baseurl}}/products/wnc-m25mse3">WNC-M25MSE3 - Silver Edition Embedded Configuration Modem</a>
          </div>
        </div>
      </div>
  </div>
</div>
{%- include display.html -%}