# Kubernetes Cluster Configs

This repository contains production-ready Kubernetes manifests and Helm values used to deploy essential components in a self-hosted Kubernetes cluster environment. It is part of a fully tested and functional homelab deployment.

Components currently included:

- 🔐 `cert-manager` – automated TLS certificate issuance using Let's Encrypt
- 🌊 `traefik` – ingress controller with Cloudflare DNS challenge support
- 💾 `longhorn` – persistent distributed storage for Kubernetes volumes
- ⚙️ `metalLB` – load balancer for bare-metal networks
- 🧩 `portainer` – web UI for managing containers and Kubernetes resources

✅ **All configuration files are tested and verified in a live working Kubernetes cluster.**

> 🔄 **Note:** This is an ongoing project. More applications, infrastructure configurations, and improvements will be added over time as the homelab evolves.

---

## 📂 Folder Overview

| Folder         | Description                                         |
|----------------|-----------------------------------------------------|
| `cert-manager` | ClusterIssuers, staging/production certificate CRs |
| `longhorn`     | Helm values, UI ingress, and secrets               |
| `metalLB`      | IP address pool and L2 advertisement config        |
| `portainer`    | PVC, ingress, and Helm overrides                   |
| `traefik`      | Middleware, Cloudflare secrets, and Helm values    |

---

## 📖 Detailed Setup Guide

For a full breakdown of this Kubernetes setup and the thinking behind each component, read the complete series of articles on my homelab blog:

🔗 [homelab.sanjuprojects.uk](https://homelab.sanjuprojects.uk)

Start here:  
➡️ [Kubernetes Series – Article 1: Cluster Setup with Proxmox](https://homelab.sanjuprojects.uk/kubernetes-cluster/)

---

## 🛠 Requirements

- Kubernetes v1.29 or later (K3s, kubeadm, etc.)
- Helm 3.x
- Static IP setup via pfSense (or similar)
- MetalLB or cloud provider LoadBalancer support

---

## 🚀 Usage

```bash
git clone https://github.com/sanju-mathew/kubernetes-cluster.git
cd kubernetes-cluster
# Deploy each component as needed using helm/kubectl
