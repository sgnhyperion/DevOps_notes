# Introduction to Kubernetes Nodes

* Kubernetes cluster was set up using **three machines**
* One machine acts as **Master Node**
* Remaining machines act as **Worker Nodes**

---

# Node Roles

## Master Node
* Handles **control plane operations**
* Does not run application workloads

## Worker Nodes
* Execute application workloads
* Run pods assigned by the master node

---

# Setting Up the Master Node

* Preliminary installations were already done
* A shell script was used for setup
* Commands used:
  * `sudo su`
  * `kubeadm init`
* This setup installs Kubernetes components:
  * etcd
  * API Server
  * Controller
  * Scheduler

---

# Understanding Pods

## What is a Pod?
* Smallest deployable unit in Kubernetes
* Can contain **one or more containers**

## Key Characteristics
* **Co-located** → Containers share network and resources
* **Co-scheduled** → All containers run on the same node

---

# Kubernetes Architecture

## Control Plane
* API Server
* etcd (key-value store)
* Controller
* Scheduler

## Data Plane
* Runs actual applications
* Includes node-level components

---

# API Server & kubectl

* `kubectl` is used to interact with the cluster
* Communicates with API Server using REST (or gRPC)
* API Server handles:
  * Authentication
  * Authorization
  * Validation
* Cluster state is stored in **etcd**

---

# Hands-On Pod Management

* Pods are created using `kubectl` commands
* Important command:
  * `kubectl get pod` → check pod status

---

# Namespaces in Kubernetes

* Used to organize and isolate resources
* Default namespaces include:
  * `default`
  * `kube-system`

---

# Network Configuration

## CoreDNS
* Handles DNS resolution inside the cluster
* Requires a network plugin to function properly

## Network Plugins
* Example: **Weave**
* Required for pod-to-pod communication

---

# Resource Scheduling

* Pods are scheduled based on:
  * Available CPU
  * Available RAM on nodes
