# Kubernetes

* Orchestrate containers
    -- Automatic bin packing
    -- Fail over
    -- Scale
    -- Load balancing: (distribute & Service discovery)
    -- Jobs

* Architecture:
-- Control plane/ Master Node
    * Controller: Ensure desired state should be matching current.
    * Scheduler: Identifies which node pod runs.
    * API server
        -> authentication: to check if user is a valid user or not
        -> authorize: to check if the user has the permission to do a certain thing or not
        -> validate
        -> talk to ETCD: It is like a database/NoSQL database
    * ETCD

-- Data plane / Work Node
    * Kubelet: work with cri to create pods
    * Kube-proxy: It is one of the components which helps in networking
    * CRI(Container runtime) -> docker, containerd, crio

--> Node : Virtual machine / Physical Machine
--> Kubectl: it is client who talks to API server of control plane through rest api

kubectl -> talks to api server using rest api -> it authentication, authorize, validates and talks to ETCD -> It talks to the kubelet -> it works with the cri to create pods