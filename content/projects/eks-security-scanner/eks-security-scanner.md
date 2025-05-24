---
title: "eks-scanner: Auditing EKS Clusters for Common Security Risks"
description: "A Go-based CLI tool for scanning AWS EKS clusters and identifying misconfigurations, privilege risks, and threat exposure."
date: 2025-05-23
layout: "single"
draft: false
tags: ["Go", "Kubernetes", "EKS", "AWS", "Security", "CLI"]
weight: 1
---
<figure style="width: 100%; max-width: 800px; margin: 2rem auto; text-align: center;">
  <img src="/images/eks-security-scanner-logo.png" alt="eks-security-scanner logo" style="width: 100%;" />
</figure>{{< github_link url="https://github.com/khaugen7/eks-security-scanner" >}}

# Project Overview

`eks-scanner` is an open source command-line tool written in Go that performs read-only security scans against Amazon EKS clusters. The project was created to deepen my practical understanding of Kubernetes security, AWS IAM integration, and threat modeling within containerized environments.

The tool is designed to provide fast, understandable feedback on common misconfigurations and security gaps without requiring any infrastructure changes or write permissions in the cluster.

## Key Features

### IAM Access Audit
Scans EKS access entries and evaluates attached IAM roles for overly permissive policies or stale access.

### Pod Privilege Check
Inspects all running pods for dangerous configurations such as privileged containers, hostPath volumes, or root execution.

### Namespace Risk Analysis
Evaluates each namespace for missing ResourceQuotas, LimitRanges, and risky RBAC bindings to default service accounts.

### Threat Graph Modeling
Generates a DOT-format or ASCII graph of identity and network relationships across the cluster by mapping pods to ServiceAccounts, IAM roles, and services they can access.

#### Dot Graph Example:

<figure style="width: 100%; max-width: 800px; margin: 2rem auto; text-align: center;">
  <img src="/images/threat-graph-dot-format.png" alt="EKS Threat Graph Example" style="width: 100%;" />
  <figcaption style="font-size: 0.9rem; color: #888; margin-top: 0.5rem; margin-bottom: 1.5rem;">
    Threat graph output visualizing pod-to-service and identity mappings
  </figcaption>
</figure>


## Learning Outcomes

Building `eks-scanner` allowed me to explore:

- The intersection of Kubernetes RBAC and AWS IAM in managed EKS clusters.

- Common privilege escalation vectors and their detection using the Kubernetes API.

- Writing modular, testable Go CLI tools with Cobra and the Kubernetes Go client.

- Threat modeling practices and visual graph generation for containerized systems.

## Usage and Scope

The tool requires AWS and Kubernetes credentials with read-only access to your cluster. No write actions are performed. It can be used interactively by security teams, DevOps engineers, or as part of a CI/CD security gate.

## Roadmap

Planned improvements include:

- JSON output support for automation pipelines

- Custom policy definitions or rulesets

- Integration with popular Kubernetes admission controllers for remediation guidance
