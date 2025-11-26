# CoLatency: A Multi-User Collaborative AR System with Heterogeneous Latency

**CoLatency** is an open-source multi-user AR application used in the paper:

> **When Latency Helps: A Performance–Experience Paradox in Collaborative Augmented Reality**  
> J.Qin et al., *Virtual Reality* (Springer), <2025>.

CoLatency allows two colocated users to interact with shared virtual spheres under **no-latency** and **heterogeneous-latency** conditions, while logging detailed interaction and network metrics such as **RTT**, timestamps, and task performance.

---

## Key Features

- **Multi-user collaborative AR** using Fusion (Host/Client and Shared modes)  
- **Colocation via OVR Spatial Anchors** for shared physical–virtual alignment  
- **Real-time RTT logging** during each user interaction  
- **Heterogeneous latency simulation** (one user experience delayed, one experience near-zero latency)  
- **Automatic log generation** for task performance and latency analysis  
- **Experiment-ready**: same codebase supports both *with-latency* and *no-latency* conditions

---

## System Overview

The CoLatency application was designed to study how network latency affects **task performance**, and **user experience** in collaborative AR.

Two users:

- stand in the same physical space,  
- see the same set of anchored virtual spheres,  
- and are instructed to **simultaneously “pop” spheres of the same color**.

All successful interactions are logged with:

- `Sphere ID`  
- `Timestamp` (simulation time)  
- `RTT` 
- `Color` of the popped sphere  

---
## Latency Configuration & Measurement

CoLatency uses Fusion’s internal networking and optional simulation features to create two latency conditions used in the experiment. CoLatency also supports several delay types, including constant delay, jitter-based delay, and packet-level disturbances.


### 1. No-Latency Condition (Shared Mode)

In the **no-latency condition**, the application runs in Fusion’s **Shared mode**, where both users share a common simulation with minimal network-induced delay.


### 2. With-Latency Condition (Heterogeneous Host/Client)

In the **with-latency condition**, the system runs in **Host/Client mode**, and **only one user** is subjected to additional simulated latency (heterogeneous latency).


---


## Build & Deploy

1. Open the project in **Unity 2022+**
2. Configure the project for **Meta Quest** (or another XR target of your choice)
3. Build and install the application on **two devices**

---
##  License

This project is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

You are free to:

- **Use**
- **Modify**
- **Distribute**

this project, including for academic and commercial purposes, **provided that you give appropriate credit and cite the corresponding paper**:

> J.Qin et al., *When Latency Helps: A Performance–Experience Paradox in Collaborative Augmented Reality*, Virtual Reality, <2025>.

For details, see the full license text in the `LICENSE` file.

---

## How to Cite CoLatency

If you use this repository, the CoLatency application, or any part of its code or logs in your research, please cite the following paper:

```bibtex
@article{qin_colatency_<2025>,
  author    = {Jingwen Qin, Yue Li, Berend Jan van der Zwaag, Ozlem Durmaz - Incel},
  title     = {When Latency Helps: A Performance--Experience Paradox in Collaborative Augmented Reality},
  journal   = {Virtual Reality},
  year      = {<2025>},
  publisher = {Springer},
  note      = {CoLatency: Open-source multi-user AR system with heterogeneous latency},
  doi       = {<DOI>}
}
---

