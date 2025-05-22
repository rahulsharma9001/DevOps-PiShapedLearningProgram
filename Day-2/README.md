# Day 2 - Kubernetes Architecture, Pod Scheduling, Node Affinity

## Core Concept Questions

## Why do we set requests and limits for CPU/memory in a production-grade product?

- Setting resource **requests** ensures the pod gets **minimum guaranteed resources**.  
- Setting **limits** ensures it doesn't **overconsume CPU/memory** and affect other pods.  
- This helps in **efficient cluster resource management** and the **stability of all running workloads**.


## When would a product team apply node affinity in Kubernetes?

**Node affinity** is used when certain workloads must run on specific nodes due to:
- **Hardware requirements** (e.g., GPU)
- **Geographical zones**
- **Environment isolation**

It ensures pods are scheduled based on **node labels**, improving:
- **Performance**
- **Compliance**
- **Resource optimization**