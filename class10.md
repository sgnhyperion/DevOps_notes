# Key Concepts in Docker Networking

## IP Addresses
* An IP address uniquely identifies a device on a network
* In Docker, each container gets its own unique IP address
* Used for communication between containers

---

## Subnetting
* Subnetting divides a network into smaller networks
* Uses CIDR notation to define network and host bits
* Example: `192.168.10.0/24`
  * `/24` → 32 − 24 = 8 host bits
  * `2^8 = 256` possible IP addresses

---

## Network ID & Broadcast ID
* **Network ID** → first IP address in the subnet
* **Broadcast ID** → last IP address in the subnet
* Broadcast ID is used to send data to all devices in the subnet

---

## Docker Zero Bridge
* Created automatically when Docker is installed
* Acts like a virtual network switch
* Allows container-to-container and external communication
* Each container has an `eth0` interface
* `eth0` connects to Docker Zero using a virtual Ethernet pair (veth)
