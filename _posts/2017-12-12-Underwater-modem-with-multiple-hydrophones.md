---
layout: post
title: Multi-channel underwater modem
banner : images/banner-pulse-custommodem.jpg
date:  2017-05-18
categories: wnc
thumbnail: images/pulse-thumbnail-multichannel.jpg
---

The Subnero underwater modems provide options for customization and extension at many levels. For many research applications, multiple synchronized recordings of a received signal from carefully positioned hydrophones are required everytime a signal is detected on the main hydrophone. In order to manage the extra receiving channels, there is an additional analog-to-digital (ADC) convertor integrated in the modem. The second ADC is managed by the UnetStack agent named `adc2`.

At the event of detection of a signal on the main hydrophone, a baseband reception notification message `RxBasebandSignalNtf` is sent by the modem. The customer's script can look for the reception of this notification message and request a recording using the secondary data acquisition system:

```java
if (msg instanceof RxBasebandSignalNtf)
    adc2 << new RecordBasebandSignalReq(recTime: msg.rxTime)
```

The time at which the signal is detected on the main hydrophone is extracted using `msg.rxTime`. The recording time can be set in the past while requesting the recording to synchronize the recorded data from the multi-channel acquisition system with the signal recorded on the main hydrophone.

At the completion of the successful recording, a `RxBasebandSignalNtf` message is received containing the recorded signal:

```java
bbmsg = receive(RxBasebandSignalNtf, 2000)
signal = bbmsg.signal
```

Since the recording is requested on the secondary data acquisition system containing multiple channels, the recorded data stored in `signal` is interleaved.
