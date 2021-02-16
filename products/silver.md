---
layout: page
title: Silver Edition Modems
banner : images/banner-silver.jpg
thumbnail : images/thumbnail-wnc-m25mss3.jpg
excerpt:
  Silver edition modems are the workhorse communication nodes for use in general commercial deployments
categories: modem
section_id: products
---

Subnero's silver edition underwater modem is the workhorse communication node to be used in the general commercial deployments with larger range and depth-rating when compared to the research edition modem. This modem also provides options for customization and extension at many levels, allowing network protocols as well as physical layer algorithms to be implemented and tested easily.

## Key Features

- Up to 15 kbps data rate\*.
- Up to 5 km communication range in tropical waters.
- Doppler resiliance of ±4 knots or better.
- Support for coherent and incoherent communication schemes.
- Support for arbitrary signal transmission as well as recording (passband, baseband).
- Support for user defined communication schemes using [UnetStack]({{ site.baseurl }}{%link products/unet.md %}).
- Support for [multiple receiving channels](./multichannel.md) for a variety of applications.

<div class='one spacing'></div>

## Available Configurations

<div class='full' style='background: #f5f5f5'>
  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-m25mse3.jpg"/>
    <div class='media-body product product-content'>
      <h3 style="text-transform: none;" id="embedded">Embedded Configuration</h3>
      <h4 style="text-transform: none;">WNC-M25MSE3</h4>
      <p>Designed with ease of integration and flexibilty as the primary focus, the embedded configuration (EC) is ideal for integration to bigger platforms such as AUV, ROVs or sensors. Available with pressure hull option for free flodded platforms.</p>
    </div>
  </div>

  <div class ='media product' style='background: #f5f5f5' >   
    <div class='media-body product product-content' style='background: #f5f5f5'>
      <h3 style="text-transform: none;" id="standalone">Standalone Configuration</h3>
      <h4 style="text-transform: none;">WNC-M25MSS3</h4>
      <p>A modem in the standalone configuration (SC) operates on external power source such as a battery (for underwater deployments) or a power supply (for deployments from the water surface).</p>
    </div>
    <img class = "ml-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-m25mss3.png"/> 
  </div>

  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-multichannel2.jpg"/>
    <div class='media-body product product-content'>
      <h3 style="text-transform: none;">Multi-channel Configuration</h3>
      <h4 style="text-transform: none;">WNC-M25MSM3</h4>
      <p>Subnero's multi-channel configuration enables a variety of applications such as synchronized acoustic recording, exploitation of spatial diversity as well as underwater positioning (e.g. USBL). <a href="{{site.baseurl}}/products/multichannel.html" target="_blank">Read more.</a></p>
    </div>
  </div>

</div>

<div class='two spacing'></div>

<h2 style="text-transform: none;" id="s_techspec">+ TECHNICAL SPECIFICATIONS</h2>

### Acoustics

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Data rate                              | Up to 15 kbps*                            |
| Operating range                        | 3-5 km (nominal, depending on channel conditions)|
| Ranging precision                      | 0.1 m                                     |
| Doppler resilience                     | ±4 knots or better                        |
| Modulation (software defined)          | PSK-OFDM, FH-BFSK                         |
| FEC (Forward Error Correction)         | - LDPC (up to 1/6 rate code)<br>- JANUS (1/2 rate convolution code)|
| JANUS support                          | Yes, subject to operating frequency band  |
| Carrier frequency                      | 24 kHz                                    |
| Bandwidth                              | 12 kHz (20 - 32 kHz)                      |
| Source level                           | 185 dB re 1 µPa @ 1 m rms (nominal)       |
| Beam pattern                           | Omnidirectional                           |

\*(depending on channel conditions and reliability requirements)


### Software

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Framework                              | [UnetStack]({{ site.baseurl }}{%link products/unet.md %})|
| User Interface                         | Interactive web UI                        |
| Software Interfaces                    | Java, Groovy, Python, C, Javascript, Julia, Matlab|

Visit [www.unetstack.net](http://www.unetstack.net) for more details.

### Electrical

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Power source                           | 22 - 28 VDC (24 VDC recommended)          |
| Power consumption                      | < 4 W (receive mode, nominal)<br>< 60 W (transmit mode, avg.)<br>< 80 W (transmit mode, max.)|
| Supported interfaces                   | Ethernet, RS232 (optional)                |
| Onboard storage                        | 32 GB (upgradable up to 1 TB)              |

- Supported battery pack details available [here](./batterypack.md).


### Mechanical

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Hull material                          | Aluminium                                 |
| Operating depth                        | Hull: 100 m<br> Transducer: 2000 m*       |
| Dimensions                             | SC: ⌀ 127 ✕ 280 mm<br> EC: ⌀ 105 ✕ 150 mm |
| Weight                                 | SC: 4.0 / 1.0 kg (air / water)<br> EC: 1.0 kg (air)|


### Additional features

| Feature                                | Details                                   |
| -------------------------------------- | ----------------------------------------- |
| Wake-up support                        | Ethernet, RS232 (optional), Acoustic (optional) |
| Arbitary waveform transmission         | Supported                                 |
| Raw waveform reception - passband      | Supported                                 |
| Raw waveform reception - baseband      | Supported                                 |

- Optional upgrades and accessories are available [here](./accessories.md).


## TODO: Contact US for a quote


<h2>Brochures</h2>
<div class="brochure-container">
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-v4.0.pdf"><img class="brochure-thumb" src="{{site.baseurl}}/brochures/modem4.jpg"></a>
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-v4.0.pdf" target="_blank">Subnero Underwater Modems</a>
</div>
<div class="brochure-container">
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-Specifications-v4.0.pdf"><img class="brochure-thumb" src="{{site.baseurl}}/brochures/spec.jpg"></a>
  <a href="{{site.baseurl}}/brochures/Subnero-Modem-Specifications-v4.0.pdf" target="_blank">Subnero Underwater Modems Technical Specifications</a>
</div>

## + Useful Links
- TODO