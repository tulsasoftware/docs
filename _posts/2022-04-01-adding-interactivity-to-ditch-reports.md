---
layout: post
title: ADDING INTERACTIVITY TO DITCH REPORTS
subtitle: ""
cover-img: /assets/img/statistics-stock.png
thumbnail-img: /assets/img/statistics-stock.png
tags: [d3, data visualization, interactive report]
---

## Existing System

Our client prides themselves on being a metrics-driven company. However, the process to distribute these values to employees seems cumbersome and frequent. After a consultation, we were asked to create a better experience for the employees to access and track these values daily.

### Sharepoint

The company has their PLM system tied into Sharepoint. Sharepoint dashboard offers a hub for all employees.

### Identifying What to Fix

- Ease of Access
- Employees use these values in their everyday workflow, they should be readily available.
- Poor Usability
- Data existis in a complex report. A user has to traverse too much data for their use-case.
- High Barrier
- A complex report prevents new employees from understanding the numbers governing their work.

## First Thoughts

After some research and thought about the issues, we proposed a concept.

### Interactive Dashboard Widgets

Charts exist to provide digest information of large datasets at the sacrifice of granularity of data. Using interactive charts, we can retain the granularity of information on the client's KPI's.

### Macro/Micro

A measurement isn't valuable on its own, the numbers are only relevant in comparison to others. We had the an idea of a macro and micro pair of widgets to quickly understand today's numbers and the sources that drive that them as well vs. the trends of the past year.

## Laying a Path

With the buy-in of the client, we perform research to cement a design.

### Sharepoint Framework (SPFx.js)

This library has been proven enterprise production-ready and allows us to use the power of javascript within Sharepoint. Using Sharepoint Server 2016 puts us in the range of official support.

### D3.js

When it comes to interactive charts in javascript, D3 is always in the conversation. We opted to use v4 for some IE11 guarantees.

### Sharepoint Apps

Our code can be bundled into a sharepoint app and shipped via the client's local app store. Again, Sharepoint Server 2016 is within range of official support.

## First Pass

With approval, we started development.

### Sunburst Chart

Our datasets had hierarchical qualitative categories each with a quantitative value. We let the data lead us to the chart and the sunburst is a great fit for uncovering our strucutre. These charts are very flashy and are often used in a sub-optimal capacity, so when we chose it we did some soul-searching to make sure we weren't led astray. Ultimately, we felt confident in our method of selection. We used this as our micro chart, displaying month-to-date values. To make better use of space, we hollowed the center and added an "always-on" indicator, so a user could get exactly what they needed without even using the chart if they needed.

### Heatmap

While looking at our data, we had even more qualitative fields available. We really wanted our macro chart to complement in more than just theory, choosing the proper chart was crucial to make this happen. Rather than viewing multiple lines or clusters of histograms, we were able to utilize a heatmap to display a rolling 12 month window of monthly bins, with an added category breakdown. Another bonus to this choice was, knowing we wanted to add interactivity, it is much more usable than its competitors. The square bins are much easier to navigate and display tooltips than points or lines on hover.

## Adding Interactivity For Ultimate Value

### Heatmap

By adding a tooltip box with the context of that month's metrics, the user gained so much power to utilize the numbers at a glance or dig deep to investigate the source of the numbers, all immediately available to the employee.

### Sunburst

The center indicator now updates with the specific values of the hovered item, replacing the existing indicator and informing the user through design that they have left a high-level context and entered a new one.

## Retrospective
### Biggest Challenges
- Finding the balance between granularity of data vs clutter
- Refresh rate of Sharepoint lists as data source
- Limitations of Sharepoint Framework and web parts within Sharepoint 2016
- Support for IE11