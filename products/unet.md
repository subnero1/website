---
layout: page
title: Underwater Network Technology
banner : images/banner-unetsim.jpg
thumbnail: images/boxart-unet.jpg
categories: unet
section_id: products
---

Commonly cited challenges in underwater networks include low bandwidth, long propagation delay, half-duplex nature of the links, high packet loss, and time-variability. To deploy successful networks in the face of such challenges, it is important to use highly optimized protocols that are specially designed for use in such networks. Specifically, cross-layer information sharing, low-bandwidth design and accurate transmission/reception timing can be critical in these protocols. Traditional layered network stacks provide good separation of concern, but result in sub-optimum protocols. Cross-layer optimization initiatives address this shortcoming by allowing direct interaction between layers.

## UnetStack : The Underwater Network Stack

UnetStack is a flexible agent-based underwater network stack that allows software-defined underwater networks to be rapidly designed, simulated, tested and deployed. The stack runs on an underwater modem or on a host computer connected to the modem, transforming the modem into a sophisticated network node. UnetStack can also serve as a gateway to private terrestrial or satellite networks, or to the Internet.

![UnetStack]({{site.baseurl}}/images/unetstack3.png){: .center-image  }

UnetStack consists of a collection of software agents that provide [well-defined services](https://unetstack.net/handbook/unet-handbook_services_and_capabilities.html){:target="_blank"}. This framework provides good separation of concern while allowing information to be shared, services to be provided, and behaviors to be negotiated between different agents. The resulting network stack is flexible and allows software-defined underwater networks to be rapidly designed, simulated, tested and deployed.

UnetStack defines commonly needed agents with services, messages, capabilities and parameters. The stack is extensible, allowing agents to provide additional services that may be used by other agents for the development of optimized network protocols. Although the stack focuses on underwater networks, it allows wired and wireless radio links to be included as part of the network.

UnetStack runs on all Subnero modems, but can be easily customized to run on modems from other manufacturers. For licensing information, please [contact us]({{ site.baseurl }}{% link contact/index.md %}).

## UnetSim : The Underwater Network Simulator

The UnetSim underwater network simulator enables a network engineer to simulate an underwater network on a single computer. It allows UnetStack agents and protocols to be simulated in realistic channel conditions, with minimum effort. The simulator was designed with two key goals:

- To be easy to learn and use, and
- To allow agent implementations to be shared between deployment environment and simulation environment (no porting required).

Essentially, once a protocol is developed and tested in simulation, it is ready to be deployed and tested at sea in any UnetStack-compatible modem.

The simulator is available free-of-charge for download from [www.unetstack.net](https://unetstack.net/downloads/){:target="_blank"}.

## How does it work?

A simple script written in a [domain-specific language](https://unetstack.net/handbook/unet-handbook_writing_simulation_scripts.html){:target="_blank"} (DSL) allows users to describe a simulation scenario in a natural way. This significantly reduces the barrier to entry for new users. A sample simulation DSL script is shown below:

```java
channel.soundSpeed = 1500.mps
modem.dataRate     = [800.bps, 2400.bps]
modem.frameLength  = [16.bytes, 64.bytes]
modem.powerLevel   = [0.dB, 0.dB]

simulate 1.hour, {
  def buoy1 = node('Buoy-1', location: [0, 0, 0])
  def buoy2 = node('Buoy-2', location: [1.km, 500.m, 0])
  def auv1  = node('AUV-1', location: [0, 100.m, 0], mobility: true)
  auv1.motionModel = [speed: 1.mps, turnRate: 1.dps]
}
```

The simulator is highly customizable, with the ability to support user-defined modem behavioral models, physics-based channel models, various motion models, customized trace file formats, etc.

Detailed documentation is available on the [UnetStack documentation page](https://www.unetstack.net/docs.html){:target="_blank"}.


## Licensing
​
UnetStack comes in 4 editions,

#### 1. Community Edition
The **Community** edition is available for download on the [UnetStack website](https://unetstack.net/){:target="_blank"} and is free for non-commercial use. If you are developing and/or simulating underwater networks for educational or other non-commercial purposes, this edition is for you. This edition contains the [UnetStack simulator](https://unetstack.net/handbook/unet-handbook_part_ii_setting_up_underwater_networks.html){:target="_blank"} as well as the [Unet audio](https://unetstack.net/handbook/unet-handbook_getting_started.html#_using_acoustic_modems){:target="_blank"}.

> NOTE: **Community** edition is not meant to access a device that has UnetStack **OEM** (e.g. Subnero modems) pre-installed on it, for a commercial use-case, as the **Community** edition is only available for educational and other non-commercial purposes. You may, however, use any of the [open-source Gateway and UnetSocket libraries](https://github.com/org-arl/unet-contrib){:target="_blank"} to connect to a UnetStack **OEM** device.

​
#### 2. Commercial Edition
The **Commercial** edition of UnetStack is similar to the **Community** edition except you may use it in commercial applications. If you want to run UnetStack in your commercial application, please [contact us](mailto:sales@subnero.com) for more details about licensing the UnetStack **Commercial** edition.
​
#### 3. OEM Edition
The **OEM** edition is the version of UnetStack installed in the Subnero modems. You can use the various [UnetStack APIs](https://unetstack.net/handbook/unet-handbook_part_iii_building_unet_applications.html){:target="_blank"} and [open source Gateway and UnetSocket libraries](https://github.com/org-arl/unet-contrib){:target="_blank"} from any other device or computer to access the modems, without needing a separate license. 


In addition, if you are interested in getting UnetStack installed on your OEM device, you can [contact us](mailto:sales@subnero.com).
​
#### 4. Commercial (Dev-tools) Edition
The **Commercial (Dev-tools)** edition of UnetStack is similar to the **Commercial** edition but it is tagged to a specific OEM device (e.g. Subnero modem) that you own. You can use this edition of UnetStack to simulate and develop software for that OEM device, as well as to run UnetStack on your workstations to connect to and control the OEM device for development and testing of any applications involving the OEM device.

Subnero modems may have an associated **Commercial (Dev-tools)** edition. [Contact us](mailto:sales@subnero.com) for more information on the **Commercial (Dev-tools)** license.


<h2>Brochures</h2>
<div class="brochure-container">
  <a href="{{site.baseurl}}/brochures/UnetStack-Brochure-v3.0.pdf"><img class="brochure-thumb" src="{{site.baseurl}}/brochures/unetstack3.jpg"></a>
  <a href="{{site.baseurl}}/brochures/UnetStack-Brochure-v3.0.pdf" target="_blank" style="font-size: 1.2em;">UnetStack3</a>
</div>
