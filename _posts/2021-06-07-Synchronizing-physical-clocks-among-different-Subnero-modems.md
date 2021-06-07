---
layout: post
title: Synchronizing physical clocks among different Subnero modems
banner : images/banner-pulse-synchronization.jpg
date:  2021-06-07
categories: wnc
thumbnail: images/pulse-thumbnail-modems.jpg
---

All Subnero modems have a “real-time clock” to keep track of time using a precise quartz crystal. Based on the defined frequency of this quartz, software running on the modem can precisely monitor the internal time. When the modem connects to the network (Internet), the software running on the modem then contacts a timer server, which is equipped with a UTC receiver or an accurate clock, to accurately reset the local timer using Network Time Protocol, also called NTP.

Although this frequency of the crystal quartz is reasonably stable, it is impossible to guarantee that all the crystals of different computers will operate at exactly the same frequency. A crystal oscillator is an electronic circuit that uses the mechanical resonance of a vibrating piezoelectric crystal to create an electrical signal with a desired frequency. The resonant frequency depends on size, shape, elasticity, and the speed of sound in the material. Due to manufacturing tolerences, these properties are not exactly identical across manufactured crystals, and so different crystals designed for the same nominal frequency produce slightly different frequency signals. Furthermore, as the operating temperature of the crystal changes, its material properties change, and so does its resonant frequency. These differences in frequency are tiny, but over long periods of time, the differences accumulate and cause the clocks to drift.

Under this circumstance, it is not easy for having multiple spatially separated modems with synchronized physical clocks. If the usage of multiple internal physical clocks is desirable, how do we synchronize them with each other?

![Clock offset between two modems]({{site.baseurl}}/images/clcok-offset.png){: .center-image  }

