---
title: "Apache Cassandra System Study"
description: "A technical deep dive into the distributed NoSQL architecture of Apache Cassandra, exploring performance, scalability, and trade-offs in modern data systems."
date: 2025-04-02T22:30:00-04:00
draft: false
tags: ["Cassandra", "NoSQL", "Distributed Systems", "Database", "Scalability"]
---
<div style="text-align: center; margin-bottom: 2rem;">
  <img src="/images/cassandra_logo.png" alt="Apache Cassandra Logo" style="max-width: 300px; width: 100%; height: auto;" />
</div>

## Overview

This system study explores the internal architecture and design decisions of [Apache Cassandra](https://cassandra.apache.org/), a distributed, peer-to-peer NoSQL database built for high performance and scalability. The project analyzes Cassandra’s strengths, trade-offs, and ideal use-cases—particularly in handling large-scale, fault-tolerant workloads.

<p style="display: flex; flex-direction: column; align-items: center; margin-bottom: 2rem; gap: 1rem;">

  <a href="https://drive.google.com/file/d/1m_NAtIGFUyoRGtECzGRUHIc0fFLDQk5A/view?usp=drive_link" target="_blank" style="display: inline-block; background-color: #1e40af; color: white; padding: 0.75rem 1.5rem; border-radius: 6px; text-decoration: none; font-weight: 600;">
    📄 View Full Technical Report (Google Doc)
  </a>

  <a href="https://youtu.be/43rrX2F5mf0" target="_blank" style="display: inline-block; background-color: #dc2626; color: white; padding: 0.75rem 1.5rem; border-radius: 6px; text-decoration: none; font-weight: 600;">
    ▶️ Watch Presentation on YouTube
  </a>

</p>

## Key Topics Covered

- **Query-Driven Data Modeling**  
  How Cassandra prioritizes performance over normalization by denormalizing data around specific query patterns.

- **Distributed Architecture**  
  How Cassandra’s masterless peer-to-peer design supports horizontal scaling and high availability with no single point of failure.

- **Cassandra Query Language (CQL)**  
  An SQL-like language that trades flexibility (no joins or subqueries) for predictable query performance.

- **Performance Demonstration**  
  A hands-on demo using the [CVE dataset](https://www.kaggle.com/datasets/andrewkronser/cve-common-vulnerabilities-and-exposures) in a local Docker instance of Cassandra, showing optimized vs. non-optimized queries with performance tracing enabled.

- **Scalability & CAP Trade-offs**  
  A practical discussion of Cassandra’s tunable consistency and CAP theorem implications.

## Tools & Technologies

- Apache Cassandra
- Docker
- CQL
- CVE vulnerability dataset

## Why It Matters

This study demonstrates the architectural strengths that make Cassandra a key player in high-throughput, distributed applications like Netflix, where it handles 30 million ops/sec. It also evaluates when Cassandra might not be a good fit (e.g., ACID-heavy or join-reliant workloads).
