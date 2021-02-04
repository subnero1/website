---
layout: page
title: Modems with multiple receiving channels
banner : images/banner-multichannel.jpg
thumbnail : images/thumbnail-wnc-multichannel.jpg
excerpt:
  Subnero's underwater acoustic modems with multiple channels for high-speed data acquisition.
categories: wnc
section_id: products
---
​
The Subnero underwater modems provide options for customization and extension at many levels. For many applications, it is often a requirement to record synchronized signals from multiple hydrophones in addition to the regular communication channel. Our modems with multiple receiving channels provide this capability thereby enabling a new range of applications

<div id="embedded"></div>
<div class='full' style='background: #f5f5f5'>

  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-multichannel2.jpg"/>    
    <div class='media-body product product-content'>
    <h3 style="text-transform: none;" id="surface">USBL Ready</h3>
          <!-- <h4 style="text-transform: none;">WNC-M25MPE3</h4> -->
          <p>A modem in the surface configuration operates on external power source and can be deployed from the surface.</p>
    </div>
  </div>
  <div class ='media product' style='background: #f5f5f5' >   
    <div class='media-body product product-content' style='background: #f5f5f5'>
    <h3 style="text-transform: none;">Exploit Spatial Diversity</h3>
          <!-- <h4 style="text-transform: none;">WNC-M25MPS3</h4> -->
          <p>A modem in the surface configuration operates on external power source and can be deployed from the surface.</p>
    </div>
    <img class = "ml-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-multichannel1.png"/> 
  </div>
</div>

<div class='two spacing'></div>

​
## Use it as a recorder using multiple hydrophones

With option to customize the number of additional channels, these devices provide unparalleled - "TODO"

Every time a signal is detected on the main hydrophone/transducer a recording can be triggered on all the hydrophones.
​
 This driver publishes its data to UnetStack using standard baseband recording messages, so that the customer’s software could request these messages. At the event of detection of a signal on the main hydrophone, a baseband reception notification message `RxBasebandSignalNtf` is sent by the modem. The customer’s script can look for the reception of this notification message and request a recording using the secondary data acquisition system.
​
## Use it to build USBL based navigation system
​
The ability to record using multiple hydrophones enables us to develop high resolution ultra short baseline (USBL) acoustic navigation system to provide an accurate range and bearing estimates to an underwater target (e.g., an acoustic transponder). The multiple hydrophones can be conveniently positioned to form a desired receiver array geometry. The arrival times (and resulting phase) of the signals on these hydrophones slightly differ based on the array geometry and can be used to estimate the direction of arrival. This technique is used for estimating the bearing of the target/source node such as an acoustic transponder. Note that this system also allows communication with other underwater assets with an acoustic modem since the USBL system is built with just a software customization of the multi-channel modem.
​
​
## Use it as a spatial diversity enabled receiver modem
​
Received signal recordings on multiple hydrophones may differ due to a different channel that each of them might experience. Since the received signals on all hydrophones may differ; an attempt to decode might result in a different result. Some of them might get decoded correctly and some might result in bit errors. It is also possible that all of the received signals get decoded to result in errors which cannot be corrected. However, the power of selection diversity and diversity combining comes into play here. Utilizing the flexibility of UnetStack, we can immediately publish a successfully decoded frame from one of the hydrophones to be consumed by user. And if none of the hydrophones and main transducer of the modem is able to successfully decode the signal, all of them can be optimally combined and fed to the decoder to potentially decode the frame.


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
