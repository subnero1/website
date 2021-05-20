---
layout: post
title: Underwater modem with a secondary data acquisition system
banner : images/banner-pulse-custommodem.jpg
date:  2017-12-12
categories: wnc
thumbnail: images/pulse-thumbnail-multichannel.jpg
---

> This is a legacy product and is now replaced with the [multi-channel modems](https://subnero.com/products/wnc-m25mss3+xch.html). This product is not available for purchase anymore.

The Subnero underwater modems provide options for customization and extension at many levels. For a research application, a customer required 4 synchronized recordings of a received signal from carefully positioned hydrophones, everytime the signal was detected on the main hydrophone. In order to fulfill this requirement, we integrated 4 preamplifiers and a USB-1608G Series high-speed USB data acquisition system in our standard modem. A driver was developed (in C language) for the multi-channel acquisition system. This driver published its data to UnetStack using standard baseband recording messages, so that the customer's software could request these messages.

At the event of detection of a signal on the main hydrophone, a baseband reception notification message `RxBasebandSignalNtf` is sent by the modem. The customer's script can look for the reception of this notification message and request a recording using the secondary data acquisition system:

```java
if (msg instanceof RxBasebandSignalNtf)
    phy << new RecordBasebandSignalReq(adc: 2, recTime: msg.rxTime)
```

The time at which the signal is detected on the main hydrophone is extracted using `msg.rxTime`. The recording time can be set in the past while requesting the recording to synchronize the recorded data from the multi-channel acquisition system with the signal recorded on the main hydrophone.

At the completion of the successful recording, a `RxBasebandSignalNtf` message is received containing the recorded signal:

```java
bbmsg = receive(RxBasebandSignalNtf, 2000)
signal = bbmsg.signal
```

Since the recording is requested on the secondary data acquisition system containing multiple channels, the recorded data stored in `signal` is interleaved.
