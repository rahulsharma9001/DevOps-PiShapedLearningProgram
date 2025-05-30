## Core Concept Questions

### 1. Why are liveness and readiness probes critical in keeping a product’s user experience stable and reliable?

Liveness and readiness probes help Kubernetes monitor the health and availability of application containers:

- **Liveness Probes** detect when a container is running but stuck or malfunctioning. If it fails, Kubernetes restarts the container automatically. This ensures recovery from deadlocks or long-running failures without manual intervention.

- **Readiness Probes** determine whether a container is ready to accept traffic. Until the readiness check passes, Kubernetes removes the pod from the service endpoints, preventing broken user experiences due to unready pods.

Together, these probes help maintain application stability, minimize downtime, and route traffic only to healthy, responsive instances—ensuring a smooth and reliable user experience.

---

### 2. How does HPA help in handling flash sales, seasonal load spikes, or traffic surges in real-world applications like an e-commerce platform?

The **Horizontal Pod Autoscaler (HPA)** automatically adjusts the number of running pods based on observed CPU or memory usage:

- During **flash sales or peak events**, HPA detects increased resource utilization and scales out the application pods to handle more requests without degrading performance.
- When the load decreases, HPA scales the pods back down, optimizing resource consumption and reducing costs.

This elasticity enables platforms to **maintain high availability and performance under unpredictable traffic**, such as Black Friday sales or festive shopping seasons, without overprovisioning resources.

---