# Introduction 

## Purpose 

In Azure, a combination of subscriptions, resource groups and resource names to organise environments. The Azure resource list is typically a big mess of everything in the subscriptions. 

Everything is by default listed in an alphabetical order, and it is typically hard to find what you are looking for and it’s not convenient for the resources cost management. 

The purpose of this document is to ensure that Azure Resources are named in a logical and consistent manner that supports good design practices and provide the efficiency for Azure Resources and cost management. 

The naming convention is used at MBIE should reflect the business structure and the services that are in use. 

Note: A resource could be an Azure compute resource or service, a file name or pretty much anything else that should have a logical name. 

# SYNTAQ's Existing Azure Tenancies 

SYNTAQ has one Azure tenancy currently, i.e. tbc.onmicrosoft.com Azure Active Directory.  

tbc.onmicrosoft.com 

This environment associates with the domain mbie.govt.nz and provides the following environments for the solutions: 

Production – Apps in full production mode, available to end-users 

Pre-production - The a production like environment with the addition of debugging and  

testing tools. Often contains production data. 

These environments, to date, have been deployed into the same subscriptions but in difference resource groups. 

Grownz4all.onmicrosoft.com 

This environment associates with the domain inp.mbie.govt.nz and provides the following environments for the solutions: 

Dev – Sandbox type environment for developers to try new features and services 

Test – Testing the solution using the required features and services 

SIT – Integration testing with other apps and services (e.g. APIs, other data sources, etc) 

UAT- User Acceptance Testing 

# Terms and definitions 

## Terms and definitions 

|Term|Definition|
|---|---|
|Azure Account |The Azure account is a global unique entity that gets you access to Azure services and your Azure subscriptions. You can create multiple subscriptions in your Azure account to create separation e.g. for billing or management purposes. In your subscription(s) you can manage resources in resources groups. |




App Service 

Azure App Service is a fully managed "Platform as a Service" (PaaS) that integrates Microsoft Azure Websites, Mobile Services, and BizTalk Services into a single service, adding new capabilities that enable integration with on-premises or cloud systems. 

App Service Plan 

Azure App Service Plan is the container for hosting Web Apps, API Apps, Mobile Apps and Function Apps. 

It is used to determine the resources available to your application (or applications) and their boundary. 

The app service plan defines what specification of hardware your app runs on, and how many servers you have. 

Application Gateway 

Azure Application Gateway works at application level is a web traffic load balancer that enables you to manage traffic to your web applications. 

 Azure Application Gateway can do URL-based routing and more. 

Availability Sets 

Availability set is a great feature Azure provides for Business continuity. So when two or more servers are in a single availability set, even if one or more of servers becomes unavailable due to any reason, rest of servers in an Availability set will provide the service. 

Enterprise  

Enrolment 

The Azure enterprise enrollment defines the shape and use of Azure services within your company from a contractual point of view. Within the enterprise agreement, you can further subdivide the environment into departments, accounts, and finally, subscriptions and resource groups to match your organisation's structure 

Key Vault 

Microsoft Azure Key Vault is a cloud-hosted management service that allows users to encrypt keys and small secrets by using keys that are protected by hardware security modules (HSMs).  

Traffic Manager 

Azure Traffic Manager is a DNS-based traffic load balancer that enables you to distribute traffic optimally to services across global Azure regions, while providing high availability and responsiveness. 

Virtual Network (VNet) 

An Azure Virtual Network (VNet) is a representation of your own network in the cloud. You can use VNets to provision and manage It is a logical isolation of the Azure cloud dedicated to your subscription.  

Load Balancer 

Azure Load Balancer works at Transport Layer and provides network level distribution but essentially only with the same azure data centre. 

Log Analytics 

Log data collected by Azure Monitor is stored in a Log Analytics workspace, which is based on Azure Data Explorer. It collects telemetry from a variety of sources and uses the Kusto query language used by Data Explorer to retrieve and analyze data. 

Logic App 

Azure Logic Apps is a cloud service that helps you automate and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across enterprises or organisations. 

Every Logic App workflow starts with a trigger, which fires when a specific event happens, or when new available data meets specific criteria. 

Network Security Groups(NSGs)  

Network Security Groups allow you to permit or deny traffic (via a rule base), to either a subnet or a network interface. By default the inbound and outbound rules include an implied deny all. Finally NSGs are stateful, meaning that the TCP sequence numbers are checked in addition to, if the connection is already established. 

Recovery Service Vaults 

A Recovery Services vault is a storage entity in Azure that houses data. The data is typically copies of data, or configuration information for virtual machines (VMs), workloads, servers, or workstations. 

Resource 

A manageable item that is available through Azure. Virtual machines, storage accounts, web apps, databases, and virtual networks are examples of resources.  

Resource Group  

Resource group - A container that holds related resources for an Azure solution. 

Subnet 

 An Azure subnet is a range of IP addresses in the VNet, you can divide a VNet into multiple subnets for organisation and security. 

Subscription 

The fundamental unit of working for a developer is an Azure Subscription. Access to the Azure services as well as the Management Portal is done through the subscription. 

 

 

