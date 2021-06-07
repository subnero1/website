---
layout: post
title: Synchronizing physical clocks among different Subnero modems
banner : images/banner-pulse-synchronization.jpg
date:  2021-06-07
categories: wnc
thumbnail: images/pulse-thumbnail-modems.jpg
---

All Subnero modems have a “real-time clock” to keep track of time using a precise quartz crystal. Based on the defined frequency of this quartz, software running on the modem can precisely monitor the internal physical time given by parameter `phy.time` in Subnero modem.

Although this frequency of the crystal quartz is reasonably stable, it is impossible to guarantee that all the crystals of different modems will operate at the same frequency. A crystal oscillator is an electronic circuit that uses the mechanical resonance of a vibrating piezoelectric crystal to create an electrical signal with the desired frequency. The resonant frequency depends on size, shape, elasticity, and the speed of sound in the material. Due to manufacturing tolerances, these properties are not identical across manufactured crystals, and so different crystals designed for the same nominal frequency produce slightly different frequency signals. Furthermore, as the operating temperature of the crystal changes, its material properties change, and so does its resonant frequency. These differences in frequency are tiny, but over long periods, the differences accumulate and cause the clocks to drift.

Under this circumstance, it is not easy for having multiple spatially separated modems with synchronized physical clocks. If the synchronization of physcial clocks across different Subnero modems is needed, how do we synchronize them with each other?

There are two major problems to be addressed to synchronize clocks among different modems:

1. Modems start at different times so there may be a *clock offset* as shown in figure below:

![Clock offset between two modems]({{site.baseurl}}/images/clock-offset.png){: .center-image }

2. Modem clocks tick at different rates causing a *clock drift* as shown in figure below:

![Clock drift between two modems]({{site.baseurl}}/images/clock-drift.png){: .center-image }


# Compensating for clock offset in Subnero modems

`Ranging` agent in UnetStack running on Subnero modem generates the clock offset information based on the message exchanges when range measurement is performed on the modem that initiates ranging. The clock offset between the two modems is populated in the ranging agent's parameter `ranging[host('B')].offset`. Where `host('B')` is the node address of modem B. More details on this can be found ![here](https://unetstack.net/handbook/unet-handbook_ranging_and_synchronization.html). 

Once, the clock offset is known, it can be used to adjust the time locally to synchronize the physical time (`phy.time`). However, if a low-drift clock is not used, there is a possibility that the clocks tick at different rates, and clocks drift faster. Let us take a look at how we can compensate for the clock drift next.

> NOTE: Subnero also provides ![low-drift clock](https://subnero.com/products/sensors.html) as an optional upgrade to the modem for users who require a low drift clock. These clocks provide much lower drift and are suitable for such applications where time synchronization is critical.

# Compensating for clock drift in Subnero modems

Since the modems might tick at different rates, one modem's clock may be faster than the other. An example is shown in the figure above where Modem A's clock is faster than Modem B, i.e., a slope of 1.2 on Modem A's clock. To compensate for this, the user of the modem can utilize a `phy.clockCalib` parameter. This parameter is a multiplier on the physical clock. So its default value is 1. If you set it to 1.2 the clock will run at 1.2x the rate of the actual hardware clock.

Therefore, to compensate Modem A's clock to run slower so that it matches Modem B's clock, we can set `phy.clockCalib = 1/1.2 = 0.83`.


The users of the modem should make measurements to figure out the nomimal values that they should set for `phy.clockCalib`. 

