# MicroServices
* Authentication: are you the right person
* Authorization: are you authorized to do that?
* multiple microservices should not talk to a single database, every microservice should have separate databases.
* MIcroservices should be stateless.

--> Breaking down a single large codebase into multiple parts, each part has only one service. Where each service talks to each other using APIs over the network.

* DNS(Domain Name System) Server: Mapping of IP and Domain names on a server over the internet.
* When we type a domain name on the browser 
    --> It goes to the dns and returns the mapped IP address.
    --> The browser make request to the real IP Address.
    --> it goes to the Load Balancer, it distributes the requests to servers to handle traffic accordind to the Path based routing and identifying the instance. 
    --> multiple instances Authentication and Authorization -> stored in database(Redis)
    --> Then it talks to the microservices according to its need
    --> Microservices talks over APIs(Rest, grpc, https, etc,.) through a load balancer because there could be multiple instances of a single microservice, therefore its Polyclot and not language dependant.

    * Service discovery: Capability to know To automatically detect and connect microservices without hardcoding IP addresses or ports

    --> MicroService to MicroService communication can happen in two ways:
       * Synchronous(simultaneously/cannot wait/instant response) 
       * Asynchronous(parallely or concurently / can wait/ don't need instant response/ eventual consistency) calls.
        --> Here we don't need load balancer because the broker(Kafka/rabbitMQ) manages the communications.
        --> Two Types:
        1. Publisher and Subscriber model: the subscribers are subscribed to a publisher, and they are notified when an event happen.
        2. Queue model: Subscriber has to go and pickup the messages.

* API Gateways: Other way of communication other than Load balancer way.
* Event Seeking: tracking API calls (time taken, instance, events, etc,.)
* Logs: Complete detail, stack trace or every call that took place between the whole process. It should be externalized, use external tools for logging(Splunk,ELK,Dynatrace, etc,.) for better troubleshooting. 

* Twelve Factor App
1. Codebase: Each service should have its own independent codebase.
2. Dependencies: Explicitly declare and isolate dependencies
    Service dependency : Microservices dependent on each other.
    Component dependency: One component (like a class, module, or function) depends on another within the same service or application.
3. Config: We should separate the configurations.
4. Backing services: 
5. Build, release, run: Strictly separate build and run stages
6. Processes: 
7. Port Binding:
8. Concurrency: ensure the service is designed to be stateless
9. Disposability:
10. Dev/prod parity
11. Logs
12. Admin processes: 


