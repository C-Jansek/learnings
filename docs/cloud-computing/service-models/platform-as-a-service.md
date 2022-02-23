---
sidebar_position: 2
---

# PaaS - Platform as a Service

Platform as a Service is a cloud computing service model where a customer can run and manage their own application(s), whithout having to maintain, configure or build the infrastructure needed to host the appication(s).

PaaS is an abstraction on top of [IaaS](infrastructure-as-a-service.md), where in addition to the managed hardware, middle ware, an operating system and a runtime are also provided by the provider.

## Characteristics

### High level programming

PaaS enables higher level programming where the complexity of the underlying infrastructure is abstracted away by the provider. This enables more focus on the application itself, as the provider takes care of maintenance and most configuration of the infrastructure (including OS and runtime).

Due to the nature of PaaS, control of underlying infrastructure is limited. There is often also a lack of operational features.

### Cost

Up- and down-scaling is often built-in, so for applications that use a fluctuating amount of resources, this can reduce costs.

For bigger applications, costs can grow fast.

### Vendor selection

Due to differences of underlying infrastructure, such as operating system and runtime configuration, vendor lock-in can occur. Applications (often) have to adapt when migrated to a different cloud provider.

## Use cases

PaaS is most often used by developers that have to host an application on a common configuration of infrastructure, or an application that is infrastructure independent.

Examples include:

- Heroku
- Microsoft Azure (partially)
- Google Cloud Platform (partially)
- Amazon Webservices (partially)

## Sources

- [Wikipedia](https://en.wikipedia.org/wiki/Platform_as_a_service)
- [IBM Technology](https://www.youtube.com/watch?v=QAbqJzd0PEE)
