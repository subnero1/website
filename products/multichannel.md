---
layout: page
title: Subnero Multi-Channel Modems
banner : images/banner-multichannel.jpg
thumbnail : images/thumbnail-wnc-multichannel.jpg
excerpt:
  Subnero's underwater acoustic modems with multiple channels for high-speed data acquisition.
categories: wnc
section_id: products
---
​
The Subnero underwater modems provide options for customization and extension at many levels. For many applications, it is often a requirement to record synchronized signals from multiple hydrophones in addition to the regular communication channel. Our modems, with multiple receiving channels provide this capability thereby enabling a new range of applications.

<div id="embedded"></div>
<div class='full' style='background: #f5f5f5'>

  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-multichannel2.jpg"/>    
    <div class='media-body product product-content'>
    <h3 style="text-transform: none;" id="surface">Acoustic Modem with Multi-Channel Recorder</h3>
          <!-- <h4 style="text-transform: none;">WNC-M25MPE3</h4> -->
          <p>Combine a versatile aocutic modem with a powerful multi-channel acoustic recorder, ideal for long term deployments.</p>
    </div>
  </div>
  <div class ='media product' style='background: #f5f5f5' >   
    <div class='media-body product product-content' style='background: #f5f5f5'>
    <h3 style="text-transform: none;">Enhanced Performance using Spatial Diversity</h3>
          <!-- <h4 style="text-transform: none;">WNC-M25MPS3</h4> -->
          <p>Having multiple synchronized channels lets you exploit spatial diversity gain to improve communication range and link robustness.</p>
    </div>
    <img class = "ml-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-multichannel1.png"/> 
  </div>
  <div class ='media product' >
    <img class = "align-self-start mr-3" alt="" src="{{site.baseurl}}/images/boxart-wnc-multichannel2.jpg"/>    
    <div class='media-body product product-content'>
    <h3 style="text-transform: none;" id="surface">USBL Ready</h3>
          <!-- <h4 style="text-transform: none;">WNC-M25MPE3</h4> -->
          <p>Develop and deploy your own prositioning algorithms to unlock USBL functionality.</p>
    </div>
  </div>
</div>

<div class='two spacing'></div>

​
## + Product Description

### 1. Recorder with multiple hydrophones

Aimed at deployments where users need the ability to record, process and communicate acoustic signals, Subnero multi-channel modems provide:
   - Multiple synchronized receiving hydrophones
   - Storage and computing power for real-time data processing
   - Acoustic communication capability
   - Ability to schedule recording or trigger recording from an external signal

### 2. Spatial Diversity enabled receiver modem
​
Utilizing the flexibility of UnetStack, users can easily combine signals recorded from various spatially separated receiving channels to successfully decode the signal, using diversity combining techniques. This translates directly to improved performance in terms of increased communication range or robust communication link. 

Users can also choose the software upgrade option to get Subnero's Unity technology in this platform. Learn more... [TODO: Link to Unity premium agent in UnetStack page].

### 3. USBL ready platform
​
The ability to record raw signals using multiple hydrophones enable users to develop high resolution Ultra Short BaseLine (USBL) capability to provide an accurate range and bearing estimates. Hydrophones can be conveniently positioned to form a desired receiver array geometry. This makes the Subnero mutli-channel modem an ideal platform for users to develop their own USBL algorithms.

Users can also opt to go for the software upgrade option to unlock the Subnero USBL functionality. Learn more... [TODO: Link to USBL premium agent in UnetStack page].


## + Technical Specifications

### General
- TODO

### Acoustic Communication
- TODO

### Acoustic Recorder
- Number of channels: 1 - 4
- Sampling rate: 128 kSa/s
- Storage: 32 GB - 256 GB

### Dimensions
- TODO

### Interface
- Ethernet
- RS232

### Contact us for a quote [TODO: Button?]


## + Additional Information (TODO: Need to fix the following description)

Subnero multi-channel modem has additional synchronized receiving channels. The software driver publishes the received signals on various channels to UnetStack using standard baseband recording messages, so that the customer’s software could request these messages. At the event of detection of a signal on the main hydrophone, a baseband reception notification message `RxBasebandSignalNtf` is sent by the modem. The customer’s script can look for the reception of this notification message and request a recording using the secondary data acquisition system.
​
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
