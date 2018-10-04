## Overview

* Monolithic vs Microservices Architecture
* What is Hystrix?
* Features of Hystrix
* Demo

---

## Monolithic vs Microservices Architecture

![Monolith vs Microservices architecture](/images/monolith_vs_microservices.png)

######Courtesy: [Martin Fowler's Articles](https://martinfowler.com/articles/microservices.html)

+++

### Monolithic Architecture

* Enterprise application is divided to 3 main parts:
    * Client side (UI)
    * Server side (services)
    * Database 
* Server side is the Monolith (bundled and executed as a single logical resource)
* Any changes will require building and testing entire application
* Horizontal scaling by running many instances behind the load balancer

+++

### Microservices Architecture

* Application built as suite of services
* Changes isolated to specific service which only requires building and testing that application
* Scales by distributing these services across multiple servers and replicating as needed

---

## What is Hystrix?

* In a distributed environment, some of the services dependencies are bound to fail.
* Hystrix is a library which helps to improve the system's resiliency
* Hystrix is designed for:
    * Stopping cascading failures in a distributed environment
    * Fail fast and rapidly recover
    * Fallback when possible

+++

### Healthy distributed system

![Healthy distributed system](/images/healthy_distributed_systems.png) 

######Courtesy: [Netflix Hystrix](https://github.com/Netflix/Hystrix/wiki)

+++

### One dependent service failure

![One dependenct service failure](/images/one_dependency_service_failure.png) 

######Courtesy: [Netflix Hystrix](https://github.com/Netflix/Hystrix/wiki)

+++

### Cascading services failure

![Cascading services failure](/images/cascading_services_failure.png)

######Courtesy: [Netflix Hystrix](https://github.com/Netflix/Hystrix/wiki)

---

## Demo