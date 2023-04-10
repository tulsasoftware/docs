---
layout: post
title: How to use Node-RED for IoT in Manufacturing - Part 1
subtitle: IIoT In Practice by Corey Thompson
cover-img: /assets/img/md/iot-manufacturing-factory-stock1.jpg
tags: [node-red, iot, manufacturing, industrial, automation, low-code]
---

# How to use Node-RED for IoT in Manufacturing - Part 1

Node-RED is a low-code, visual programming tool that allows you to create IoT applications by wiring together hardware devices, APIs and online services. It was originally developed by IBM for internal use but was made open-source in 2016¹. Since then, it has been adopted by the automation industry as an easy way to create Industrial IoT applications that collect, process, and share data through the internet¹².

In this blog post series, we will show you how to use Node-RED for IoT in manufacturing. We will cover the following topics:

- Part 1: What is Node-RED and why use it for IoT in manufacturing?
- [Part 2: How to install and run Node-RED on an IoT gateway?]({% post_url /2023-04-04-node-red-in-iot-manufacturing-part2 %})
- [Part 3: How to create a simple IoT application with Node-RED?]({% post_url /2023-04-05-node-red-in-iot-manufacturing-part3 %})

## What is Node-RED and why use it for IoT in manufacturing?

Node-RED is a programming tool that uses a browser-based editor to wire together flows using nodes that represent hardware devices, APIs, online services, or functions. Each node has a specific role and can be configured with properties. Nodes can be connected by wires to define the data flow between them. The flows can be deployed to a Node-RED runtime that runs on a server, a device, or in the cloud³.

Node-RED is especially suited for IoT in manufacturing because:

- It supports a wide range of communication protocols and data formats that are commonly used in industrial environments, such as OPC-UA, Modbus, MQTT, JSON, etc⁴.
- It provides a large collection of nodes that can be used to interact with various hardware devices, such as PLCs, sensors, actuators, cameras, etc⁴.
- It allows you to create complex data processing logic with minimal coding by using built-in nodes or custom functions³.
- It enables you to integrate with various online services and platforms that can provide additional functionality or analytics for your IoT application, such as databases, cloud services, dashboards, etc³.
- It offers a user-friendly and intuitive interface that makes it easy to create and modify flows without requiring advanced programming skills³.

Some examples of IoT applications that can be created with Node-RED are:

- Data acquisition and pre-processing: You can use Node-RED to collect data from various sources, such as sensors, PLCs, cameras, etc., and apply filters, transformations, aggregations, or calculations on the data before sending it to a database or a cloud service⁵.
- Data visualization and monitoring: You can use Node-RED to create dashboards that display real-time or historical data from your IoT devices or services using charts, gauges, tables, maps, etc. You can also use Node-RED to monitor the status of your devices or services and send alerts or notifications if any issues are detected⁵.
- Data analysis and optimization: You can use Node-RED to perform data analysis on your IoT data using various methods, such as machine learning, statistics, anomaly detection, etc. You can also use Node-RED to optimize your processes or operations based on the insights gained from the data analysis⁵.

In summary, Node-RED is a powerful and flexible tool that can help you create IoT applications for manufacturing in a fast and easy way.

In the next part of this blog post series, we will show you how to install and run Node-RED on an IoT gateway.

Stay tuned!

1. [What is Node-RED? - How Can I Use it to Create IoT Applications?](https://realpars.com/node-red/) Accessed 4/10/2023.
2. [Node-RED in Industrial IoT: a growing standard - United](https://learn.umh.app/blog/node-red-in-industrial-iot-a-growing-standard/) Accessed 4/10/2023.
3. [Would you use Node-RED in a production environment for IoT industry](https://discourse.nodered.org/t/would-you-use-node-red-in-a-production-environment-for-iot-industry-applications/19358) Accessed 4/10/2023.
4. [FlowForge nabs $7.2M to help companies integrate IoT using Node-RED](https://techcrunch.com/2022/11/03/flowforge-nabs-7-2m-to-help-companies-integrate-iot-using-node-red/) Accessed 4/10/2023.
5. [What is Node-RED? - How Can I Use it to Create IoT Applications?](https://realpars.com/node-red/) Accessed 4/10/2023.
6. [IoT Gateways with Node-RED in the Internet of Things](https://www.welotec.com/iot-gateways-and-their-central-role-in-the-internet-of-things/) Accessed 4/10/2023.