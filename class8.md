# Containers vs Virtual Machines

* Containers are more lightweight than virtual machines
* Containers share the host OS instead of carrying a full OS
* This leads to faster startup time and better resource usage

* Both containers and virtual machines provide isolation
* Virtual machines use a hypervisor for isolation
* Containers use Linux namespaces and cgroups for isolation

---

# How Containers Work

## Namespace Isolation
* Linux namespaces isolate:
  * Process IDs
  * Hostnames
  * Network access
  * User IDs
  * Inter-process communication
  * File systems

## Control Groups (Cgroups)
* Manage CPU and memory allocation
* Ensure fair resource sharing between containers
* Prevent one container from affecting others

---

# Docker and Kernel Interaction

* Docker interacts directly with the Linux kernel
* No hypervisor is required on Linux systems
* Containers run efficiently using the host kernel

---

# Running Containers on Different Systems

## Linux
* Containers run natively
* Uses host machine’s Linux kernel

## Windows & macOS
* Docker runs inside a lightweight Linux virtual machine
* Required because these systems do not natively support Linux kernel
