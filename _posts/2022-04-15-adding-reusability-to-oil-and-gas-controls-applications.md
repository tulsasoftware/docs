---
layout: post
title: ADDING REUSABILITY TO OIL & GAS CONTROLS APPLICATIONS
subtitle: Leveraging IIoT In Practice by Corey Thompson
cover-img: /assets/img/genesis-system.png
thumbnail-img: ""
share-img: /assets/img/genesis-system.png
tags: [iiot, iot, mqtt, weimueller, arduino, hmi]
---

I got the chance to design a system for a customer that needed the ability to decouple their PLC logic from their hardware using Modbus over RS485. The issue is that certain brands of hardware could not only change their Modbus register mappings but sometimes they had different schema in place such as values spanning multiple registers with varying endianness.

We decided that the most cost effective way to do it was to create a customer converter for each Brand's implementation using an Arduino which would format the values into a standardized MQTT message that an ecosystem would be tightly coupled to.

Using this approach we are able to quickly swap brands of control hardware based on customer request, allowing a multi-tenant PLC ecosystem.