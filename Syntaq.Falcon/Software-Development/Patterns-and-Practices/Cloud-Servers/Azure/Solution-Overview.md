# Terms and Definitions

The following table contains the glossary of the common terms, definition and acronyms used in this document.

|Term| Definition|
|---|---|
|Azure| Microsoft Azure is a cloud platform that offers Cloud computing services from Microsoft managed data centres which are found around the globe including in Australia, the USA and other locations|
|Cloud|A third party provided set of services (SaaS, PaaS, IaaS)  that provides customers with the infrastructural environment containing computer hardware and software which is accessed over the internet thereby removing the need for entities to have their own physical data centres containing their own servers.
|IaaS|Infrastructure as a service (IaaS) is a service model that delivers computer infrastructure on an outsourced basis to support enterprise operations. Typically, IaaS provides hardware, storage, servers and data centre space or network components; it may also include software. Operational Support costs remain the Customers responsibility|
|PaaS|Cloud platform services, also known as Platform as a Service (PaaS), provide cloud components to certain software while being used mainly for applications. PaaS delivers a framework for developers that they can build upon and use to create customized applications. All servers, storage, and networking can be managed by the enterprise or a third-party provider while the developers can maintain management of the applications. This drives savings in Operational Support costs.|

# Overview
This architecture builds on the Microsoft reference architecture pattern to [Improve scalability in a web application](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/app-service-web-app/scalable-web-app). 

The main differences are:
•	**Primary and secondary regions**. This architecture uses two regions to achieve higher availability. The application is deployed to each region. During normal operations, network traffic is routed to the primary region. If the primary region becomes unavailable, traffic is routed to the secondary region.
•	**Front Door**. [Front Door](https://docs.microsoft.com/en-us/azure/frontdoor/) routes incoming requests to the primary region. If the application running that region becomes unavailable, Front Door fails over to the secondary region.
•	**Geo-replication** of SQL Database.

A multi-region architecture provide higher availability than deploying to a single region. If a regional outage affects the primary region, you can use Front Door to fail over to the secondary region. This architecture can also help if an individual subsystem of the application fails.
There are several general approaches to achieving high availability across regions:

•	Active/passive with hot standby. Traffic goes to one region, while the other waits on hot standby. Hot standby means the VMs in the secondary region are allocated and running at all times.
•	Active/passive with cold standby. Traffic goes to one region, while the other waits on cold standby. Cold standby means the VMs in the secondary region are not allocated until needed for failover. This approach costs less to run, but will generally take longer to come online during a failure.
•	Active/active. Both regions are active, and requests are load balanced between them. If one region becomes unavailable, it is taken out of rotation.

# Software Components

# Hardware Components

# Cloud Services

# Design Considerations

# Development Environment

# Network
## Network Diagram

## IP Addressing

## DNS Records

## Routing

## Azure Network Security Groups

## Firewall rules

## Proxy requirements

## Switching Requirements

## Additional Requirements

# Servers

# Other Azure Resources
## Application Gateway
### Global Provisioning Details

### Front-end Provision Details

### Backend Provisioning Details

### Routing Rules

## Key vault
### Global Provisioning Details

### Post Creation - Provision Details

## Storage Accounts
### Global Provisioning Details

### Storage - Provision Details

### File Sharing - Provision Details






