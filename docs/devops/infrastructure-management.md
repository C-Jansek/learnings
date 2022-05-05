---
sidebar_position: 3
---

# Infrastructure Management

## Scaling

When more users start using an application, the applications resources should **scale up** to keep up with the growing demand. Without good [scalability](../thesaurus#scalability), users will experience slowdowns or even disruptions to the application.

Scalability can happen through either [vertical scaling](../thesaurus#vertical-scalability) or [horizontal scaling](../thesaurus#horizontal-scalability).

Vertical scaling is simple and affordable, but it does require downtime to perform the upgrade of the machine.

Horizontal scaling does not require downtime for existing servers, which is the main reason that most DevOps teams choose horizontal scaling. Managing more servers is more complex however, and it is often also more expensive than vertical scaling.

Scaling is often not cheap, and teams look for the sweet spot between cost and performance with the ability to grow. [Elasticity](../thesaurus#elasticity) is important when demand shrinks (momentarily). When using pay-per-use infrastructure services such as [Infrastructure as a Service](../cloud-computing/service-models/infrastructure-as-a-service.md), high amounts of money can be saved.

## Virtualization

Virtualization technology allows one physical computer (such as a server) to run multiple virtual machines (VMs). Each VM is a distinct environment. It has its own operating system, as well as dependencies and users.

Virtualization allows for more efficient use of resources. It also makes management of multiple (virtual) machines easier. Virtualization management tools make it more easy to maintain multiple machines, when compared to installing and managing individual servers.

## Containerization

Containerization is a form of virtualization. Virtual environments called containers include instances of applications, as well as their dependencies. Since containers contain dependencies as well, this allows for more consistent environments across the different [deployment environments](operations-team#Deployment-Environments).

In comparison to Virtual Machines, containers do not include their own operating system. They instead share the operating system of the host machine. This makes containers smaller and faster to spin up (start) and they use less resources. The more efficient use of resources enables even more efficient scaling.

## Orchestration

Orchestration tools instruct many individual components, such as containers, on how to perform certain actions. This ensures consistency across the entire infrastructure system.

Orchestration tools automatically perform tasks such as:

- Deploying containers across multiple servers
- Restarting failed containers
- Rolling out updates without downtime
- Horizontal scaling of containerized applications

## Infrastructure as Code (IaC)

Infrastructure as Code (IaC) is the act of defining infrastructure properties in machine readable configuration files. These configuration files are then stored and tracked in version control systems.

Infrastructure configuration used to be performed manually. This was error-prone and time-consuming. Over time these configurations across servers would become out of sync due to human error. This is know as configuration drift (ToDo).

Using machine readable configuration files to store these configurations, and tracking them in version control systems enables easier automation and rollback.

Infrastructure as Code and orchestration tools rely on the principle of _immutable infrastructure_. Rather than updating the configuration on a server, new servers with the updated configuration are created and the old servers are destroyed. Configuration files, together with immutable infrastructure eliminate the risks of configuration drift as it guarantees that all servers are created (and thus currently running) with the same configuration as the configuration files.

Without VMs and containers, it would be rather costly to clean up and set up physical servers every time the configuration changed.

## In-House Infrastructure (on-premises)

Traditionally the company acquires, configures, and maintains physical infrastructure components themselves. These components include servers, power supplies, and cooling.Hardware failure, malicious use, outdated software and scalability were common problems for companies.

While the cost to maintain is high, In-House Infrastructure (on-premises) is fully customizable. The company is also less dependent on third-parties and sensitive data remains inside the company.

## Cloud Infrastructure

See also [Cloud computing as a service](../cloud-computing/cloud-computing-as-a-service.md).

A third-party company owns, houses and manages the physical infrastructure. Cloud-based infrastructure is mostly possible because of virtualization technology. It allows cloud providers to manage and split-up vast amounts of physical resources between clients.

It allows for:

- Specialization - Outsource infrastructure
- Quick scaling - High amounts of physical resources available
- Efficient scaling - Sharing resources between companies
