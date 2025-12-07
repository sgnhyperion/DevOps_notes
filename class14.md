# Pods and Containers
* Pods are the **smallest deployable units** in Kubernetes
* A pod represents a **single running instance** in the cluster
* Each pod can have **one or more containers**
* Containers are lightweight, fast, and efficient
* Containers bring the benefits of containerization into pods

---

# Replica Sets
* Ensure a **fixed number of pod replicas** are always running
* Used for **scaling** and **high availability**
* If a pod or node fails, a **new pod is created automatically**
* Helps maintain the **desired state** of the application

---

# Deployments
* Provide **declarative updates** to applications
* Manage transitions between application versions
* A deployment **wraps around a ReplicaSet**
* Supports **rolling updates and rollbacks**
* Deployment controller manages pods and replica sets

---

# YAML Configurations
* Deployments and ReplicaSets are defined using **YAML files**
* YAML specifies:
  * Desired state
  * Number of replicas
* Main difference:
  * `kind: ReplicaSet`
  * `kind: Deployment`

---

# Example Deployment YAML
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.16.1
