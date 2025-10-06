# AWS EKS Deployment

This repository contains configuration templates and scripts to deploy an **Amazon EKS (Elastic Kubernetes Service)** cluster using two methods:  
1. **eksctl** (automatic provisioning)  
2. **AWS CLI** (manual provisioning)  

---

## 📦 What’s in This Repo

- `cluster.yaml` / `cluster2.yaml` — Kubernetes cluster definitions  
- `eks-cluster-role-trust-policy.json` — IAM trust policy for cluster roles  
- Additional supporting YAML/JSON templates for infrastructure setup  

---

## 🛠️ Deployment Methods

### Using eksctl (Automatic)  
Prerequisites:  
- `eksctl` installed  
- `kubectl` installed  
- IAM permissions to create AWS resources  

Usage:
```bash
eksctl create cluster -f cluster.yaml
