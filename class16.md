# Kubernetes Networking Model

## Design Rules
- Pod-to-Pod without NAT
- Node-to-Pod without NAT
- Pod IP visible cluster-wide

---

## Pod Networking
Each Pod has its own network namespace.
Connected via veth pairs to bridge.

Cross-node routing handled by CNI.

---

## Service Networking
iptables/IPVS handle DNAT.
CoreDNS resolves names.

---

## Internet Access
Egress uses SNAT.
Ingress uses LoadBalancer or Ingress Controller.