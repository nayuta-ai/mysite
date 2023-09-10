---
title: "Intro"
date: 2023-09-10T18:04:50+09:00
---
## What is this article
Containerization has become a fundamental technology in modern software development and operations. While many are familiar with container orchestration platforms like Kubernetes and Docker, it's equally important to understand the underlying low-level runtimes that power containers. This document describes the implementation of a low-level runtime for containers.

## Abstraction
### Part1 (low level container runtime architecture)
A low-level runtime for containers is the core component responsible for managing the lifecycle of containers. It handles container creation, execution, and monitoring. Low-level runtimes interface directly with the kernel and are the foundation upon which higher-level container platforms are built. Low-level runtime for containers consists of three main linux components, such as Mount, Unshare, Cgroup and also some architecture such as IPC(Inter-Process Communication), Capabilities, RLimit, and etc.
### Part2 (IPC)
IPC (Inter-Process Communication) for containers refers to the mechanism by which processes running inside a container can communicate with each other or with processes outside the container. IPC is a fundamental concept in operating systems that allows processes to share data, signals, and synchronization primitives. In the context of containers, IPC is used to manage interactions between processes running within the same container or across different containers.
### Part3 (Mount)
In the context of containers, "mount" refers to the process of attaching a filesystem or directory from the host system or another source into the container's filesystem. This allows the containerized application to access and manipulate files and directories located outside of the container environment. Container filesystems are typically isolated from the host system for security and portability reasons, but mounting allows controlled access to specific resources.
### Part4 (OCI)
OCI (Open Container Initiative) runtime, also known as the OCI runtime specification, is a standardized interface that defines how container runtimes interact with container images and the host operating system. The OCI runtime specification aims to provide a common, vendor-neutral API for launching and managing containers, allowing container images to be compatible across different container runtimes.
### Part5 (Cgroup)
Control Groups, or cgroups for short, are a Linux kernel feature that allows you to control and manage the resource usage (such as CPU, memory, and I/O) of processes and groups of processes. Cgroups are particularly important in the context of containerization because they enable fine-grained resource isolation and allocation for containers.
## Environment and version
- OS: Mac, Linux
- rust, docker
## Targets
- Those who is interested in System Programming, Container Technology and Rust
- Those who want to commit to OCI and other OSS.