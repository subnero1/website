---
layout: post
title: WNC-M25MSS3 Silver Edition Standalone Configuration Modem
banner : images/banner-wnc-m25mss3.jpg
thumbnail : images/thumbnail-wnc-m25mss3.jpg
excerpt:
  Silver edition modems are the workhorse communication nodes for use in general commercial deployments
categories: modem
section_id: products
---


WNC-M25MSS3 is a silver edition underwater modem in standalone (gateway) configuration. This modem is the workhorse communication node to be used in the general commercial deployments with larger range and depth-rating when compared to the research edition modem. A modem in the standalone configuration operates on external power source and can be deployed from the surface.  This modem also provides options for customization and extension at many levels, allowing network protocols as well as physical layer algorithms to be implemented and tested easily. The applications can be develeoped using a [simulator]({{ site.baseurl }}{link products/unetsim.md}) before the commercial deployments. The modem runs the [UnetStack]({{ site.baseurl }}{link products/unetstack.md}) underwater networking stack, and provides a wide-range of functionality such as data transmission, navigation, time synchronization, and networked operations.


## Technical specifications

|  Specification                |  Details                                                                             |
| ------------------------------| -------------------------------------------------------------------------------------|
|  **General**                  |                                                                                      |
|  Data rate                    |  0.5 kbps (Control link) Up to 15 kbps (Data link)                                   |
|  Communication range          |  up to 3 km (nominal, depending on channel conditions)                               |
|  Ranging precision            |  0.1 m                                                                               |
|  Doppler precision            |  up to 4 knots                                                                       |
|  Software framework           |  UnetStack (software-defined), www.unetstack.net                                     |
|  **Physical**                 |                                                                                      |
|  Operating depth              |  up to 300 m                                                                         |
|  Housing                      |  Aluminium                                                                           |
|  **Interface**                |                                                                                      |
|  Connectivity                 |  RS232, Ethernet, Acoustic commands                                                  |
|  Software interface           |  UnetStack agents (Java, Groovy, Python), Interactive web UI, Linux sockets, JSON/TCP|
|  **Power**                    |                                                                                      |
|  Power supply                 |  24 VDC (external)                                                                   |
|  **Acoustic**                 |                                                                                      |
|  Carrier frequency            |  24 kHz (typical)                                                                    |
|  Bandwidth                    |  16 kHz (nominal)                                                                    |
|  Source level                 |  max. 185 dB re 1 μPa @ 1 m (rms)                                                    |
|  Modulation (software-defined)|  PSK-OFDM, incoherent OFDM, FH-BFSK, JANUS (subject to operating frequency band)     |


Detailed documentation is available on the [UnetStack documentation page](https://www.unetstack.net/docs.html).
