# Kubernetes YAML & Core Concepts – Short Notes

## Kubernetes YAML Structure
* Most Kubernetes YAML files have **4 main fields**:
  * **apiVersion** → API version used (for compatibility & features)
  * **kind** → Type of object (Pod, ReplicaSet, Deployment, etc.)
  * **metadata** → Information about the object (name, labels, etc.)
  * **spec** → Desired state (what you want Kubernetes to create)

---

## Pods
* Pod is the **smallest deployable unit** in Kubernetes
* Contains **one or more containers**
* Containers in a pod:
  * Share resources
  * Are **co-located** and **co-scheduled**
* If a container crashes, Kubernetes **automatically replaces it**
* No manual intervention needed

---

## YAML Syntax Basics
* Kubernetes YAML supports 3 data types:
  * **Key-Value** → `key: value`
  * **List** → `- item`
  * **Map** → Nested key-value structures

---

## ReplicaSets

## Purpose
* Ensures a **fixed number of pod replicas** are always running
* If a pod or node fails, new pods are created automatically

## ReplicaSet YAML Structure
* **kind:** ReplicaSet
* **replicas:** Number of pod instances (e.g., `replicas: 3`)
* **selector:** Matches labels of pods it should manage
* **labels:** Used to group and manage pods (similar to cloud tags)

---

## Internal Working

## Kubernetes Components
* **Kubelet**
  * Runs on nodes
  * Manages pod lifecycle
  * Reports node status to API Server

* **API Server**
  * Entry point of the cluster
  * Handles authentication, authorization, validation
  * Stores data in etcd

* **Controllers**
  * Watch current vs desired state
  * Take action if mismatch occurs

* **Scheduler**
  * Decides which node a pod should run on
  * Based on CPU, RAM, and constraints

---

## Pod Lifecycle & Recovery
* Controllers continuously monitor pods
* If a pod fails:
  * Controller detects mismatch
  * API Server is instructed to create a new pod
* Ensures desired state is always maintained

---

## Basic kubectl Commands
* `kubectl apply -f file.yaml` → Create or update resources
* `kubectl delete -f file.yaml` → Delete resources
* `kubectl get <resource>` → List resources (pods, rs, etc.)
