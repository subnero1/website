---
layout: page
title: WNC-M25MSS3
banner : images/banner-silver.jpg
thumbnail : images/thumbnail-wnc-m25mss3.jpg
excerpt: Subnero silver edition modems are the workhorse communication nodes for use in general commercial deployments.
categories: modem
section_id: products
---

## Silver Edition Standalone Configuration Modem

Subnero's silver edition underwater modem is the workhorse communication node to be used in the general commercial deployments. This modem also provides options for customization and extension at many levels, allowing network protocols as well as physical layer algorithms to be implemented and tested easily.

## Key Features

- Up to 15 kbps data rate\*.
- Up to 5 km communication range in tropical waters.
- Ranging functionality with 0.1 m precision.
- Doppler resilience of ±4 knots or better.
- Support for coherent and incoherent communication schemes.
- Support for arbitrary signal transmission as well as recording (passband, baseband).
- Support for user defined communication schemes using [UnetStack]({{ site.baseurl }}{%link products/unet.md %}).
- Support for [multiple receiving channels](./wnc-m25mss3+xch.md) for a variety of applications.

\* Depending on channel conditions and reliability requirements.

<h3><a href="mailto:sales@subnero.com">Contact US for a quote</a></h3>

<div class='full' style='background: #f5f5f5'>

  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-m25mss3.png"/>
    <div class='media-body product product-content'>
    <h3 style="text-transform: none;" id="surface">Standalone Configuration</h3>
        <p>A modem in the standalone configuration (SC) operates on external power source such as a battery (for underwater deployments) or a power supply (for deployments from the water surface).</p>
    </div>
  </div>
</div>

<div class='two spacing'></div>
<div class='wrap-collapsible'>
<h2 style="text-transform: none;" id="s_techspec">TECHNICAL SPECIFICATIONS</h2>
<input id ='tech-specs' class='toggle' type='checkbox'>
<label class='lbl-toggle' for='tech-specs'></label>
<div class='collapsible-content' markdown="1">

### Communication

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Modulation (software defined)          | PSK-OFDM, FH-BFSK                         |
| FEC (Forward Error Correction)         | - LDPC (up to 1/6 rate code)<br>- JANUS (1/2 rate convolution code)|
| JANUS support                          | Yes, subject to operating frequency band  |
| Carrier frequency                      | 24 kHz                                    |
| Bandwidth                              | 12 kHz (20 - 32 kHz)                      |
| Source level                           | 185 dB re 1 µPa @ 1 m rms (nominal)       |

### Software

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Framework                              | [UnetStack]({{ site.baseurl }}{%link products/unet.md %})|
| User Interface                         | Interactive web UI                        |
| Software Interfaces                    | Java, Groovy, Python, C, JavaScript, Julia, Matlab|

### Electrical

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Power supply                           | 22 - 28 VDC (24 VDC recommended)          |
| Power consumption                      | < 4 W (receive mode, nominal)<br>< 60 W (transmit mode, avg.)<br>< 80 W (transmit mode, max.)|
| External interface                     | Ethernet (10/100 Mbps)*                   |
| On-board storage                       | 32 GB*                                    |

### Mechanical

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Hull material                          | Aluminum*                                 |
| Operating depth                        | 100 m*                                    |
| Dimensions                             | ⌀ 127 ✕ 280 mm                            |
| Operating temperature                  | 0 to 40 °C                                |

\* Upgrades available. [Read more](./accessories.md).

</div>
</div>

<div class='wrap-collapsible'>
  <h2>Brochures</h2>
  <input id ='compatibility' class='toggle' type='checkbox'>
  <label class='lbl-toggle' for='compatibility'></label>
  <div class='collapsible-content'>
<div class="brochure-container">
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-Brochure.pdf" target="_blank"><img class="brochure-thumb" src="{{site.baseurl}}/brochures/modem4.jpg"></a>
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-Brochure.pdf" target="_blank">Subnero Underwater Modems</a>
</div>
<div class="brochure-container">
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-Specifications.pdf" target="_blank"><img class="brochure-thumb" src="{{site.baseurl}}/brochures/spec.jpg"></a>
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-Specifications.pdf" target="_blank">Subnero Underwater Modems Technical Specifications</a>
</div>
</div>
</div>
