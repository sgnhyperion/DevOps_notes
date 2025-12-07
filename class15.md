# Services in Kubernetes
* Services provide a **stable network endpoint (IP/DNS)** for Pods
* Used to **expose applications** running on a group of Pods
* Service remains stable even if Pods are recreated

---

# Types of Services

## ClusterIP
* Exposes service on a **cluster-internal IP**
* Accessible **only inside the cluster**

## NodePort
* Exposes service on **each node’s IP and a fixed port**
* Automatically creates a **ClusterIP service**
* Can be accessed from outside the cluster using `NodeIP:NodePort`

---

# Important Concepts

## Service Discovery
* Services discover Pods using **labels**
* Automatically connects traffic to matching Pods

## Load Balancing
* Distributes traffic **evenly across Pods**
* Ensures no single Pod is overloaded

---

# Example Analogy
* Like multiple attendants at a movie theater
* Users can approach **any attendant**
* Requests are handled without waiting at a single point

---

# Load Balancers

## Internal Load Balancer
* Distributes traffic **within the cluster**
* Balances requests across Pods

## External Load Balancer
* Handles **internet traffic**
* Routes external requests to Kubernetes nodes

---

# YAML Files in Kubernetes
* Kubernetes resources are defined using **YAML**
* Common fields:
  * **apiVersion** → API version
  * **kind** → Resource type (Service, Deployment, etc.)
  * **metadata** → Name and namespace
  * **spec** → Desired behavior of the resource
