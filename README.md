# Kubernetes Installation Guide

This guide helps you install a **Kubernetes cluster** using prebuilt scripts for both the **master** and **worker** nodes.
---

## Step 1: Install Kubernetes Master Node

Download and run the setup script:

```bash
git clone https://github.com/ttnguyenblog/k8s.git
cd /k8s
chmod +x master.sh
./master.sh
```

---

## Step 2: Install Kubernetes Worker Node

```bash
chmod +x worker.sh
./worker.sh
```

---

## Step 3: Verify Cluster Status

Check if nodes are joined successfully:

```bash
kubectl get nodes --watch
```

---

## ✅ Step 4: Run Test Pod

Deploy a test pod to verify the cluster is working:

```bash
kubectl run nginx --image=nginx
kubectl get po --watch
```

