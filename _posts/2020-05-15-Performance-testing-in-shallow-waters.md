---
layout: post
title: Performance testing in shallow waters
banner : images/banner-pulse-articles5.jpg
date:  2020-05-15
categories:
- wnc
- media
thumbnail: images/pulse-thumbnail-deployment.jpg
---

Acoustic wireless communications have always been very challenging in shallow coastal waters as compared to the deep ocean. This is due to several factors such as multi-path, Doppler due to strong currents, varying bathymetry, etc. It gets even more challenging when you have to share the propagation channel with several marine vessels constantly injecting bubbles into the communication channel.

This is why, we at Subnero, constantly test our underwater acoustic modems in these challenging conditions, to push the limits of what is possible.

During February 2020, we conducted a set of experiments at the [Singapore Strait](https://en.wikipedia.org/wiki/Singapore_Strait), to test the communication range between two of our modems in shallow waters. The goal of the test was to establish a maximum communication range at a given data rate with more than 70% packet success ratio.

![Test setup]({{site.baseurl}}/images/test-setup.jpg){: .center-image  }

We are pleased to announce that the Subnero [M25M series platinum edition modems](https://subnero.com/products/platinum.html) have achieved over 2 km of communication range while configured at a data rate of 1.3 kbps (DATA channel) with a packet success ratio of 70% or more. The average depth of the communication channel was 15m. Both the transmitting and receiving modems were deployed at the mid-water column. However, due to very strong currents, the modems were at an angle of 45° at times. The strong currents also caused the constant motion of the deployment platform and hence a Doppler of up to 4 knots was recorded. This also shows the Doppler resilience of the Subnero modems.

![Strong current displacing the modems]({{site.baseurl}}/images/deployment.png){: .center-image  }

The modems used their OFDM modulation ([DATA channel](https://unetstack.net/handbook/unet-handbook_physical_service.html#_control_and_data_channels)) with a 1/6th rate LDPC setting as the forward error correction method. After transmitting and receiving 5,000 packets in both directions, we were able to conclude a packet success ratio greater than 70%.

### Get in touch
If you would like to know more about Subnero underwater acoustic modems, get in touch with us at sales@subnero.com.
