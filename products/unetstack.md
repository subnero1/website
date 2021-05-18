---
layout: page
title:  Underwater Network Stack
banner : images/banner-unetstack.jpg
thumbnail : images/boxart-unet.jpg
excerpt:
  Agent-based underwater network stack to transform modems into sophisticated network nodes
categories: software
section_id: products
---

UnetStack is a flexible agent-based underwater network stack allows software-defined underwater networks to be rapidly designed, simulated, tested and deployed. The stack runs on an underwater modem or on a host computer connected to the modem, transforming the modem into a sophisticated network node. UnetStack can also serve as a gateway to private terrestrial or satellite networks, or to the Internet.

UnetStack runs on all Subnero modems, but can be easily customized to run on modems from other manufacturers. For licensing information, please [contact]({{ site.baseurl }}{% link contact/index.md %}) us.

## Details

![UnetStack]({{site.baseurl}}/images/unetstack.png)

Commonly cited challenges in underwater networks include low bandwidth, long propagation delay, half-duplex nature of the links, high packet loss, and time-variability. To deploy successful networks in the face of such challenges, it is important to use highly optimized protocols that are specially designed for use in such networks. Specifically, cross-layer information sharing, low-bandwidth design and accurate transmission/reception timing can be critical in these protocols. Traditional layered network stacks provide good separation of concern, but result in sub-optimum protocols. Cross-layer optimization initiatives address this shortcoming by allowing direct interaction between layers. UnetStack takes a somewhat different approach. It consists of a collection of software agents that provide [well-defined services](https://www.unetstack.net/agent-ref.html){:target="_blank"}. This framework provides good separation of concern while allowing information to be shared, services to be provided, and behaviors to be negotiated between different agents. The resulting network stack is flexible and allows software-defined underwater networks to be rapidly designed, [simulated]({{ site.baseurl }}{% link products/unetsim.md %}), tested and deployed.

UnetStack defines commonly needed agents with services, messages, capabilities and parameters. The stack is extensible, allowing agents to provide additional services that may be used by other agents for the development of optimized network protocols. Although the stack focuses on underwater networks, it allows wired and wireless radio links to be included as part of the network.

UnetStack is implemented in Java and Groovy, and is based on the open-source [fjåge](https://github.com/org-arl/fjage){:target="_blank"} lightweight agent framework. Although it is primarily designed for use on embedded devices, it can be run on desktops or clusters when simulating underwater networks. It provides a basic set of agents that allow an underwater network to be deployed. Designed for extensibility, UnetStack allows additional agents for optimized protocols to be rapidly developed, tested and deployed. The stack can easily be integrated with most underwater modems.

In the UnetStack, agents play the role that _layers_ play in traditional network stacks. However, as the agents are not organized in any enforced hierarchy, they are free to interact in any way suitable to meet application needs. This promotes low-overhead protocols and cross-layer information sharing. A driver agent offering a _Physical_ service usually provides access to the physical layer implementation in a modem. Multiple agents providing similar services may coexist in the modem (e.g. drivers for multiple modems, acoustic and RF links, etc).

To use UnetStack with a third-party modem, a physical agent ([modem driver](https://www.unetstack.net/modems.html){:target="_blank"}) has to be developed for that modem. This is usually a straightforward process that a third-party developer can undertake with our support, or directly engage us to develop.
