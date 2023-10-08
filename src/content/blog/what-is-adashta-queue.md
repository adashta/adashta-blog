---
title: 'What is Adashta Queue ?'
description: 'Adashta is currently working on adashta queue, A real time messaging tool that will seamlessly transfer data between different devices.'
pubDate: 'Oct 08 2023'
heroImage: '../../../public/what-is-adashta-queue.png'
category: 'Knowledge'
tags: []
---

Adashta is an open source organization working with a vision to streamline real-time data communication between multiple devices.

Currently working on **Adashta Queue** a real time messaging tool that will seamlessly transfer data between different devices.

This document will give a walkthrough on the functionality of Adashta Queue.

![Multiple Devices](https://lh4.googleusercontent.com/5cuyfiRx1dHgYetNE2B89C-hdNGD-eDbuqp3641hq3_piM_Ci-0_ZUOj03Np-nzb1P57Kk6S3BmnKqTCey6nWisVVVh47QGoJCZIKbSMt6TW-mYfnQ0wwsYhdITd1qQIYp6G1ADI258hAbkOm9L58QM)

Adashta Queue will be written in Go due to its fast execution speed and built-in support for concurrent operations.

## Features

Adashta Queue will work as an intermediary between clients and servers (nodes). Each node will connect to Adashta using a simple SDK.

![Adashta Queue Features](https://lh6.googleusercontent.com/79YzdxfkjJWmkkYM8ipmxl8SDoh_xyXXgh9cEd0ROnLmuuTnhbX7HQkMiVaM2TegfVQJAse7IL7TCksbHh36JaddPnwXeSQf1AtzEOuPOWZuaAvY2OuJOgKEo7jwPfnxkJzzgsJ8D-e0-1UA1NaqxGs)

It will provide features like -

1. Bidirectional Queue - Both server / client can exchange unlimited messages with each other.
2. Load Balancer - Automatically balance the traffic among servers. (Session stickiness will be there).
3. Data Storage - Store the data for a specified time and it will be fetchable even after consumption.
4. Message Scheduling - Server can schedule a message to be sent to the client.
5. Middlewares - Write middlewares to transform the data transferring b/w client and server.
6. Clustering - Automatically detect connected servers and create a cluster between them.

## Plugin Support

A plugin is a software component which can add a specific functionality to the Adashta Queue.[![](https://lh4.googleusercontent.com/xWKQiRF3TWngXI8f4EhQZ9ei1X0Kb5V1YJXLHU5hBjnEUz6PdzJLTlGuhsKsnF5n5OsQPug3CHpHEvGkgUJwPv01u41Z3jCE8JclzhYO1PbjzU4m3V-jsZkupwhZbPoRgMg8-ubiRVjSpENsStW3Vxk)](https://lh4.googleusercontent.com/xWKQiRF3TWngXI8f4EhQZ9ei1X0Kb5V1YJXLHU5hBjnEUz6PdzJLTlGuhsKsnF5n5OsQPug3CHpHEvGkgUJwPv01u41Z3jCE8JclzhYO1PbjzU4m3V-jsZkupwhZbPoRgMg8-ubiRVjSpENsStW3Vxk)

Adashta Queue will provide support for various official plug and play plugins like –

1. Real Time Charts
2. Real Time Push Notifications
3. Real Time User / Web Analytics
4. Real Time Chats
5. Data Transformation Middlewares
6. Real Time Webhooks

Users can install these plugins from Adashta Plugin Hub.

Adashta Plugin Hub will be a marketplace for community developers and open source contributors to distribute their plugins publicly.

Developers can also create and host their plugins on **Adashta Plugin Hub**.

Plugins can be created in -
1. Javascript
2. Lua

[![](https://lh3.googleusercontent.com/-CnIvbs2B_wVb97HnY37l--JWaz5u2nwpVMA69ZdbJVJLporC6TKqLUPnaY1xyvlYMQJKExZSWySdOB44uEI-egenxB_YgMmjo6QNa_YXE8tSk-azl34d6bqRQiYfFDwDtFBCR7DXgM_3CDRDRvWgXo)](https://lh3.googleusercontent.com/-CnIvbs2B_wVb97HnY37l--JWaz5u2nwpVMA69ZdbJVJLporC6TKqLUPnaY1xyvlYMQJKExZSWySdOB44uEI-egenxB_YgMmjo6QNa_YXE8tSk-azl34d6bqRQiYfFDwDtFBCR7DXgM_3CDRDRvWgXo)

## Components

There will be there major components -

1. Client SDK
2. Server SDK
3. Adashta Queue

### Client SDK

A software development kit that will be used to create and consume messages from Adashta queues on the client side.

This SDK will be provided by Adashta through a Content Delivery Network (CDN) link. Users simply need to place the script tag on their website like –


```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/sockjs-client/1.6.1/sockjs.js">
…
</script>
```

And then there will be three functions that the client needs to call -

```javascript
adashta.connect(); // (Used to connect with Adashta Queue)
adashta.produce(); // (Used to produce message in Adashta Queue)
adashta.consume(); // (Used to consume message from Adashta Queue)
```

### Server SDK

A software development kit that will be used to create and consume messages from Adashta queues on the server side.

This SDK will be provided by Adashta through Package Managers (npm, go packages).

Users simply need to import the package like –

```javascript
import { Adashta } from 'adashta';
```

And then there will be three functions that the server needs to call -

```javascript
adashta.connect(); // (Used to connect with Adashta Queue)
adashta.produce(); // (Used to produce message in Adashta Queue)
adashta.consume(); // (Used to consume message from Adashta Queue)

```

### Adashta Queue

Adashta Queue will be a self-hosted docker image that will serve as an intermediary of message communication between the client and the server.

This docker image will be provided by Adashta through [docker hub](https://hub.docker.com "docker hub"). Users can host and run this docker image by their own server.

```shell
docker run adashta-queue
```

## Final Words

We are looking for open source contributors who can contribute and be an early part of Adashta.

Since this project is in the idea stage, we are asking for your support in shaping this idea by providing your expertise. Please mail us your feedback at [contact@adashta.io](contact@adashta.io "contact@adashta.io") or create a pull request.

If you want to join us, Please have a look at our [CONTRIBUTING.md](https://github.com/adashta/adashta-queue/blob/main/CONTRIBUTING.md "CONTRIBUTING.md").

You can mail us at [contact@adashta.io](contact@adashta.io "contact@adashta.io") for any queries.

