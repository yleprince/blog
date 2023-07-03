---
title: "What is Yarn?"
date: 2023-07-03T12:00:48Z
---

# What is Yarn?

YARN, which stands for Yet Another Resource Negotiator, is a cluster management technology in Apache Hadoop. It is responsible for managing resources and scheduling tasks across a Hadoop cluster, allowing multiple applications to run simultaneously and efficiently on the same cluster.

YARN was introduced in Hadoop 2.x as a replacement for the previous generation MapReduce framework, which had limitations in terms of scalability and resource utilization. YARN separates the resource management and job scheduling functionalities of Hadoop, enabling more flexibility and extensibility.

The main components of YARN are:

ResourceManager: The ResourceManager is the central authority that manages resources and coordinates application execution across the cluster. It keeps track of available resources, negotiates resource allocations with the NodeManagers, and handles the scheduling of tasks.

NodeManager: Each node in the cluster runs a NodeManager, which is responsible for managing resources on that node. It monitors the resource usage (CPU, memory, etc.) of the node and communicates with the ResourceManager for resource allocation and task execution.

ApplicationMaster: Each application running on the cluster has its own ApplicationMaster. The ApplicationMaster is responsible for negotiating resources with the ResourceManager and coordinating the execution of tasks on the NodeManagers. It handles task scheduling, monitors their progress, and reports back to the ResourceManager.

YARN supports multiple types of applications, not just MapReduce jobs. It provides a general framework for running distributed applications, including interactive query engines, graph processing frameworks, and stream processing systems, among others. This flexibility makes YARN a powerful tool for managing various workloads on a Hadoop cluster.

In summary, YARN is a cluster management technology in Hadoop that enables efficient resource utilization, scalability, and multi-tenancy by separating resource management and job scheduling functions. It allows multiple applications to run simultaneously on a Hadoop cluster, making it a crucial component for large-scale data processing and analytics.

----

sources:
- [hadoop.appache.org doc]([https://docs.scala-lang.org/tour/annotations.html](https://hadoop.apache.org/docs/stable/hadoop-yarn/hadoop-yarn-site/YARN.html)https://hadoop.apache.org/docs/stable/hadoop-yarn/hadoop-yarn-site/YARN.html)
- [chat gpt]()
