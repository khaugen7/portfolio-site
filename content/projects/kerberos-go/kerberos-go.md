---
title: "Kerberos-GO: Simulating Kerberos Authentication in Go"
description: "A client-server application implementing a simplified Kerberos authentication protocol, developed as an educational project in Go."
date: 2025-04-01T21:47:39-04:00
layout: "single"
draft: false
tags: ["Go", "Kerberos", "Authentication", "Security", "Client-Server"]
featured_image: "/images/kerberos_protocol.png"
weight: 1
---
<figure style="width: 100%; max-width: 800px; margin: 2rem auto; text-align: center;">
  <img src="/images/kerberos_diagram.png" alt="Kerberos Diagram" style="width: 100%;" />
  <figcaption style="font-size: 0.9rem; color: #888; margin-top: 0.5rem;">
    Kerberos Authentication Flow
  </figcaption>
</figure>{{< github_link url="https://github.com/khaugen7/kerberos-go" >}}

# Project Overview

Kerberos-GO is a client-server application designed to emulate the Kerberos authentication protocol. Developed as my inaugural project in Go, this endeavor provided valuable insights into both the language and the intricacies of secure authentication mechanisms.​

## Key Features

### Authentication Server (AS)
Handles initial client authentication requests and issues Ticket Granting Tickets (TGTs).​

### Ticket Granting Server (TGS)
Processes TGTs to provide service tickets for access to specific resources.​

### File Server (FS)
Validates service tickets and facilitates access to requested files.​

### Client Application
Initiates authentication and requests file downloads post-authentication.​

## Learning Outcomes

Embarking on this project enhanced my understanding of:​

- Implementing symmetric encryption techniques in Go.​

- Managing secure communications between distributed systems.​

- Structuring Go applications for scalability and maintainability.​

## Disclaimer

This application was developed solely as a learning exercise and should not be used for authentication or management of sensitive information of any kind.